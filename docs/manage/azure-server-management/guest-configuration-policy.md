---
title: Azure Policy ゲスト構成拡張機能
description: Azure Policy のゲスト構成拡張機能を使用して Azure VM 内の構成設定を監査する方法を、Azure 向けのクラウド導入フレームワークを使用して学習します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 05/10/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: operate
ms.custom: internal
ms.openlocfilehash: cc67a0d31b32522a32c331e9fcd798e259b17e11
ms.sourcegitcommit: 9d76f709e39ff5180404eacd2bd98eb502e006e0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "100631918"
---
# <a name="azure-policy-guest-configuration-extension"></a>Azure Policy ゲスト構成拡張機能

[Azure Policy ゲスト構成拡張機能](/azure/governance/policy/concepts/guest-configuration)を使用して、仮想マシン内の構成設定を監査できます。 ゲスト構成は、現在 Azure VM 上でのみサポートされています。

ゲスト構成ポリシーの一覧を見つけるには、Azure Policy ポータル ページで「**ゲスト構成**」を検索するか、PowerShell ウィンドウで次のコマンドレットを実行して一覧を見つけます。

```powershell
Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Guest Configuration"}
```

> [!NOTE]
> ゲスト構成機能は、追加のポリシー セットをサポートするために定期的に更新されます。 新しいサポート対象ポリシーを定期的に確認し、役立つかどうかを評価してください。

## <a name="deployment"></a>デプロイ

次の PowerShell スクリプトの例を使用して、これらのポリシーをデプロイします。

- Windows および Linux コンピューターのパスワード セキュリティ設定が正しく設定されていることを確認します。
- Windows VM で証明書の有効期限が近づいていないことを確認します。

 このスクリプトを実行する前に、[Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) コマンドレットを使用してサインインします。 スクリプトを実行するときに、ポリシーを適用するサブスクリプションの名前を指定する必要があります。

```powershell

    # Assign Guest Configuration policy.

    param (
        [Parameter(Mandatory=$true)]
        [string] $SubscriptionName
    )

    $Subscription = Get-AzSubscription -SubscriptionName $SubscriptionName
    $scope = "/subscriptions/" + $Subscription.Id

    $PasswordPolicy = Get-AzPolicySetDefinition -Name "3fa7cbf5-c0a4-4a59-85a5-cca4d996d5a6"
    $CertExpirePolicy = Get-AzPolicySetDefinition -Name "b6f5e05c-0aaa-4337-8dd4-357c399d12ae"

    New-AzPolicyAssignment -Name "PasswordPolicy" -DisplayName "[Preview]: Audit that password security settings are set correctly inside Linux and Windows machines" -Scope $scope -PolicySetDefinition $PasswordPolicy -AssignIdentity -Location eastus

    New-AzPolicyAssignment -Name "CertExpirePolicy" -DisplayName "[Preview]: Audit that certificates are not expiring on Windows VMs" -Scope $scope -PolicySetDefinition $CertExpirePolicy -AssignIdentity -Location eastus

```

## <a name="next-steps"></a>次のステップ

重要なファイル、サービス、ソフトウェア、レジストリの変更に対して[変更の追跡とアラートを有効にする](./enable-tracking-alerting.md)方法をご確認ください。

> [!div class="nextstepaction"]
> [重要な変更の追跡とアラートを有効にする](./enable-tracking-alerting.md)

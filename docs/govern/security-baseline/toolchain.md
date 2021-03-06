---
title: Azure でのセキュリティ ベースライン ツール
description: セキュリティ ベースライン規範をサポートするポリシーとプロセスを成熟させるのに、Azure ネイティブ ツールがどのように役立つかについて説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 09/17/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: govern
ms.custom: internal
ms.openlocfilehash: ea3fdbc23847b1e0c20c84bade64e5d0e96b439e
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101787639"
---
# <a name="security-baseline-tools-in-azure"></a>Azure でのセキュリティ ベースライン ツール

[セキュリティ ベースライン規範](./index.md)は、[クラウド ガバナンスの 5 つの規範](../governance-disciplines.md)のうちの 1 つです。 この規範は、ネットワーク、資産、および最も重要なものとしてクラウド プロバイダーのソリューションに存在するデータを保護するポリシーを確立する方法に重点を置いています。 クラウド ガバナンスの 5 つの規範のうち、セキュリティ ベースライン規範にはデジタル資産とデータの分類が含まれます。 また、リスク、ビジネスの許容度、およびデータ、資産、ネットワークのセキュリティに関連付けられた軽減戦略のドキュメントも含まれます。 技術的な観点から、この規範は、[暗号化](../../decision-guides/encryption/index.md)、[ネットワーク要件](../../decision-guides/software-defined-network/index.md)、[ハイブリッド ID 戦略](../../decision-guides/identity/index.md)、および[リソース グループ](../../decision-guides/resource-consistency/index.md)全体でセキュリティ ポリシーの[適用を自動化](../../decision-guides/policy-enforcement/index.md)するツールに関する決定にも関わります。

Azure ツールの次の一覧は、この規範をサポートするポリシーとプロセスを成熟させるのに役立ちます。

| ツール | [Azure portal](https://azure.microsoft.com/features/azure-portal/) と [Azure Resource Manager](/azure/azure-resource-manager/management/overview) | [Azure Key Vault](/azure/key-vault/)  | [Azure AD](/azure/active-directory/fundamentals/active-directory-whatis) | [Azure Policy](/azure/governance/policy/overview) | [Azure Security Center](/azure/security-center/security-center-introduction) | [Azure Monitor](/azure/azure-monitor/overview) |
|------------------------------------------------------------|---------------------------------|-----------------|----------|--------------|-----------------------|---------------|
| アクセスの制御をリソースとリソースの作成に適用する   | はい                             | いいえ              | はい      | いいえ           | いいえ                    | いいえ            |
| 仮想ネットワークをセキュリティで保護する                                    | はい                             | いいえ              | いいえ       | はい          | いいえ                    | いいえ            |
| 仮想ドライブを暗号化する                                     | いいえ                              | はい             | いいえ       | いいえ           | いいえ                    | いいえ            |
| PaaS ストレージとデータベースを暗号化する                         | いいえ                              | はい             | いいえ       | いいえ           | いいえ                    | いいえ            |
| ハイブリッドの ID サービスを管理する                            | いいえ                              | いいえ              | はい      | いいえ           | いいえ                    | いいえ            |
| リソースの許可される型を制限する                         | いいえ                              | いいえ              | いいえ       | はい          | いいえ                    | いいえ            |
| geo リージョンの制限を適用する                          | いいえ                              | いいえ              | いいえ       | はい          | いいえ                    | いいえ            |
| ネットワークとリソースのセキュリティ正常性を監視する          | いいえ                              | いいえ              | いいえ       | いいえ           | はい                   | はい           |
| 悪意のあるアクティビティを検出する                                  | いいえ                              | いいえ              | いいえ       | いいえ           | はい                   | はい           |
| 事前に脆弱性を検出する                        | いいえ                              | いいえ              | いいえ       | いいえ           | はい                   | いいえ            |
| バックアップとディザスター リカバリーを構成する                     | はい                             | いいえ              | いいえ       | いいえ           | いいえ                    | いいえ            |

セキュリティ ツールとサービスの完全なリストについては、「[Azure で利用できるセキュリティ サービスとテクノロジ](/azure/security/fundamentals/services-technologies)」を参照してください。

お客様は、一般にサードパーティのツールを使用して、セキュリティ ベースライン規範のアクティビティを有効にします。 詳細については、「[Azure Security Center でのセキュリティ ソリューションの統合](/azure/security-center/security-center-partner-integration)」の記事を参照してください。

セキュリティ ツールに加えて、[Microsoft 365 のコンプライアンス管理](https://www.microsoft.com/microsoft-365/enterprise/compliance-management)には、広範なガイダンス、レポート、および移行計画プロセスの一環としてのリスク評価の実行に役立つ関連ドキュメントが含まれます。

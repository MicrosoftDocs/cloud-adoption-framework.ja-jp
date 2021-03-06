---
title: クラウド導入フレームワークのエンタープライズ規模のランディング ゾーンを Azure に実装する
description: Azure 向けのクラウド導入フレームワークにおけるエンタープライズ規模のアーキテクチャの実装オプションについて説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 06/15/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: ready
ms.custom: think-tank
ms.openlocfilehash: f66cc1e1478810e885b86fd6623faf36678642d7
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101787231"
---
# <a name="implement-cloud-adoption-framework-enterprise-scale-landing-zones-in-azure"></a>クラウド導入フレームワークのエンタープライズ規模のランディング ゾーンを Azure に実装する

ビジネス要件のため、最初からガバナンス、セキュリティ、運用が完全に統合された高度なランディング ゾーンの初期実装が必要な場合は、ここで示すエンタープライズ規模の例のオプションを使用してください。 このアプローチでは、Azure portal かコードとしてのインフラストラクチャを使用して、環境を設定および構成できます。 また、組織の準備が整ったら、ポータルとコードとしてのインフラストラクチャ (推奨) の間で切り替えることもできます。

## <a name="example-implementation"></a>実装例

次の表では、モジュール形式の実装の例を示します。

| デプロイ例 | 説明 | GitHub のリポジトリ | Deploy to Azure (Azure へのデプロイ) |
|---------|---------|---------|---------|---------|---------|---------|---------|
| エンタープライズ規模の基盤 | これは、エンタープライズ規模の導入に対して推奨される基盤です。 | [GitHub の例](https://github.com/Azure/Enterprise-Scale/blob/main/docs/reference/wingtip/README.md) | [例を Azure にデプロイする](https://portal.azure.com/#blade/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fwingtip%2FarmTemplates%2Fes-foundation.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fwingtip%2FarmTemplates%2Fportal-es-foundation.json) |
| エンタープライズ規模の Virtual WAN | Virtual WAN ネットワーク モジュールをエンタープライズ規模の基盤に追加します。 | [GitHub の例](https://github.com/Azure/Enterprise-Scale/blob/main/docs/reference/contoso/Readme.md) | [例を Azure にデプロイする](https://portal.azure.com/#blade/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fcontoso%2FarmTemplates%2Fes-vwan.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fcontoso%2FarmTemplates%2Fportal-es-vwan.json) |
| エンタープライズ規模のハブ アンド スポーク | ハブ アンド スポークのネットワーク モジュールをエンタープライズ規模の基盤に追加します。 | [GitHub の例](https://github.com/Azure/Enterprise-Scale/blob/main/docs/reference/adventureworks/README.md) |[例を Azure にデプロイする](https://portal.azure.com/#blade/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fadventureworks%2FarmTemplates%2Fes-hubspoke.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FEnterprise-Scale%2Fmain%2Fdocs%2Freference%2Fadventureworks%2FarmTemplates%2Fportal-es-hubspoke.json) |

## <a name="next-steps"></a>次のステップ

上記の例では、エンタープライズ規模のアプローチの継続的な学習をサポートする簡単なデプロイ オプションが提供されています。 これらの例をエンタープライズ規模の運用バージョンで使用する前に、[エンタープライズ規模のアーキテクチャ](./architecture.md)を確認してください。

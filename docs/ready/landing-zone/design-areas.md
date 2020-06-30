---
title: 適切に設計したランディング ゾーンの設計領域
description: 適切に設計したランディング ゾーンの設計領域。
author: BrianBlanchard
ms.author: brblanch
ms.date: 06/15/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: ready
ms.openlocfilehash: ff839cb704ce79910fc29d6954712a0337a53e1e
ms.sourcegitcommit: 9b183014c7a6faffac0a1b48fdd321d9bbe640be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2020
ms.locfileid: "85077012"
---
# <a name="modular-design-areas-considered-by-all-azure-landing-zones"></a>すべての Azure ランディング ゾーンで考慮されるモジュール設計領域

各 Azure ランディング ゾーンの実装オプションとして、次の設計領域の実装に役立つデプロイ アプローチと定義された設計原則が用意されています。 実装オプションを選択する前に、この記事を参考にしてその設計領域について理解を深めてください。

> [!NOTE]
> 次の設計領域は、ランディング ゾーンをデプロイする前に検討する必要がある事項の概要を示しています。 この記事は、意図的に詳しくもなく、実用的でもありませんが、簡単なリファレンスとして利用できます。 [ランディング ゾーンの実装オプション](./implementation-options.md)の記事の次の手順は、デプロイにこだわりのある設計原則と実用的な手順を用意することです。  

デプロイ オプションに関係なく、次の各事項を検討し、設計領域ごとに判断する必要があります。 これらの判断は、各ランディング ゾーンが依存するプラットフォームの基盤に影響を与えます。

| 設計領域  | 目的  | 関連する方法 |
|---|---|---|
| エンタープライズ登録 | Azure を契約している企業のお客様にとって、適切なテナントの作成と登録は重要な初期段階です。 | Ready |
| ID | ID およびアクセス管理 (IAM) は、パブリック クラウドの主要なセキュリティ境界です。 セキュリティで保護された完全に準拠したアーキテクチャの基盤です。 | Ready |
| ネットワーク トポロジと接続 | ネットワークと接続性の決定は、どのようなクラウド アーキテクチャでも同様に重要な基本的な側面です。 | Ready |
| リソースの編成 | クラウド導入の規模が拡大するにつれて、サブスクリプションの設計と管理グループの階層に関する考慮事項は、ガバナンス、運用管理、および導入パターンに影響を与えます。 | ガバナンス |
| ガバナンスの規範 | セキュリティ、ガバナンス、コンプライアンス ポリシーの監査と適用を自動化します。 | ガバナンス |
| 運用ベースライン | クラウドで安定して継続的な運用を行うには、可視性、運用コンプライアンス、保護および復旧機能を提供する運用ベースラインが必要です。 | 管理する |
| ビジネス継続性とディザスター リカバリー (BCDR) | BCDR には、信頼性と迅速な復旧の基盤が用意されています。 | 管理する |
| デプロイ オプション | 最適なツールとテンプレートを配置し、ランディング ゾーンとサポート リソースをデプロイします。 | Ready |

## <a name="next-steps"></a>次のステップ

次の記事で説明するように、これらの設計領域は長期にわたって実装し、クラウドの運用モデルへと拡張することができます。 また、各設計領域に定義された配置から始まる、豊富なこだわりの実装オプションがあります。

モジュールの設計領域を理解したら、次の手順は、クラウドの導入計画と要件に最適な[ランディング ゾーン実装オプション](./implementation-options.md)を選択することです。

> [!div class="nextstepaction"]
> [実装オプションを選択する](./implementation-options.md)
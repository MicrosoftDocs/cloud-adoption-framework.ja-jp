---
title: 最新のコンテナー導入の戦略
description: シナリオが計画に与える影響について説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 03/01/2021
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: strategy
ms.openlocfilehash: ed78eeae296d2a2bb2c80ea6006ef8e92622709e
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101800096"
---
# <a name="strategic-impact-of-modern-containers"></a>最新のコンテナーの戦略的影響

ベスト プラクティスでは、[クラウド導入フレームワークの戦略手法](../../strategy/index.md)を使用して、一元化された単一のクラウド導入戦略を作成することを推奨しています。 まだ行っていない場合は、[戦略と計画のテンプレート](https://raw.githubusercontent.com/microsoft/CloudAdoptionFramework/master/plan/cloud-adoption-framework-strategy-and-plan-template.docx)を使用して、クラウドの導入戦略を記録します。

この記事では、戦略に影響を与えるコンテナーに関するいくつかの考慮事項について説明します。

## <a name="modern-container-motivations"></a>最新のコンテナーの動機

多くの場合、組織は、イノベーションの優先度が高い場合にコンテナーを選択します。 しかし、高度なコンポーネント化されたクラウドネイティブ アプリケーションの管理も、非常に一般的な推進理由です。 コンテナー化されていないワークロードを移行する場合で、ワークロード内の最小限の機能変更によってワークロードの移植性と環境の一貫性を得ることができる場合は、最初にワークロードをコンテナー化することも健全な選択肢である可能性があります。

Kubernetes は、組織がコンテナーの利点を活用し、コンテナー化された環境やワークロードの全体的な操作を改善しやすくするオーケストレーションのレイヤーを提供します。 Azure では、Azure Kubernetes サービス (AKS) がサービスとしてエンドツーエンドのコンテナー オーケストレーションを提供します。

## <a name="modern-container-outcomes"></a>最新のコンテナーの結果

コンテナーと Kubernetes の導入作業の影響を測定するために、次のようないくつかの重要な結果を追跡および評価できます。

- **プロビジョニングとスケーリング時間:** インフラストラクチャの弾力性。ワークロードをサポートするリソースをプロビジョニングやスケーリングするための時間を短縮します。
- **開発時間の短縮:** 一貫性のある標準化された環境で開発ツール、自動デプロイ、統合監視を組み合わせることにより、開発者は、開発環境や運用環境のインフラストラクチャの構成サポートよりも、優れた製品を構築することに集中できます。
- **ワークロードの移植性:** 共通のコンテナー化された環境を使用して、アプリケーションをどこにでも移動します。 Kubernetes クラスターと基になるインフラストラクチャの間に抽象レイヤーがあるため、開発環境と運用環境の間、またはクラウド プロバイダー間で、クラウド プロバイダーのネイティブ ソリューションよりも少ない労力で、ワークロードを移動できます。
- **安全なデプロイ プラクティス:** Kubernetes のワークロードとコンストラクトでは、多くのデプロイ方法がサポートされており、信頼性の高い方法でワークロードをロールアウトできます。
- **統合アクセス管理:** 既存の ID およびアクセス管理 (IAM) プロバイダーとクラスターの統合により、デプロイのすべての段階で安全な環境が確保されます。
- **インフラストラクチャの分離:** Kubernetes クラスターは、パブリックなクラウド ソリューションから、完全にプライベートなソリューションまでさまざまです。そのため、目的のレベルに合わせてワークロードとそのランタイム環境の公開を制御できます。
- **ネットワーク可観測性:** 必要なセキュリティ上の結果を得るために、Kubernetes クラスターに出入りするトラフィックを内部トラフィックの監視と制御の対象にすることができます。
- **人材の保有期間:** 最新のインフラストラクチャでは、使用することが非常に望ましいと考えられている、業界標準のクラウドに依存しない最新のツールを使用することにより、人材の採用や保有が改善されています。

## <a name="next-step-plan-for-modern-containers"></a>次のステップ: 最新のコンテナーの計画

次の記事の一覧では、クラウド導入のシナリオを成功させるために役立つクラウド導入の取り組みの特定のポイントについて説明します。

- [最新のコンテナーの計画](./plan.md)
- [環境または Azure ランディング ゾーンを確認する](./ready.md)
- [最新のコンテナーへのワークロードの移行](./migrate.md)
- [最新のコンテナー ソリューションを使用したイノベーション](/azure/architecture/reference-architectures/containers/aks-start-here?toc=/azure/cloud-adoption-framework/toc.json&bc=/azure/cloud-adoption-framework/_bread/toc.json)
- [最新のコンテナー ソリューションのガバナンス](./govern.md)
- [最新のコンテナー ソリューションの管理](./manage.md)

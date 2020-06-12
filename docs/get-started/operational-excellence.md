---
title: 作業を開始しましょう。オペレーショナル エクセレンスを実現する
description: デジタル変革におけるオペレーショナル エクセレンスの基本について説明します。
author: JanetCThomas
ms.author: janet
ms.date: 05/15/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: overview
ms.openlocfilehash: 9a207590049021a6bb373ab13ff30c5c26431238
ms.sourcegitcommit: 070e6a60f05519705828fcc9c5770c3f9f986de5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2020
ms.locfileid: "83814411"
---
# <a name="get-started-deliver-operational-excellence-during-digital-transformation"></a>作業を開始しましょう。デジタル変革におけるオペレーショナル エクセレンスを実現する

デジタル変革においてオペレーショナル エクセレンスを確立するにはどうすればよいのでしょうか。 オペレーショナル エクセレンスは、IT の意思決定に直接影響を与えるビジネス機能です。 オペレーショナル エクセレンスを実現するには、収益、リスク、コストへの影響に注目して、顧客と利害関係者の価値に重点を置く必要があります。

この組織変更管理アプローチには、以下が必要となります。

- 戦略の定義
- ビジネス成果の明確化
- 変更管理の計画

クラウドの観点から、導入後の変更を行い、運用プロセスを継続的に改善することによって、リスクとコストの影響を管理できます。 監視する領域には、クラウド導入ライフサイクル全体にわたるシステムの自動化、IT 運用の管理プラクティス、リソースの整合性の規範が含まれます。

この記事の手順を利用することで、戦略チームは、オペレーショナル エクセレンスを一貫して確保するために必要な組織変更管理を主導できます。

企業全体およびポートフォリオ全体のオペレーショナル エクセレンスは、組織変更管理に対する期待を調整して報告するための戦略と計画のピア プロセスから始まります。 以下の手順は、技術チームが、オペレーショナル エクセレンスの達成に必要な規範を実現するのに役立ちます。

![オペレーショナル エクセレンスの概要](../_images/get-started/operational-excellence-map.png)

## <a name="step-1-define-a-strategy-to-guide-digital-transformation-and-operational-excellence-expectations"></a>手順 1:デジタル変革とオペレーショナル エクセレンスの期待の指針となる戦略を定義する

デジタル変革およびオペレーショナル エクセレンスの取り組みの基盤となるのは明確なビジネス戦略です。 IT 部門はコストを削減し、IT プロセスを効率化できます。 明確な戦略がないと、それらの変更が、より広範な変革の取り組みで特定されたビジネス成果に及ぼす可能性のある影響を把握することが難しくなります。

**成果物:**

- [戦略と計画のテンプレート](https://archcenter.blob.core.windows.net/cdn/fusion/readiness/Microsoft-Cloud-Adoption-Framework-Strategy-and-Plan-Template.docx)に、動機、成果、業務上の正当な理由を記録します。
- 学習メトリックが十分に理解され、ビジネス成果のセクションに含まれていることを確認します。 これらのメトリックは、IT 部門内でのオペレーショナル エクセレンスのアクティビティと報告の指針となります。

**成果物の完遂をサポートするうえでのガイダンス:**

- [動機を把握する](../strategy/motivations.md): 重要なビジネス イベントや、移行の動機によっては、コストが重視される傾向があります。 これらの領域は、後のすべての作業でコスト管理の重要性を高める可能性があります。 一方、イノベーションまたは移行による成長に関連した未来志向の動機の場合、営業収益がより重視されます。 動機を理解することは、コスト管理の優先順位を決めるうえで役立ちます。
- [ビジネス成果](../strategy/business-outcomes/index.md):一部の財政上の成果では、コストが極端に重視される傾向があります。 目的の成果を財務上のメトリックに対応付ける場合は、初期段階でコスト管理ガバナンス規範に投資してください。
- [業務上の正当な理由](../strategy/cloud-migration-business-case.md): 業務上の正当な理由は、クラウド導入の財務計画全体の概要を示します。 これは、最初の予算編成に役立つ情報源となる可能性があります。
- [メトリックの学習](../strategy/learning-metrics.md):包括的なビジネス戦略とより戦術的な変更管理計画の整合性を維持するために、学習メトリックを確立します。 これらのメトリックは、計画に向けて反復的かつ段階的な進捗状況を示すように設計する必要があります。

<!-- markdownlint-disable MD033 -->
<br>

| 説明責任チーム | 実行責任チームとサポート チーム |
| --- | --- |
| <li> クラウド戦略チーム | <li> クラウド導入チーム <li> クラウド ガバナンス チーム <li> クラウド運用チーム <li> クラウドのセンター オブ エクセレンスまたは中央 IT |

## <a name="step-2-develop-an-organizational-change-management-plan-to-span-cloud-adoption"></a>手順 2:クラウド導入を拡大するための組織変更管理の計画を策定する

組織変更管理は、包括的なビジネス戦略に対応するために、人員、プロセス、テクノロジを微調整する反復的なアプローチです。 デジタル変革のためのオペレーショナル エクセレンスの場合、このアプローチは、IT 中心のクラウド導入計画を軸に行われることも少なくありません。

**成果物:**

- [戦略と計画のテンプレート](https://archcenter.blob.core.windows.net/cdn/fusion/readiness/Microsoft-Cloud-Adoption-Framework-Strategy-and-Plan-Template.docx)を更新して、目的の戦略を実現するために必要な変更を反映させます。 記録する変更には、次のようなものがあります。

  - 既存のデジタル資産の評価。
  - 必要な変更とそれに伴う作業を反映するクラウド導入計画。
  - 計画に基づいて実現する必要がある組織変更。
  - 既存のチームが必要な作業を成功させるために必要となるスキルに対処するための計画。

**成果物の完成をサポートするためのガイダンス:**

- [インベントリの収集](../digital-estate/inventory.md): 導入前に、デジタル資産を分析するためのデータ ソースを確立します。
- [ベスト プラクティス - Azure Migrate](../plan/contoso-migration-assessment.md): Azure Migrate を使用してインベントリを収集します。
- [増分型の合理化](../digital-estate/rationalize.md#incremental-rationalization):増分型の合理化を進める中で、定量分析によって、予算編成のためにクラウドの候補が特定されます。
- [コスト モデルと予測モデルの対応付け](../digital-estate/calculate.md): Azure Cost Management を使用して、[予算を作成](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets?toc=/azure/cloud-adoption-framework/toc.json&bc=/azure/cloud-adoption-framework/_bread/toc.json)することにより、コスト モデルと予測モデルを対応付けます。
- [クラウド導入計画の作成](../plan/plan-intro.md#build-your-cloud-adoption-plan): 実用的なワークロード、資産、タイムラインの詳細を含む計画を作成します。

<!-- markdownlint-disable MD033 -->
<br>

| 説明責任チーム | 実行責任チームとサポート チーム |
| --- | --- |
| <li> クラウド戦略チーム | <li> クラウド導入チーム <li> クラウド ガバナンス チーム <li> クラウド運用チーム <li> クラウドのセンター オブ エクセレンスまたは中央 IT |

## <a name="step-3-manage-change-across-cloud-adoption-efforts"></a>手順 3:クラウドの導入作業全体で変更を管理する

ビジネス成果の実現は、導入のウェーブを継続的に実現した結果です。 これらのウェーブとしては、移行サイクルとイノベーション サイクルがあります。 どちらの場合も、オペレーショナル エクセレンスは、通常の変更管理サイクルから始まります。

各ウェーブ (アジャイル用語では "リリース") では、一連のワークロードをクラウドに提供します。 導入の各ウェーブが完了すると、クラウド戦略チームは、学習メトリック、ビジネス成果、戦略全体に関する進捗状況を報告します。 同様に、導入の各ウェーブが完了すると、導入チームは、優先順位付けされたワークロードを計画に反映するためにバックログを更新する必要があります。 これらの更新は、ビジネス プランの変更と顧客のニーズの変化に基づいています。

**成果物:**

- 市場の状況の変化や最新の技術革新の波の終息に合わせた戦略および変更管理計画の継続的なテストと改善。

**成果物の完成をサポートするためのガイダンス:**

- [リリース計画](../digital-estate/approach.md): リリース計画を使用した変更管理の手法。
- [増分型の合理化](../digital-estate/rationalize.md#incremental-rationalization):反復的な変更管理手法。 管理可能な変更のウェーブをサポートするために、リリース バックログの管理に重点を置きます。
- [10 のパワー アプローチ](../digital-estate/rationalize.md#release-planning): 変更管理計画を制限します。 段階的な変更と反復的な導入作業のバランスをとるために、継続的な基盤となる 10 個のワークロードの詳細な分析と計画に重点を置きます。
- [イテレーション パスの調整](../plan/iteration-paths.md): 現在のイテレーション パスを確保するために、各リリースで詳細を更新および追加します。
- [ワークロードの評価](../migrate/azure-migration-guide/assess.md?tabs=challenge-assumptions): 最新の一連の移行優先順位を評価し、それに基づいて行動するためのクラウド導入チームの取り組み。
- [ビジネス価値の合意](../innovate/business-value.md): 新しいイノベーションの各リリースでビジネス価値を確実に一致させるためのクラウド導入チームの取り組み。

<!-- markdownlint-disable MD033 -->
<br>

| 説明責任チーム | 実行責任チームとサポート チーム |
| --- | --- |
| <li> クラウド戦略チーム | <li> クラウド導入チーム |

## <a name="value-statement"></a>バリュー ステートメント

上記の手順は、デジタル変革全体を通じてオペレーショナル エクセレンス要件を確立するためのビジネス主導型のアプローチの概要を示しています。 このアプローチは、運用モデルの他の機能を遂行する一貫した基盤を提供します。

![共有アーキテクチャの原則](../_images/shared-principles.png)

## <a name="next-steps-to-delivering-operational-excellence-across-the-portfolio"></a>ポートフォリオ全体でオペレーショナル エクセレンスを実現するための次のステップ

オペレーショナル エクセレンスには、信頼性、パフォーマンス、セキュリティ、コストの最適化のための規律あるアプローチが必要です。 このシリーズの残りのガイダンスを使用して、自動化の一貫したアプローチによってこれらの原則を実装します。

- **コストの最適化**: [エンタープライズ コストの管理](./manage-costs.md)に関する入門ガイドを使用して、運用コストを継続的に最適化します。
- **セキュリティ:** [ポートフォリオ全体でのセキュリティの実装](./security.md)に関する入門ガイドを使用して、ポートフォリオ全体のエンタープライズ セキュリティを統合することでリスクを軽減します。
- **パフォーマンス管理:** [企業全体のパフォーマンス管理](./performance.md)に関する入門ガイドを使用して、IT 資産のパフォーマンスがビジネス プロセスをサポートできるようにします。
- **信頼性:** [信頼性を創出する制御の実装](./reliability.md)に関する入門ガイドを使用して、信頼性を高め、ビジネスの中断を削減します。
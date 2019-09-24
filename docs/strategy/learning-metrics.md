---
title: 有意義な学習メトリックに取り組みを整合させる方法
titleSuffix: Microsoft Cloud Adoption Framework for Azure
description: 学習メトリックの概念の説明
author: BrianBlanchard
ms.author: brblanch
ms.date: 04/04/2019
ms.topic: guide
ms.service: cloud-adoption-framework
ms.subservice: strategy
ms.openlocfilehash: f761f85fa4b21b35e8428985707176624b92a5ec
ms.sourcegitcommit: 443c28f3afeedfbfe8b9980875a54afdbebd83a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2019
ms.locfileid: "71032079"
---
<!-- markdownlint-disable MD026 -->

# <a name="how-can-we-align-efforts-to-meaningful-learning-metrics"></a>有意義な学習メトリックに取り組みを整合させる方法

[ビジネス上の成果の概要](./business-outcomes/index.md)に関するページでは、変換がビジネスに及ぼす影響を測定し通信する方法について説明しました。 残念ながら、こうした成果の一部が測定可能な結果を生み出すまでに何年もかかかることがあります。 役員会や経営幹部は、長期間にわたる 0% デルタを示すレポートでは満足できません。

学習メトリックは、長期的なビジネスの成果へと環流できる、中期的な、より短い期間のメトリックです。 これらのメトリックは、成長の思考様式と適切に整合し、回復性が高まるようにカルチャを位置付けるのに役立ちます。 学習メトリックは、長期的なビジネス目標に対して予想される進展不足ではなく、成功の早期メトリックを浮き彫りにするものです。 このメトリックは、失敗の早期メトリックも浮き彫りにします。これにより、プランについて学び、それを調整する絶好の機会が得られる可能性が高くなります。

このフレームワークにおける素材の多くと同様に、望ましいビジネス上の成果に最も適合する[変革の過程](../govern/guides/index.md)に読者が精通していることが前提となっています。 この記事では、変換の過程ごとのいくつかの学習メトリックの概要を示し、概念について説明します。

## <a name="cloud-migration"></a>クラウド移行

この変革では、IT 運用に重点を置きながら、コスト、複雑さ、および効率に焦点を当てます。 この変換の背後にある最も簡単に測定されるデータが、クラウドへの資産の移動です。 この種類の変革では、デジタル資産は、仮想マシン (VM)、これらの VM をホストするラックまたはクラスター、データセンター運用コスト、システムを維持するための必要な資本コスト、および時間の経過に伴うこれらの資産の減価償却に基づいて測定されます。

VM がクラウドに移動されるにつれて、従来のオンプレミスの資産への依存は軽減されます。 資産の保守のコストも軽減します。 残念ながら、企業は、クラスターがプロビジョニング解除され、データセンターのリースの有効期限が切れるまでコスト削減を実現できません。 多くの場合、減価償却サイクルが完了するまで、取り組みのすべての価値は実現されません。

財務諸表を作成する前に、必ず CFO または財務部門と足並みをそろえてください。 ただし、IT チームは一般に、消費される CPU、メモリ、ストレージに基づいて、各 VM の現在の金銭的コスト値と将来の金銭的コスト値を見積もることができます。 続いて、移行される各 VM にこの値を適用して、取り組みによる直近のコスト節約と将来の金銭的価値を見積もることができます。

## <a name="application-innovation"></a>アプリケーションの刷新

クラウド対応アプリケーションの刷新は主に、カスタマー エクスペリエンスのほかに、企業から提供される製品やサービスを消費しようという顧客の意欲に重点を置いています。 変更の増分がコンシューマーや顧客の購買行動に影響するまでには時間がかかります。 ただし、アプリケーションの刷新のサイクルは、他の形の変革よりも大幅に短い傾向があります。 従来のアドバイスは、影響を与えたい特定の行動の理解から始め、それらの行動を学習メトリックとして使用するべきだということです。 たとえば、e コマース アプリケーションでは、購入合計や追加購入がターゲットの行動になります。 動画の企業では、動画ストリームの視聴時間がターゲットになり得ます。

顧客行動メトリックの問題は、外部の変数に影響されやすいという点です。 そのため、多くの場合、学習メトリックに関連する統計情報を含めることが重要です。 関連する統計情報として、リリースの周期、リリースごとに解決されたバグ、単体テストのコード カバレッジ、ページ ビュー数、ページのスループット、ページの読み込み時間、その他のアプリ パフォーマンス メトリックなどがあります。 それぞれが、コード ベースとカスタマー エクスペリエンスに対するさまざまな変化とアクティビティを示し、上位の顧客行動パターンに関連付けることができます。

## <a name="data-innovation"></a>データの刷新

業界の変化、市場の混乱、製品およびサービスの変革は、数年かかることがあります。 クラウド対応のデータ刷新の取り組みにおいて、実験が成功の判断にとって重要になります。 パーセントによる確率、失敗した実験の数、トレーニング済みモデルの量などの予測メトリックを共有することによって、透明性を確保します。 失敗は成功よりも速く累積します。 これらのメトリックは良好ではない可能性があり、データを適切に活用するために必要な時間と投資を経営陣が理解することが重要です。

反対に、データ ドリブン学習には、いくつかの肯定的なメトリックが関連付けられることがよくあります (異種データ セットの集中化、データ イングレス、データの民主化)。 チームが将来の顧客について学習している間、実際の結果は今日生成されます。 利用できる学習メトリックには、次のようなものがあります。

- 使用可能なモデルの数
- 使用されたパートナー データ ソースの数
- イングレス データを生成するデバイス
- イングレス データの量
- データの種類

さらに価値のあるメトリックは、結合されたデータ ソースから作成されるダッシュボードの数です。 この数は、新しいデータ ソースによって影響を受ける現在の状態のビジネス プロセスを反映しています。 新しいデータ ソースをオープンに共有することによって、企業は、Power BI などのレポート ツールを使用してデータを利用し、増分的分析情報を生成して、ビジネスの変化を推進できます。

## <a name="next-steps"></a>次の手順

学習メトリックの整合が済んだら、チームは、これらのメトリックに対して[デジタル資産の評価](../digital-estate/index.md)を開始できます。 結果は、[変換バックログまたは移行バックログ](../migrate/migration-considerations/prerequisites/technical-complexity.md)になります。

> [!div class="nextstepaction"]
> [デジタル資産を評価する](../digital-estate/index.md)
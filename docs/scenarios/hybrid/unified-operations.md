---
title: ハイブリッド、マルチクラウド、およびエッジの統合運用
description: ハイブリッド、マルチクラウド、およびエッジの各デプロイにわたって一貫した運用管理を実現するための効果的な制御を実装します。
author: brianblanchard
ms.author: brblanch
ms.date: 01/12/2021
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: strategy
ms.custom: e2e-hybrid
ms.openlocfilehash: 1f1385095de368d52e4a4790c0267defbc96bb80
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101801382"
---
# <a name="introduction-to-unified-operations"></a>統合運用の概要

ハイブリッド、マルチクラウド、およびエッジにわたる 1 つのクラウド ダッシュボード。

ハイブリッド、マルチクラウド、エッジのデプロイ アプローチは、多くの場合、運用コストの増加につながる可能性があります。 予期しないコストの増加は、クラウド プロバイダーごとに一組の運用プラクティスがあることで、重複または異なる運用が行われた結果です。 **統合運用** とは、一組のツールとプロセスを維持し、一組の共通するガバナンスおよび運用管理プラクティスを使用して各クラウド プロバイダーを一貫して管理するという計画的なアプローチです。

## <a name="understand-and-minimize-costs-through-unified-operations"></a>統合運用によってコストを把握して最小化する

ハイブリッドとマルチクラウド戦略では、オーバーヘッド コストにおける最初の増加は、ネットワーク、ID、ガバナンス、セキュリティ、運用ツールなど、クラウド プラットフォーム ユーティリティの重複によるものが考えられます。 長期的には、多様な環境を管理するために必要なスキルを備えた人材を主力部門やチームに配属するなどのビジネス上の課題が生じる場合があります。

ハイブリッドとマルチクラウド戦略では、多くの意思決定者が、クラウドはオンプレミス テクノロジよりコストが高いという誤った結論に導かれてきました。 Microsoft が委託した Forrester Consulting の最近の調査では、ハイブリッドとマルチクラウド戦略によって、組織の [3 年間の投資収益率の大幅な増加と、オンプレミス インフラストラクチャおよび人件費の大幅な削減](https://azure.microsoft.com/resources/forrester-tei-microsoft-azure-iaas/)を実現できることが判明しました。 さらに、アクセンチュアと Wservice による環境とエネルギーに関する主要な調査では、クラウド ソリューションによって大規模なデプロイでエネルギー効率が大幅に向上すると結論付けられました。これは、[組織のエネルギー使用量と二酸化炭素排出量が、オンプレミスにインストールされたビジネス アプリケーションと比較して 30% 以上削減され](https://download.microsoft.com/download/7/3/9/739BC4AD-A855-436E-961D-9C95EB51DAF9/Microsoft_Cloud_Carbon_Study_2018.pdf)、小規模なデプロイでは、共有クラウド サービスを使用することによって 90% 以上の削減が達成されるためです。

組織は、リスクの克服、オーバーヘッド コストの増加、主要部門への人員配置に関連する課題に対してシンプルなアプローチを使用して、全体的な運用を最新化し、最適化することができます。 **統合運用** とは、短期的な重複と技術スタッフに対する長期的な負担を軽減する、ハイブリッド、マルチクラウド、およびエッジ クラウド戦略に対するアプローチです。 この記事では、統合運用を使用して、1 つのエンタープライズ コントロール プレーンを、ハイブリッド、マルチクラウド、およびエッジの各環境に配置された分散資産へと拡張するプロバイダー ニュートラル アプローチについて説明します。

その他の記事では、統合運用に対する Azure のアプローチの概要、ハイブリッド、マルチクラウド、およびエッジの異種環境での[ガバナンス](./govern.md)と[運用管理](./manage.md)の実現について説明します。 統合運用に対する Azure 固有アプローチでの全体的な目標は、どの場所でも、どのインフラストラクチャでも、IT 資産のインベントリ作成、整理、管理を行うことです。 この一元化されたエンタープライズ コントロール プレーンによって、オンプレミス、マルチクラウド、およびエッジの各環境で一貫したクラウド運用管理エクスペリエンスが実現します。

## <a name="primary-cloud-platform"></a>プライマリ クラウド プラットフォーム

ハイブリッド、マルチクラウド、およびエッジ戦略の成功は、プライマリ クラウド プラットフォームから始まります。

![プロセスをサポートするための設備、サービス、およびコントロールを備えたプライマリ クラウド プラットフォーム。](../../_images/hybrid/primary-cloud-provider.png)

パブリックとプライベートのどちらのクラウドにあるかに関わらず、プライマリ クラウド プラットフォームは、定義された一連のクラウド設備と共に運用プロセスがホストされている場所です。 Azure では、これらの設備は [Azure リージョン](https://azure.microsoft.com/global-infrastructure/)ですが、オンプレミスではデータセンターの場合があります。 これらの設備では、中心となる運用を管理し、プラットフォームでホストされている他のワークロードをサポートするために必要なクラウド サービスがホストされています。 プライマリ クラウド プラットフォームには、そのクラウド内での運用をサポートするように設計された一連のコントロールも含まれています。

> [!NOTE]
> プライマリ クラウド プラットフォームでは、ワークロードについては、すべて、または大部分でさえホストされていない可能性がありますが、**運用管理、ガバナンス、コンプライアンス、セキュリティなどでのコア プロセスを完了するために必要なサービスとコントロールはホストされています**。
>
> [!CAUTION]
> お客様は既にプライマリ クラウド プラットフォームを使用している場合があります。 残念ながら、多くのクラウド プラットフォームは、運用でハイブリッド、マルチクラウド、またはエッジのデプロイ オプションが必要になる前に設計および構築されました。 これにより、多くの場合、お客様は、各クラウド プラットフォーム間でクラウド サービスを管理するために異なるクラウド コントロールを使用してプロセスをレプリケートしています。 クラウド戦略でハイブリッド、マルチクラウド、またはエッジのデプロイ オプションが要求され、**かつ** お使いのプライマリ クラウド プラットフォームでそれらがサポートされていない場合は、統合運用に必要な機能をデプロイできるプラットフォームを検討してください。
>

## <a name="defining-unified-operations"></a>統合運用の定義

統合運用の仕組みの概念は単純です。ハイブリッド、マルチクラウド、またはエッジのデプロイにプライマリ クラウド プロバイダーのコントロールを適用するために、拡張機能 (つまりゲートウェイ) を実装します。 オンプレミス、マルチクラウド、およびエッジの異種環境で一貫して運用を管理します。

統合運用の実装では、1 つのエンタープライズ コントロール プレーンが組織の分散された資産全体に拡張されます。それにより、あらゆる場所のあらゆるインフラストラクチャに、一貫した管理、アプリケーション開発、クラウド サービスが大規模に提供されます。 組織に対する一貫した管理とガバナンスを実現するために、そのようなクラウド コントロールを備えたゲートウェイによって、オンプレミス、マルチクラウド、およびエッジの異種環境に一貫した運用管理とデータ サービスが提供されます。

プライマリ クラウド プラットフォームを特定する際は、自分のポートフォリオに含まれるすべてのクラウドを管理するために必要なツールセットがクラウドにあることを確認することが重要です。 多くのクラウド プラットフォームは、運用でハイブリッド、マルチクラウド、またはエッジのデプロイ オプションが必要になる前に設計および構築されました。 現在の運用ツールの機能が不十分な場合、運用チームは、各クラウド プラットフォームでクラウド サービスを管理するために、さまざまなクラウド コロントロールを使用してプロセスをレプリケートする必要がある場合があります。 クラウド戦略でハイブリッド、マルチクラウド、またはエッジのデプロイ オプションが要求され、**かつ** お使いのプライマリ クラウド プラットフォームでそれらがサポートされていない場合は、統合運用に必要な機能をデプロイできるプラットフォームを検討してください。

## <a name="unified-operations"></a>統合運用

大規模な分散された資産のポートフォリオ全体で 1 つのクラウド管理と運用エクスペリエンス (一貫したガバナンス、管理、アプリケーション開発、およびクラウド サービスを、あらゆる場所のあらゆるインフラストラクチャに提供する) を使用することで、組織の将来のイノベーション、機敏性、およびビジネス成長を向上させることができる統合されたハイブリッドおよびマルチクラウド戦略が実現します。 管理とデータのサービスをオンプレミス、マルチクラウド、およびエッジに拡張するクラウド コントロールのゲートウェイを追加することにより、組織にとって一貫した管理とガバナンス、および組織の将来のイノベーション、機敏性、ビジネス成長を向上させることができる不可欠なハイブリッドおよびマルチクラウド戦略がどこでも可能になります。 ハイブリッド、マルチクラウド、またはエッジのデプロイにプライマリ クラウド プロバイダーのコントロールを適用するために、拡張機能 (ゲートウェイ) を実装します。

![統合運用では、クラウド コントロールがハイブリッド、マルチクラウド、エッジのデプロイに拡張される](../../_images/hybrid/primary-cloud-provider-extended.png)

> [!WARNING]
> 統合運用の実装は、比較的容易な場合があります。 ただし、お使いのクラウド プラットフォームで、必要となる主要な統合運用プロセスを管理できない場合は、他のクラウドへの拡張機能 (ゲートウェイ) を作成するための費用のかかる開発に伴い、追加の設備投資が必要になります。 お客様が重複または分割された運用とプロセスを作成する理由の主な制約要因は、このような制限がある既存のプライマリ クラウド プラットフォームです。
>
> 統合運用の実装に対して一貫性のないアプローチを取ることで、(重複するクラウド プラットフォーム ユーティリティや運用ツールによって) 運用コストが増加し、(必要なクラウド スキルを持たないチームが配属されることで) ビジネスに悪影響があるなど、組織でコストの非効率性が増加します。
>

現在のプライマリ クラウド プロバイダーによって統合運用に必要な機能が提供されない場合は、最新のクラウド プロバイダーを使用して運用とプロセスを最適化することを検討してください。

## <a name="unified-operations-decomposed"></a>分解された統合運用

この図では、統合運用に必要な個々のコンポーネントを表示し、それらがどのように相互に作用しているかを示しています。 次のセクションでは、統合運用の各コンポーネントについて詳細な概要を提供します。

![統合運用を実現するために必要なコンポーネントを示すインフォグラフィック (この記事の残りの部分で説明)](../../_images/hybrid/unified-operations.png)

## <a name="customer-processes"></a>顧客プロセス

統合運用の主な目的は、複数のデプロイにわたって、できるだけ多くのプロセスの一貫性を作成することです。 ハイブリッド、マルチクラウド、エッジのすべてのデプロイで、100% の機能パリティを達成できるクラウド サービス プロバイダーは存在しません。 ただし、プロバイダーはすべてのデプロイで共通するベースライン機能セットを提供して、[ガバナンス](./govern.md)と[運用管理](./manage.md)のプロセスで一貫性を確保できるようにする必要があります。

![統合運用でサポートできる顧客プロセス](../../_images/hybrid/unified-operations-customer-processes.png)

通常、顧客は、定義されているガバナンスおよび運用管理プロセス内で一貫性を提供できる必要があります。 長期的な要件を満たすために、統合運用ソリューションは、以下に示すこれらの共通プロセスに合うようにスケーリングできる必要があります。

### <a name="common-governance-processes-tasks"></a>共通のガバナンス プロセス (タスク)

- **コスト管理:** コストを表示、管理、または最適化し、**クラウドに関連した IT 支出リスクの軽減ガイダンスを特定して提供します**。
- セキュリティ ベースライン: 推奨されるセキュリティ コントロールからの要件を監査、適用、または自動化し、**セキュリティに関連したビジネス リスクの軽減ガイダンスを提供します**。
- **リソースの整合性:** リソースとサービスをオンボード、整理、および構成し、**潜在的なビジネス リスクに対するリスク軽減ガイダンスを提供します**。
- **ID ベースライン:** ユーザーの ID とアクセスに対する認証と承認を実施し、**潜在的な ID に関連したビジネス リスクに対するリスク軽減ガイダンスを提供します**。
- **デプロイの高速化:** (デプロイ、構成の配置、再利用可能な資産に対して) テンプレート、自動化、パイプラインを使用し、**準拠しており、整合性があり、反復可能なリソースのデプロイと構成を確保するためのポリシーを確立することによって** 一貫性を推進します。

### <a name="common-operations-management-processes-tasks"></a>共通の運用管理プロセス (タスク)

- **インベントリと可視性:** すべての資産を考慮し、そのレポート作成を確保し、**エンタープライズレベル環境でインベントリの実行状態を収集して監視します**。
- **最適化された運用:** サポートされているリソースを追跡、修正、最適化し、**一貫性のない修正プログラム管理による構成のずれや脆弱性に起因するビジネス中断リスクを最小限に抑えます**。
- **保護とリカバリー:** バックアップ、ビジネス継続性、ディザスター リカバリーのベストプラクティス、および **予防不可能な停止の期間と影響を軽減します**。
- [プラットフォームの運用](../../manage/azure-management-guide/platform-specialization.md): (重大度が中から高のワークロードを対象とする) SQL、WVD、SAP などの共通テクノロジ プラットフォームに対する専門の運用。
- [ワークロードの運用](../../manage/azure-management-guide/workload-specialization.md): (優先度が高くミッションクリティカルなワークロードを対象とする) 高度な運用が要求される専門の運用。

プラットフォームとワークロードの運用はどちらも、同等の "*反復プロセス*" を実行して、**システム設計を改善し、修復を自動化し、サービス カタログを使用して変更をスケーリングし、システム設計、自動化、およびスケーリングを継続的に改善します**。

プライマリ クラウド プラットフォームでは、プロセスを自動化し、ガバナンスと運用管理に関する前述の目標を達成するために必要な技術的機能とツールを提供できる必要があります。 統合運用ソリューションを使用すると、ハイブリッド、マルチクラウド、エッジのすべてのデプロイにこれらのプロセスを拡張できます。

## <a name="primary-cloud-controls"></a>プライマリ クラウド コントロール

プライマリ クラウド プラットフォームには、クラウドで一般的に必要とされる顧客プロセスを容易にしたり自動化したりするためのいくつかの重要な機能が含まれている必要があります。

![次の箇条書きに記載された共通のクラウド コントロール](../../_images/hybrid/unified-operations-cloud-controls.png)

### <a name="basic-features"></a>基本機能

大規模にクラウド導入計画を提供するためには、これらのすべての基本機能が必要です。

- デプロイされたすべての資産を **検索、インデックス作成、グループ化、タグ付け** して、基本の可視性と管理を拡張します。
- 一貫性のあるデプロイのために **ツールをテンプレート化、自動化、および拡張** します。
- **アクセスおよびセキュリティ境界を作成して**、デプロイされた資産を保護します。

### <a name="enhanced-features"></a>拡張機能

多くの場合、ハイブリッドとマルチクラウド環境を大規模に運用するためには、次の拡張機能のほとんどが必要になります。

- **パフォーマンスとインベントリのレポート作成**
- **セキュリティとコンプライアンスの監査と自動化**
- **アプリケーションと依存関係の追跡とレポート作成**

### <a name="automated-controls"></a>自動コントロール

運用を最新化し運用コストを最適化するツールを使用して環境を自動化します。

- **環境とゲスト内のポリシー**
- **構成と更新**
- **保護と回復**

多くの場合、これらの機能は、現在プライマリ クラウド プロバイダーを運用するために使用しているコントロール セットに既に含まれています。 そのコントロール セットには、多くの追加機能と自動プロセスが含まれている可能性があります。 それらは、統合運用ソリューションでハイブリッド、マルチクラウド、エッジにわたって利用できる必要がある主要なコントロール機能です。

これらの機能が主要なコントロールとして実装されているため、上記の機能によって、通常、分割または重複する運用が発生します。 前述のように、統合運用の実装に対して一貫性のないアプローチを取ることによって、運用コストの増加 (たとえば、重複するクラウド プラットフォーム ユーティリティや運用ツールなど) による影響を受けたり、組織のコスト効率が低下したり、クラウド導入体験の初期段階で大きな資本支出が発生したりする可能性があります。

### <a name="hybrid-multicloud-gateway-and-enterprise-control-plane"></a>ハイブリッド、マルチクラウドのゲートウェイおよびエンタープライズ コントロール プレーン

プライマリ クラウド コントロールを拡張するには、拡張機能 (ゲートウェイ) を構成する必要があります。 この種類の拡張機能を使用すると、コントロールでは、クラウド プラットフォームの外部にデプロイされているリソースを表示および操作できるようになります (**実際には、1 つのコントロール プレーンを作成し、異種環境での可視性を向上させます**)。

Microsoft のクラウド プラットフォームである [**Azure Arc**](/azure/azure-arc/overview) はその拡張機能です。 Azure Arc では、Azure クラウドの管理に使用される同じコントロールとプロセスが、他のパブリックおよびプライベート クラウドとエッジに拡張されます。 これらのクラウド コントロールによって、オンプレミス、マルチクラウド、およびエッジの異種環境における一貫したガバナンスと運用管理プロセスに対する統合運用アプローチが可能になります。

統合運用により、Azure の "オペレーティング システム" である [**ARM**](/azure/azure-resource-manager/management/overview) (Azure Resource Manager) の範囲が拡張されます。 ARM は Azure の外部に到達して、Azure 内に散在するリソースを射影し、それらを第一級市民として表現します。 Azure のサービスと管理をあらゆる種類のインフラストラクチャに導入することで、統合運用アプローチによって Azure の範囲が拡張されて、新しいハイブリッドおよびマルチクラウド ソリューションが実現されます。

統合運用アプローチを使用すると、一元化された可視性、運用、およびコンプライアンスによって、すべての環境をどこからでも整理、管理、およびセキュリティで保護することができます。 デプロイから監視まで、標準化されたアプリケーション サービスを使用して、あらゆる場所で大規模にクラウド アプリケーションを構築できます。 常に最新状態の Azure Arc 対応サービスを使用して、Azure サービスをあらゆる場所で、素早く、一貫して、大規模にデプロイできます。

ガバナンスと運用管理で一貫性のあるコントロールとプロセスを使用して従来型、クラウド ネイティブ、および分散型のエッジ アプリケーションを構築、運用、管理することで、散在している資産にクラウド イノベーションを適用できます。 新しいハイブリッドとマルチクラウドのシナリオは、簡素化された管理と高速化されたアプリケーション開発、および IT 資産全体にわたる、あらゆるインフラストラクチャのすべてのリソース環境に拡張される一貫性のある Azure サービスから引き出すことができます。

標準化、相互運用性、コンプライアンスに焦点を当てた一元的な Azure コントロール プレーンにより、ハイブリッドおよびマルチクラウド インフラストラクチャ全体で一貫性のある可視性と統一されたガバナンスおよび運用管理が可能になります。これにより、生産性を向上させ、リスクを軽減し、組織におけるクラウドの導入と移行プラクティスおよびテクノロジを推進できます。

## <a name="next-steps"></a>次のステップ

ハイブリッドとマルチクラウド体験を開始するには、まず、[ハイブリッドとマルチクラウドの戦略に関する記事](./strategy.md)をご覧ください。

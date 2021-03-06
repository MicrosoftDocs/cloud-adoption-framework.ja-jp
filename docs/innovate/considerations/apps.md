---
title: デジタル発明のためのアプリケーションを介したエンゲージ
description: データを形にし、顧客を引き付けてイノベーションを支援するエクスペリエンスを生み出すアプリケーション ソリューションを作成する方法について説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 10/17/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: innovate
ms.custom: internal
ms.openlocfilehash: 1cb3e460efa4f49f2c2d0146835aed19aa7e4aba
ms.sourcegitcommit: 9e4bc0e233a24642853f5e8acbeb9746b2444024
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "102115018"
---
# <a name="engage-via-applications"></a>アプリケーションを介したエンゲージ

「[データの民主化](./data.md)」で説明されているように、データは新しい "石油" です。 データは、デジタル経済のほとんどのイノベーションの燃料です。 この例えで言うと、アプリケーションは、必要とする人々に燃料を届けるために必要な給油所であり、インフラストラクチャもあります。

場合によっては、データだけでも、変化を促し顧客のニーズを満たすには十分です。 しかし、一般的には、顧客のニーズに対するソリューションには、データを形にしてエクスペリエンスを生み出すアプリケーションが必要です。 アプリケーションはユーザーを引き入れるための方法であり、顧客のトリガーに応えるために必要なプロセスのホームです。 アプリケーションは、顧客がデータを提供し、ガイダンスを受け取る方法です。 この記事では、検証予定の仮説に基づいて適切なアプリケーション ソリューションを組み立てるのに役立つ、いくつかの原則をまとめます。

![アプリケーションを介したエンゲージ](../../_images/innovate/engage-via-apps.png)

## <a name="shared-code"></a>共有コード

顧客からのフィードバック、市場の変化、イノベーションの機会により迅速かつ正確に反応できるチームは、通常、それぞれの市場でイノベーションをリードします。 革新的なアプリケーションの最初の原則は、[グロース マインドセットの概要](./learn.md#growth-mindset)に関する記事の「コードを共有する」にまとめられています。 時がたつにつれて、カルチャへのフォーカスからイノベーションが生まれます。 イノベーションを維持するには、多様な視点と貢献が必要になります。

イノベーションに備えるために、すべてのアプリケーション開発を共有コード リポジトリから始める必要があります。 コード リポジトリを管理するために最も広く採用されているツールは [GitHub](https://guides.github.com) です。このツールでは、共有コード リポジトリをすばやく作成できます。 または、[Azure Repos](/azure/devops/repos/get-started/what-is-repos) は、コードの管理に使用できる Azure DevOps Services のバージョン管理ツールのセットです。 Azure Repos では、次の 2 種類のバージョン管理が提供されています。

- [Git](/azure/devops/repos/get-started/what-is-repos#git):分散バージョン管理。
- [Team Foundation バージョン管理 (TFVC)](/azure/devops/repos/get-started/what-is-repos#tfvc):集中バージョン管理。

## <a name="citizen-developers"></a>市民開発者

プロ開発者はイノベーションに欠かせない存在です。 仮説が大筋で正しいことが証明されたら、大規模なソリューションを安定させて準備するためにプロ開発者が必要とされます。 この記事で述べる原則のほとんどには、プロ開発者のサポートが必要です。 残念ながら、現在のトレンドでは、開発者よりプロ開発者の需要が多いことが示されています。 さらに、プロフェッショナル開発が要求されれば、イノベーションのコストとペースはいっそう不十分になる可能性があります。 これらの課題に対し、市民開発者は、開発作業を拡大し、初期仮説の検証を迅速化する手段を提供します。

アプリケーション インターフェイスのための [Power Apps](/powerapps/powerapps-overview)、プロセスと予測のための [AI Builder](/powerapps/use-ai-builder)、ワークフローのための [Microsoft Power Automate](/power-automate/)、データ利用のための [Power BI](/power-bi/) といったツールを使用して初期仮説を検証できる場合、市民開発者を利用することが実用的で効果的な可能性があります。

> [!NOTE]
> 仮説のテストを市民開発者に頼るときは、プロ開発者がサポート、レビュー、ガイダンスを提供できるようにしておくことが推奨されます。 仮説が大筋で検証されたら、より堅牢なプログラミング モデルにアプリケーションを移行するプロセスによって、イノベーションの成果をさらに得られるようになります。 初期のプロセス定義にプロ開発者が関与すれば、後々の移行をよりクリーンにできる可能性があります。

## <a name="intelligent-experiences"></a>インテリジェントなエクスペリエンス

インテリジェントなエクスペリエンスとは、最新の Web アプリケーションのスピードとスケールに、Cognitive Services やボットのインテリジェンスを融合したものです。 これらの各テクノロジ単独でも、顧客のニーズを満たすには十分かもしれません。 しかし、スマートに組み合わせれば、デジタル エクスペリエンスによって満たすことのできるニーズの範囲を広げながら、開発コストを抑えることができます。

### <a name="modern-web-apps"></a>最新の Web アプリ

顧客のニーズを満たすためにアプリケーションまたはエクスペリエンスが必要なとき、最速の方法は最新の Web アプリケーションです。 最新の Web エクスペリエンスは、内部または外部の顧客をすばやく引き付けることができ、ソリューションのイテレーションを迅速化します。

### <a name="infusing-intelligence"></a>インテリジェンスを使用する

機械学習と AI は、開発者にとってますます利用しやすくなっています。 予測機能を備えた共通 API を広く利用できるようになり、データや予測へのアクセスが広がったことで、開発者は、より良く顧客のニーズを満たすことができます。

ソリューションにインテリジェンスを追加することで、音声テキスト変換、テキスト翻訳、Computer Vision、さらに画像検索が可能になります。 これらの拡張された機能によって、開発者はより簡単に、インテリジェンスを利用してインタラクティブな最新エクスペリエンスを提供するソリューションを構築できます。

### <a name="bots"></a>ボット

ボットは、コンピューターを使用しているという感覚が薄く、人 (少なくとも知的なロボット) とやり取りしているように感じられるエクスペリエンスを提供します。 もう人が直接介入する必要がないような、繰り返し発生する単純なタスク (ディナーの予約やプロファイル情報の収集など) を自動化されたシステムに移行するために使用できます。 ユーザーは、テキスト、インタラクティブ カード、および音声を使ってボットと会話します。 ボットとの対話では、簡単な質問と回答や、サービスへのアクセスをインテリジェントに提供する洗練された会話などが可能です。

ボットは、最新の Web アプリケーションによく似ていて、インターネットに接続し、API を使ってメッセージを送受信します。 ボットの機能は、ボットの種類によって大きく異なります。 最新のボット ソフトウェアでは、さまざまなテクノロジーとツールを利用して、さまざまなプラットフォーム上でより複雑なエクスペリエンスを提供しています。 一方、シンプルなボットでは、コードをほとんど使わずに、メッセージを受信し、そのメッセージをそのままユーザーに返すことができます。

ボットは、ファイルの読み取りと書き込み、データベースや API の使用、一般的な計算タスクの処理といった、他の種類のソフトウェアと同じ操作を実行できます。 ボットの特徴は、人と人のコミュニケーションによく見られるメカニズムを使用する点にあります。

## <a name="cloud-native-solutions"></a>クラウドネイティブ ソリューション

クラウドネイティブ アプリケーションは一から構築され、クラウドの規模やパフォーマンスに合わせて最適化されます。 クラウドネイティブ アプリケーションは、通常、マイクロサービス、サーバーレス、イベントベース、またはコンテナーベースのアプローチを使用して構築されます。 一般に、クラウドネイティブ ソリューションでは、マイクロサービス アーキテクチャ、マネージド サービス、継続的デリバリーの組み合わせを使用することによって、信頼性が実現され、市場投入までの時間が短縮されます。

クラウドネイティブ ソリューションにより、集中型の開発チームは、モノリシックな集中型ソリューションを必要とすることなく、ビジネス ロジックの制御を維持できます。 このようなソリューションは、市民開発者と最新エクスペリエンスの入力の一貫性を推進する要としても機能します。 最後に、クラウドネイティブ ソリューションでは、市民開発者とプロフェッショナル開発者に、できるだけ阻害されずに安全にイノベーションを起こす自由を与えることで、イノベーションが加速されます。

## <a name="innovate-through-existing-solutions"></a>既存のソリューションによるイノベーション

多くの顧客仮説は、既存のソリューションを最新化したバージョンによって最も良く実現できます。 現在のビジネス ロジックで顧客のニーズが (ほぼ) 満たされている場合、最新化したソリューションを基盤に構築することで、イノベーションを加速できる場合があります。

アプリケーションのわずかなリファクタリングなど、ほとんどの形式の最新化はクラウド導入フレームワークの[移行方法論](../../migrate/index.md)に含まれています。 その方法論により、クラウド導入チームが[デジタル資産](../../digital-estate/index.md)をクラウドに移行するプロセスがガイドされます。 [Azure 移行ガイド](../../migrate/azure-migration-guide/index.md)では、同じ方法論に対して、少数のワークロードや単一のアプリケーションにも適した合理化されたアプローチを提供しています。

ソリューションの移行と最新化が完了したら、さまざまな方法でソリューションを使用して、新しい革新的なソリューションを作成し、顧客のニーズに応えることができます。 たとえば、[市民開発者](#citizen-developers)が仮説を検証したり、プロフェッショナル開発者が[インテリジェントなエクスペリエンス](#intelligent-experiences)や[クラウドネイティブ ソリューション](#cloud-native-solutions)を作成したりできます。

### <a name="extend-an-existing-solution"></a>既存のソリューションを拡張する

ソリューションの拡張は、最新化の一般的な形式の 1 つです。 顧客仮説が次の条件を満たす場合、このアプローチによって最速でイノベーションを実現できる可能性があります。

- 既存のビジネス ロジックが既存の顧客ニーズを (ほぼ) 満たしている。
- エクスペリエンスの改善によって、特定の顧客群のニーズ満足度が高まる。
- 実用最小限の製品 (MVP) ソリューションに必要なビジネス ロジックが集中化されている。これは通常、[n 層](/azure/architecture/guide/architecture-styles/n-tier)、Web サービス、API、または[マイクロサービス](/azure/architecture/guide/architecture-styles/microservices)設計によって実現されます。 このアプローチでは、クラウドでホストされる新しいエクスペリエンスで既存のソリューションをラップします。 Azure では、このソリューションは Azure App Service で運用される見込みです。

### <a name="rebuild-an-existing-solution"></a>既存のソリューションを再構築する

アプリケーションを簡単に拡張できない場合、ソリューションのリファクタリングが必要になることがあります。 このアプローチでは、ワークロードはクラウドに移行されます。 アプリケーションを移行した後、その一部を Web サービスまたは[マイクロサービス](/azure/architecture/guide/architecture-styles/microservices)として変更または複製し、既存のソリューションと並行してデプロイします。 並列サービスベースのソリューションは、拡張されたソリューションと同様に扱うことができます。 このソリューションでは、クラウドでホストされる新しいエクスペリエンスで既存のソリューションを単にラップします。 Azure では、このソリューションは Azure App Service で運用される見込みです。

> [!CAUTION]
> ソリューションのリファクタリングや再設計、またはビジネス ロジックの一元化は、顧客価値を生み出すのではなく、時間を消費する[技術的スパイク](./build.md#reduce-complexity-and-delay-technical-spikes)をすぐに引き起こす可能性があります。 これは、イノベーションにとって、特に仮説検証の初期においてはリスクになります。 ソリューションの設計をわずかに創造的にするだけで、既存のソリューションのリファクタリングを必要としない MVP への道が開けるはずです。 初期仮説を大筋で検証できるまでは、リファクタリングを遅らせるのが賢明です。

## <a name="operating-model-innovations"></a>運用モデルのイノベーション

アプリケーションを作成するための最新の革新的なアプローチに加えて、アプリケーションの運用においても注目すべきイノベーションがあります。 これらのアプローチによって、多くの組織に変化が生じました。 最も顕著なものの 1 つは、[クラウドのセンター オブ エクセレンス](../../organize/cloud-center-of-excellence.md)運用モデルです。 優れた人員が揃い、成熟したビジネス チームには、ソリューションに対して独自の運用サポートを提供するという選択肢があります。

クラウドのセンター オブ エクセレンスにみられる、このようなセルフサービス型の運用管理モデルでは、ソリューション環境内で制御を厳格化し、イテレーションを迅速化することができます。 これらの目標は、運用管理と説明責任をビジネス チームに移管することによって達成されます。

既存のソリューションのグローバル需要をスケーリングまたは充足しようとするのであれば、顧客仮説の検証にはこのアプローチで十分かもしれません。 ソリューションを移行して若干最新化した後、ビジネス チームはそれを拡張してさまざまな仮説をテストできます。 これらには、一般に、パフォーマンス、グローバル配信、および IT 運用によって妨げられているその他の顧客ニーズに関心を持つ顧客コーホートが含まれます。

## <a name="reduce-overhead-and-management"></a>オーバーヘッドと管理を削減する

ソリューション内で保守するものが多ければ多いほど、ソリューションのイテレーションには時間がかかります。 これは、利用可能な帯域幅に対する運用の影響を減らすことで、イノベーションを加速できることを意味します。

革新的なソリューションを提供するために必要な多くのイテレーションに備えるには、先を読むことが重要です。 たとえば、サーバーレス オプションを優先することによって、プロセス初期の運用負担を最小化します。 Azure では、[Azure App Service](/azure/app-service/overview) や[コンテナー](/azure/containers/)をサーバーレス アプリケーションの選択肢に含めることができます。

これと並行して、Azure では、同じくオーバーヘッドを削減するサーバーレスのトランザクション データという選択肢が提供されます。 [Azure 製品カタログ](/azure/) には、完全なデータ プラットフォームを必要とせずにデータをホストするためのデータベース オプションが用意されています。

## <a name="next-steps"></a>次のステップ

仮説とソリューションにもよりますが、この記事の原則は、MVP の定義を満たしてユーザーを引き付けるアプリケーションの設計に役立てることができます。 次に紹介する[導入の強化](./ci-cd.md)の原則では、アプリケーションとデータをより速く効率的に顧客のもとに届ける方法を示します。

> [!div class="nextstepaction"]
> [導入の強化](./ci-cd.md)

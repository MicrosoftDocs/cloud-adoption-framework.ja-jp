---
title: AI アプリケーション
description: Microsoft Azure Cognitive Services を利用して、アプリケーションに AI を導入します。
author: v-hanki
ms.author: janet
ms.date: 07/14/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: innovate
ms.custom: think-tank
ms.openlocfilehash: a147a8b5eef8c5cc5b80310e6555c80b95d10c15
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101789288"
---
# <a name="ai-applications-and-agents"></a>AI アプリケーションとエージェント

アプリケーションへの AI の導入は、困難かつ時間がかかる作業になる場合があります。 最近までは、機械学習を深く理解したうえで、データの取得、モデルのトレーニング、一括でのデプロイを行うために数カ月をかけて開発する必要がありました。 それでも、成功は保証されていませんでした。 その道のりには、阻害要因、注意事項、また、AI 投資の価値をチームが実感できなくなる落とし穴が数多くありました。

## <a name="ai-applications"></a>AI アプリケーション

Microsoft Azure Cognitive Services では、これらの課題が取り除かれ、生産性、エンタープライズ対応、および信頼性が高くなるように設計されています。 独自のモデルを構築してデプロイしなくても、AI の最新の進歩に合わせて構築することが可能になります。それどころか、大規模なデータ サイエンス チームを設けなくても、見る、聞く、話す、理解する、さらには推論を始めるアプリケーションを迅速に作成できるように、数行の簡単なコードだけを使用して AI モデルをデプロイすることが可能になっています。

AI アプリケーションの一般的なシナリオには、以下が含まれます。

- センチメント分析
- オブジェクトの検出
- 翻訳
- パーソナル化
- ロボット プロセスの自動化

開始時に、以下のチェックリストとリソースを使用するとアプリケーションの開発とデプロイを計画するのに役立ちます。

- Azure Cognitive Services 内で提供されている多数の機能とサービスについて、特に使用する予定のものに関してを詳しく理解していますか。
- これらのモデルをトレーニングしてカスタマイズするカスタム データがあるかどうかを判断します。 カスタマイズ可能な Cognitive Services があります。
- Azure Cognitive Services を使用する複数の方法があります。 SDK と REST API 両方の起動と実行に関するクイックスタート チュートリアルを確認します。 注: Cognitive Services SDK は、C# 、Python、Java、JavaScript、および Go を含む、多くの一般的な開発言語で利用できます。
- これらの Cognitive Services をコンテナーにデプロイする必要があるかどうかを判断します。

## <a name="ai-applications-checklist"></a>AI アプリケーションのチェックリスト

開始するには、最初に、Azure Cognitive Services 内のさまざまなカテゴリおよびサービスについて理解します。 製品ページを参照して詳細を確認し、デモを操作して視覚、音声、言語、意思決定など、利用可能な機能について詳しく把握します。 また、一般的なシナリオを紹介し、Cognitive Services を利用して最初のアプリケーションを作成する方法について示した電子書籍もあります。

- [Cognitive Services](/azure/cognitive-services/what-are-cognitive-services)
- [製品/サービス全体の対話型デモのページ](https://azure.microsoft.com/services/cognitive-services/)
- [コグニティブ API を使用してインテリジェントなアプリを構築する](https://azure.microsoft.com/resources/building-intelligent-apps-with-cognitive-apis/) (電子書籍)

視覚、言語、音声、意思決定、または Web 検索全体に使用するサービスを選択します。 REST API または SDK のどちらを使用する場合でも、ページの各カテゴリでは、一連のクイック スタート、チュートリアル、攻略ガイドが提供されています。

<!-- docutune:casing "Intelligent Kiosk" -->

また、インテリジェント キオスクをダウンロードし、これらのサービスを体験してデモ実行することもできます。

- [Cognitive Services のドキュメント](/azure/cognitive-services/)
- [コグニティブ API を使用してインテリジェントなアプリを構築する](https://azure.microsoft.com/resources/building-intelligent-apps-with-cognitive-apis/) (電子書籍)
- [インテリジェント キオスクをインストールして Cognitive Services 機能について理解する](https://github.com/Microsoft/Cognitive-Samples-IntelligentKiosk)

詳細については、Azure Cognitive Services のコンテナー サポートに関する以下のページを参照してください。

- [Azure Cognitive Services でのコンテナーのサポート](/azure/cognitive-services/cognitive-services-container-support)

AI ソリューションの以下の参照アーキテクチャを確認してください。

- [AI + 機械学習](/azure/architecture/browse/#ai--machine-learning)

## <a name="ai-agents"></a>AI エージェント

Microsoft の Azure AI プラットフォームでは、開発者がプロジェクトを変革し推進できるように支援することを目的としています。 具体的には、会話型 AI のために、Azure では Azure Bot Service および Bot Framework SDK とツールが用意されており、開発者はこれらを使用して豊富な会話エクスペリエンスを構築できます。 さらに、開発者は Language Understanding (LUIS)、QnA Maker、Speech サービスなどの Azure Cognitive Services (API として使用可能なドメイン固有の AI サービス) を使用して、チャットボットがエンド ユーザーの発話を理解して会話できるようにする機能を追加できます。

会話 AI やチャットボットのソリューションが使用される一般的なシナリオを以下に示します。

- 情報提供 Q&A チャットボット
- カスタマー サービスまたはサポート チャットボット
- IT ヘルプ デスクまたは HR チャットボット
- eコマースまたはセールス チャットボット
- 音声対応デバイス

> [!NOTE]
> Microsoft では、コードが不要かわずかなコードしか使用しないエクスペリエンスでチャットボットを構築したいと考えている開発者向けに、Bot Framework 上に構築された Power Virtual Agents を提供しています。 また、開発者は、自分でボットをホストしたり、Cognitive Services を使用して自然言語やその他の AI モデルを制御したりする必要はありません。

## <a name="ai-agents-checklist"></a>AI エージェントのチェックリスト

Azure Bot Service と Microsoft Bot Framework についての理解を深めます。

- Bot Framework は、SDK (C#、JavaScript、Python、Java で使用可能) を提供するオープンソース オファリングであり、開発者によるボットの設計、構築、およびテストを支援します。 また、Bot Framework Composer での無料のビジュアル作成キャンバスと、Bot Framework Emulator でのテスト ツールも提供されています。
- Azure Bot Service は Azure 内の専用サービスで、これを使用することにより、お客様は Azure でボットをホストまたは公開したり、人気のあるチャネルに接続したりできます。

- [Azure Bot Service と Bot Framework の概要](/azure/bot-service/bot-service-overview-introduction)を読む
- [ボット設計の原則](/azure/bot-service/bot-service-design-principles)について確認する
- [Bot Framework SDK とツールの最新バージョン](/azure/bot-service/what-is-new)を入手する

作業を開始する最も簡単な方法の 1 つは、Azure Cognitive Services の一部である QnA Maker を使用することです。これを使用すると、FAQ ドキュメントや Web サイトをインテリジェントに変換して、Q&A エクスペリエンスを数分で作成できます。

- [QnA Maker を使用して Q&A 機能を備えたボットを迅速に作成する](/azure/bot-service/bot-builder-tutorial-add-qna)
- [QnA Maker サービス](https://www.qnamaker.ai/)をテストする

ボット開発用の Bot Framework SDK とツールをダウンロードして使用します。

- [Bot Framework Composer の 5 分間のクイック スタート](/composer/)
- [Bot Framework SDK でボットを構築してテストする (C#、JavaScript、Python)](/azure/bot-service/dotnet/bot-builder-dotnet-sdk-quickstart)

Cognitive Services を追加してボットをさらにインテリジェントにする方法を学習します。

- [AI アプリケーションを構築するための開発者ガイド](https://www.oreilly.com/library/view/a-developers-guide/9781492080619/) (電子書籍)
- [Cognitive Services](/azure/cognitive-services/) の詳細を確認する

Bot Framework ソリューション アクセラレータを使用して独自の仮想アシスタントを構築する方法と、カレンダー、電子メール、目的地、To Do などの一般的なスキルのセットを選択する方法について学習します。

- [Bot Framework の仮想アシスタント ソリューション](https://microsoft.github.io/botframework-solutions/index)

## <a name="next-steps"></a>次のステップ

その他の AI ソリューション カテゴリを調べる:

- [機械学習](./machine-learning.md)
- [ナレッジ マイニング](./knowledge-mining.md)

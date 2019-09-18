---
title: ビジネス変更プランを開発するためのガイダンス
titleSuffix: Microsoft Cloud Adoption Framework for Azure
description: ワークロードをクラウドに移行するタスクに重点を置いたクラウド移行内のプロセス。
author: BrianBlanchard
ms.author: brblanch
ms.date: 04/04/2019
ms.topic: guide
ms.service: cloud-adoption-framework
ms.subservice: migrate
ms.openlocfilehash: 44296faa9b5be56988babe9e0a847564d51148c3
ms.sourcegitcommit: a26c27ed72ac89198231ec4b11917a20d03bd222
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2019
ms.locfileid: "70839061"
---
# <a name="business-change-plan"></a>ビジネス変更プラン

従来、IT は新しいワークロードのリリースを監視してきました。 データセンターの移行やクラウドへの移行などの大きな変革時に、IT リード導入の類似パターンを適用できます。 ただし、従来のアプローチでは、追加のビジネス価値を実現する機会を逃す可能性があります。 このため、移行したワークロードを実稼働に昇格する前に、ユーザー導入への広範なアプローチの実装をお勧めします。 この記事では、ビジネス変更プランを標準ユーザー導入プランに追加する方法について説明します。

## <a name="traditional-user-adoption-approach"></a>従来のユーザー導入アプローチ

ユーザー導入プランは、ユーザーが新しいテクノロジを導入したり、特定のテクノロジを変更したりする方法に重点を置いています。 このアプローチは、ユーザーに新しいツールを紹介する場合に長年の実績があります。 一般的なユーザー導入プランでは、IT は、ビジネス環境に取り込まれる技術的変更に関連付けられているインストール、構成、保守、トレーニングに重点を置きます。

アプローチはさまざまに異なることがありますが、ほとんどのユーザー導入プランには汎用的なテーマが存在します。 これらのテーマは一般に、段階的な改善に合わせたリスク コントロールと円滑化のアプローチに基づきます。 次の図に示す Eason Matrix は、さまざまな導入の種類についてそれらのテーマの背後にある推進力を表します。

![ユーザー導入の懸念事項の Eason Matrix](../../../_images/eason-matrix.jpg)

*ユーザー導入の種類の Eason Matrix。*

これらのテーマは多くの場合に、ユーザーへの新しいソリューションの導入では、主にリスク コントロールと変更の円滑化に重点を置くべきであるという前提に基づきます。 さらに、IT はテクノロジの変更によるリスクと、その変更の円滑化に主に重点を置いてきました。

## <a name="creating-business-change-plans"></a>ビジネス変更プランの作成

ビジネス変更プランでは、技術的変更だけを見るのではなく、移行作業でのすべてのリリースで、一定のレベルのビジネス プロセスの変更が発生するものと想定します。 技術的な変更からのアップストリームとダウンストリームを考慮します。 次の質問は、参加者が、ビジネス変更の観点からユーザー導入について考え、ビジネスへの効果を最大にするために役立ちます。

**アップストリームの質問。** アップストリームの質問では、ユーザーの導入が行われる前に発生する影響や変更について考えます。

- 期待される[ビジネスの成果](../../../business-strategy/business-outcomes/index.md)は定量化されていますか?
- ビジネスへの影響を定義済みの[学習メトリック](../../../business-strategy/learning-metrics.md)にマップしていますか?
- どのビジネス プロセスやチームがこの技術的ソリューションを利用しますか?
- テストとフィードバックのためにパワー ユーザーを最もうまく調整できるのは社内の誰ですか?
- 影響を受けるビジネス リーダーが、優先順位付けと移行計画に関与しましたか?
- この変更に影響を受ける可能性があるビジネスに重要なイベントや日がありますか?
- ビジネス変更プランは効果を最大にしながらも、ビジネスの中断を最小限に抑えますか?
- ダウンタイムが予想されますか? ダウンタイム期間についてエンドユーザーに伝達していますか?

**ダウンストリームの質問。** 導入が完了したら、ビジネス変更を開始できます。 残念ながら、ここで多くのユーザー導入プランが終了します。 ダウンストリームの質問は、技術的な変更の完了後に、クラウド戦略チームが変革に重点を置き続けるために役立ちます。

- ビジネス ユーザーは、変更にうまく対応していますか?
- 技術的な変更が導入されたところで、パフォーマンスの期待が維持されていますか?
- ビジネス プロセスまたはカスタマー エクスペリエンスは予想したように変化していますか?
- 学習メトリックを実現するために追加の変更が必要ですか?
- 変更は、目標のビジネスの成果に合致しましたか? そうでない場合、なぜですか?
- ビジネスの成果に寄与するために追加の変更が必要ですか?
- この変更の結果として、マイナスの影響は確認されていますか?

ビジネス変更プランは、会社ごとに異なります。 これらの質問の目標は、各リリースに関連する変更にビジネスをうまく統合できるようにすることです。 各リリースを、導入されるテクノロジの変更として見るのではなく、ビジネス変更プランとして考えることで、ビジネスの成果を獲得しやすくなる可能性があります。

## <a name="next-steps"></a>次の手順

ビジネスの変更を文書化し、計画したら、[ビジネス テスト](./business-test.md)を開始できます。

> [!div class="nextstepaction"]
> [移行時のビジネス テスト (UAT) のガイダンス](./business-test.md)

## <a name="references"></a>参照

- Eason, K.(1988) _Information technology and organizational change_ (情報技術と組織の変化)、ニューヨーク:Taylor と Francis
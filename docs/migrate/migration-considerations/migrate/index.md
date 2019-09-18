---
title: 移行の実行
titleSuffix: Microsoft Cloud Adoption Framework for Azure
description: 移行の実行
author: BrianBlanchard
ms.author: brblanch
ms.date: 04/04/2019
ms.topic: guide
ms.service: cloud-adoption-framework
ms.subservice: migrate
ms.openlocfilehash: 21520edecc7ba874713561672cd0bd38aa96c0a2
ms.sourcegitcommit: a26c27ed72ac89198231ec4b11917a20d03bd222
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2019
ms.locfileid: "70818235"
---
# <a name="execute-a-migration"></a>移行を実行する

ワークロードを評価した後、それをクラウドに移行できます。 この一連の記事では、移行の実行に関係する可能性があるさまざまなアクティビティについて説明します。

## <a name="objective"></a>目的

移行の目的は、単一のワークロードをクラウドに移行することです。

## <a name="definition-of-done"></a>"*完了*" の定義

移行フェーズは、ワークロードとワークロードを機能させるために必要なすべての依存する資産がステージングされ、クラウドでテストする準備が整ったときに完了します。 ワークロードを本番環境で使用するための準備は、最適化プロセスで実行されます。

この "*完了*" の定義は、テスト プロセスとリリース プロセスに応じて変化する可能性があります。 このシリーズの次の記事に[昇格モデルの決定](./promotion-models.md)についての説明があり、移行されたワークロードを本番環境に昇格させる最適な時機を理解するのに役立ちます。

## <a name="accountability-during-migration"></a>移行中の説明責任

移行プロセス全体の説明責任は、クラウド導入チームが担います。 ただし、クラウド戦略チームのメンバーにも、次のセクションで説明するいくつかの責任があります。

## <a name="responsibilities-during-migration"></a>移行中の責任

概要レベルの説明責任に加え、個人またはグループが直接責任を負う必要があるアクションがあります。 責任者の割り当てを必要とするいくつかのアクティビティを次に示します。

- **修復。** ワークロードのクラウドへの移行を妨げている互換性の問題を解決します。
  - [技術的な複雑さと変更管理](../prerequisites/technical-complexity.md)に関する前提条件の記事で説明したように、このアクティビティの実行方法を判断する前に、意思決定を行っておく必要があります。 具体的には、実際の移行作業と同じスプリント中にクラウド導入チームが修復を完了するのか? または、別のイテレーションで、ウェイブまたはファクトリ モデルを使用して修復を完了するのか? この基本的なプロセスの質問に対して、チームの全メンバーから回答を得ることができない場合は、[前提条件](../prerequisites/index.md)に関するセクションに戻ることをお勧めします。
- **レプリケーション。** VM、データ、およびアプリケーションをクラウド上のリソースと同期させるために、各資産のコピーをクラウド上に作成します。
  - 昇格モデルによっては、このアクティビティを完了するには別のツールが必要な場合があります。
- **ステージング。** ワークロードのすべての資産のレプリケーションと検証を行った後、ビジネス テストとビジネス変更プランを実行するために、ワークロードをステージングできます。

## <a name="next-steps"></a>次の手順

移行プロセスをおおまかに理解したら、[昇格モデルを決定する](./promotion-models.md)ことができます。

> [!div class="nextstepaction"]
> [昇格モデルを決定する](./promotion-models.md)
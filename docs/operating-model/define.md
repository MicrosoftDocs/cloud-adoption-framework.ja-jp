---
title: クラウド運用モデルを定義する
description: クラウド導入フレームワークを使用して運用モデルを定義する方法について説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 08/14/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: overview
ms.custom: internal, operating-model
ms.openlocfilehash: de79b75fae4bdfb6e9b9e27defbcf1451453dc14
ms.sourcegitcommit: 9cd2b48fbfee229edc778f8c5deaf2dc39dfe2d6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "99226990"
---
# <a name="define-your-cloud-operating-model"></a>クラウド運用モデルを定義する

クラウド運用モデルは複雑です。 非常に多くのお客様が、自身のクラウド運用モデルを定義する際に、小さなことで行き詰まっています。 循環参照に連続して陥ってしまいがちです。 循環参照を回避するために、クラウド導入フレームワークには、大量の意思決定を小規模な実践に分解するための、補完的で段階的な一連の手法が用意されています。

## <a name="cloud-adoption-framework-alignment"></a>クラウド導入フレームワークの配置

ビジネスでクラウド運用モデルを定義するのに役立つように、クラウド導入フレームワークでは、運用モデルの各側面が手法として分類されます。 各手法および関連する実行可能な実践は、今後の状態操作を定義するうえで役立つように作成されています。

![クラウド導入フレームワークの手法](../_images/caf-overview-new.png)

### <a name="support-to-develop-your-operating-model"></a>運用モデルの開発をサポートする

クラウド導入フレームワークの次の領域は、運用モデルの領域を拡大できるように設計された段階的な手法です。

- [管理](../manage/index.md):テクノロジの運用管理に対して継続中のプロセスを調整し、価値を最大化し、中断を最小限に抑えます。
- [ガバナンス](../govern/index.md):導入に一貫性を与えます。 ガバナンス要件またはコンプライアンス要件に合わせて調整し、クロスクラウド環境を維持します。
- [セキュリティ戦略](../strategy/define-security-strategy.md): 全体的なセキュリティ戦略の定義付けに役立ちます。
- [整理](../organize/index.md):クラウドで必要な機能の概要を示します。 また、ユーザーを整理して、責任を調整する方法も定義します。

### <a name="collective-output-of-the-operating-model"></a>運用モデルの集合出力

環境は、どのように運用したいかを表すものである必要があります。 運用モデルを定義するときは、環境の準備状況が、運用、ガバナンス、セキュリティ、および組織の要件と一致している必要があります。

- [準備完了](../ready/index.md):Azure ランディング ゾーンには、デプロイ ガイダンスと参照実装が用意されており、環境構成という形で、運用モデルの意思決定に影響を与えています。

> [!NOTE]
> 準備手法には、Azure ランディング ゾーンに対する実装オプションがいくつか用意されています。
>
> - **小規模から始めて拡張する:** 運用モデルの各側面を定義するときに、クラウド プラットフォームを構築するように設計されています。
> - **エンタープライズ規模:** 一連の定義済み運用モデルの意思決定に基づいて、エンタープライズ対応のアーキテクチャを構築します。

### <a name="dependencies-and-inputs-to-operating-model-decisions"></a>運用モデルの決定に対する依存関係と入力

ビジネス戦略と集合型クラウド導入計画は、運用モデルを定義する際に考慮する必要がある入力です。

- [戦略](../strategy/index.md): ビジネス戦略を把握し、クラウド導入戦略によって実現可能な取り組みにマッピングするためのガイダンスです。
- [計画](../plan/index.md): バックログを確立し、進行中の変更を調整する、アジャイルベースの変更管理ガイダンスです。

## <a name="next-steps"></a>次のステップ

上記の手法のいずれかを実行する前に、次の記事を参照し、一般的なクラウド運用モデルを比較して、要件に近いモデルを見つけてください。 この記事は、クラウド プラットフォーム全体で、必要な運用モデルに移行するために、最も実行可能な出発点と一連の実践を確立するのに役立ちます。

> [!div class="nextstepaction"]
> [一般的なクラウド運用モデルを比較する](./compare.md)

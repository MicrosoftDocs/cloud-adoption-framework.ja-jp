---
title: Windows Virtual Desktop のデプロイ後とリリースのプロセス
description: クラウド導入フレームワークのベスト プラクティスを使用して、Windows Virtual Desktop のインスタンスの移行またはデプロイのリリース プロセスについて学習します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 07/17/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: migrate
ms.custom: internal
ms.openlocfilehash: 4470ac3e78b436414e18fc5038e73c51832629d6
ms.sourcegitcommit: b6f2b4f8db6c3b1157299ece1f044cff56895919
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2020
ms.locfileid: "97025641"
---
# <a name="windows-virtual-desktop-post-deployment"></a>Windows Virtual Desktop のデプロイ後

Windows Virtual Desktop インスタンスの移行またはデプロイに向けたリリース プロセスは、比較的簡単です。 このプロセスは、[Windows Virtual Desktop の概念実証](./proof-of-concept.md)で使用されているものと同じです。

- ユーザーのサンプリングについて、アプリケーション グループとデプロイされたデスクトップのパフォーマンスと待機時間をテストします。
- エンド ユーザーをオンボードして、次のものを介した接続方法について説明します。
  - [Windows デスクトップ クライアント](/azure/virtual-desktop/connect-windows-7-and-10)
  - [Web クライアント](/azure/virtual-desktop/connect-web)
  - [Android クライアント](/azure/virtual-desktop/connect-android)
  - [macOS クライアント](/azure/virtual-desktop/connect-macos)
  - [iOS クライアント](/azure/virtual-desktop/connect-ios)

## <a name="post-deployment"></a>配置後

リリースが完了したら、[Windows Virtual Desktop をより適切に操作するため、ログ記録と診断](/azure/virtual-desktop/diagnostics-log-analytics#push-diagnostics-data-to-your-workspace)を追加するのが一般的です。 また、一般的に、運用チームはプールされたホストとデスクトップ仮想マシンを [Azure サーバー管理のベスト プラクティス](../../manage/azure-server-management/index.md)にオンボードして、レポート、修正プログラム、および事業継続とディザスター リカバリーの構成を管理します。

このリリース プロセスはこの移行シナリオの対象外ではありますが、以後移行を繰り返していく中で、追加のワークロードを Azure に移行する必要性がこのプロセスによって明らかになる場合があります。 Microsoft 365 または Azure Active Directory を構成していない場合、クラウド導入チームは、デスクトップ シナリオのリリース時にこれらのサービスにオンボードできます。 ハイブリッド運用モデルでは、運用チームは、Intune、System Center、または他の構成管理ツールを統合して、運用、コンプライアンス、セキュリティを向上させることもできます。

## <a name="next-steps"></a>次のステップ

Windows Virtual Desktop の移行が完了したら、クラウド導入チームはその次のシナリオ固有の移行を開始できます。 または、移行すべきデスクトップが他にもある場合は、次の Windows Virtual Desktop の移行またはデプロイのガイドとして、この記事のシリーズを再び利用できます。

- [Windows Virtual Desktop の移行またはデプロイの計画](./plan.md)
- [環境または Azure ランディング ゾーンを確認する](./ready.md)
- [Windows Virtual Desktop の概念実証を作成する](./proof-of-concept.md)
- [Windows Virtual Desktop の移行またはデプロイを評価する](./migrate-assess.md)
- [Windows Virtual Desktop インスタンスをデプロイまたは移行する](./migrate-deploy.md)
- [Windows Virtual Desktop のデプロイを運用環境にリリースする](./migrate-release.md)

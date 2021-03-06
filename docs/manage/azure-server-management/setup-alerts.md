---
title: 基本アラートを設定する
description: Azure サーバー管理サービスを使用して、IT チームによる問題把握に役立つアラートと通知を設定する方法を説明します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 05/10/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: operate
ms.custom: internal
ms.openlocfilehash: 9508b43837944ebfeb2bb1c10b93ff8fb9fed36f
ms.sourcegitcommit: 9e4bc0e233a24642853f5e8acbeb9746b2444024
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "102113675"
---
# <a name="set-up-basic-alerts"></a>基本アラートを設定する

問題が発生したときに通知を受け取ることは、リソース管理の重要な部分です。 アラートにより、メトリック、ログ、サービスの正常性の問題からのトリガーに基づいて、クリティカルな状態が事前に通知されます。 Azure サーバー管理サービスのオンボードの一環として、IT チームによる問題把握に役立つアラートと通知を設定できます。

## <a name="azure-monitor-alerts"></a>Azure Monitor アラート

Azure Monitor には[アラート](/azure/azure-monitor/alerts/alerts-overview)機能があり、問題が発生したときにメールやメッセージで通知を受け取ることができます。 これらの機能は、サーバーやその他のリソースによって生成されるログやメトリックなどの共通データ監視プラットフォームに基づいています。 Azure Monitor の共通のツール セットを使用すると、複数のリソースから結合されたデータを分析し、それを使用してアラートをトリガーできます。 こうしたトリガーには次のものが含まれます。

- メトリックの値。
- ログの検索クエリ。
- アクティビティ ログのイベント。
- 基になっている Azure プラットフォームの正常性。
- Web サイトの可用性のテスト。

このサービスによって収集される監視データの提供元の詳しい説明については、[Azure Monitor データ ソースの一覧](/azure/azure-monitor/agents/data-sources)に関するページを参照してください。

Azure portal を使用して手動でアラートを作成および管理する方法の詳細については、[Azure Monitor のドキュメント](/azure/azure-monitor/alerts/alerts-metric)を参照してください。

## <a name="automated-deployment-of-recommended-alerts"></a>推奨アラートの自動デプロイ

<!-- docutune:casing "Alert Toolkit" -->

このガイドでは、基本的なインフラストラクチャを監視する 15 種類のアラートを作成することをお勧めします。 デプロイ スクリプトは、[Alert Toolkit](https://github.com/Microsoft/manageability-toolkits) GitHub リポジトリにあります。

このパッケージでは、次のアラートが作成されます。

- ディスク領域不足
- 使用可能なメモリが少ない
- CPU 使用率が高い
- 予期しないシャットダウン
- 破損したファイル システム
- 一般的なハードウェア障害

このパッケージでは、例として HPE サーバー ハードウェアが使用されています。 関連付けられている構成ファイルの設定を、お使いの OEM ハードウェアを反映するように変更します。 構成ファイルに、パフォーマンス カウンターをさらに追加することもできます。 パッケージをデプロイするには、`New-CoreAlerts.ps1` ファイルを実行します。

## <a name="next-steps"></a>次のステップ

継続中の運用をサポートする運用とセキュリティのメカニズムについて学習します。

> [!div class="nextstepaction"]
> [継続中の管理とセキュリティ](./ongoing-management-overview.md)

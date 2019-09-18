---
title: Azure のしくみ
titleSuffix: Microsoft Cloud Adoption Framework for Azure
description: Azure の内部機能の説明
author: alexbuckgit
ms.author: abuck
ms.date: 04/04/2019
ms.topic: guide
ms.service: cloud-adoption-framework
ms.subservice: overview
ms.custom: governance
ms.openlocfilehash: 6aabf9545aa6774b63d3dbd201373273c3f8f1ab
ms.sourcegitcommit: a26c27ed72ac89198231ec4b11917a20d03bd222
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2019
ms.locfileid: "70837753"
---
<!-- markdownlint-disable MD026 -->

# <a name="how-does-azure-work"></a>Azure のしくみ

Azure は、Microsoft のパブリック クラウド プラットフォームです。 Azure では、サービスとしてのプラットフォーム (PaaS)、サービスとしてのインフラストラクチャ (IaaS)、およびマネージド データベース サービスを含む大規模なサービス コレクションを提供しています。 しかし、そもそも Azure とはどんなもので、どのように動作するのでしょう。

<!-- markdownlint-disable MD034 -->

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE2ixGo]

他のクラウド プラットフォームと同様に、Azure は**仮想化**と呼ばれる技術に依存しています。 ほとんどのコンピューター ハードウェアは単純に、シリコン単位で永続的または半永続的にエンコードされた命令のセットであるため、ソフトウェアでエミュレートできます。 ソフトウェアの命令をハードウェアの命令にマップするエミュレーション レイヤーを使用して、仮想化されたハードウェアが実際のハードウェア自体であるかのように、ソフトウェアで実行できます。

基本的に、クラウドとは、顧客に代わって仮想化されたハードウェアを実行する、1 つまたは複数のデータセンターにある物理サーバーのセットです。 では、クラウドはどのようにして、膨大な数の顧客に対する、仮想化されたハードウェアの大量のインスタンスを作成、開始、停止、および削除しているのでしょうか。

これを理解するために、データセンターのハードウェアのアーキテクチャを見てみましょう。 各データセンターの内部は、サーバー ラックに置かれているサーバーのコレクションです。 各サーバー ラックには、ネットワーク接続と電力配分装置 (PDU) を提供するネットワーク スイッチと共に、多数のサーバー **ブレード**が格納されています。 場合によっては、ラックは、**クラスター**と呼ばれるより大規模な単位にグループ化されています。

各ラックまたはクラスター内では、ほとんどのサーバーが、ユーザーに代わってこれらの仮想化されたハードウェア インスタンスを実行するように指示されています。 しかし、一部のサーバーでは、ファブリック コントローラーと呼ばれるクラウド管理ソフトウェアが実行されます。 **ファブリック コントローラー**は、さまざまな役割を担う分散アプリケーションです。 ファブリック コントローラーはサービスを割り当て、実行しているサーバーおよびサービスの正常性を監視し、エラーが発生した場合はサーバーを回復させます。

ファブリック コントローラーの各インスタンスは、通常は**フロント エンド**と呼ばれるクラウド オーケストレーション ソフトウェアを実行している別のサーバー セットに接続されます。 フロント エンドでは、Web サービス、RESTful API、およびクラウドが実行するすべての関数で使用される内部 Azure データベースをホストしています。

たとえば、フロントエンドは、顧客の要求を処理するサービスをホストして、Azure リソース (たとえば、[仮想マシン](/azure/virtual-machines)、[Cosmos DB](/azure/cosmos-db/introduction) などのサービス) を割り当てます。 最初に、フロント エンドはユーザーを検証して、要求されたリソースを割り当てる権限がそのユーザーにあることを確認します。 権限がある場合、フロント エンドはデータベースを確認して十分な容量のあるサーバー ラックを検出し、そのラックのファブリック コントローラーにリソースを割り当てるよう命令します。

そのため基本的に、Azure は膨大なサーバーおよびネットワーク ハードウェアのコレクションであり、これは、これらのサーバー上にある仮想化されたハードウェアおよびソフトウェアの構成および操作をうまく調整する分散アプリケーションの複雑なセットを実行します。 Azure を強化しているのは、この調整機能です。Azure がバックグラウンドでハードウェアの保守やアップグレードをすべて行うので、ユーザーは、これらを担う必要がなくなりました。

## <a name="next-steps"></a>次の手順

Azure 内部について理解できました。次に、クラウド リソース ガバナンスについて確認します。

> [!div class="nextstepaction"]
> [リソース ガバナンスについて確認する](../governance/resource-consistency/what-is-governance.md)

<!-- links -->

[docs-add-users-to-aad]: /azure/active-directory/add-users-azure-active-directory?toc=/azure/architecture/cloud-adoption-guide/toc.json
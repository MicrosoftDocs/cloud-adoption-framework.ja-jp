---
title: ソフトウェア定義ネットワーク意思決定ガイド
description: Azure のクラウド導入フレームワークを使用して、ソフトウェア定義ネットワークによってどのようにソフトウェアによって一元的に管理された仮想化ネットワークが提供されるのかを学びます。
author: alexbuckgit
ms.author: abuck
ms.date: 02/11/2019
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: decision-guide
ms.custom: internal
ms.openlocfilehash: 3d5eb758311b11831bdb85bf23c0f24099329e93
ms.sourcegitcommit: b6f2b4f8db6c3b1157299ece1f044cff56895919
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2020
ms.locfileid: "97023210"
---
# <a name="software-defined-networking-decision-guide"></a>ソフトウェア定義ネットワーク意思決定ガイド

ソフトウェア定義ネットワーク (SDN) は、ソフトウェアを使用して一元管理、構成、および変更できる仮想ネットワーク機能を可能にするように設計されたネットワーク アーキテクチャです。 SDN では、物理ルーター、ファイアウォール、およびオンプレミス ネットワークで使用されるその他のネットワークデバイスに該当する仮想化されたものを使用して、クラウドベースのネットワークを作成できます。 SDN は、Azure などのパブリック クラウド プラットフォーム上にセキュリティで保護された仮想ネットワークを作成するために欠かすことはできません。

## <a name="networking-decision-guide"></a>ネットワークの意思決定ガイド

![ネットワーク オプションを最も簡単なものから最も複雑なものまでプロットし、その下に整合するジャンプ リンクを示す](../../_images/decision-guides/decision-guide-software-defined-network.png)

ジャンプ先:[PaaS のみ](./paas-only.md) | [クラウドネイティブ](./cloud-native.md) | [クラウド DMZ](./cloud-dmz.md) | [ハイブリッド](./hybrid.md) | [ ハブ アンド スポーク モデル](./hub-spoke.md) | [詳細](#learn-more)

SDN では、さまざまな度合いの価格と複雑さを持ついくつかのオプションが提供されます。 上の検出ガイドは、これらのオプションを、特定のビジネスおよびテクノロジ戦略に最も整合するようにすばやく個人用に設定するためのリファレンスを提供します。

このガイドに示されている変曲点は、クラウド戦略チームがネットワーク アーキテクチャに関して意思決定する前に行った、いくつかの重要な意思決定によって異なります。 これらの中で最も重要なのは、[デジタル資産の定義](../../digital-estate/index.md)および[サブスクリプション設計](../subscriptions/index.md)に関連する意思決定です (これには、クラウド会計やグローバル市場の戦略に関連して行った意思決定の情報も必要になる可能性があります)。

VM の数が 1,000 未満の小さな単一リージョン デプロイでは、この変曲点によって大きく影響を受ける可能性はあまりありません。 逆に、1,000 台を超える VM、複数の事業単位、または複数の地政学的市場が関与する大規模な導入作業では、SDN に関する意思決定に加え、この重要な変曲点によって大きく影響を受ける可能性があります。

## <a name="choose-the-right-virtual-networking-architectures"></a>適切な仮想ネットワーク アーキテクチャの選択

このセクションでは、適切な仮想ネットワーク アーキテクチャの選択に役立つように意思決定ガイドをさらに詳細に説明します。

クラウド ベースの仮想ネットワークを作成するために SDN テクノロジを実装するには多くの方法があります。 移行で使用される仮想ネットワークをどのように構築するか、およびこれらのネットワークが既存の IT インフラストラクチャとどのように対話するかは、ワークロードの要件とガバナンスの要件の組み合わせによって異なります。

クラウド移行を計画するときにどの仮想ネットワーク アーキテクチャまたはアーキテクチャの組み合わせを考慮すべきかを計画する場合は、組織にとって何が適切かを判定するのに役立つ次の質問を考慮してください。

| Question | PaaS のみ | クラウドネイティブ | クラウド DMZ | ハイブリッド | ハブ アンド スポーク |
|-----|-----|-----|-----|-----|-----|
| ワークロードでは PaaS サービスのみを使用し、それらのサービス自体によって提供されるものを超えるネットワーク機能は必要ありませんか? | はい | いいえ | いいえ | いいえ | いいえ |
| ワークロードにはオンプレミスのアプリケーションとの統合が必要ですか? | いいえ | いいえ | はい | はい | はい |
| 成熟したセキュリティ ポリシーや、オンプレミスのネットワークとクラウド ネットワークの間のセキュリティで保護された接続を確立していますか? | いいえ | いいえ | いいえ | はい | はい |
| ワークロードにはクラウド ID サービスでサポートされていない認証サービスが必要ですか、またはオンプレミスのドメイン コントローラーへの直接アクセスが必要ですか? | いいえ | いいえ | いいえ | はい | はい |
| 多数の VM やワークロードをデプロイして管理する必要がありますか? | いいえ | いいえ | いいえ | いいえ | はい |
| リソースに対する制御を個々のワークロード チームに委任している間、一元管理およびオンプレミスの接続を提供する必要がありますか? | いいえ | いいえ | いいえ | いいえ | はい |

## <a name="virtual-networking-architectures"></a>仮想ネットワークのアーキテクチャ

主なソフトウェア定義ネットワーク アーキテクチャの詳細について説明します。

- **[PaaS のみ](./paas-only.md):** ほとんどのサービスとしてのプラットフォーム (PaaS) 製品では、限られた一連の組み込みのネットワーク機能がサポートされているため、ワークロードの要件をサポートするための明示的に定義されたソフトウェア定義ネットワークは不要である可能性があります。
- **[クラウドネイティブ](./cloud-native.md):** クラウドネイティブ アーキテクチャでは、クラウド プラットフォームの既定のソフトウェア定義ネットワーク機能上に構築された仮想ネットワークを使用して、クラウドベースのワークロードがサポートされます。オンプレミスまたは他の外部リソースへの依存はありません。
- **[クラウド DMZ](./cloud-dmz.md):** オンプレミス ネットワークとクラウド ネットワーク間の制限された接続をサポートします。この 2 つの環境間のトラフィックを厳重に制御する境界ネットワークの実装を通して、セキュリティで保護されます。
- **[ハイブリッド](./hybrid.md):** ハイブリッド クラウド ネットワークでは、オンプレミスのリソースにアクセスできる信頼できるクラウド環境内の仮想ネットワークが可能です。その逆も可能です。
- **[ハブ アンド スポーク](./hub-spoke.md):** ハブ アンド スポーク アーキテクチャでは、外部の接続や共有サービスを一元管理したり、個々のワークロードを分離したり、潜在的なサブスクリプションの制限を克服したりできます。

## <a name="learn-more"></a>詳細情報

Azure でのソフトウェア定義ネットワークの詳細については、次の記事を参照してください。

- [Azure Virtual Network](/azure/virtual-network/virtual-networks-overview)。 Azure では、コアの SDN 機能は、物理的なオンプレミスのネットワークに類似したクラウドとして機能する Azure Virtual Network によって提供されます。 仮想ネットワークはまた、プラットフォーム上のリソース間の既定の分離境界としても機能します。
- [Azure のネットワーク セキュリティのベスト プラクティス](/azure/security/fundamentals/network-best-practices)。 セキュリティの脆弱性を最小限に抑えるように仮想ネットワークを構成する方法に関する Azure セキュリティ チームからの推奨事項。

## <a name="next-steps"></a>次のステップ

ソフトウェア定義ネットワークは、クラウド導入プロセス中のアーキテクチャの決定で必要なコア インストラクチャ コンポーネントの 1 つにすぎません。 アーキテクチャの決定ガイドの概要を参照して、他の種類のインフラストラクチャの設計に関する決定を行うときに使用される代替パターンまたはモデルを確認してください。

> [!div class="nextstepaction"]
> [アーキテクチャの意思決定ガイド](../index.md)

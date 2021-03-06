---
title: Azure のセキュリティに関するベスト プラクティス
description: Microsoft が Azure のセキュリティに関するベスト プラクティスとして推奨していることについて説明します。
author: JanetCThomas
ms.author: brblanch
ms.date: 09/18/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: reference
ms.custom: internal
ms.openlocfilehash: addf252cc68e0a7bb2f7435e3d17804bdb09c38a
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101786075"
---
# <a name="azure-security-best-practices"></a>Azure のセキュリティに関するベスト プラクティス

以下に示すのは、Microsoft がお客様と自社の環境から得た教訓に基づいて推奨する、Azure のセキュリティに関する優先度の高いベスト プラクティスです。

[Microsoft Tech Community](https://techcommunity.microsoft.com/t5/video-hub/top-10-best-practices-for-azure-security/m-p/1698837) で、これらのベスト プラクティスのビデオ プレゼンテーション を参照できます。

## <a name="1-people-educate-teams-about-the-cloud-security-journey"></a>1.ユーザー: クラウド セキュリティのための移行の過程についてチームを教育する

"_チームは、自分たちが進む移行の過程を理解している必要があります。_ "

**内容**: セキュリティ担当および IT 担当チームに、クラウド セキュリティのための移行の過程と、対処することになる次のような変化について教育します。

- クラウド上の脅威に対する変化
- 責任共有モデルと、それがセキュリティに与える影響
- クラウド導入に一般的に付随する、カルチャと役割または責任の変化

**理由**: クラウドへの移行は重大な変化であり、セキュリティに関する考え方とアプローチに変化が求められます。 セキュリティが組織にもたらす結果は変化しませんが、クラウドでこれを実現する最善の方法は多くの場合に変化し、大幅に変化する場合もあります。

クラウドへの移行は、多くの点で、一戸建てから高層の高級賃貸マンションへの引っ越しに似ています。 基本的なインフラストラクチャ (配管、電気など) を引き続き使用し、同じような活動 (人付き合い、料理、テレビ、インターネットなど) を行いますが、多くの場合、ビルに付属する設備 (ジム、レストランなど) とその提供者および管理者、自分の毎日のルーチンには大きな違いがあります。

**対象者**: セキュリティおよび IT の組織でセキュリティの職責にある全員が、このコンテキストと変化を理解している必要があります (CIO または CISO から技術者まで)。

**方法**: クラウド環境への移行時にデプロイおよび運用を適切に行うために必要なコンテキストをチームに提供します。

Microsoft は、お客様と自社の IT 組織がクラウドへの移行の過程で得た教訓を公開しています。

- セキュリティ組織での[セキュリティ ロールと責任](../organize/cloud-security.md)の進化
- [脅威の環境、ロール、デジタル戦略の進化](/security/compass/microsoft-security-compass-introduction#evolution-of-threat-environment-roles--digital-strategies-2004)
- [セキュリティ、戦略、ツール、脅威のトランスフォーメーション](/security/compass/microsoft-security-compass-introduction#transformation-of-security-strategies-tools--threats-1513)
- ご自身の移行の過程で役立つ、[ハイパースケール クラウド環境をセキュリティで保護する経験から Microsoft が学んだこと](/security/compass/microsoft-security-compass-introduction#microsoft-security-practices-1349)

Azure セキュリティ ベンチマーク「[GS-3: 組織の役割、責任、責務の整合](/azure/security/benchmarks/security-controls-v2-governance-strategy#gs-3-align-organization-roles-responsibilities-and-accountabilities)」も参照してください。

## <a name="2-people-educate-teams-on-cloud-security-technology"></a>2.ユーザー: クラウド セキュリティ テクノロジについてチームに教育する

"_どこに向かっているのかを皆が理解する必要があります。_ "

**内容**: 次のようなクラウド リソースのセキュリティ保護に関する技術教育のために、チームの時間を確保します。

- クラウド テクノロジとクラウド セキュリティ テクノロジ
- 推奨される構成とベスト プラクティス
- 技術的な詳細情報が必要な場合の確認先

**理由**: 技術チームは、情報に基づいた適切なセキュリティ上の意思決定を行うために、技術情報にアクセスする必要があります。 技術チームは実際の職務を通じて新しいテクノロジを学ぶことに優れていますが、多くの場合、クラウドの詳細情報の量は、学習を日常業務に適合させる彼らの能力を上回ります。

技術の学習に専念する時間を作ることで、人々がクラウドのセキュリティを評価し、既存のスキルとプロセスをどのように適合させるかを考える能力に自信をつける時間を確保できます。 軍隊で最も有能な特殊作戦チームでさえ、最高のパフォーマンスを発揮するには訓練と情報が必要です。

**対象者**: クラウド テクノロジを直接操作するすべてのロール (セキュリティと IT の部門) に、クラウド プラットフォームとそのセキュリティ保護の方法に関する技術の学習に専念する時間を確保する必要があります。

さらに、セキュリティおよび IT 技術マネージャー (および多くの場合、プロジェクト マネージャー) は、クラウド リソースを保護するための技術的な詳細情報に精通している必要があります (これにより、クラウド イニシアチブをより効果的に主導および調整できるようになります)。

**方法**: セキュリティの技術担当者が、クラウド資産をセキュリティで保護する方法に関するトレーニングをマイペースで進められるように時間を確保します。 常に実現できるとは限りませんが、理想的には、熟練したインストラクターとハンズオン ラボが用意された正式なトレーニングにアクセスできるようにします。

> [!IMPORTANT]
> ID プロトコルは、クラウドでのアクセス制御に不可欠ですが、オンプレミスのセキュリティでは優先されないことが多いため、セキュリティ チームは、これらのプロトコルとログに確実に精通することに集中する必要があります。

Microsoft は、技術担当者が Azure リソースのセキュリティを強化し、コンプライアンスをレポートするうえで役立つ広範なリソースを提供しています。

- Azure Security
  - AZ-500 [ラーニング パス](/learn/certifications/exams/az-500?tab=tab-learning-paths) (および認定)
  - [Azure セキュリティ ベンチマーク (ASB)](/azure/security/benchmarks/) – Azure セキュリティの規範的なベスト プラクティスと制御
    - [Azure のセキュリティ ベースライン](/azure/security/benchmarks/security-baselines-overview) – 個々の Azure サービスに対する ASB の適用
  - [Microsoft のセキュリティのベスト プラクティス](/security/compass/microsoft-security-compass-introduction) - ビデオとドキュメント
- Azure のコンプライアンス
  - Azure Security Center での[規制に対するコンプライアンス](/azure/security-center/security-center-compliance-dashboard)の評価
- ID プロトコルとセキュリティ
  - [Azure のセキュリティのドキュメント サイト](/azure/security/)
  - Azure AD Authentication の [YouTube シリーズ](https://www.youtube.com/playlist?list=PLLasX02E8BPD5vC2XHS_oHaMVmaeHHPLy)
  - [Azure Active Directory を使用した Azure 環境のセキュリティ保護](https://azure.microsoft.com/resources/securing-azure-environments-with-azure-active-directory/)

Azure セキュリティ ベンチマーク「[GS-3: 組織の役割、責任、責務の整合](/azure/security/benchmarks/security-controls-v2-governance-strategy#gs-3-align-organization-roles-responsibilities-and-accountabilities)」も参照してください。

## <a name="3-process-assign-accountability-for-cloud-security-decisions"></a>3.プロセス:クラウドのセキュリティに関する意思決定の説明責任を割り当てる

"*セキュリティに関する意思決定は、その説明責任を負う者がいなければ行われません。* "

**内容**: エンタープライズ Azure 環境に対して各種類のセキュリティ上の意思決定を行う担当者を指定します。

**理由**: セキュリティに関する意思決定の担当者を明確にすると、クラウドの導入スピードがアップし、"**かつ**" セキュリティが向上します。 だれも意思決定を行う権限を実感しておらず、だれに意思決定を求めるべきかが不明であり、情報に基づく意思決定を調べる動機がないため、通常、欠如によって摩擦が生じます。 この摩擦によって、ビジネス目標、開発者のタイムライン、IT の目標、セキュリティの保証が頻繁に妨げられ、次のような結果になります。

- セキュリティ承認待ちによるプロジェクトの停滞
- セキュリティの承認を待つことができなかった安全でないデプロイ

**対象者**: セキュリティ リーダーが、クラウドに関するセキュリティ上の意思決定を行うことに説明責任を負うチームまたは個人を指定します。

**方法**: 主要なセキュリティ上の意思決定を行う責任を持つグループ (または個人) を指定します。

これらの所有者と連絡先情報を文書化し、セキュリティ、IT、クラウドの各担当チーム内でこれを広く知らせて、すべてのロールが簡単に連絡できるようにします。

セキュリティ上の意思決定が必要な一般的な領域、説明、通常どのチームが決定を行うかを以下に示します。

| 決定         | 説明           | 一般的なチーム  |
| ------------- |-------------| -----|
| ネットワークのセキュリティ | Azure Firewall、ネットワーク仮想アプライアンス (および関連するルーティング)、WAF、NSG、ASG などの構成とメンテナンス。 | "_通常は、ネットワーク セキュリティに焦点を絞った [インフラストラクチャとエンドポイントのセキュリティ](../organize/cloud-security-infrastructure-endpoint.md) チーム_"  |
| ネットワーク管理 | 企業全体の仮想ネットワークとサブネットの割り当て | "_通常は、[中央 IT 運用](../organize/central-it.md)部門の既存のネットワーク運用チーム_" |
| サーバー エンドポイントのセキュリティ | サーバー セキュリティ (修正プログラムの適用、構成、エンドポイントのセキュリティなど) の監視と修復 | "_通常は、[中央 IT 運用](../organize/central-it.md)と [インフラストラクチャとエンドポイントのセキュリティ](../organize/cloud-security-infrastructure-endpoint.md)の担当チームが共同で行う_" |
| インシデントの監視と対応 | SIEM またはソース コンソール (Azure Security Center、Azure AD Identity Protection など) でセキュリティ インシデントを調査して修復する | "_通常は [セキュリティ運用](../organize/cloud-security-operations-center.md)チーム_" |
| ポリシー管理 | Azure ロールベースのアクセス制御 (Azure RBAC)、Azure Security Center、管理者保護戦略、および Azure リソースを管理するための Azure Policy の使用についての指針を定める | "_通常は、[ポリシーと標準](../organize/cloud-security-policy-standards.md) + [セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)の担当チームが共同で行う_" |
| ID に関するセキュリティと標準 | Azure AD のディレクトリ、PIM/PAM の使用、MFA、パスワードまたは同期の構成、アプリケーション ID 標準についての指針を定める | "_通常は、[ID とキーの管理](../organize/cloud-security-identity-keys.md) + [ポリシーと標準](../organize/cloud-security-policy-standards.md) + [セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)の担当チームが共同で行う_"  |

> [!NOTE]
>
> - 意思決定者は、この責任が伴うクラウドの領域において適切な教育を受けている必要があります。
> - 記録を残し、組織を長期にわたって導くために、決定事項をポリシーと標準に確実に文書化します。

Azure セキュリティ ベンチマーク「[GS-3: 組織の役割、責任、責務の整合](/azure/security/benchmarks/security-controls-v2-governance-strategy#gs-3-align-organization-roles-responsibilities-and-accountabilities)」も参照してください。

## <a name="4-process-update-incident-response-processes-for-cloud"></a>4. プロセス:クラウドのインシデント対応プロセスを更新する

"_緊急時に緊急時の計画を立てる時間はありません。_ "

**内容**: プロセスを更新し、Azure クラウド プラットフォーム上のセキュリティ インシデントに対応するためにアナリストを準備します (導入済みの [ネイティブ脅威検出ツール](../get-started/security.md#step-1-establish-essential-security-practices)を含む)。 プロセスを更新し、チームを準備して、インシデント調査、修復、脅威ハンティング時に最大限のパフォーマンスを発揮できるように、シミュレートされた攻撃を使用して練習します。

**理由**: アクティブな攻撃者は、状況を制御することがすぐに困難になる可能性のある差し迫ったリスクを組織にもたらします。そのため、攻撃に対して迅速に対応する必要があります。 企業のデータ、システム、アカウントをホストしているすべてのクラウド プラットフォームを含む資産全体に対して、このインシデント対応 (IR) プロセスを有効にする必要があります。

多くの類似点がある一方で、クラウド プラットフォームには、既存のプロセスを破綻させる可能性のあるオンプレミス システムとの重要な技術的な違いがあります。これは通常、情報が別の形式で利用可能であるためです。 セキュリティ アナリストは、不慣れな環境に対して迅速に対応する必要があり、そのため対応が遅くなる可能性があるという課題を抱えている場合があります (特に、従来のオンプレミス アーキテクチャとネットワークやディスクのフォレンジックア プローチについてのみトレーニングされている場合)。

**対象者**: IR プロセスの最新化は、通常、他のグループからの知識と専門知識をサポートする [セキュリティ運用](../organize/cloud-security-operations-center.md)部門によって主導されます。

- **スポンサー:** このプロセス最新化は、通常、セキュリティ運用担当部長 (または同等のスポンサー) が支援します。
- **実行:** 既存のプロセスを適合させる (または、初めて作成する) ことは、次のことを含む共同作業です。

  - **[セキュリティ運用](../organize/cloud-security-operations-center.md)** インシデント管理チームまたはリーダー – プロセスに対する更新と、法律担当およびコミュニケーションや広報担当のチームを含む主要な外部関係者の統合を主導する
  - **[セキュリティ運用](../organize/cloud-security-operations-center.md)** セキュリティ アナリスト – 技術的なインシデント調査とトリアージに関する専門知識を提供する
  - **[中央 IT 運用](../organize/central-it.md)** - クラウド プラットフォームに関する専門知識を (直接、クラウドのセンター オブ エクセレンスを通じて、または直接、または外部のコンサルタントを通じて) 提供する

**方法**: プロセスを更新し、アクティブな攻撃者を見つけたときに何をすればよいかがわかるように、チームを準備します。

- **プロセスとプレイブック:** 既存の調査、修復、脅威ハンティングのプロセスを、クラウド プラットフォームのしくみ (新しいまたは異なるツール、データ ソース、ID プロトコルなど) の違いに合わせて調整します。

- **教育:** クラウド全体の変革、プラットフォームのしくみに関する技術的な詳細、新しいまたは更新されたプロセスについてアナリストを教育することで、アナリストがどのような違いがあるかを把握し、必要なものがどこで見つかるかを理解できるようにします。

"**主要な対象領域**: " リソースのリンクには多くの詳細が記載されていますが、教育および計画の取り組みで重点を置くべき重要な領域は次のとおりです。

- **共有責任モデルとクラウド アーキテクチャ:** セキュリティ アナリストにとって Azure は、馴染みのある VM や、オンプレミスとは大きく異なるその他のサービス (Azure SQL Azure Functions など) を含む多くのサービスを提供するソフトウェア定義データセンターです。そこでは、最も価値のあるデータが、基礎になる OS または VM のログではなく、サービス ログまたは専用の脅威検出サービスの中に存在します (Microsoft が運用し、複数の顧客にサービスを提供する)。 アナリストは、このコンテキストを理解して日常のワークフローに統合し、予想されるデータ、それを取得する場所、それに使用される形式がわかるようにする必要があります。
- **エンドポイント データ ソース:** 多くの場合、直接ディスク アクセスという従来のアプローチとは対照的に、Azure Security Center や EDR システムなどのネイティブ クラウド検出ツールを使用すると、クラウドでホストされているサーバー上の攻撃やマルウェアに関する分析情報やデータの取得が、より高速、簡単、正確に行えるようになります。 直接ディスクのフォレンジックは、それが可能であり法的手続きのために必要とされるシナリオに対して利用可能 ([Azure でのコンピューター フォレンジック](/azure/architecture/example-scenario/forensics/)) ですが、これは多くの場合、攻撃を検出して調査するには最も効率の悪い方法です。
- **ネットワークと ID のデータ ソース:** クラウド プラットフォームの多くの機能では、主に ID を使用して Azure portal へのアクセスなどのアクセス制御が行われます (ただし、ネットワーク アクセス制御も広く使用されています)。 このため、アナリストはクラウド ID プロトコルについて理解を深め、インシデントの調査と修復をサポートするために、攻撃者のアクティビティ (および正当なユーザー アクティビティ) について完全で詳細な全体像を把握する必要があります。 ID ディレクトリとプロトコルもオンプレミスとは異なり、通常は、オンプレミスでよく見られる LDAP、Kerberos、NTLM、Active Directory ではなく、SAML、OAuth、OIDC とクラウド ディレクトリに基づいています。
- **実習:** シミュレートされた攻撃と対応は、組織内のセキュリティ アナリスト、脅威ハンター、インシデント マネージャー、およびその他の関係者にとって、組織の反射的対応と技術的な準備を確立するのに役立ちます。 実際の職務を通じて学び、適応することは、インシデント対応の当然の部分ですが、緊急時に知る必要があることを最小限に抑えるために作業する必要があります。

**主要リソース:**

- [インシデント対応のリファレンス ガイド](https://aka.ms/IRRG) (IRRG)
- [独自のセキュリティ インシデント対応プロセスを構築する](https://msrc-blog.microsoft.com/2019/07/01/inside-the-msrc-building-your-own-security-incident-response-process/)ためのガイダンス
- [Azure のログとアラート](/azure/security/fundamentals/log-audit)
- Microsoft セキュリティのベスト プラクティス
  - [セキュリティ、戦略、ツール、脅威のトランスフォーメーション](/security/compass/microsoft-security-compass-introduction#transformation-of-security-strategies-tools--threats-1513)
  - [セキュリティ運用](/security/compass/security-operations-videos-and-decks)
- サイバー防御オペレーション センター (CDOC) から Microsoft が学んだこと
  - [得られた全体的な教訓](https://www.microsoft.com/security/blog/2019/02/21/lessons-learned-from-the-microsoft-soc-part-1-organization/)
  - [インシデント調査](https://www.microsoft.com/security/blog/2019/12/23/ciso-series-lessons-learned-from-the-microsoft-soc-part-3b-a-day-in-the-life/)
  - [インシデントの修復](https://www.microsoft.com/security/blog/2020/05/04/lessons-learned-microsoft-soc-part-3c/)

Azure セキュリティ ベンチマーク「[IR-1: 準備 – インシデント対応プロセスを Azure 用に更新する](/azure/security/benchmarks/security-controls-v2-incident-response#ir-1-preparation--update-incident-response-process-for-azure)」も参照してください。

## <a name="5-process-establish-security-posture-management"></a>5.プロセス:セキュリティ態勢管理を確立する

"*まず、自らを知ること。* "

**内容**: 次のようにして、Azure 環境のセキュリティ態勢を積極的に管理するようにします。

- 次に対する責任の明確な所有権を割り当てる
  - セキュリティ態勢の監視
  - 資産に対するリスクの軽減
- これらのタスクの自動化と簡略化

**理由**: セキュリティの検疫に関する一般的なリスクを迅速に特定して修復すると、組織としてのリスクが大幅に軽減されます。

ソフトウェア定義というクラウド データセンターの性質のため、広範な資産のインストルメンテーションによって、セキュリティ リスク (ソフトウェアの脆弱性、セキュリティ構成の不備など) を継続的に監視できます。 開発者と IT チームが VM、データベース、その他のリソースをすばやくデプロイできることで、リソースが安全に構成されて積極的に監視されるようにする必要性も生じます。

これらの新しい機能によって新しい可能性が提供されますが、それらから価値を実現するには、それらを使用するための責任を割り当てる必要があります。 急速に進化するクラウド運用を継続的に実行するには、人が行うプロセスを可能な限り簡素化し、自動化する必要もあります。 [セキュリティ原則](/azure/architecture/framework/security/security-principles)の「シンプルさを促進する」を参照してください。

> [!NOTE]
 > 簡素化とオートメーションの目標は、職を排除することではなく、反復的なタスクの負担を人々から取り除くことで、IT チームや DevOps チームとの提携や教育など、より価値の高い、人間のアクティビティに専念できます。

**対象者**: 通常、これは次の 2 セットの責任に分けられます。

- **[セキュリティ態勢管理](../organize/cloud-security-posture-management.md)** – この新しい機能は、多くの場合、既存の脆弱性管理またはガバナンス機能が進化したものです。 これには、Azure Security Center セキュリティ スコアで保護されたスコアやその他のデータ ソースを使用した全体的なセキュリティ態勢の監視、リスクを軽減するためのリソース所有者との積極的な連携、セキュリティ リーダーへのリスクの報告が含まれます。
- **セキュリティ修復:** これらのリスクに対処することについての説明責任を、これらのリソースの管理を担当するチームに割り当てます。 これは、独自のアプリケーション リソースを管理している DevOps チームか、 **[中央 IT 運用](../organize/central-it.md)** のテクノロジ専門チームである必要があります。

  - "**コンピューティングおよびアプリ リソース:**"
    - **アプリケーション サービス** - アプリケーション開発またはセキュリティ チーム
    - **コンテナー** - アプリケーション開発またはインフラストラクチャ/IT 運用、あるいはその両方
    - **VM/スケールセット/コンピューティング** - IT/インフラストラクチャ運用
  - "**データおよびストレージ リソース:**"
    - **SQL/Redis/Data Lake Analytics/Data Lake Store** - データベース チーム
    - **ストレージ アカウント** - ストレージまたはインフラストラクチャ チーム
  - "**ID およびアクセス リソース:**"
    - **サブスクリプション** - ID チーム
    - **Key Vault** – ID または情報/データ セキュリティ チーム
  - "**ネットワーク リソース** - ネットワーク セキュリティ チーム
  - "**IoT セキュリティ** - IoT 運用チーム

**方法**: セキュリティは全員の職務ですが、現在、それがどれだけ重要か、何をどのように行うのかを全員が知っているわけではありません。

- リソース所有者が可用性、パフォーマンス、コスト、およびその他の成功要因について説明責任を負うのと同様に、セキュリティ リスクについて説明責任を負うようにします。
- セキュリティ リスクが資産にとって重要である理由、リスクを軽減するために何を行う必要があり、生産性の低下を最小限に抑えてそれを実装する方法についてリソース所有者が明確に理解できるようにサポートします。

> [!IMPORTANT]
> 多くの場合、リソースをセキュリティで保護する理由、対象、方法についての説明は、リソースの種類が異なっても類似していますが、各チームが既に知っていて配慮していることに関連付けることが重要です。 セキュリティ チームは、チームを成功させることに焦点を合わせた信頼できるアドバイザー兼パートナーとして、IT および DevOps チームと連携する必要があります。

**ツール**: Azure Security Center の [セキュリティ スコア](/azure/security-center/security-center-secure-score)は、さまざまな資産に関する、Azure において最も重要なセキュリティ情報の評価を表します。 これは、態勢管理の出発点となるものであり、カスタムの Azure ポリシーやその他のメカニズムで必要に応じて補完することができます。

**頻度**: Azure セキュリティ スコアを確認する一定の頻度 (通常は月 1 回) を設定し、具体的な改善目標を定めたイニシアティブを計画します。 頻度は必要に応じて増やすことができます。

> [!TIP]
 > 可能な場合は、アクティビティをゲーム化してエンゲージメントを高めます。たとえば、DevOps チーム向けにスコアを最も高める楽しいコンテストや賞を作ります。

Azure セキュリティ ベンチマーク「[GS-2: セキュリティ態勢管理の戦略を定義する](/azure/security/benchmarks/security-controls-v2-governance-strategy#gs-2-define-security-posture-management-strategy)」も参照してください。

## <a name="6-technology-require-passwordless-or-multi-factor-authentication-mfa"></a>6.テクノロジ: パスワードレス認証または多要素認証 (MFA) を必須にする

"*自社のセキュリティは、間違いなく専門の攻撃者が管理者のパスワードを推測したり盗んだりできないものだと言えますか?*

**内容**: 重大な影響がある管理者全員に、パスワードレス認証または多要素認証 (MFA) の使用を義務付けます。

**理由**: 古いスケルトン キーでは現代の泥棒から家を保護できないのと同じように、パスワードでは、現在の一般的な攻撃からアカウントを保護することはできません。 技術的な詳細については、「[パスワードは重要ではない](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/your-pa-word-doesn-t-matter/ba-p/731984)」を参照してください。

かつて MFA は面倒な追加の手順でしたが、現在のパスワードレス アプローチは、Windows Hello やモバイル デバイスでの顔認識などの生体認証アプローチを使用すると、ログオン エクスペリエンスが向上します (パスワードを覚えたり入力したりする必要はありません)。 さらに、ゼロ トラスト アプローチを使用すると、信頼されたデバイスが記憶されます。これにより、帯域外の MFA アクションの要求を減らすことができます (「[ユーザー サインインの頻度](/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime#user-sign-in-frequency)」を参照してください)。

**対象者**: パスワードと多要素の取り組みは、通常、[ID とキーの管理](../organize/cloud-security-identity-keys.md)または [セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)あるいはその両方によって主導されます。

- **スポンサー:** 通常、これは CISO、CIO、または ID 担当部長が支援します。
- **実行:** これは次のことを含む共同作業です。
  - [ポリシーと標準](../organize/cloud-security-policy-standards.md)担当チームが明確な要件を確立
  - [ID とキーの管理](../organize/cloud-security-identity-keys.md)または[中央 IT 運用](../organize/central-it.md)によるポリシーの実装
  - コンプライアンスを確保するための[セキュリティ コンプライアンス管理](../organize/cloud-security-compliance-management.md)による監視

**方法**: パスワードレスまたは MFA 認証を実装し、その使用方法について管理者をトレーニングします (必要な場合)。また、管理者に対して、記述されたポリシーを使用することに従うように要求します。 これは、次の 1 つまたは複数のテクノロジによって実現できます。

- [パスワードレス (Windows Hello)](/windows/security/identity-protection/hello-for-business/hello-identity-verification)
- [パスワードなし (Authenticator アプリ)](/azure/active-directory/authentication/howto-authentication-phone-sign-in)
- [Azure Multifactor Authentication](/azure/active-directory/authentication/howto-mfa-userstates)
- サードパーティの MFA ソリューション

> [!NOTE]
> 現在、テキスト メッセージ ベースの MFA は攻撃者が比較的安価にバイパスできるため、パスワードレスとより強力な MFA を重視してください。

Azure セキュリティ ベンチマーク「[ID-4: すべての Azure Active Directory ベースのアクセスに強力な認証制御を使用する](/azure/security/benchmarks/security-controls-v2-identity-management#id-4-use-strong-authentication-controls-for-all-azure-active-directory-based-access)」も参照してください。

## <a name="7-technology-integrate-native-firewall-and-network-security"></a>7.テクノロジ: ネイティブ ファイアウォールとネットワーク セキュリティを統合する

"*ネットワーク攻撃に対するシステムとデータの保護を簡略化します。* "

**内容**: Azure Firewall、Azure Web App Firewall (WAF)、および分散型サービス拒否 (DDoS) の緩和策をネットワーク セキュリティ アプローチに統合することによって、ネットワークのセキュリティ戦略とメンテナンスを簡略化します。

**理由**: わかりやすくすることはセキュリティにとって重要です。そうすることで、混乱、誤りの防止、およびその他の人為的なエラーによるリスクの可能性が軽減されるからです。 [セキュリティ原則](/azure/architecture/framework/security/security-principles)の「シンプルさを促進する」を参照してください。

ファイアウォールと WAF は、悪意のあるトラフィックからアプリケーションを保護するための重要な基本セキュリティ制御ですが、そのセットアップとメンテナンスは複雑で、セキュリティ チームの多くの時間と注意を費やすことがあります (カスタムのアフターパーツを車に追加するのと同様)。 Azure のネイティブ機能を使用すると、ファイアウォール、Web アプリケーション ファイアウォール、分散型サービス拒否 (DDoS) の軽減策などの実装と運用を簡単に行うことができます。

これにより、Azure サービスのセキュリティの評価、セキュリティ運用の自動化、アプリケーションや IT ソリューションとのセキュリティの統合など、価値の高いセキュリティ タスクにチームの時間と注意を向けることができます。

**対象者**:

- **スポンサー:** このネットワーク セキュリティ戦略の更新は、通常、セキュリティ リーダーまたは IT リーダーあるいはその両方によって後援されます。
- **実行:** これらをクラウド ネットワークのセキュリティ戦略に統合することは、次のことを含む共同作業です。

  - **[セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)** - クラウド ネットワークおよびクラウド ネットワーク セキュリティのリーダーとのクラウド ネットワーク セキュリティ アーキテクチャを確立します。
  - **クラウド ネットワークのリーダー** ([中央 IT 運用](../organize/central-it.md)) + **クラウド ネットワーク セキュリティのリーダー** ([インフラストラクチャ セキュリティ チーム](../organize/cloud-security-infrastructure-endpoint.md))
    - セキュリティ アーキテクトによるクラウド ネットワークのセキュリティ アーキテクチャの確立
    - ファイアウォール、NSG、WAF の機能を構成し、WAF ルールについてアプリケーション アーキテクトと連携する
  - **アプリケーション アーキテクト:** ネットワーク セキュリティ部門と連携して、可用性を損なうことなくアプリケーションを保護するために WAF のルールセットと DDoS 構成を構築および調整する

**方法**: 運用を簡略化することを検討している組織には、2 つのオプションがあります。

- **既存の機能とアーキテクチャを拡張する:** 多くの組織では、既存のファイアウォール機能の使用を拡張することを選択しています。これにより、特にクラウドを初めて導入する場合に、既存の投資を活用してスキルとプロセスを統合できます。
- **ネイティブ セキュリティ制御を採用する:** ますます多くの組織が、サードパーティの機能を統合する複雑さを避けるために、ネイティブ制御を使用することを希望しています。 これらの組織は一般的に、負荷分散、ユーザー定義ルート、ファイアウォールまたは WAF 自体の構成の誤りや、さまざまな技術チーム間での受け渡しの遅延を回避することを求めています。 このオプションは、コードとしてのインフラストラクチャのアプローチを採用する組織にとって特に魅力的です。組み込み機能はサードパーティの機能よりも簡単に自動化およびインストルメント化できるためです。

Azure ネイティブ ネットワーク セキュリティ機能に関するドキュメントは次の場所にあります。

- [Azure Firewall](/azure/firewall/overview)
- [Azure Web アプリケーション ファイアウォール (WAF)](/azure/web-application-firewall/)
- [Azure DDoS Protection](/azure/virtual-network/ddos-protection-overview)

[Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/apps?page=1&search=firewall) には、多くのサードパーティ製ファイアウォール プロバイダーが含まれています。

Azure セキュリティ ベンチマーク「[NS-4: 外部ネットワーク攻撃からアプリケーションやサービスを保護する](/azure/security/benchmarks/security-controls-v2-network-security#ns-4-protect-applications-and-services-from-external-network-attacks)」も参照してください。

## <a name="8-technology-integrate-native-threat-detection"></a>8.テクノロジ: ネイティブ脅威検出を統合する

"*Azure システムとデータに対する攻撃の検出と対応を簡略化します。* "

**内容**: セキュリティ運用と SIEM にネイティブの脅威検出機能を組み込むことで、脅威の検出と対応の戦略を簡略化します。

**理由**: セキュリティ運用の目的は、平均応答時間 (MTTA) と修復 (MTTR) のインシデントによって測定される、環境にアクセスするアクティブな攻撃者の影響を軽減することです。 これには、インシデント対応のすべての要素の精度と速度が必要であるため、ツールの品質とプロセス実行の効率が最重要になります。

クラウド テクノロジの違いと高速な変化のペースにより、オンプレミスの脅威の検出向けに設計された既存のツールとアプローチを使用して脅威の検出を向上させることは困難です。 ネイティブに統合された検出は、現在の脅威とクラウド プラットフォームの変化に対応できる、クラウド プロバイダーによって維持される業界規模のソリューションを提供します。

これらのネイティブ ソリューションにより、セキュリティ運用チームは、不慣れなログ データからのアラートの作成、ツールの統合、メンテナンス タスクに時間を消費するのではなく、インシデントの調査と修復に専念できます。

**対象者**: これは通常、[セキュリティ運用](../organize/cloud-security-operations-center.md)チームによって主導されます。

- **スポンサー:** これは通常、セキュリティ運用担当部長 (または同等のスポンサー) によって後援されます。
- **実行:** ネイティブ脅威検出の統合は、以下を含む共同作業です。
  - **[セキュリティ運用](../organize/cloud-security-operations-center.md):** アラートを SIEM とインシデント調査プロセスに統合し、クラウドのアラートとその意味、ネイティブ クラウド ツールの使用方法についてアナリストを教育します。
  - **[インシデントの準備](../organize/cloud-security-incident-preparation.md):** クラウド インシデントを実習に組み込み、チームの準備を進めるための実習を確実に実施するようにします。
  - **[脅威インテリジェンス](../organize/cloud-security-threat-intelligence.md):** クラウド攻撃に関する情報を調査して統合し、チームにコンテキストとインテリジェンスの情報を提供します。
  - **[セキュリティのアーキテクチャ](../organize/cloud-security-architecture.md):** ネイティブ ツールをセキュリティ アーキテクチャのドキュメントに統合します。
  - **[ポリシーと標準](../organize/cloud-security-policy-standards.md):** 組織全体でネイティブ ツールを有効にするための標準とポリシーを設定します。 コンプライアンスについて監視します。
  - **[インフラストラクチャとエンドポイント](../organize/cloud-security-infrastructure-endpoint.md)**  /  **[中央 IT 運用](../organize/central-it.md):** 検出を構成して有効にし、コード ソリューションとしてオートメーションとインフラストラクチャに統合します。

**方法**: 使用するすべてのリソースに対して Azure Security Center で [脅威検出](/azure/security-center/threat-protection)を有効にし、上で説明したように、各チームにこれらをプロセスに統合してもらいます。

Azure セキュリティ ベンチマーク「[LT-1: Azure リソースの脅威検出を有効にする](/azure/security/benchmarks/security-controls-v2-logging-threat-detection#lt-1-enable-threat-detection-for-azure-resources)」も参照してください。

## <a name="9-architecture-standardize-on-a-single-directory-and-identity"></a>9.アーキテクチャ:単一のディレクトリと ID で標準化する

"*複数の ID とディレクトリを処理したい人はいません。* "

**内容**: Azure 内のアプリケーションとユーザーごとに 1 つの Azure AD ディレクトリと 1 つの ID で標準化します (すべてのエンタープライズ ID 機能について)。

> [!NOTE]
> このベスト プラクティスは、具体的にはエンタープライズ リソースに言及しています。 パートナー アカウントの場合は、[Azure AD B2B](/azure/active-directory/external-identities/what-is-b2b) を使用すると、ディレクトリ内にアカウントを作成して管理する必要がありません。 お客様または市民アカウントの場合は、[Azure AD B2C](/azure/active-directory-b2c/) を使用して管理します。

**理由**: 複数のアカウントと ID ディレクトリを使用すると、生産性の高いユーザー、開発者、IT および ID 管理者、セキュリティ アナリスト、およびその他のロールの日常のワークフローに不要な摩擦や混乱が生じます。

複数のアカウントとディレクトリを管理することによって、複数のアカウント間で同じパスワードを再利用したり、攻撃者が対象としている古いまたは破棄されたアカウントの可能性が増えたりするなど、セキュリティに関する不適切な実践の動機も生まれます。

特定のアプリケーションまたはワークロードに対して (LDAP などに基づいて) カスタム ディレクトリを短時間で立ち上げる方がより簡単に見えることがありますが、これにより、設定と管理のための統合とメンテナンスの作業が大幅に増えます。 これは、既存のエンタープライズ テナントを使用するのではなく、追加の Azure テナントまたは追加のオンプレミスの Active Directory フォレストを設定するという決定と多くの点で似ています。 [セキュリティ原則](/azure/architecture/framework/security/security-principles)の「シンプルさを促進する」も参照してください。

**対象者**: これは、多くの場合、[セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)または [ID とキー管理](../organize/cloud-security-identity-keys.md)の担当チームによって行われる、チーム間の作業です。

- **スポンサー:** 通常、これは [ID とキー管理](../organize/cloud-security-identity-keys.md)および [セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)部門が支援します (ただし、一部の組織では、CISO または CIO による支援が必要になる場合があります)。
- **実行:** これは次のことを含む共同作業です。
  - **[セキュリティのアーキテクチャ](../organize/cloud-security-architecture.md):** セキュリティと IT アーキテクチャのドキュメントと図に組み込む
  - **[ポリシーと標準](../organize/cloud-security-policy-standards.md):** ポリシーを文書化し、コンプライアンスを監視する
  - **[ID とキーの管理](../organize/cloud-security-identity-keys.md)** または **[中央 IT 運用](../organize/central-it.md)** 部門が、機能を有効にし、アカウントや教育などを提供して開発者をサポートすることによって、ポリシーを実装
  - **アプリケーション開発者** または **[中央 IT 運用](../organize/central-it.md)部門あるいはその両方:** アプリケーションと Azure サービス構成で ID を使用する (責任は DevOps 導入のレベルによって異なります)

**方法**: 新しい "_グリーンフィールド_" 機能 (現在は成長中) で始める実用的なアプローチを採用し、フォローアップの演習として既存のアプリケーションやサービスの "_ブラウンフィールド_" の課題を解消します。

- **グリーンフィールド:** 今後すべてのエンタープライズ ID で、ユーザーごとに 1 つのアカウントを持つ単一の Azure AD ディレクトリを使用する必要があるという明確なポリシーを確立して実装します。

- **ブラウンフィールド:** 多くの組織では、複数のレガシ ディレクトリと ID システムを所有しています。 継続的な管理の摩擦コストが、クリーンアップのための投資を超えた場合に対処します。 ID 管理と同期のソリューションでは、これらの問題の一部を軽減できますが、ユーザー、管理者、および開発者にシームレスなエクスペリエンスを提供するセキュリティと生産性の機能が緊密に統合されません。

ID の使用を統合するための最適なタイミングは、アプリケーション開発サイクル中の次の場合です。

- クラウドのアプリケーションを最新化する
- DevOps プロセスを使用してクラウド アプリケーションを更新する

非常に独立性の高い事業単位である場合や規制要件がある場合、別のディレクトリとすることに合理的な理由がありますが、他のすべての状況では複数のディレクトリを使用しないようにする必要があります。

Azure セキュリティ ベンチマーク「[ID-1: Azure Active Directory を中央 ID および認証システムとして標準化する](/azure/security/benchmarks/security-controls-v2-identity-management#id-1-standardize-azure-active-directory-as-the-central-identity-and-authentication-system)」も参照してください。

> [!IMPORTANT]
> 単一アカウント規則の唯一の例外は、特権を持つユーザー (IT 管理者とセキュリティ アナリストを含む) は、標準ユーザー タスクと管理タスクのために別々のアカウントを持つ必要があるということです。
>
> 詳細については、Azure セキュリティ ベンチマークの[特権アクセス](/azure/security/benchmarks/security-controls-v2-privileged-access)に関するページを参照してください。

## <a name="10-architecture-use-identity-based-access-control-instead-of-keys"></a>10.アーキテクチャ:(キーではなく) ID ベースのアクセス制御を使用する

**内容**: 可能な限り、キーベースの認証ではなく Azure AD ID を使用します (Azure のサービス、アプリケーション、API など)。

**理由**: キーベースの認証は、クラウド サービスと API に対する認証に使用できますが、キーを安全に管理する必要があり、適切に実行する (特に大規模に) のは容易ではありません。 セキュリティで保護されたキー管理は、セキュリティの専門家でない開発者やインフラストラクチャ担当者には困難であり、安全に実行できないことが多く、組織に大きなセキュリティ リスクが生じます。

ID ベースの認証は、秘密のローテーション、ライフサイクル管理、管理委任などの成熟した機能によって、これらの課題の多くを克服します。

**対象者**: これは、多くの場合、[セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)または [ID とキー管理](../organize/cloud-security-identity-keys.md)の担当チームによって行われる、チーム間の作業です。

- **スポンサー:** 通常、これは [セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md)または [ID とキー管理](../organize/cloud-security-identity-keys.md)部門が支援します (ただし、一部の組織では CISO または CIO による支援が必要になる場合があります)。
- **実行:** これは次のことを含む共同作業です。
  - **[セキュリティのアーキテクチャ](../organize/cloud-security-architecture.md):** セキュリティおよび IT アーキテクチャの図とドキュメントに組み込まれています。
  - **[ポリシーと標準](../organize/cloud-security-policy-standards.md):** ポリシーを文書化し、コンプライアンスを監視する。
  - **[ID とキーの管理](../organize/cloud-security-identity-keys.md)** または **[中央 IT 運用](../organize/central-it.md)** 部門が、機能を有効にし、アカウントや教育などを提供して開発者をサポートすることによって、ポリシーを実装
  - **アプリ開発者** または **[中央 IT 運用](../organize/central-it.md)あるいはその両方:** アプリケーションと Azure サービス構成で ID を使用する (責任は DevOps 導入のレベルによって異なります)。

**方法**: ID ベースの認証を使用するための組織の基本設定と習慣を設定するには、プロセスに従ってテクノロジを有効にする必要があります。

**このプロセスの内容は次のとおりです。**

1. 既定の ID ベースの認証および許容される例外を明確に示す **ポリシーと標準を確立** します。
2. 新しいアプローチを使用する理由、実行する必要があること、およびその方法について、開発者とインフラストラクチャ担当チームを **教育** します。
3. 変更を実用的な方法で **実装** します。現在および将来採用される新しいグリーンフィールド機能 (新しい Azure サービス、新しいアプリケーション) から始めて、既存のブラウンフィールド構成のクリーンアップを行います。
4. コンプライアンスを **監視** し、開発者およびインフラストラクチャ チームと共にフォローアップします。

**テクノロジ:** サービスやオートメーションなどの人間以外のアカウントには、[マネージド ID](/azure/active-directory/managed-identities-azure-resources/overview) を使用します。 Azure マネージド ID によって、Azure AD 認証をサポートする Azure のサービスとリソースに対して認証を行うことができます。 認証は事前に定義されたアクセス許可規則によって有効になり、ソース コードまたは構成ファイル内でハードコーディングされた資格情報を使用せずに済みます。

マネージド ID をサポートしていないサービスの場合、Azure AD を使用して、リソース レベルでアクセス許可が制限された[サービス プリンシパル](/azure/active-directory/develop/app-objects-and-service-principals)を代わりに作成します。 証明書の資格情報を使用してサービス プリンシパルを構成し、クライアント シークレットにフォールバックすることをお勧めしました。 どちらの場合も、[Azure Key Vault](/azure/key-vault/general/overview) を Azure マネージド ID と組み合わせて使用し、ランタイム環境 (Azure 関数など) でキー コンテナーから資格情報を取得できるようにすることができます。

Azure セキュリティ ベンチマーク「[ID-2: アプリケーション ID を安全かつ自動的に管理する](/azure/security/benchmarks/security-controls-v2-identity-management#id-2-manage-application-identities-securely-and-automatically)」も参照してください。

## <a name="11-architecture-establish-a-single-unified-security-strategy"></a>11.アーキテクチャ:単一の統合セキュリティ戦略を確立する

"*ボートが前進するには、全員が同じ方向に漕ぐ必要があります。* "

**内容**: すべてのチームが、エンタープライズ システムとデータを有効にし、セキュリティで保護する単一の戦略に整合しているようにします。

**理由**: 複数のチームが共通の戦略に整合せず、ばらばらに作業した場合、各自のアクションが意図せず相互に悪影響を与え、不要な摩擦が生じて、すべてのユーザーの目標達成速度が低下する可能性があります。

多くの組織でこれが一貫して実施されている例の 1 つは、資産のセグメント化です。

- "_ネットワーク セキュリティ チーム_" は、"_フラット ネットワーク_" をセグメント化してセキュリティを強化する戦略を (多くの場合、物理サイト、割り当てられた IP アドレスや範囲などに基づいて) 策定します。
- それとは別に、"_ID チーム_" は、組織についての理解と知識に基づいて、グループおよび Active Directory 組織単位 (OU) に関する戦略を策定しました。
- "_アプリケーション チーム_" は、これらのシステムは使用するのが難しいと感じていることがよくあります。ビジネスの運用、目標、リスクについてのインプットと理解が制限された状態で設計されているためです。

このような状況が発生した組織では、チームに頻繁にファイアウォールの例外についての競合が発生し、それによる悪影響がセキュリティ (例外は通常承認される) と生産性 (ビジネスに必要なアプリケーション機能のデプロイが遅くなる) の両方に生じます。

セキュリティで批判的思考を強制することで健全な摩擦を発生させることができますが、この競合で発生するのは、目標を妨げる異常な摩擦だけです。 詳細については、セキュリティ戦略ガイダンスの「[適切なレベルのセキュリティ上の摩擦](../strategy/define-security-strategy.md#modernize-your-security-strategy)」をご覧ください。

**対象者**:

- **スポンサー:** 通常、統合戦略は CIO、CISO、CTO が共同で支援し (多くの場合、一部の高レベルの要素に対するビジネス リーダーのサポートを伴います)、各チームの代表者によって支持されます。
- **実行:** セキュリティ戦略は全員が実装する必要があるため、チーム全体からのインプットを統合して、所有権、賛同、成功の可能性を高める必要があります。
  - **[セキュリティ アーキテクチャ](../organize/cloud-security-architecture.md):** セキュリティ戦略と結果のアーキテクチャを構築し、チームからのフィードバックを積極的に収集して、さまざまなユーザーのためにプレゼンテーション、ドキュメント、図で文書化します。
  - **[ポリシーと標準](../organize/cloud-security-policy-standards.md):** 適切な要素を標準およびポリシーに取り入れ、コンプライアンスを監視します。
  - **すべてのテクニカル IT 担当およびセキュリティ担当チーム:** インプットの要件を指定し、エンタープライズ戦略に整合するように実装します。
  - **アプリケーションの所有者と開発者:** 適用される戦略に関するドキュメント (理想的には、各自のロールに合わせて調整したガイダンス) を読み、理解します。

**方法**:

すべてのチームからのインプットと積極的な参加を含むクラウドのセキュリティ戦略を構築し、実装します。 プロセス ドキュメントの形式はさまざまですが、常に次のものが含まれる必要があります。

- **チームからの積極的なインプット:** 通常、組織内のユーザーが賛成しない戦略は失敗します。 理想的には、すべてのチームを同じ部屋に集めて、戦略を共同で構築します。 私たちがお客様と一緒に実施しているワークショップでは、多くの場合、組織が事実上縦割りで運用されていることが判明し、それらの会議で互いに初めて顔を合わせることがよくあります。 また、包括性が必要とされることもわかりました。 一部のチームが招待されていない場合は、通常、すべての参加者が参加するまで (またはプロジェクトが先に進むまで)、この会議を繰り返す必要があります。
- **文書化されていて明確に伝わる:** すべてのチームは、セキュリティを統合する理由、セキュリティで重要なこと、セキュリティの成功がどのように見えるかなど、セキュリティ戦略 (理想的にはテクノロジ戦略全体のセキュリティ コンポーネント) を認識している必要があります。 これには、アプリケーション チームと開発チームに固有のガイダンスが含まれている必要があります。そうすることで、ガイダンスの関連性のない部分を読む必要がない、明確な優先順位が示されたガイダンスを手に入れることができます。
- **安定していながら柔軟である:** 戦略は比較的一貫した安定した状態に保つ必要がありますが、アーキテクチャとドキュメントは、明確にするため、また、クラウドの動的な特性に対応するために、変更が必要になる場合があります。 たとえば、使用しているサードパーティの次世代ファイアウォールから Azure Firewall に移行し、その方法に関する図やガイダンスを調整した場合でも、悪意のある外部トラフィックをフィルターで除外することは、戦略的な必須事項として一貫性を保ちます。
- **セグメンテーションから開始する:** クラウド導入の過程で、チームは大小さまざまな戦略トピックに取り組みますが、どこかから始める必要があります。 セキュリティ戦略は、後で変更するのが難しく、ビジネスのインプットと多数の技術チームの両方を必要とする基本的な決定であるため、エンタープライズ資産のセグメンテーションから開始することをお勧めします。

Microsoft では、[セグメント化戦略の Azure への適用](/security/compass/microsoft-security-compass-introduction#azure-components-and-reference-model-2151)に関するビデオ ガイダンス、および[企業のセグメント化](/security/compass/governance#enterprise-segmentation-strategy)と[それに合わせたネットワーク セキュリティ](/security/compass/network-security-containment#align-network-segmentation-with-enterprise-segmentation-strategy)に関するドキュメントを公開しています。

クラウド導入フレームワークには、次のことを行うチームを支援するためのガイダンスが含まれています。

- **[クラウド戦略チームを結成する](../get-started/team/cloud-strategy.md):** 理想的には、既存のクラウド戦略にセキュリティを統合する必要があります。
- **[セキュリティ戦略を構築または最新化する](../strategy/define-security-strategy.md):** クラウド サービスと最新の脅威の現代におけるビジネスおよびセキュリティの目標を達成します。

[Azure セキュリティ ベンチマークのガバナンスと戦略](/azure/security/benchmarks/security-controls-v2-governance-strategy)に関する記事もご覧ください。

---
title: 競合する優先順位のバランスを取る
description: 競合する優先順位のバランスを取る戦略を見い出します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 03/04/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: strategy
ms.custom: internal
ms.openlocfilehash: 06fcd59e26240a01c8b64e391c7e36595cc77de9
ms.sourcegitcommit: b8f8b7631aabaab28e9705934bf67dad15e3a179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2021
ms.locfileid: "101787945"
---
# <a name="balance-competing-priorities"></a>競合する優先順位のバランスを取る

デジタル変革過程に着手することは、ビジネス チームとテクノロジ チーム全体の利害関係者に対する強制的な機能のようなものです。 成功への道は、競合する優先順位のバランスを取る組織の能力にしっかりと根ざしています。

他のデジタル変革と同様に、クラウドの導入によって、導入のライフサイクル全体で競合する優先順位が明らかになります。 他の形態の変革と同様に、こうした優先順位の中でバランスを見つけられるかどうかが、ビジネス価値の実現に大きな影響を与えます。 このような競合する優先順位のバランスを取るには、利害関係者間の (場合によっては個人の協力者との) 開かれた (時には難しい) 会話が必要になります。

この記事では、各手法の実行中に一般的に議論される競合する優先順位の一部について概要を説明します。 この高度な認識を持つと、クラウド導入戦略を立てる際に、このような議論に備えることができます。

![クラウド導入ライフサイクルの概要](../_images/caf-overview.png)

以下のセクションは、上記のクラウド導入ライフサイクルのフローに沿っています。 ただし、クラウド導入は (シーケンシャル プロセスではなく) 反復的であり、このような競合する優先順位はクラウド導入過程のさまざまな時点で出現する (場合によっては再び出現する) ことを認識することが重要です。

## <a name="general-theme-of-the-cloud-adoption-framework-approach"></a>クラウド導入フレームワーク アプローチの一般的なテーマ

モノリシック ソリューションと高度な計画は、いずれも一連の仮定に基づいて構築されており、時間の経過と共に正確であることが証明される場合とされない場合があります。 クラウドを導入することは、多くの場合、ビジネス チームと技術チームにとって新しいエクスペリエンスです。 ほとんどの新しいエクスペリエンスや学習機会と同様に、こうした仮定は、高い確率で間違っていたと証明されます。

このフレームワーク内のほとんどのガイダンスでは、技術的な決定の遅延に関して実績のあるアジャイルの基本原則に従うことが好ましいアプローチです。 このアプローチでは、一般的な最終状態を確立し、初期実装に迅速に移行し、仮定をテストして検証し、早期にリファクターして仮定に対処するという一貫したパターンに従います。 このような成長マインドセットでは、学んだことが最大限に生かされ、ビジネス価値に対するリスクが最小限に抑えられますが、多少のあいまいさを受け入れる必要があります。

場合によっては、あいまいさは誤った仮定よりも恐ろしい (またはより危険な) ものになります。 このフレームワークは、実行時のあいまいさの学習と対処を重視していますが、分析ベースまたは仮定ベースのアプローチを重視する必要がある場合もよくあります。 以下のセクションでは、各セクションで少なくとも 1 つの "範囲の拡張例" を説明し、2 回目のより深いイテレーションが重要な場合について説明します。

## <a name="balance-during-the-strategizing-phase"></a>戦略フェーズでのバランス

戦略手法の中心となる目的は、利害関係者間の連携関係を作り上げることです。 定義が完了すると、その連携された戦略的なポジションによって、各手法全体で行動が促進され、技術的な決定が望ましいビジネスの成果と合うようになります。 利害関係者間の連携関係を築くことで、共通セットの競合する優先順位が作られます。つまり、**正当な理由の深さ** と **業務の成果が出るまでの時間** です。

**競合する優先順位:**

- **正当な理由の深さ:** 多くの場合、利害関係者は、詳細な財務分析と完全な業務上の正当な理由が、戦略の方向と問題なく合致することを望んでいます。 残念ながら、このレベルの分析では、データの収集と分析が可能になるまでに長時間かかる場合があります。
- **業務の成果が出るまでの時間:** 逆に、利害関係者は、定義された時間枠内で業務の成果を出す責任を負うことがよくあります。 分析と評価に時間がかかると、技術的な作業が始まる前に、そのような成果を達成できなくなる危険性があります。

**最小範囲:** このバランスを見つけるには、プロセスの早い段階で利害関係者間で議論する必要があります。 この戦略手法では、この初期の取り組みの間は連携の範囲を制限することを推奨します。 この推奨されるアプローチでは、利害関係者は、一連の主要な動機、測定可能な成果、高度な業務上の正当な理由に焦点を合わせます。 利害関係者は、少数の初期プロジェクトまたはパイロットに迅速に取り組み、必要な学習機会を促進する必要があります。

**範囲の拡張例:** 初期のビジネス分析でビジネスに悪影響が及ぶ危険性が高いとわかった場合、利害関係者は、業務上の正当な理由の段階で、詳細な分析をより時間をかけて慎重に評価する必要があります。

## <a name="balance-during-the-planning-phase"></a>計画フェーズでのバランス

戦略フェーズでの優先順位と同様に、計画フェーズでも、初期計画と技術的な決定の遅延のバランスを取る必要があります。

**競合する優先順位:**

- クラウドでの技術的な実装に関する **初期計画の深さ** には、多くの場合、多数の仮定が含まれています。 特に、チームのスキルにギャップがある場合、環境の検出のギャップに悩まされたり、ワークロードのアーキテクチャの最終状態が明確に定義されません。 こうした仮定はいずれも、詳細なクラウド導入計画でよく見られます。 これらの仮定を取り除くには、実験、パイロット、および定性分析が必要です。
- **技術的な決定の遅延** では、技術的な決定を下すタイミングを遅くするほど、その決定がより正確になると仮定します。 アジャイル製品計画の基本原則に従うことで、技術的な決定を遅らせ、適切なタイミングで十分な情報を得られるようになります。 ただし、このアプローチでは、初期計画のあいまい度がはるかに高くなります。

**最小範囲:** アジャイル製品開発アプローチでは、管理しやすい計画内で即時のアクションを推進するように推奨されています。 計画手法では、次の手順でこのバランスを実現することをお勧めします。 自動検出ツールを使用して完全なデジタル資産の目録を作成します。ただし、段階的な合理化を使用して、今後 1 か月から 3 か月くらいの作業の計画を立てます。 迅速に対応するために、組織の適切な連携を確保します。 割り当てられたチームのスキル準備計画を立てます。 戦略と計画のテンプレートを使用して、初期バックログを迅速にデプロイします。

**範囲の拡張例:** クラウド導入計画の遂行は、時間に左右される、または影響の大きいビジネス イベントに対応している場合があります。 成功するには一定期間内に多数の資産を移行する必要がある場合、上記の手順に続いてより深い計画作業が行われることがよくあります。 このようなシナリオで成功するための鍵は、十分な計画を立ててから、完全なエンゲージメントを計画することです。 このアプローチによって、計画がビジネスの成果を妨げる可能性が低くなります。

## <a name="balance-during-the-readiness-phase"></a>準備フェーズでのバランス

導入チームがクラウドへの最初の手順の準備をしているとき、導入までにかかる時間と長期的な運用の間で優先順位が競合することがよくあります。 チームは、タスクをチーム内で遂行する方がよいか、管理される方がよいかを悩む場合があります。 このような悩みは、プラットフォームの開発には物理的な資産と獲得サイクルが必要な従来の IT 環境で必ず生じます。 ただし、IT プラットフォーム全体がコードで定義されている場合、従来の開発戦略 (リファクターなど) では、最初から適切に管理する必要が軽減されます。

**競合する優先順位:**

- **長期的な運用:** 多くの場合、お客様は、現在の運用管理、ガバナンス、およびセキュリティ システムと同等の機能を満たすクラウド環境を確保するという要望が妨げになっています。 現在のお客様の調査によると、90% を超えるお客様がこの思考様式を超えたサポートを必要としています。 この妨げる要素によって、業務の成果を遅らせたり防いだりする数か月間の遅延が追加されます。
- **導入までの時間:** Azure Policy、Azure Blueprints、管理グループなどのクラウドベースのツールを使用すると、IT プラットフォーム全体のリファクタリングが簡単になります。 さらに、事前に定義されたランディング ゾーンがあると、多くの同等の機能要件を既に満たしている環境への展開を加速できる、意見に基づいたポジションを用意できます。 長期的な運用への影響を最小限に抑えながら、市場投入までの時間を短縮できる可能性があります。

**最小範囲:** 準備手法は、迅速な導入から長期的な運用への直接的な道筋を示しています。 このアプローチは、環境のリファクタリングを可能にするツールの基本的な概要から始まります。 これらのツールと環境要件に基づいて、お客様は事前に定義されたランディング ゾーン (それぞれ、コード モデルとしてインフラストラクチャを使用して提供されます) の選択に導かれます。 クラウド導入の過程でこのコードをリファクターし、運用、セキュリティ、および管理を向上させることができます。

<!-- docutune:casing "Govern and Manage methodologies" -->

**範囲の拡張例:** **クラウドで 1,000 を超える資産 (アプリケーション、インフラストラクチャ、またはデータ資産)** をホストすることを導入計画の中期目標 (24 か月以内) としているチームの場合、ランディング ゾーンのより堅牢なビューが推奨されます。 このような状況では、最初のランディング ゾーンの会話中に、ガバナンスと管理の手法を検討する必要があります。 ただし、このより深い検討により、クラウド導入計画に数週間から数か月が追加されることがよくあります。 業務の成果への影響を最小限に抑えるために、導入チームは、より成熟したランディング ゾーンと中央アーキテクチャ ソリューションの作成と並行して、クラウド内で実際のワークロードをパイロットする必要があります。

## <a name="balance-during-the-migration-phase"></a>移行フェーズでのバランス

移行作業段階で、導入チームは、ワークロードが現状のままの構成でクラウドに再ホストされると仮定するのが一般的です。 このことは、すべてのワークロードを再構築してクラウド機能をより有効に活用する先進的な考え方と直接競合します。 ただし、この 2 つは相互に排他的ではなく、共通のプロセスで管理される場合は補完的です。

**競合する優先順位:**

- **再ホスト:** お客様は、多くの場合、移行を、現在の状態構成ですべての資産をクラウドにレプリケートする "_リフト アンド シフト_" 動作と同等と考えます。 その結果、IT ポートフォリオ内の誤差がほとんどなくなります。 このアプローチは、既存のデータセンターの資産を廃止する最速の方法でもあります。
- **再設計:** 各ワークロードのアーキテクチャを最新化することで、コスト、パフォーマンス、および運用全体のクラウドの価値が最大化されます。 ただし、このアプローチは非常に時間がかかり、多くの場合、各アプリケーションのソース コードへのアクセスが必要です。

**最小範囲:** 初期段階の計画では、このオプションは技術的な決定ではなく、最初のビジネスの仮定であることを明確に理解したうえで、計画に再ホスト オプションを使用します。 この移行手法では、クラウド導入チームは移行されたワークロードごとにこの仮定を検討します。 この手法では、各ワークロードまたはグループ、または移行ファクトリを作成するワークロードの評価/移行/昇格アプローチに従います。 評価フェーズで、導入チームは、各ワークロードの技術的な適合とアーキテクチャを評価します。 アーキテクチャ内のコンポーネントの多くはリファクタリングと最新化のために選択される傾向があるため、その評価作業が純粋なリフトアンドシフト アプローチになることはほとんどありません。

**範囲の拡張例:** メインフレームや多層マイクロサービス アプリケーションなどのミッション クリティカルな、または機密性の高いワークロードの場合、評価フェーズでワークロードのより深い評価が必要になる場合があります。 このような再構築の状況では、お客様は Microsoft Azure Well-Architected Review と [Microsoft Azure Well-Architected Framework](/azure/architecture/framework) を使用して、評価の間にワークロードの要件を調整する必要があります。

## <a name="balance-during-the-innovation-phase"></a>イノベーション フェーズでのバランス

真の顧客向けイノベーションによって、計画された機能セットを実現する必要性と、顧客の共感を得るプロセスとの間に共通の競合する優先順位が生み出されます。

**競合する優先順位:**

- **機能の焦点:** イノベーションの初期計画は、顧客のニーズを満たす一連の機能を提供する既存のデジタル資産とクラウド機能に基づいて構築されます。 この計画によって技術的な実装を簡単に促進し、開発作業に焦点を絞った機能を実現できます。 このアプローチは、多くの場合、一時的には利害関係者が満足しますが、顧客行動に影響を与えるイノベーションを促進する可能性が低くなります。
- **顧客の共感:** 初期計画は、開発のビジネス面の重要な部分であり、定期的なレポートに含める必要があります。 一方、顧客の共感の学習、測定、および構築は、イノベーションの取り組みにおいて成功のより正確な尺度となります。 機能よりも顧客に焦点を当てると、短期的および長期的な顧客満足度と業務の成果につながる可能性が高くなります。

**最小範囲:** イノベーション手法では、ビジネス価値の合意を通じて戦略と計画を統合する方法が示されます。 また、このガイドでは、実装のベスト プラクティスと共に、イノベーションの各分野を加速できるクラウド ネイティブ ツールを紹介します。 最後に、プロセスの改善に関するセクションでは、クラウド導入過程で計画と戦略を尊重しながら、顧客の共感を構築するためのアプローチを示します。 このアプローチは、できる限り少ないテクノロジを使用してイノベーションを実現することに焦点を当てています。

**範囲の拡張例:** イノベーションは、ミッションクリティカルなワークロードや機密性の高いワークロードに左右される場合があります。 "顧客" が社内ユーザーの場合、最初期のイテレーションの間は、開発作業がミッションクリティカルで機密性の高い可能性があります。 このようなシナリオでは、導入チームが Microsoft Azure Well-Architected Review と Microsoft Azure Well-Architected Framework を使用して、プロセスの初期段階で高度なアーキテクチャ設計を評価する必要があります。

## <a name="balance-during-the-governance-phase"></a>ガバナンス フェーズでのバランス

クラウド ガバナンスの実践とは、2 つの競合する優先事項 (速度と機敏性という事項と適切に統制された環境という事項) の間で一定のバランスを保つことです。 クラウド ガバナンス チームは、統一された制御と変更の最小化により、ビジネスに対するリスクを評価および最小化することに焦点を当てています。 導入チームは、新しいリスクが必ず生じ、それによって変化がもたらされる業務の成果の推進に焦点を当てています。

**競合する優先順位:**

- **適切な統制:** リスクを最小限に抑えるように設計されたすべての制御は、変更の一部の妨げになったり、設計の選択肢の制約になったりします。 制御は、適切に統制された環境には不可欠です。 ただし、制御を個別に設計および展開すると、防ぐつもりのリスクと同じくらいの損害が生じる可能性があります。
- **速度と機敏性:** 速度と機敏性は、デジタル経済における基本的なビジネス要件です。 どちらも、イノベーションや導入を妨げるものを最小限に抑えて変更を推進する能力が必要です。 ガバナンスを分離して変更を推進すると、意図しない形でビジネスに悪影響を及ぼす可能性のある新しいリスクが生じます。

**最小範囲:** ガバナンス手法では、ガバナンスも導入も単独で行われるべきではないことが推奨されます。 この手法は、ガバナンスの規律の理解と、ビジネス リスク、ポリシー、およびプロセスに関する会話から始まります。 ガバナンス チームは、クラウド導入の全過程でアクティブなメンバーとして、クラウド導入計画内の具体的なリスクに対処するための最小限の一連のガードレールを実装できます。 時間の経過と共に、ガバナンス チームは、新しいガードレールをリファクターおよび拡張し、新しいリスクに対応することができます。 このアプローチを採用すると、リスクを最小限に抑えながら、学習とイノベーションを最大化できます。

**範囲の拡張例:** ビジネス リスクが高い場合は (特に導入の初期段階では)、クラウド ガバナンス チームは必要に応じてガバナンスの実装の拡大を加速します。 このより高いレベルのガバナンスを追加するには、同じガイダンスと演習を使用できますが、タイミングを早める必要がある場合があります。 一部のシナリオでは、最初のランディング ゾーンの展開段階で、ガバナンスの高度な状態が必要になる場合もあります。

## <a name="balance-during-the-management-phase"></a>管理フェーズでのバランス

運用管理に関する IT ビジネス モデルは、過去 10 年間にわたって継続的に進化しています。 ハードウェア メンテナンスが IT の中核的な価値提案ではなくなるにつれて、運用管理に対する見方も変わりました。 IT がビジネス価値の提供に重点を置くようになるにつれて、運用管理チームは、運用なし/低運用と広範な投資とのバランスを取ることの間で対立します。

**競合する優先順位:**

- **広範な投資:** 環境全体の停止回避、迅速な復旧、および監視に等しく投資することは、運用管理に対する従来のアプローチです。 このアプローチはコストがかかり、場合によっては、クラウド ベンダーが提供するサポート製品が重複する可能性があります。
- **運用なしと低運用:** クラウドネイティブの運用ツールを使用して、以前はフルタイムの従業員が行っていた反復的なタスクを最小限に抑えます。 運用管理モデルでこれらの運用上の依存関係を減らすと、このような従業員は解放され、より多くの成果を上げられるようになります。 このアプローチだけでも、運用のサポートを軽減できる可能性があります。

**最小範囲:** 管理手法では、クラウドネイティブの運用なしベースラインを確立することが推奨されます。 運用なしベースラインではすべてのビジネス ニーズが満たされるわけではないことを認めたうえで業務に取り組み、コミットメントを定義し、投資をより適切に調整します。 すべてのワークロードの共通ニーズを満たすためにベースラインを拡張します。 次に、プラットフォーム チームまたは特定のワークロード チームが、適切に管理された環境内で適切に管理されたソリューションを維持できるようにします。

**範囲の拡張例:** ほとんどの環境では、IT が運用することに多額を投資することにビジネス価値があるワークロードの割合はわずかです。 このようなシナリオでは、IT チームは、Microsoft Azure Well-Architected Review と Microsoft Azure Well-Architected Framework を使用して、より詳細な運用をガイドすることもできます。

## <a name="balance-during-the-organization-phase"></a>整理フェーズでのバランス

この記事全体で競合する優先事項は、速度と機敏性に対するビジネス ニーズに応える IT の意欲を反映しています。 これと同じシフトが組織図 (または仮想チーム構造) の変更に反映され、ビジネスの成果に対するサポートが強化されます。 IT リーダーはチーム構造を検討するときに、一般的に 2 つの競合する優先事項 (一元管理と委任管理) に対処します。

**競合する優先順位:**

- **一元管理:** この運用モデルでは、厳格なポリシーを実施するために必要なすべての管理の一元化に焦点が当てられています。 このモデルでは、IT はイノベーション、速度、機敏性を妨げるものになります。 ただし、IT は安定性、コンプライアンス、およびセキュリティのレベルを高めることができます。
- **委任管理:** この分散型の運用モデルでは、各 DevOps チームまたはビジネス アプリケーション チームが、事業目標の達成に必要なソリューションに基づいて、独自の一連の管理を用意することを前提としています。 このモデルでは、チームが道から外れないように IT がガードレールを用意します。ただし、強制される技術的な制約の数をできる限り最小限に抑えます。

**最小範囲:** ほとんどの組織は、時間の経過と共に自然な一連の進化を経ます。 整理手法では、最も一般的な一連の進化の概要を説明します。 推奨されるガイダンスは、チームが委任管理アプローチを実現するために、クラウド センター オブ エクセレンス (CCoE) 構造に向かって取り組むことです。

**範囲の拡張例:** 一元管理の必要性がトリガーされる状況はさまざまです。 サード パーティのコンプライアンス要件と一時的なセキュリティ侵害は、一元管理のトリガーの 2 つの例です。 このような状況では、一般的に、制限ポリシーと厳格で固定された管理を確立する必要があります。 ただし、イノベーションと導入を継続するには、中央の IT チームが各ワークロードの重要度と機密性に基づいてこのような管理を実現することをお勧めします。 管理が少なく、範囲またはリスク プロファイルを減らした環境を用意することで、管理が必要な場合でも柔軟に対応できます。

## <a name="next-steps"></a>次のステップ

クラウド移行の取り組みの価値を最大限に高めるために、[移行、イノベーション、実験のバランスを取る](./balance-the-portfolio.md)方法を確認します。

> [!div class="nextstepaction"]
> [ポートフォリオのバランスを取る](./balance-the-portfolio.md):

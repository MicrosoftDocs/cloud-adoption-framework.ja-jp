---
title: 名前付け規則を定義する
description: Azure のリソースと資産の名前付けに関する考慮事項について説明し、Azure のリソースと資産の名前の例を確認します。
author: BrianBlanchard
ms.author: brblanch
ms.date: 12/01/2020
ms.topic: conceptual
ms.service: cloud-adoption-framework
ms.subservice: ready
ms.custom: internal, readiness, fasttrack-edit
ms.openlocfilehash: 5250b4b3876516bbc3239477435cc08adc59494e
ms.sourcegitcommit: 9e4bc0e233a24642853f5e8acbeb9746b2444024
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "102115749"
---
# <a name="define-your-naming-convention"></a>名前付け規則を定義する

有効な名前付け規則は、各リソースに関する重要な情報からリソース名を作成します。 適切な名前にすると、リソースの種類、それに関連付けられたワークロード、そのデプロイ環境、およびそれをホストしている Azure リージョンをすばやく識別できます。 たとえば、米国西部リージョンに存在する運用 SharePoint ワークロードのパブリック IP リソースは `pip-sharepoint-prod-westus-001` になります。

![Azure リソース名のコンポーネント](../../_images/ready/resource-naming.png)

*図 1:Azure リソース名のコンポーネント。*

## <a name="naming-scope"></a>名前付けスコープ

すべての Azure リソースの種類には、リソース名が一意である必要があるレベルを定義するスコープがあります。 リソースには、そのスコープ内の一意の名前が必要です。

たとえば、仮想ネットワークにはリソース グループ スコープがあります。つまり、指定されたリソース グループには `vnet-prod-westus-001` という名前の 1 つのネットワークだけが存在できます。 他のリソース グループは `vnet-prod-westus-001` という名前の独自の仮想ネットワークを持つことができます。 サブネットはスコープが仮想ネットワークに設定されるため、仮想ネットワーク内の各サブネットは個別の名前を持つ必要があります。

パブリック エンドポイントを含む PaaS サービスや仮想マシンの DNS ラベルなどの一部のリソース名はグローバル スコープを持つため、Azure プラットフォーム全体で一意である必要があります。

![Azure リソース名のスコープ レベル](../../_images/ready/resource-naming-scope.png)

*図 2:Azure リソース名のスコープ レベル。*

リソース名には長さの制限があります。 名前付け規則を作成するときに、名前に埋め込まれるコンテキストと、そのスコープおよび長さの制限のバランスをとることが重要です。 詳細については、「[Azure リソースの名前付け規則と制限事項](/azure/azure-resource-manager/management/resource-name-rules)」を参照してください。

### <a name="recommended-naming-components"></a>推奨される名前付けコンポーネント

名前付け規則を作成する場合は、リソース名に反映させる重要な情報を特定します。 リソースの種類によって関連する情報は異なります。 次の一覧は、リソース名を作成するときに役立つ情報の例を示しています。

リソース名の長さの制限を超えないようにするために、名前付けコンポーネントの長さは短いままにしてください。

| 名前付けコンポーネント | 説明 |
|--|--|--|
| **リソースの種類** | Azure リソースまたは資産の種類を表す省略形。 この構成要素は、多くの場合、名前のプレフィックスまたはサフィックスとして使用されます。 詳細については、「[Azure リソースの種類に推奨される省略形](./resource-abbreviations.md)」を参照してください。 例: `rg`、`vm` |
| **事業単位** | リソースが属しているサブスクリプションまたはワークロードを所有する会社の最上位の部門。 小規模な組織では、このコンポーネントは 1 つの会社の最上位の組織要素を表す可能性があります。 例: `fin`、`mktg`、`product`、`it`、`corp` |
| **アプリケーションまたはサービス名** | リソースが属しているアプリケーション、ワークロード、またはサービスの名前。 例: `navigator`、`emissions`、`sharepoint`、`hadoop` |
| **サブスクリプションの種類** | リソースが含まれているサブスクリプションの目的に関する概要の説明。 多くの場合は、デプロイ環境の種類または特定のワークロードによって分類されます。 例: `prod`、`shared`、`client` |
| **デプロイ環境&nbsp;** | リソースによってサポートされているワークロードの開発ライフサイクルのステージ。 例: `prod`、`dev`、`qa`、`stage`、`test` |
| **リージョン** | リソースがデプロイされている Azure リージョン。 例: `westus`、`eastus2`、`westeu`、`usva`、`ustx` |

## <a name="example-names-for-common-azure-resource-types"></a>一般的な Azure リソースの種類の名前の例

次のセクションでは、エンタープライズ クラウドのデプロイにおける一般的な Azure リソースの種類のいくつかのサンプル名を示します。

> [!NOTE]
> これらの名前の例の一部では、`mktg-prod-001` など、3 桁の埋め込みスキーム (`###`) が使用されています。
>
> 構成管理データベース (CMDB)、IT 資産管理ツール、または従来のアカウンティング ツールでこれらの資産が管理されている場合、埋め込みにより、資産の読みやすさが向上し、並び替えが強化されます。 デプロイされた資産が IT 資産の大規模なインベントリまたはポートフォリオの一部として一元的に管理されている場合、埋め込みアプローチは、インベントリの名前付けを管理するためにこれらのシステムで使用されるインターフェイスと適合します。
>
> 残念ながら、従来の資産埋め込みアプローチは、非埋め込み数値に基づいて資産を反復処理する場合のある、コードとしてのインフラストラクチャのアプローチでは問題が発生する可能性があります。 このアプローチは、デプロイまたは自動構成管理のタスクにおいて一般的です。 これらのスクリプトでは、埋め込みを定期的に削除し、埋め込まれた数値を実数に変換する必要があります。これにより、スクリプトの開発と実行時間が遅くなります。
>
> 組織に適したアプローチを選択してください。 ここで紹介する埋め込みは、インベントリの番号付けに対して一貫したアプローチを使用することの重要性を示すもので、どちらのアプローチが優れているかを示すものではありません。 (埋め込みの有無に関係なく) 番号付けスキームを選択する前に、長期的な運用に影響する内容をさらに評価してください:CMDB や資産管理のソリューションまたはコードベースのインベントリ管理。 その後、運用ニーズに最適な埋め込みオプションを採用します。

<!-- cspell:ignore cloudapp azurewebsites servicebus -->

<!-- cspell:ignoreRegExp [a-z]+-[a-z]+ -->
<!-- cspell:ignoreRegExp `[a-z]+` -->
<!-- cspell:ignoreRegExp [a-z]+\d+ -->
<!-- cspell:ignoreRegExp _[a-z]+[\\-] -->

## <a name="example-names-general"></a>名前の例:全般

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **管理グループ** | 事業単位および/または <br> 環境の種類 | *mg-\<business unit>[-\<environment type>]* <br><br> <li> `mg-mktg` <li> `mg-hr` <li> `mg-corp-prod` <li> `mg-fin-client` |
| **サブスクリプション** | アカウント/エンタープライズ契約 | *\<business&nbsp;unit>-\<subscription&nbsp;type>-\<###>* <br><br> <li> `mktg-prod-001` <li> `corp-shared-001` <li> `fin-client-001` |
| **リソース グループ** | サブスクリプション | *rg-\<app&nbsp;or&nbsp;service&nbsp;name>-<subscription&nbsp;type>-\<###>* <br><br> <li> `rg-mktgsharepoint-prod-001` <li> `rg-acctlookupsvc-shared-001` <li> `rg-ad-dir-services-shared-001` |
| **API 管理サービス インスタンス** | グローバル | *apim-\<app&nbsp;or&nbsp;service&nbsp;name>* <br><br> `apim-navigator-prod` |
| **管理対象 ID** | リソース グループ | *id-\<app&nbsp;or&nbsp;service&nbsp;name>* <br><br> <li> `id-appcn-keda-prod-eastus2-001` |

## <a name="example-names-networking"></a>名前の例:ネットワーク

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **仮想ネットワーク** | リソース グループ | *vnet-\<subscription&nbsp;type>-\<region>-\<###>* <br><br> <li> `vnet-shared-eastus2-001` <li> `vnet-prod-westus-001` <li> `vnet-client-eastus2-001` |
| **サブネット** | 仮想ネットワーク | *snet-\<subscription>-\<region>-\<###>* <br><br> <li> `snet-shared-eastus2-001` <li> `snet-prod-westus-001` <li> `snet-client-eastus2-001` |
| **ネットワーク インターフェイス (NIC)** | リソース グループ | *nic-<##>-\<vm&nbsp;name>-\<subscription>-\<###>* <br><br> <li> `nic-01-dc1-shared-001` <li> `nic-02-vmhadoop1-prod-001` <li> `nic-02-vmtest1-client-001` |
| **パブリック IP アドレス** | リソース グループ | *pip-\<vm&nbsp;name&nbsp;or&nbsp;app&nbsp;name>-\<environment>-\<region>-\<###>* <br><br> <li> `pip-dc1-shared-eastus2-001` <li> `pip-hadoop-prod-westus-001` |
| **Load Balancer** | リソース グループ | *lb-\<app&nbsp;name&nbsp;or&nbsp;role>-<environment>-\<###>* <br><br> <li> `lb-navigator-prod-001` <li> `lb-sharepoint-dev-001` |
| **ネットワーク セキュリティ グループ (NSG)** | サブネットまたは NIC | *nsg-\<policy&nbsp;name&nbsp;or&nbsp;app&nbsp;name>-\<###>* <br><br> <li> `nsg-weballow-001` <li> `nsg-rdpallow-001` <li> `nsg-sqlallow-001` <li> `nsg-dnsblocked-001` |
| **ローカル ネットワーク ゲートウェイ** | 仮想ゲートウェイ | *lgw-\<subscription&nbsp;type>-\<region>-\<###>* <br><br> <li> `lgw-shared-eastus2-001` <li> `lgw-prod-westus-001` <li> `lgw-client-eastus2-001` |
| **仮想ネットワーク ゲートウェイ** | 仮想ネットワーク | *vgw-\<subscription&nbsp;type>-\<region>-\<###>* <br><br> <li> `vgw-shared-eastus2-001` <li> `vgw-prod-westus-001` <li> `vgw-client-eastus2-001` |
| **サイト間接続** | リソース グループ | *cn-\<local&nbsp;gateway&nbsp;name>-to-\<virtual&nbsp;gateway&nbsp;name>* <br><br> <li> `cn-lgw-shared-eastus2-001-to-vgw-shared-eastus2-001` <li> `cn-lgw-shared-eastus2-001-to-vgw-shared-westus-001` |
| **VPN 接続** | リソース グループ | *cn-\<subscription1>-\<region1>-to-\<subscription2>-\<region2>-* <br><br> <li> `cn-shared-eastus2-to-shared-westus` <li> `cn-prod-eastus2-to-prod-westus` |
| **ルート テーブル** | リソース グループ | *route-\<route&nbsp;table&nbsp;name>* <br><br> <li> `route-navigator` <li> `route-sharepoint` |
| **DNS ラベル** | グローバル | *\<DNS&nbsp;A&nbsp;record&nbsp;for&nbsp;VM>.\<region>.cloudapp.azure.com* <br><br> <li> `dc1.westus.cloudapp.azure.com` <li> `web1.eastus2.cloudapp.azure.com` |

## <a name="example-names-compute-and-web"></a>名前の例:コンピューティングと Web

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **仮想マシン** | リソース グループ | *vm\<policy name or app name>\<###>* <br><br> <li> `vmnavigator001` <li> `vmsharepoint001` <li> `vmsqlnode001` <li> `vmhadoop001` |
| **VM ストレージ アカウント** | グローバル | *stvm\<performance type>\<app name or prod name>\<region>\<###>* <br><br> <li> `stvmstcoreeastus2001` <li> `stvmpmcoreeastus2001` <li> `stvmstplmeastus2001` <li> `stvmsthadoopeastus2001` |
| **Web アプリ** | グローバル | *app-\<app name>-\<environment>-\<###>.azurewebsites.net* <br><br> <li> `app-navigator-prod-001.azurewebsites.net` <li> `app-accountlookup-dev-001.azurewebsites.net` |
| **関数アプリ** | グローバル | *func-\<app name>-\<environment>-\<###>.azurewebsites.net* <br><br> <li> `func-navigator-prod-001.azurewebsites.net` <li> `func-accountlookup-dev-001.azurewebsites.net` |
| **クラウド サービス** | グローバル | *cld-\<app name>-\<environment>-\<###>.cloudapp.net}* <br><br> <li> `cld-navigator-prod-001.azurewebsites.net` <li> `cld-accountlookup-dev-001.azurewebsites.net` |
| **Notification Hubs 名前空間** | グローバル | *ntfns-\<app name>-\<environment>* <br><br> <li> `ntfns-navigator-prod` <li> `ntfns-emissions-dev` |
| **通知ハブ** | Notification Hubs 名前空間 | *ntf-\<app name>-\<environment>* <br><br> <li> `ntf-navigator-prod` <li> `ntf-emissions-dev` |

## <a name="example-names-databases"></a>名前の例:データベース

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **Azure SQL Database サーバー** | グローバル | *sql-\<app name>-\<environment>* <br><br> <li> `sql-navigator-prod` <li> `sql-emissions-dev` |
| **Azure SQL データベース** | Azure SQL Database | *sqldb-\<database name>-\<environment>* <br><br> <li> `sqldb-users-prod` <li> `sqldb-users-dev` |
| **Azure Cosmos DB データベース** | グローバル | *cosmos-\<app name>-\<environment>* <br><br> <li> `cosmos-navigator-prod` <li> `cosmos-emissions-dev` |
| **Azure Cache for Redis インスタンス** | グローバル | *redis-\<app name>-\<environment>* <br><br> <li> `redis-navigator-prod` <li> `redis-emissions-dev` |
| **MySQL データベース** | グローバル | *mysql-\<app name>-\<environment>* <br><br> <li> `mysql-navigator-prod` <li> `mysql-emissions-dev` |
| **PostgreSQL データベース** | グローバル | *psql-\<app name>-\<environment>* <br><br> <li> `psql-navigator-prod` <li> `psql-emissions-dev` |
| **Azure SQL Data Warehouse** | グローバル | *sqldw-\<app name>-\<environment>* <br><br> <li> `sqldw-navigator-prod` <li> `sqldw-emissions-dev` |
| **SQL Server Stretch Database** | Azure SQL Database | *sqlstrdb-\<app name>-\<environment>* <br><br> <li> `sqlstrdb-navigator-prod` <li> `sqlstrdb-emissions-dev` |

## <a name="example-names-storage"></a>名前の例:ストレージ

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **ストレージ アカウント (全般)** | グローバル | *st\<storage name>\<###>* <br><br> <li> `stnavigatordata001` <li> `stemissionsoutput001` |
| **Storage アカウント (診断ログ)** | グローバル | *stdiag\<first 2 letters of subscription name and number>\<region>\<###>* <br><br> <li> `stdiagsh001eastus2001` <li> `stdiagsh001westus001` |
| **Azure StorSimple** | グローバル | *ssimp\<app name>-\<environment>* <br><br> <li> `ssimpnavigatorprod` <li> `ssimpemissionsdev` |
| **Azure Container Registry** | グローバル | *acr\<app name>\<environment>\<###>* <br><br> <li> `acrnavigatorprod001` |

## <a name="example-names-ai-and-machine-learning"></a>名前の例:AI と機械学習

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **Azure Cognitive Search** | グローバル | *srch-\<app name>-\<environment>* <br><br> <li> `srch-navigator-prod` <li> `srch-emissions-dev` |
| **Azure Cognitive Services** | リソース グループ | *cog-\<app name>-\<environment>* <br><br> <li> `cog-navigator-prod` <li> `cog-emissions-dev` |
| **Azure Machine Learning ワークスペース** | リソース グループ | *mlw-\<app name>-\<environment>* <br><br> <li> `mlw-navigator-prod` <li> `mlw-emissions-dev` |

## <a name="example-names-analytics-and-iot"></a>名前の例:Analytics と IoT

| 資産の種類 | Scope | 形式と例 |
|--|--|--|
| **Azure Data Factory** | グローバル | *adf-\<app name>\<environment>* <br><br> <li> `adf-navigator-prod` <li> `adf-emissions-dev` |
| **Azure Stream Analytics** | リソース グループ | *asa-\<app name>-\<environment>* <br><br> <li> `asa-navigator-prod` <li> `asa-emissions-dev` |
| **Data Lake Analytics アカウント** | グローバル | *dla\<app name>\<environment>* <br><br> <li> `dlanavigatorprod` <li> `dlanavigatorprod` |
| **Data Lake Storage アカウント** | グローバル | *dls\<app name>\<environment>* <br><br> <li> `dlsnavigatorprod` <li> `dlsemissionsdev` |
| **イベント ハブ** | グローバル | *evh-\<app name>-\<environment>* <br><br> <li> `evh-navigator-prod` <li> `evh-emissions-dev` |
| **HDInsight - HBase クラスター** | グローバル | *hbase-\<app name>-\<environment>* <br><br> <li> `hbase-navigator-prod` <li> `hbase-emissions-dev` |
| **HDInsight - Hadoop クラスター** | グローバル | *hadoop-\<app name>-\<environment>* <br><br> <li> `hadoop-navigator-prod` <li> `hadoop-emissions-dev` |
| **HDInsight - Spark クラスター** | グローバル | *spark-\<app name>-\<environment>* <br><br> <li> `spark-navigator-prod` <li> `spark-emissions-dev` |
| **IoT ハブ** | グローバル | *iot-\<app name>-\<environment>* <br><br> <li> `iot-navigator-prod` <li> `iot-emissions-dev` |
| **Power BI Embedded** | グローバル | *pbi-\<app name>-\<environment>* <br><br> <li> `pbi-navigator-prod` <li> `pbi-emissions-dev` |

## <a name="example-names-integration"></a>名前の例:統合

| 資産の種類 | Scope | 形式と例|
|--|--|--|
| **Service Bus** | グローバル | *sb-\<app name>-\<environment>.servicebus.windows.net* <br><br> <li> `sb-navigator-prod` <li> `sb-emissions-dev` |
| **Service Bus キュー** | Service Bus | *sbq-\<query descriptor>* <br><br> <li> `sbq-messagequery` |
| **Service Bus トピック** | Service Bus | *sbt-\<query descriptor>* <br><br> <li> `sbt-messagequery` |

## <a name="next-steps"></a>次のステップ

リソースと資産に名前を付けるときにさまざまな Azure リソースの種類に使用する推奨される省略形を確認します。

> [!div class="nextstepaction"]
> [Azure リソースの種類に推奨される省略形](./resource-abbreviations.md)

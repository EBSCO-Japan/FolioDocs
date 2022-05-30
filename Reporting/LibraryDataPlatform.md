---
title: "Library Data Platform"
linkTitle: "Library Data Platform"
date: 2021-10-26
weight: 10
tags: ["parenttopic"]
---


**注：**  [WOLFcon 2021 presentation](https://www.youtube.com/watch?v=SM1vq0zvxsY) で図書館データプラットフォームの概要が説明されています。


LDPソフトウェアがFOLIOに接続するためには、OkapiとFOLIOデータベースへの読み取り専用のアクセス権が必要です。LDPは、機関のスタッフによってローカルにホストされ管理されることもあれば、第三者にホスティングサービスを委託して管理されることもあります。[システム要件](https://github.com/library-data-platform/ldp/blob/release-1.1/doc/Admin_Guide.md#software)はLDPのドキュメントに記載されています。

## LDPのインストールと設定　

LDPの詳細な設定方法については、LDPリポジトリにある下記のリンク先のガイドをご覧ください。また、LDPの最新バージョンや修正プログラムも公開されています。

### 管理ガイド
* [概要](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#1-overview): 簡単な紹介と概要
* [システム要件](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#2-system-requirements): ソフトウェアとハードウェアの要件
* [インストール](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#3-installation): 前提条件のインストールとLDPのビルド
* [データベースの構成](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#4-database-configuration): データベースの設定と構成
* [サーバーの構成](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#5-server-configuration): サーバーの設定、構成、起動、アップデート
* [直接抽出](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#6-direct-extraction): FOLIOデータベースからの直接抽出の設定
* [データプライバシー](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#7-data-privacy): 個人データを匿名化するためのオプション
* [参照](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#reference): 設定ファイルの参照先: ldpconf.json

### 構成ガイド
* [フルアップデートのスケジュール](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Config_Guide.md#1-scheduling-full-updates): フルアップデートの設定  
* [外部キー](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Config_Guide.md#2-foreign-keys): 外部キーの推論を可能にする機能
* [参照](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Config_Guide.md#reference): 設定ファイルの参照先：dbconfig.general

## 導出表の設定

コミュニティが開発した[レポートクエリ](./FolioAnalytics.md#using-queries-from-the-folio-analytics-repository)や[アドホッククエリ](./FolioAnalytics.md#ad-hoc-querying-using-ldp-tables) をレポート利用者に十分に利用してもらうために、[派生テーブル](https://github.com/folio-org/folio-analytics/tree/release-1.0/sql/derived_tables)の夜間更新設定が強く推奨されます。なお、LDPデータベースでは*views*や*materialized view*の使用はサポートされておらず、LDPソフトウェアがデータ更新を行えなくなる可能性があります。

[FOLIO Reporting Derived Tables (Guide)](https://github.com/folio-org/folio-analytics/blob/release-1.0/sql/derived_tables/README.md)の設定方法は、Githubに記載されています。


## データプライバシー

LDPは、GDPRをはじめとするデータプライバシー要件に対応しています。管理者は、あらかじめ定義された一連のテーブルを除外することができます。

それぞれの機能の有効化および設定方法については、[匿名化ガイド](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#7-data-privacy) を参照してください。

以下のリンク先のページでは、潜在的な個人情報を含む属性をリストアップしています。

* [ユーザーモジュール](https://wiki.folio.org/display/RPT/Potential+personal+data%3A+List+of+FOLIO+attributes?src=contextnavpagetreemode): 匿名化を有効にするとLDPに読み込まれなくなるテーブル
* [組織モジュール](https://wiki.folio.org/display/RPT/Potential+personal+data+in+mod-organizations-storage?src=contextnavpagetreemode): 組織における潜在的な個人情報モジュール

## ローカルデータの追加

[ユーザーガイド](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/User_Guide.md#4-local-tables)に記載されているように、ローカルデータをLDPにロードして作成することも可能です。ローカルスキーマを使用する以外に、ユーザーグループや目的別に別々のスキーマを設定することも検討できます。

### スキーマの利用
スキーマという概念により、一つのデータベースの中でテーブルや権限を整理することができます。LDPでは、当初4つの関連スキーマを用意しています。

* public: バインドされた FOLIO テナントから抽出されたすべてのテーブルとその現在のデータが含まれます。
* [history](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/User_Guide.md#5-historical-data): 過去に更新された、あるいは既に存在しないかもしれないデータを格納します。
* [folio_reporting](https://github.com/folio-org/folio-analytics/blob/release-1.0/sql/derived_tables/README.md): コミュニティによって作成され、サポートされているすべての [導出テーブル](https://github.com/folio-org/folio-analytics/tree/release-1.0/sql/derived_tables) が含まれています。
* [local](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/User_Guide.md#4-local-tables): レポートユーザが独自のデータを作成したりインポートしたりするための共通領域

既存のスキーマの他に、ローカルなニーズ（例えば、異なる部門にデータを提供する、機密データを分離して保護する）に合わせて、自由にスキーマを作成することができます。

スキーマの概念とスキーマの設定方法については、 [Postgresのスキーマに関するドキュメント](https://www.postgresql.org/docs/11/ddl-schemas.html#DDL-SCHEMAS-PRIV)を参照してください。

権限の詳細な設定については、Postgresに組み込まれている [Roles](https://www.postgresql.org/docs/11/user-manag.html) と [Privileges](https://www.postgresql.org/docs/11/ddl-priv.html) という概念も参照してください。

### データの移動と読み込み
LDPへのデータのロードと移動は、一般的なデータベースと同様に簡単です。

Postgresの場合、一般的なアプローチは2つあります。

* [COPY](https://www.postgresql.org/docs/11/sql-copy.html): csvファイル経由でテーブルデータを移動するSQLコマンド
* [pg_dump](https://www.postgresql.org/docs/11/app-pgdump.html) / [pg_restore](https://www.postgresql.org/docs/11/app-pgrestore.html): データのインポートとエクスポートを行うためのPostgresコマンドラインツール

## LDPにおけるFOLIOデータのカバー状況

As of [version 1.1.11](https://github.com/library-data-platform/ldp/tree/1.1.11), the LDP pulls data from the following FOLIO modules:

* mod-circulation-storage
    * /cancellation-reason-storage/cancellation-reasons
    * /fixed-due-date-schedule-storage/fixed-due-date-schedules
    * /loan-policy-storage/loan-policies
    * /loan-storage/loans
    * /loan-storage/loan-history
    * /patron-action-session-storage/patron-action-sessions
    * /patron-notice-policy-storage/patron-notice-policies
    * /request-policy-storage/request-policies
    * /request-preference-storage/request-preference
    * /request-storage/requests
    * /scheduled-notice-storage/scheduled-notices
    * /staff-slips-storage/staff-slips
* mod-configuration
    * /configurations/entries
* mod-email
    * /email
* mod-feesfines
    * /accounts
    * /comments
    * /feefines
    * /feefineactions
    * /lost-item-fees-policies
    * /manualblocks
    * /overdue-fines-policies
    * /owners
    * /payments
    * /refunds
    * /transfer-criterias
    * /transfers
    * /waives
* mod-courses
    * /coursereserves/copyrightstatuses
    * /coursereserves/courselistings
    * /coursereserves/courses
    * /coursereserves/coursetypes
    * /coursereserves/departments
    * /coursereserves/processingstatuses
    * /coursereserves/reserves
    * /coursereserves/roles
    * /coursereserves/terms
* mod-finance-storage
    * /finance-storage/budgets
    * /finance-storage/fiscal-years
    * /finance-storage/fund-types
    * /finance-storage/funds
    * /finance-storage/group-fund-fiscal-years
    * /finance-storage/groups
    * /finance-storage/ledgers
    * /finance-storage/transactions
* mod-inventory-storage
    * /alternative-title-types
    * /call-number-types
    * /classification-types
    * /contributor-name-types
    * /contributor-types
    * /electronic-access-relationships
    * /holdings-note-types
    * /holdings-storage/holdings*
    * /holdings-types
    * /identifier-types
    * /ill-policies
    * /instance-formats
    * /instance-note-types
    * /instance-relationship-types
    * /instance-statuses
    * /instance-storage/instance-relationships
    * /instance-storage/instances*
    * /instance-types
    * /item-damaged-statuses
    * /item-note-types
    * /item-storage/items*
    * /location-units/campuses
    * /location-units/institutions
    * /location-units/libraries
    * /loan-types
    * /locations
    * /material-types
    * /modes-of-issuance
    * /nature-of-content-terms
    * /service-points
    * /service-points-users
    * /statistical-code-types
    * /statistical-codes
* mod-invoice-storage
    * /invoice-storage/invoice-lines
    * /invoice-storage/invoices
    * /voucher-storage/voucher-lines
    * /voucher-storage/vouchers
* mod-orders-storage
    * /acquisitions-units-storage/memberships
    * /acquisitions-units-storage/units
    * /orders-storage/alerts
    * /orders-storage/order-invoice-relns
    * /orders-storage/order-templates
    * /orders-storage/pieces
    * /orders-storage/po-lines
    * /orders-storage/purchase-orders
    * /orders-storage/receiving-history
    * /orders-storage/reporting-codes
* mod-organizations-storage
    * /organizations-storage/addresses
    * /organizations-storage/categories
    * /organizations-storage/contacts
    * /organizations-storage/emails
    * /organizations-storage/interfaces
    * /organizations-storage/organizations
    * /organizations-storage/phone-numbers
    * /organizations-storage/urls
* mod-users
    * /addresstypes
    * /departments
    * /groups
    * /proxiesfor
    * /users

\* - The LDP supports [direct extraction](https://github.com/library-data-platform/ldp/blob/1.1.11/doc/Admin_Guide.md#6-direct-extraction) for these tables, rather than using the module APIs.
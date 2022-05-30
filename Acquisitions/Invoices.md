---
title: "Invoices"
linkTitle: "Invoices"
date: 2021-08-02
weight: 20
tags: ["parenttopic"]
---

「請求書」アプリは、図書館が注文した資料の支払いを管理するためのアプリです。また、必要に応じて既存の請求書を検索し、編集することができます。

請求書アプリで使用する用語の定義は次の通りです。


*   **会計コード。** 組織を参照して、決済システムで図書館が使用するコード。
*   **収集ユニット。** 調達レコードに追加できるレイヤーで、そのユニットに割り当てられていないユーザーがそれらのレコードを操作することを制限するものです。例えば、図書館システム内の異なる図書館を表すために、収集ユニットを作成することができます。ユニットは、設定アプリで図書館によって定義され、決定されます。詳しくは、[設定 > 収集ユニット](../Settings/Settings_acquisition_units.md)を参照してください。

*   **調整金（Adjustment）。** 発注した資料のほかに請求書に追加される料金。送料、為替レートが調整金として一般的です。
*   **バッチグループ** 請求書をまとめて処理するグループ。一般的に、同じ図書館からの請求書は一緒に処理されます。
*   **ファンド。** 元帳の中の具体的なお金の配分。
*   **請求書明細。** 各請求書内で支払われる個々の明細行。各明細行は、支払い対象の資料の説明、発生したコスト、およびベンダーの参照番号で構成されています。請求書は、主にこれらの明細行の情報がまとまったものです。
*   **組織。** あなたの図書館が関係するすべての機関（これは資料を購入する機関である場合も、そうでない場合もあります）。
*   **ベンダー。** あなたの図書館が資料を購入するすべての機関。
*   **ベンダー請求書番号。** この請求書のためにベンダーから提供された番号。
*   **支払伝票（Voucher）番号。** FOLIOから外部の金融システムにエクスポートされた支払依頼を識別するために、システムが生成する番号です。

## 権限

以下の権限により、請求書アプリとのやり取りが可能になり、アプリ内でできること、できないことが決定されます。「ユーザー」アプリでユーザーに権限を割り当てることができます。これらの権限のいずれもがユーザーに割り当てられていない場合、そのユーザーは請求書アプリや関連情報を見ることができません。

以下は、請求書アプリの全権限です。


*   **Invoice: All permissions for create, view, edit and delete invoice.** This permission allows the user to create, view, edit, and delete invoices.
*   **Invoice: Assign acquisition units to new invoice.** This permission allows the user to assign acquisition units to new invoices.
*   **Invoice: Approve invoice.** This permission allows the user to approve invoices.
*   **Invoice: Download batch file from invoice record.** This permission allows users to download the batch file from the invoice record.
*   **Invoice: Manage acquisition units.** This permission allows the user to change the assignment of acquisition units for an invoice.
*   **Invoice: Pay Invoice.** This permission allows the user to approve invoices for payment.


## 請求書の作成

請求書には、図書館がベンダーに発注した資料の支払金額のリストが含まれています。

1. 「請求書」ペインで、「新規作成」をクリックします。
2. 「ベンダー請求書の作成」ウィンドウで、「請求書情報」「調整金」「ベンダー情報」「拡張情報」「リンクとドキュメント」の各セクションに必要事項を入力します。これらのセクションで利用可能なフィールドとアクションの詳細については、以下のセクションの説明を参照してください。
3. 請求書に関する必要な情報をすべて入力したら、「保存して閉じる」をクリックします。

### 請求書情報

このセクションは、ヘッダー情報を含みます。請求書日付、ステータス、バッチグループのみがこのセクションの必須フィールドです。

*   **請求書日付（必須）。** 請求書が作成された日付。
*   **ステータス（必須）。** 請求書のステータス。新しい請求書のデフォルトのステータスは "オープン" です。"レビュー済" もドロップダウン・リストにあります。
*   **支払期限。** 請求書の支払期日。
*   **条件。** ビジネスや契約上の条件など、請求書に関連する追加的な条件。
*   **承認日。** ユーザーが請求書を承認した日。
*   **承認者。** 請求書を承認したユーザー。
*   **収集ユニット。** 請求書に割り当てられた収集ユニット。
*   **請求先名。** 「請求先名」のドロップダウンリストで、請求書の送付先を選択します。住所を選択すると、請求先住所が表示されます。住所は、「設定」アプリで設定します。詳しくは、「設定 > テナント > 住所」を参照してください。
*   **バッチグループ（必須）。** 請求書をグループ化するバッチグループを指定します。
*   **小計。** 発注されたすべての商品の代金。
*   **調整金合計。** 請求書のすべての調整金の合計額。
*   **合計金額。**  発注した商品の代金と請求書の調整金額を合算したもの。 
*   **ロックトータル。** 請求書の総支出額。
*   **ノート。** 請求書に関連するその他のコメント。


### 調整金

調整金とは、注文した商品以外に請求書に追加される費用のこと。一般的な調整金項目としては、配送料と為替レートがあります。ドロップダウン・メニューからプリセットの調整金項目を選択するか、新規に調整金項目を作成することができます。

プリセット調整金を作成するには、[設定 > 請求書 >調整金](../Settings/Settings_invoices.md#設定--請求書--調整金)を参照してください。


#### 調整金の選択

「調整金を追加」をクリックすると、プリセットされた調整金の一覧から選択することができます。これらのオプションは、図書館で以前に使用された調整金を表しています。


#### 調整金の作成

新しい調整金を作成する場合は、「調整金を追加」をクリックします。


*   **説明（必須）。** 調整金の説明。
*   **金額（必須）。** 調整金の金額。
*   **タイプ。** 通貨またはパーセントを選択します。注：この選択は、以前に入力した金額にも適用されます。
*   **比例配分（必須）** 
調整金額を比例配分する方法を選択します。「明細行単位」「金額単位」「数量単位」「比例配分しない」のいずれかを選択してください。
*   **合計金額との関係（必須）。** 一つ選択：追加（In addition to）、含む（Included with）、分離（Separate from）。
*   **会計にエクスポート** このチェックボックスを選択すると、外部の支払システムに送信される、この請求書に関する支払伝票情報に、調整金の詳細が送信されます。


### ベンダー情報
  
1. 組織から提供された 「ベンダー請求書番号」を入力します。
2. 組織を選択するには、「組織検索」をクリックします。「組織選択」ダイアログでは、検索ボックスおよび/またはフィルタを使用して、組織を見つけます。選択する組織をクリックします。 
3. ベンダーを選択すると、自動的にベンダーの会計コードが表示されます。別のコードが必要な場合は、ドロップダウン・リストから選択してください。

### 拡張情報


1. ドロップダウンメニューから、**支払い方法**：現金、クレジットカード、電子送金（EFT）、預金口座、小切手、銀行為替手形、内部送金、その他、を選択します。
2. 既存の購読をチェックしたい場合は、**購読の重複をチェックする** チェックボックスを選択します。注：現在、システムロジックは実装されていないため、重複する購読をチェックすることはありません。
3. 外部の財務システムに支払伝票を送信する場合は、**会計にエクスポート** チェックボックスをクリックします。
4. ドロップダウンリストから **通貨** を選択します。デフォルト値は、主要通貨としてテナント設定に保存されています。詳細については、**設定** > **テナント** > **言語とローカライゼーション** を参照してください。デフォルト以外の通貨を選択した場合、システムには**現在の為替レート**が表示されます。
5. **現在の為替レート**の値を上書きするために為替レートの値を入力したい場合は、**設定した為替レートを使用**のチェックボックスを選択し、**為替レート設定ボックス**にレートを入力してください。

### リンクとドキュメント

このセクションでは、電子化された物理的な請求書やベンダーからのメールなど、請求書レコードにドキュメントを添付することができます。ファイルを直接アップロードすることも、外部のファイル管理システムに保存されているファイルへのURLリンクを追加することも可能です。また、物理的な請求書の写真やベンダーからの電子メールなど、請求書に付随するドキュメントを添付することもできます。


#### リンクの追加

1. 「リンクの追加」をクリックします。
2. ファイルリンクを識別するために**リンク名**を入力します。
3. オプション：有効なWebサイトの**外部URL**を入力します。

リンクを削除したい場合は、**削除アイコン**をクリックします。

#### ドキュメントの追加

ドキュメントを追加する方法は2つあります。

* ファイルをボックスにドラッグ＆ドロップする方法、または
* 「ファイルを選択」をクリックすると、ローカルファイルからドキュメントを追加することができます。

文書を削除する場合は、**削除アイコン**をクリックします。

## 請求書の検索

請求書の検索は、「検索とフィルター」ペインで行います。請求書を検索するには、ボックスに検索キーワードを入力します。 ドロップダウンリストから「すべて」を選択すると、以下のフィールドのいずれかを通して検索できます。


*   **すべて。** ドロップダウン・リストのすべてのフィールドを検索します。これはデフォルトの検索です。
*   **支払伝票番号。** 請求書の支払伝票番号。
*   **ベンダー請求書番号。** 請求書のベンダー請求書番号。
*   **会計コード。** 請求書の会計コード。

また、「検索とフィルターペインで任意のフィルターを選択して、請求書を検索することができます。さらに、検索を行った後にフィルターを適用して、検索結果を限定することもできます。フィルタの詳細については、以下のセクションを参照してください。

### ステータス

「検索とフィルター」ペインで、**ステータス**をクリックし、適用可能なフィルタを選択します。

* **オープン。** 現在、あなたの図書館でオープンになっている請求書です。これは、新しい請求書のデフォルトのステータスです。
* **レビュー済み。** あなたの図書館がレビューした請求書です。請求書を 「レビュー済み」に設定するには、ベンダー請求書作成画面、またはベンダー請求書編集画面のドロップダウンリストで「レビュー済み」ステータスを選択します。
* **承認済み。** あなたの図書館が承認した請求書です。請求書を承認するには、「アクション」メニューを使用します。
* **支払い済み。** あなたの図書館が支払いをした請求書です。請求書を支払うには、「アクション」メニューを使用します。
* **キャンセル。** あなたの図書館がキャンセルした請求書です。注：請求書のキャンセル機能は、将来のリリースで利用可能になる予定です。


### ベンダー名

特定のベンダーの請求書を検索するには、次の手順に従います。

1.「検索とフィルター」 ペインで、「ベンダー名」をクリックします。
2. 「組織の検索」をクリックします。
3. 「組織の選択」ダイアログで、ベンダを検索します。
4. ベンダーをクリックして、**ベンダー名**フィールドを入力します。検索結果は、請求書ペインに表示されます。 

組織の検索については、[組織 > 組織の検索](./Organizations.md#searching-for-an-organization)を参照してください。


### 作成日

請求書の作成日で検索する場合は、以下の手順で行います。

1. 「検索とフィルター」ペインで、「作成日」をクリックします。
2. **From** ボックスに開始日を、**To** ボックスに終了日を入力します。
3. 「適用」をクリックします。検索結果が請求書ペインに表示されます。

### 請求書日付
 
請求書の日付をもとに請求書を検索するには、以下の手順で行います。

1. 「検索とフィルター」ペインで、「請求書日付」をクリックします。
2. **From** ボックスに開始日を、**To** ボックスに終了日を入力します。
3. 「適用」をクリックします。検索結果が請求書ペインに表示されます。 

### 収集ユニット

特定の収集ユニットに割り当てられた請求書を検索するには、次の手順に従います。

1. 「検索とフィルター」ペインで、「収集ユニット」 をクリックします。
2. ドロップダウンリストから、必要な収集ユニットを選択します。検索結果は、請求書ペインに表示されます。

### タグ

特定のタグが付与された請求書を検索するには、以下の手順で行います。

1. 「検索とフィルター」「タグ」をクリックします。
2. ドロップダウンリストからタグを選択します。検索結果は、請求書ペインに表示されます。

### 支払期日

請求書を支払期日で検索するには、以下の手順で行います。

1. 「検索とフィルター」ペインで、「支払期日」をクリックします。
2. 「From」ボックスに開始日を、「To」ボックスに終了日を入力します。
3. 「適用」をクリックします。検索結果は、請求書ペインに表示されます。 

### 支払い方法

「検索とフィルター」ペインで、**支払い方法**をクリックし、該当するフィルターを選択します。

*   **現金。** 現金で支払われる請求書。
*   **クレジットカード。** クレジットカードで決済される請求書。
*   **電子送金（EFT）。** 電子送金で支払われる請求書。
*   **預金口座。** 口座振替で支払われる請求書。
*   **物理的な小切手。** 物理的な小切手で支払われる請求書。
*   **銀行為替手形。** 銀行手形で支払われる請求書。
*   **内部送金。**  組織内の振替で支払われる請求書。
*   **その他。** 上記と異なる方法で支払われた請求書。


### 承認日 

請求書を承認日で検索する場合は、以下の手順で行います。

1. 「From」 ボックスに開始日、「To」 ボックスに終了日を入力します。
2. 「適用」をクリックします。検索結果は、「請求書」ペインに表示されます。

### ソース

請求書をソースでフィルタリングするには、以下のうち1つ以上を選択します：

* **ユーザー。** FOLIO ユーザーが作成した請求書。 
* **API。** Application Programming Interface を介して作成された請求書。
* **EDI。** 電子データ交換により作成された請求書。
* **MARC。** MAchine-Readable Cataloging フォーマットのレコードインポートによってインポートされた請求書。

### 会計にエクスポート

「会計にエクスポート」のチェックボックスに基づいて請求書をフィルタリングするには、以下を選択します。

*   **はい。**  「会計にエクスポート」チェックボックスが選択されている請求書。
*   **いいえ。** 「会計にエクスポート」チェックボックスが選択されていない請求書。

## 請求書詳細の表示

請求書を検索すると、「請求書」ペインに以下の情報が表示されます。

*   **ベンダー請求書番号。** この請求書のためにベンダーから提供された番号。
*   **ベンダー。** ベンダーの名称。
*   **請求書日付。** 請求書の作成日。
*   **ステータス。** この請求書のステータス。
*   ** 合計金額(システム).** 請求書の発注された品目および調整金の合計金額。

検索結果で、請求書をクリックすると表示されます。 「ベンダー請求書番号」ペインに、請求書に関する追加情報が表示されます。

### 請求書情報


請求書情報セクションの項目については、[請求書の作成 > 請求書情報](#請求書情報)をご覧ください。また、このセクションには、以下の情報も含まれています。

*   **ソース。** この請求書が作成された方法。ユーザー、API、EDI、または MARC。
*   **請求先住所。** 請求先名と関連付けられた住所です。請求先名については、[請求書の作成 > 請求書情報](#請求書情報)を参照してください。
*   **総ユニット数。** 請求書に記載されたオーダーの全項目。

### 請求明細

請求明細を使用すると、請求書を未発注の発注明細にリンクさせたり、既存の発注と関連のない請求明細を作成したりすることができます。各明細行は、タイトル、支払い情報、コスト詳細、調整金で構成されています。

このセクションは、発注のすべての請求明細を一覧表示します。リストには、以下が表示されます。

*   **発注明細番号。** 発注明細番号。
*   **説明。** 発注明細の発注されたタイトル。
*   **ファンドコード。** 請求書明細の支払原資となるファンドコード。
*   **数量。** 発注された数量。
*   **小計。** 調整金を追加する前の請求書のコスト。
*   **調整金。** 請求書に関連する調整金の額。
*   **合計金額。** 発生したすべてのコスト。
*   **ベンダー参照番号。** ベンダーに固有の、取得する資料の一意の識別子。ベンダーごとに、資料の種類によって異なるタイプの識別子が提供されています。

#### 請求明細行を請求書に追加

1. 「追加」をクリック。
2. 「発注明細の選択」 ウィンドウの 「検索とフィルター」 ボックスで、キーワードを入力して発注明細を検索します。
3. オプション：結果をフィルターします。
4. 「検索」をクリックします。検索結果は、「検索結果」ペインに表示されます。
5. 1つまたは複数の発注明細を選択するには、発注明細番号の左側にあるチェックボックスを選択し、「保存」をクリックします。発注明細は、請求書明細表に表示されます。

注：請求書の組織と一致しないベンダーを含む発注を選択した場合、確認ダイアログが表示されます。「確認」をクリックすると、選択した発注明細で継続できます。「キャンセル」をクリックすると、別の発注明細を選択することができます。


#### 請求書明細の新規作成


既存の発注明細と関連付けられていない請求書明細を作成するには、以下の手順に従います。

1. 「新規作成」をクリック
2. 「請求書明細の作成」ウィンドウで、「請求書情報」「ファンド配分」「調整」セクションを入力します。これらのセクションで利用可能なフィールドとアクションの詳細については、以下のセクションの説明を参照してください。
3. 「保存して閉じる」をクリックします。確認メッセージが表示され、請求書明細表に請求書明細が表示されます。

##### 請求書明細情報

*   **説明。** 請求書明細の説明またはタイトル。請求対象の資料、サービス、料金などが含まれる。
*   **発注明細番号。** 請求書明細の発注明細番号。
*   **請求書明細番号。** 請求書明細の請求書明細番号。
*   **ベンダー参照番号。** 
請求書明細のベンダー参照番号。ベンダー参照番号の詳細については、[発注 > 発注に注文明細を追加する > ベンダー参照番号](./Orders.md#vendor-1}) を参照してください。
*   **ステータス。** 請求書明細のステータス。
*   **サブスクリプション情報。**この請求書明細のサブスクリプション情報。
*   **サブスクリプション開始日。** サブスクリプションが開始する日付。
*   **サブスクリプション終了日。** サブスクリプションが終了する日付。
*   **コメント。** 請求書明細に関するその他のコメント。
*   **アカウント番号。** 請求書明細のアカウント番号です。このドロップダウンリストには、請求書上で選択されたベンダーのアカウント番号が含まれています。もし、そのベンダーの「組織」レコードに一つ以上のベンダーアカウントが存在する場合、最初のアカウントがこのフィールドにデフォルト値として表示されます。
*   **会計コード。** 請求書明細の会計コード。
*   **数量。** 請求書明細の項目数。
*   **小計。** 請求書明細の全項目の費用です。注：小計は、「設定 > テナント > 言語とローカライズ」で定義された通貨でのファンド分配に使用されます。
*   **支払準備金を解放。** 請求書のコストが割り当てられたファンドに対して、請求書のコストを解放します。

### ファンド分配

*   **調整金。** 請求書のファンドに適用される調整金。
*   **ファンド。** 金額を分配するファンド。 
*   **経費クラス。** 金額を分配するファンド内の経費クラス。
*   **値。** ファンドに割り当てられた金額。
*   **金額。** ファンドに課金される金額。
*   **初期支払準備金。** ファンドにコミットされた最初の金額。
*   **現在の支払準備金。** 資金に充当された現在の金額。

### 調整金

*   **説明。** 調整金の説明。
*   **金額。** 調整金の金額。
*   **比例配分** 調整金が複数の請求書明細に分散しているかどうかを判断します。
*   **合計金額との関係。** 調整金が請求書の総額に含まれるか、追加されるか、または別であるかを指定します。

### ベンダー詳細

*   **ベンダー請求書番号。** 請求書のベンダー請求書番号。
*   **ベンダー名。**  ベンダーの名称。
*   **会計コード。** 請求書の会計コード。


### リンクとドキュメント

このエリアには、請求書に添付されたすべてのリンクとドキュメントが含まれています。**外部URL**または**ドキュメント名**をクリックすると、ドキュメントが表示されます。

## 請求書の編集

1. 編集したい請求書を探し、選択します。
2. **アクション** > **編集** をクリックします。
3. 請求書を編集します。すべての項目が編集可能なわけではありません。 「ステータス」フィールドは編集可能なので、ドロップダウンリストで「レビュー済み」を選択することにより、請求書を「レビュー済み」に設定することができます（オプション）。
4. 「保存して閉じる」 をクリックすると、確認メッセージが表示され、請求書が更新されます。

### 請求明細

過去の発注で使用された請求明細行は、図書館のシステムに記録として残ります。いつでも、これらの明細行にアクセスし、再利用することができます。また、必要な情報を入力することで、新しい明細を作成することができます。

発注が参照する通貨やベンダーが請求書と異なる場合、操作の前に確認が求められます。注：支払いは、請求書に記載されている情報に基づいて割り当てられます。

請求書明細について、詳細は [請求書 > 請求書詳細の表示](#請求書詳細の表示)を参照してください。


##### ファンド分配

ファンド分配について、詳細は [請求書の表示 > ファンド分配](#ファンド分配)を参照してください。

##### 調整金


###### 調整金の選択

調整金の選択について、詳細は [請求書の作成 > 調整金の選択](#調整金の選択)を参照してください。


###### 調整金の作成

調整金の作成について、詳細は [請求書の作成 > 調整金の作成](#調整金の作成)を参照してください。


## 請求書の削除

請求書の削除は、「オープン」「レビュー済み」「キャンセル」の状態であれば可能です。 「承認済み」または「支払済み」に遷移すると、請求書を削除することはできません。

1. 削除したい請求書を探し、選択します。
2.  「ベンダー請求書番号」 ペインで、**アクション** > **削除** をクリックします。
3. 「請求書を削除」ダイアログで、**削除**をクリックします。確認メッセージが表示され、請求書が削除されます。


## 請求書の承認

支払金額が「支払待ち」とみなされ、支払伝票が作成されるためには、請求書の承認が必要です。承認できるのは、請求書明細のある請求書のみです。このアクションを実行できるのは、「請求書を承認する」権限を持つ人だけです。

注：ある発注明細に接続された1つ以上の請求書が「承認」されると、その発注明細の支払ステータスは「一部支払済み」に変更されます。

ロックされた合計を入力する場合、ユーザーが請求書を承認する前に、すべての請求書明細と調整金の金額が、ロックされた合計金額と等しくなければなりません。請求書を承認すると、支払伝票、及び、「支払い待ち」のトランザクションが作成されます。「支払伝票」は、請求書の支払いに必要な情報を提供する仕組みで、外部の支払いシステムにエクスポートすることができます。各請求書は、すべてのファンドチャージがファンド外部アカウント番号でグループ化された、一意の支払伝票を生成します。

 支払伝票のエクスポートの詳細は
 [設定 > 請求書 > バッチグループ設定](../Settings/Settings_invoices.md#設定--請求書--バッチグループ設定)を参照してください。

請求書の承認は、以下の手順で行います：

1. 承認したい請求書を探し、選択します。
2. 「ベンダー請求書番号」 ペインで、**アクション** > **承認** をクリックします。
3. 「請求書の承認」 ダイアログで、**承認** をクリックします。確認メッセージが表示され、請求書が承認されます。

## 支払伝票（Voucher）の表示


請求書が承認されると、請求書の支払伝票が作成され、請求書レコードに追加されます。 請求書の支払伝票を見るには、以下の手順で行います。

1. 「検索とフィルター」 ペインを使用して、表示したい請求書を探し、選択します。
2. 「ベンダー請求書番号」ペインで、「支払伝票情報」セクションまでスクロールダウンしてください。 このセクションには、請求書支払伝票に関する主要な情報が表示されます。
3. 支払伝票のすべての情報をフルスクリーンで表示するには、「支払伝票を表示」 をクリックします。 

 ### 支払伝票情報

*   **ステータス。** 請求書の支払い伝票の状態：「支払待ち」または「支払済み」。
*   **支払伝票番号。**  システムによって割り当てられた、この支払伝票の番号。
*   **支払伝票日付。** 請求書が承認され、支払伝票が作成された日付。
*   **合計金額。** 支払伝票明細の合計金額。
*   **為替レート。** トランザクションを生成するために使用される為替レート。
*   **支払番号。**   支払いに対応する、外部システムの識別子。
*   **アカウント番号。** 請求書に記載されている支払い方法に対するベンダー組織のアカウント番号。 この値は、ベンダーの組織レコードのアカウントセクションに、この請求書に使用されている支払方法のためのアカウント番号が含まれている場合にのみ設定されます。
*   **アカウントコード。**  外部の買掛金システムにおいて、ベンダー組織を識別するためのベンダー会計コード。
*   **要封入。**  支払方法が「小切手」の場合、外部の会計システムに対して、この請求書に封入が必要であることを示します。「会計にエクスポート」チェックボックスがtrueに設定され、この請求書に対して支払伝票が作成されると、支払伝票エクスポートファイルのEnclosure neededデータエレメントにtrueという値が含まれます。

*   **ベンダー。** ベンダーの名称。
*   **住所 1。** ベンダーの住所 1。
*   **住所 2。** ベンダーの住所 2。
*   **市。** ベンダーの市。
*   **州/県/地域。** ベンダーの州、県、地域。
*   **郵便番号。** ベンダーの郵便番号。
*   **国。** ベンダーの国。


### 支払伝票明細

支払伝票明細は、ファンド外部アカウント番号でグループ化されます。 例えば、ある請求書に、同じファンド外部アカウント番号を含む、複数の請求書明細がある場合、それらの請求書明細の合計金額を含む支払伝票明細がひとつだけ生成されます。

*   **外部アカウント番号。**  ファンドの外部アカウント番号。
*   **合計。** 支払伝票明細表の下部に表示される、すべての支払伝票明細の合計金額です。

支払伝票明細表には、各伝票明細の、次の情報が含まれています：

*   **明細番号。**
*   **グループ。**
*   **ファンドコード。**
*   **外部アカウント番号。**
*   **金額。**



## 請求書の支払い

請求書のステータスを「支払い済み」に更新するには、「支払いアクション」を使用します。「支払いアクション」は、「設定 > 請求書 > 承認 > 1クリックで承認と支払い」の設定がオフの場合、「アクションメニュー」で利用可能です。 これにより、図書館は、請求書の承認と請求書の支払いに別々のアクションを使用することができます。 この設定がオフの場合、「支払いアクション」を利用する前に、請求書を承認する必要があります。 請求書の「支払い済み」ステータスへの移行は、発注が完全に受入されている場合には、発注ステータスが「クローズ」に更新されるトリガーとなります。


ワンクリックで承認と支払いを行う設定については、[設定 > 請求書 > 承認](../Settings/Settings_invoices.md#設定--請求書--承認)をご参照ください。


請求書を支払うには、以下の手順で行います。

1. 「検索とフィルター」ペインを使用して、支払いたい請求書を検索し、選択します。
2. 「アクション」 メニューで、「支払」を選択します。


## 支払伝票の詳細を表示し、エクスポートファイルをダウンロードする

外部の買掛金管理システムにエクスポートする支払伝票を含むバッチファイルを生成する処理は、[請求書 > 設定 > バッチグループ設定](../Settings/Settings_invoices.md#設定--請求書--バッチグループ設定)で管理します。 「会計にエクスポート」チェックボックスがONになっている請求書の支払伝票で、請求書のステータスが「承認」になっており、以前のジョブ実行で抽出されていないもののみがエクスポートの対象となります。 エクスポートジョブの完了後、エクスポートに関する詳細を確認したり、エクスポートジョブに含まれる請求書を検索して、支払伝票全体のエクスポートファイルのコピーを閲覧したりすることができます。 支払伝票エクスポートの詳細を表示し、ファイル全体のコピーをローカルのダウンロードフォルダにダウンロードするには、以下の手順に従います。


1. 「検索とフィルター」 ペインを使用して、表示したい請求書を探し、選択します。
2. 「ベンダー請求書番号」ペインで「支払伝票エクスポート詳細」セクションまでスクロールダウンします。 
3. 支払伝票エクスポートファイル全体をダウンロードするには、バッチファイル名の横にある下向き矢印のダウンロードアイコンをクリックします。 このファイルには、ジョブ実行時にまだエクスポートされていない「支払済み」ステータスの支払伝票がすべて含まれます。

### バウチャーエクスポート詳細



*   **バッチグループ。**
*   **バッチファイル名。**
*   **バッチファイルステータス。**



### 支払伝票エクスポートファイル



バウチャーエクスポートファイルには、以下のデータ要素が含まれます。

*   accountingCode
*   amount
*   batchedVoucherLines/0/amount
*   batchedVoucherLines/0/fundCodes/0
*   batchedVoucherLines/0/externalAccountNumber
*   enclosureNeeded
*   exchangeRate
*   folioInvoiceNo
*   invoiceCurrency
*   status
*   systemCurrency
*   type
*   vendorInvoiceNo
*   vendorName
*   voucherDate
*   voucherNumber
*   vendorAddress/addressLine1
*   vendorAddress/addressLine2
*   vendorAddress/city
*   vendorAddress/stateRegion
*   vendorAddress/zipCode
*   vendorAddress/country


## 支払伝票を編集し出金情報を追加する

外部の買掛金システムから請求書の支払伝票の出金情報を追加するには、「アクション」メニューを使用して請求書の支払伝票を編集します。

1. 「検索とフィルター」ペインを使用して、支出情報を更新したい請求書を検索し、選択します。
2. 「支払伝票情報」セクションで、「支払伝票を表示」ボタンをクリックします。
3. 「支払伝票を全画面表示」 ウィンドウから、「アクション」 メニューを開き、「編集」 を選択します。
4. 以下のフィールドに支出情報を入力します。
5. 「保存して閉じる」をクリックします。 

支払伝票上で編集可能な項目は以下の通りです：


*   **支払番号。** 小切手番号など、支払いに対応する外部システムからの識別子を入力します。
*   **支払日。**  外部システムの支払トランザクションの日付を入力します
*   **支払金額。**  支出金額を入力します。小数点を含められます。
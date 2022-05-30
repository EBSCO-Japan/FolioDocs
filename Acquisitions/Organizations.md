---
title: "Organizations"
linkTitle: "Organizations"
date: 2021-05-10
weight: 40
tags: ["parenttopic"]
---

「組織」アプリは、図書館が関わる組織を管理するためのアプリです。組織のレコードは、連絡先、ウェブサイト、インターフェース、アカウントなど、組織に関する情報を保存する場所です。作成した組織は、次のアプリでFOLIOの収集・電子リソース管理領域と共有されます：「発注」「請求書」「受入」「契約」「ライセンス」「eUsage」です。

組織アプリに関する用語の定義：


*   **収集ユニット。** 調達レコードに追加できるレイヤーで、そのユニットに割り当てられていないユーザーがそれらのレコードを操作することを制限するものです。例えば、図書館システム内の異なる図書館を表すために、収集ユニットを作成することができます。ユニットは、設定アプリで図書館によって定義され、決定されます。詳しくは、[設定 > 収集ユニット](../Settings/Settings_acquisition_units.md)を参照してください。

*   **組織。** あなたの図書館が関わるすべての機関（これはあなたが資料を購入する機関である場合もあれば、そうでない場合もあります）。
*   **ベンダー。** あなたの図書館が資料を購入するすべての機関。


## パーミッション

以下に示す権限によって、組織 アプリと対話し、アプリ内でできること、できないことを決定することができます。「ユーザー」アプリでユーザーに権限を割り当てることができます。これらの権限のいずれもがユーザーに割り当てられていない場合、ユーザーは組織アプリや関連情報を表示できません。

以下は、組織アプリの全権限です。


*   **Organizations: Assign acquisitions units to new organization.** This permission allows the user to assign acquisition units to the organization when creating a new record
*   **Organizations: Interface usernames and passwords: view.** This permission allows the user to view the usernames and passwords that appear in the Interface section.
*   **Organizations: Interface usernames and passwords: view, edit, create, delete.** This permission allows the user to create, edit, and delete the usernames and passwords that appear in the Interface section. Note: This permission must always have the Organizations: View, edit, create or Organizations: View, edit, delete permissions assigned along with it.
*   **Organizations: Manage acquisition units.** This permission allows the user to change the assignment of acquisition units for the organization when editing a record.
*   **Organizations: View.** This permission allows the user to search and view organization records and settings. The user can also access Contacts and Interfaces but cannot access Interface usernames and passwords.
*   **Organizations: View, edit.** This permission allows the user to edit and view organizations. The user can also access Contacts and view organization settings, but they cannot access Interface usernames and passwords.
*   **Organizations: View, edit, create.** This permission allows the user to create, edit, and view organizations. The user can also access Contacts and view organization settings, but they cannot access Interface usernames and passwords.
*   **Organizations: View, edit, delete.** This permission allows the user to view, edit, and delete organizations. The user can also access Contacts and view organization settings, but they cannot access Interface usernames and passwords.


## 組織の作成

一般的な組織、もしくは特定のベンダーとして組織を作成します。ベンダーとして組織を作成する場合は、ベンダーに関連する情報を追加できます。ベンダーの作成について詳しくは、[ベンダーの作成](#creating-a-vendor)を参照してください。

1. **組織** ペインで **新規**をクリック。

2. **組織の作成** ウィンドウで、「サマリー」、「連絡先」、「担当者」、「インターフェース」の各セクションを入力します。 これらのセクションで利用可能なフィールドとアクションの詳細については、以下のセクションの説明を参照してください。

3. 組織について必要な情報をすべて入力したら、**保存して閉じる**をクリックします。組織が保存され、「組織」ペインに追加されます。


### サマリー



*   **名称（必須）。** 組織の名前。
*   **コード（必須）。** 組織の一意な識別子。注：ベンダーコードは重複できません。各組織のコードは、異なるものでなければなりません。
*   **会計コード。** 組織を参照し、図書館が支払いシステムで使用する会計コード。
*   **組織ステータス（必須）。** 組織のステータスを選択します。「アクティブ」、「非アクティブ」、「保留」のいずれかを選択します。ここで選択したステータスは、「発注」アプリと「請求書」アプリで評価されます。組織がアクティブなステータスを持つベンダーである場合にのみ、発注はオープンにすることができ、請求書は支払うことができます。組織のレコードが下書きであることを示すために、「保留」のステータスを使用することができます。
*   **デフォルト言語。** 組織のデフォルト言語を選択します。
*   **ベンダー。** ベンダー組織を作成している場合は**ベンダー** チェックボックスをチェックします。詳細は [ベンダーを作成](#creating-a-vendor) に記載があります。
*   **調達ユニット。** 組織レコードに適用する調達ユニットを選択します（使用する場合）。詳細は[Settings > Acquisition units]("/settings_acquisition_units.md") に記載があります。
*   **説明。** 組織についての説明。
*   **別名。** 組織が使用する代替名（略称や旧名など）。


#### 別名の追加

注：別名の追加は任意です、しかし、 **別名の追加** をクリックすると、 **別名** を追加、または [別名を削除](#別名を削除) しないと組織レコードが保存できなくなります。
1. **別名の追加** をクリック。

2. テキストボックスに **別名** を入力。

3. オプション：別名に関する **説明** をテキストボックスに入力。

4. 必要に応じて繰り返してください。組織を保存すると、別名が保存されます。


#### 別名の削除

1. 削除したい別名を探します。

2. **ゴミ箱アイコン**をクリックします。組織を保存すると、別名が削除され、レコードから削除されます。


### 連絡先情報
「連絡先情報」セクションには、組織の個々の人に固有のものではない、組織の連絡先情報を格納します。後述の[担当者連絡先](#contact-people)セクションで、特定の個人の連絡先を追加することができます。

連絡先情報のカテゴリは、設定アプリで設定します。このセクションで入力した連絡先情報の種類にカテゴリーを割り当てると、組織を表示するときに、連絡先情報がそのカテゴリーでソートされます。



*   **住所。** 組織に関連する住所です。複数のアドレスを追加できます。
*   **電話番号。** 組織に関連する電話番号です。複数の電話番号を追加できます。
*   **メールアドレス。** 組織に関連する電子メールアドレスです。複数のメールアドレスを追加できます。
*   **URL。** 組織に関連するURLです。複数のWebサイトやFTP接続を追加できます。


#### 住所の追加

1. **住所の追加** をクリック。

2. 住所の情報を入力。

3. 必要に応じて繰り返してください。組織を保存すると、住所が保存されます。注：複数のアドレスを追加する場合は、組織のプライマリー住所の上部にある **プライマリー住所として使用する** チェックボックスを選択します。


#### 住所の削除

1. Find the address you want to delete.

2. **ゴミ箱アイコン**をクリック。 The address は削除され、保存をするとレコードから消えます。


#### 電話番号の追加

1. Click **Add phone number**.

2. Enter the Phone number in the box.

3. Optional: Select the **Type** of number it is from the drop-down list: Office, Mobile, Fax, or Other.

4. Optional: Select the **Language** spoken at that number from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed. The phone number saves once you save the organization. Note: If you are adding multiple numbers, select the **Use as primary phone** checkbox at the top of the organization’s primary number.


#### 電話番号の削除

1. Find the phone number you want to delete.

2. **ゴミ箱アイコン**をクリック。 The phone number is removed and is deleted once you save the organization.


#### Eメールアドレスの追加

1. Click **Add email**.

2. Enter the **Email address** in the box.

3. Optional: Enter a **Description** of the email in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed.The email address saves once you save the organization. Note: If you are adding multiple email addresses, select the **Use as primary email** checkbox at the top of the organization’s primary email address.


#### Eメールアドレスの削除

1. Find the email address you want to delete.

2. **ゴミ箱アイコン**をクリック。 The email address is removed and is deleted once you save the organization.


#### URLの追加

The URL can be a website or FTP link.

1. Click **Add URL**.

2. Enter the **URL** in the box.

3. Optional: Enter a **Description** of the URL in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the URL.

6. Repeat steps 1-5 as needed. The URL saves once you save the organization. Note: If you are adding multiple URLs, select the **Use as primary URL** checkbox at the top of the organization’s primary URL.


#### Deleting a URL

1. Find the URL you want to delete.

2. **ゴミ箱アイコン**をクリック。 The URL is removed and is deleted once you save the organization.


### 担当者連絡先


#### 連絡先の新規作成

連絡先を新規作成する場合は [担当者連絡先の作成](#creating-a-contact-person)を参照してください。


#### Adding an existing contact 

1. Click **Add contact**.

2. In the **Add contacts** dialog, search for the contact you want to add.

3. In the **Search results**, select the **checkbox** next to the contact(s) you want to add. You can add multiple contacts at a time.

4. Click **Save**. The contact(s) appear under the Contact people section. 


#### 連絡先の削除

1. 削除したい連絡先を探す。

2. **x**をクリックします。連絡先は削除され、組織を保存するとレコードから削除されます。


### インターフェイス

インターフェイスとは、ウェブサイト、ソフトウェア、ポータルサイトなどで、組織からの発注を管理したり、統計情報を収集したりするために使用するものです。


#### インタフェースの新規作成

詳しくは、「インターフェイスの作成」を参照してください。


#### 既存のインターフェイスの追加

1. Click **Add interface**.

2. In the **Add interfaces** dialog, search for the interface you want to add.

3. In the **Search results**, select the checkbox next to the interface(s) you want to add. You can add multiple interfaces at a time.

4. Click **Save**. The interface(s) appear under the Interface section.


#### 組織レコードのインターフェイスの削除

1. 削除したインターフェイスを見つけます。

2. **x**をクリック。 インターフェイスは削除され、保存をするとレコードから消えます。


## ベンダーの作成

1. In the **Organizations** pane, click **New**.

2. In the **Create organization** window, in the **Summary** section, select the **Vendor** checkbox. Vendor sections appear.

3. 続けてサマリーセクションに記入します。連絡先情報、担当者連絡先、インターフェース、ベンダー情報、ベンダー条件、EDI情報、およびアカウントの各セクションを入力します。これらのセクションで使用できるフィールドとアクションの詳細については、以下のセクションの説明を参照してください。

3. Once you have included all of the information you want about the vendor, click **Save & close**. The vendor is saved and added to the Organizations pane.


### サマリー

詳しくは、[サマリー](#サマリー)を参照してください。


### 連絡先情報

For more information, see [Contact information](#contact-information).


### 担当者連絡先

For more information, see [Contact people](#contact-people).


### Interface

For more information, see [Interface](#interface).


### ベンダー情報

発注や請求書にベンダーを適用する際に表示されるデフォルトのいくつかは、「ベンダー情報」に入力した情報から設定されます。



*   **支払方法。**  請求書のベンダーに対するデフォルトの支払い方法として表示させたい支払い方法。詳しくは [請求書 > Extended information]("/invoices.md#extended-information") を参照。
*   **ベンダー通貨。** ベンダーが受け入れる通貨。
*   **アクティベーション間隔（予定）。** ベンダーの標準的なアクティベーション間隔を日数で指定します。注：ここで入力した間隔は、そのベンダーに関連する発注の「電子リソースの詳細」セクションにある「アクティベーション期限日」フィールドで使用されます。例えば、間隔を365に設定した場合、「アクティベーション期限日」フィールドには、発注明細を作成した日から1年後の日付が入力されます。
*   **請求書発行間隔（予定）。** ベンダーの標準的な請求書発行間隔を日数で指定します。現在、この情報は請求書に表示されません。
*   **クレーム期間。** ベンダーの標準クレーム期間（日数）。
*   **受領間隔（予定）** 発注した商品がベンダーから届くまでの標準的な期間を日数で表したもの。
*   **割引率。** ベンダーと交渉した割引額をパーセント値で表示します。ベンダーとの注文のための発注を作成するとき、この値がデフォルトとして割引フィールドに表示されます。
*   **更新アクティベーション間隔。** このベンダーの標準的な更新アクティベーション間隔を日数で示したもの。
*   **サブスクリプション期間。** ベンダーの標準的なサブスクリプション期間（日数）。
*   **会計にエクスポート。** このベンダーの請求書が、外部の会計システムへのエクスポート用の支払伝票レコードを作成することを示すために、**会計にエクスポート** チェックボックスを選択します。組織レコードのこの値は、ベンダーの請求書を作成する際に、請求書の「会計にエクスポート」フィールドのデフォルト値を設定します。


### 税

「税」に入力した情報は、発注にベンダーを適用する際に表示されるデフォルト値を設定します。


*   **Tax ID。** ベンダーの連邦納税者番号（Federal Tax Identification Number）。これはEmployer Identification Number (EIN)とも呼ばれ、事業体を識別するために使用されます。
*   **税率。** ベンダーの標準税率。付加価値税(VAT)の支払い義務があるベンダーの場合、参考のためにここにパーセンテージ値を保存することができます。
*   **VAT支払義務。** ベンダーが付加価値税（VAT）の納税義務者であることを示すには、**VAT支払義務** チェックボックスを選択します。


### ベンダー条件

ベンダー条件とは、ベンダーとの契約の概要である。契約内容は、アクイジション/フルフィルメント関連またはe-リソース関連の場合があります。ここに入力された値は、発注や請求書の記録には表示されません

注：ベンダー条件の追加は任意ですが、**追加**をクリックした場合、**名前**を追加するか、ベンダー用語を削除しないと組織のレコードは保存されません。


#### ベンダー条件の追加

1. Click **Add**.

2. Enter the **Name** of the term in the box.

3. Optional: Enter or select the **Discount %** in the box.

4. Optional: Enter a **Reference URL** in the box.

5. Optional: Enter any **Notes** about the agreement in the box.

6. Repeat steps 1-5 as needed. Terms are saved once you save the vendor.


#### ベンダー条件の削除

1. Find the vendor term you want to delete.

2. Select the **trash can icon**. The term is removed and is deleted once you save the vendor.


### EDI 情報

EDI（electronic data interchange）情報とは、発注を送信/受信する際や、請求書を受信する際に使用する情報です。注：FOLIOとEDIの機能は現在開発中であり、このセクションに入力される情報は参考程度にお考えください。


#### EDI 基本情報



*   **Vendor EDI code.** The vendor identifier for EDI transactions
*   **Vendor EDI type.** Select one of the Vendor EDI types, which designates the type of identifier used as the vendor identifier: 014/EAN, 31B/US-SAN, 091/Vendor-assigned, or 092/Customer-assigned.
*   **Library EDI code.** The library identifier for EDI transactions
*   **Library EDI type.** Select one of the Library EDI types, which designates the type of identifier used as the library identifier: 014/EAN, 31B/US-SAN, 091/Vendor-assigned, or 092/Customer-assigned.
*   **Prorate tax.** If the tax is prorated on orders or invoices, select the **Prorate tax** checkbox. This indicates that the library expects to prorate summary tax on invoices from the vendor across all invoice lines as a percentage by value.
*   **Prorate fees.** If fees are prorated on orders or invoices, select the **Prorate fees** checkbox. This indicates that the library expects to prorate fees on invoices from the vendor across all invoice lines as a percentage by value.
*   **EDI naming convention.** The naming convention that sets the expected structure to be used for outgoing FOLIO EDI files, such as the prefix or file extension. Example: .edu
*   **Send account number.** If you send your account number with orders or invoices, select the **Send account number** checkbox. If selected, the account number will be required for the PO/POL and output in the EDI order file.
*   **What messages are expected for this vendor?** If your library expects to send EDI orders to the vendor, select the **Orders** checkbox. If your library expects to receive EDI invoices from the vendor, select the **Invoices** checkbox.
*   **Notes.** Enter any notes about the EDI information for this vendor.


#### FTP 詳細



*   **EDI FTP.** Select FTP format in which the library expects to transact with the vendor: SFTP or FTP.
*   **FTP mode.** Select the transmission mode the library expects to use with the vendor: ASCII or Binary.
*   **Server address.** The address for the vendor’s FTP server.
*   **FTP connection mode.** Select the connection mode: Active or Passive.
*   **Username.** The username for the FTP, if a login username is required for this vendor.
*   **Password.** The password for the FTP, if a login password is required for this vendor. The password is automatically hidden. Click **Show** to display the password. Click **Hide** to stop displaying the password.
*   **FTP port.** The FTP port number.
*   **Order directory.** The subdirectory where orders should be placed, if different from the main FTP directory for this vendor. Ex: /directory.
*   **Invoice directory.** The subdirectory where invoices should be retrieved, if different from the main FTP directory for this vendor. Ex: /directory.
*   **Notes.** Any notes about the FTP details for this vendor.


#### スケジューリング



*   **Schedule EDI.** If you want to schedule the EDI, select the **Schedule EDI** checkbox.
*   **Date.** Select the date you want to begin the scheduled EDI.
*   **Time.** Select the time for the scheduled EDI.
*   **Weekly.** Select the days on which the EDI will run.
*   **Send to emails.** A comma-separated list of emails to which vendor EDI notifications will be sent. Ex: [jane.doe@example.edu](mailto:jane.doe@example.edu), library.staff@example.edu
*   **Notify all EDI.** If you want to notify the email addresses about any kind of EDI transaction, select the **Notify all EDI** checkbox.
*   **Notify invoice only**. If you want to notify the email addresses about invoices only, select the **Notify invoice only** checkbox.
*   **Notify error only.** If you want to notify the email addresses only if an EDI error occurs, select the **Notify error only** checkbox.
*   **Check now.** To verify the EDI connection, click **Check now**. Note: This feature is currently in development.
*   **Notes.** Enter any notes about the EDI schedule.


### アカウント

アカウントとは、資料を発注する際に使用するベンダーのアカウントのことです。

Note: Adding an account is optional, but if you click **Add**, you must fill in the required fields or delete the account in order to save the organization record.


#### アカウントの追加

1. Click **Add**.

2. Enter the account **Name** in the box.

3.  **アカウント番号** を入力します。この番号は、通常、ベンダーから割り当てられます。注：ここで入力したアカウント番号は、そのベンダーのすべての発注や請求書にデフォルト値として表示されます。このセクションで複数のアカウントを設定した場合、最初のアカウント番号が発注や請求書のデフォルト値として表示されますが、ベンダーに紐づくアカウント番号がすべて含まれるドロップダウンリストから、適切な番号を選択することができます。

4. Optional: Enter a **Description** of the account in the box.

5. Optional: Enter the **Accounting code** in the box.

6. Select the **Payment method** from the drop-down list.

7. Select the **Account status** from the drop-down list.

8. Optional: Enter **Contact** info in the box.

9. Enter the **Library code** in the box. This is the library-supplied code for the account with the vendor.

10. Enter the **Library EDI code** in the box.

11. Optional: Enter any **Notes** about the account in the box.

12. Optional: Select any **Acquisition units** from the drop-down list. For more information on acquisition units, see [Settings > Acquisition]("/settings_acquisition_units.md") units.

13. Repeat steps 1-13 as needed. Accounts are saved once you save the vendor.


#### アカウントの削除

1. Find the account you want to delete.

2. **ゴミ箱アイコン**をクリック。 The account is removed and is deleted once you save the vendor.


## 組織の検索

 **検索とフィルター** ペインで組織を検索できます。組織を検索するには、ボックスに検索語を入力します。ドロップダウンリストで **全部** を選択すると、次のフィールドのいずれかを通して検索できます。



*   **全部。** すべてのフィールド。これはデフォルトの検索です。
*   **名称。** 組織の名称。 
*   **コード。** 組織の一意な識別子。
*   **言語。** 組織のデフォルト言語。
*   **別名。** 組織が使用する代替名（略称や旧名など）。
*   **アカウントコード。** 、図書館が支払いシステムで組織を参照するために使用するアカウントコード。
*   **Tax ID。** 図書館のtax ID。

You can also search for organizations by selecting any of the filters in the **Search & filter** pane. Additionally, you can apply the filters after you perform a search to limit your results. See the sections below for more information.


### 組織のステータス

組織をステータスで絞り込むには、次のいずれかを選択します：



*   **アクティブ。** 現在、図書館で使用している組織。
*   **非アクティブ。** 現在、図書館で以前使用されていた組織。
*   **保留中。** まだ使用可能になっていない組織。「保留中」は、組織のレコード作成がまだ完了していないことを示すことができる。


### タグ

To search for organizations assigned with specific tags, follow these steps:

1. In the **Search & filter** pane, click **Tags**.

2. Select the tag(s) from the drop-down list. Your results appear in the Organizations pane.


### ベンダー

To filter organizations by whether or not they are a vendor, select one of the following:



*   **Yes.** ベンダーである（ベンダーのチェックボックスが選択されている）組織。
*   **No.** ベンダーではない組織。


### Country

To search for organizations with offices in a specific country, follow these steps:

1. In the **Search & filter** pane, click **Country**.

2. Select the country from the drop-down list. Your search results appear in the Organizations pane.


### Languages

To search for organizations that communicate in a specific language, follow these steps:

1. In the **Search & filter** pane, click **Languages**.

2. Select the language from the drop-down list. Your search results appear in the Organizations pane.


### 支払方法

options:ベンダーレコードの[ベンダー情報](#vendor-information)セクションに記載されている、デフォルトの支払い方法で組織を絞り込むには、次のオプションのいずれかを選択します：



*   **現金。** デフォルトの支払い方法は現金。
*   **クレジットカード。** デフォルトの支払い方法はクレジットカード。
*   **電子決済。** デフォルトの支払い方法は電子決済（electronic funds transfer）。
*   **預金口座。** デフォルトの支払い方法は預金口座。
*   **小切手（紙）。** デフォルトの支払い方法は紙の小切手。
*   **銀行為替手形。** デフォルトの支払い方法は銀行為替手形。
*   **内部送金。** デフォルトの支払い方法は内部送金（internal transfer）.
*   **その他。** デフォルトの支払い方法はその他の方法。


### 調達ユニット

To search for organizations to which one or more acquisitions units have been assigned, follow these steps:

1. In the **Search & filter** pane, click **Acquisitions unit**.

2. Select the acquisitions unit from the drop-down list. The search results appear in the Organizations pane.


## 組織詳細の表示

組織を検索すると、「組織」ペインに次の情報が表示されます：



*   **名称。** 組織の名称。
*   **コード。** 組織の一意な識別子。
*   **説明。** 組織の説明。
*   **組織ステータス。** 組織のステータス：アクティブ、非アクティブ、保留中。
*   **ベンダー。** 組織がベンダーかどうか。

検索結果で、組織をクリックすると詳細が表示されます。組織の詳細ペインに、その組織に関する追加情報が表示されます。


## 組織の編集

1. [Find the organization you want to edit](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Actions > Edit**.

3. Edit the organization.

4. Click **Save & close**. The organization is saved and updated.


### ベンダーを組織に変更する

注：ベンダーを組織に変更すると、レコードからすべてのベンダー情報、ベンダー条件、EDI 情報、およびアカウントが削除されます。

1. [Find the organization you want to edit](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, clear the **Vendor** checkbox.

3. In the Confirm vendor data deletion dialog, click **Confirm**. The Vendor information, Vendor terms, EDI information, and Accounts sections are removed.

4. Make any additional changes to the organization.

5. Click **Save & close**. The organization is saved and updated.


## 組織の削除

1. [Find the organization you want to delete](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Actions > Delete**.

3. In the **Delete organization** dialog, click **Delete**. The organization is deleted and a confirmation message appears.


## Adding a tag to an organization

1. [Find the organization you want to tag](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click the **tag icon**.

3. In the **Tags** pane, either select a tag from the box or enter a tag. 

4. Click the **X** on the **Tags** pane to close the pane and save the tag. The tag number updates to the number of tags applied to the organization.


## Adding a note to an organization

1. [Find the organization to which you want to add a note](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Notes > New**.

3. In the **New note** window, select the **Note type** from the drop-down list. Note types are created in the Settings app. For more information, see Settings > Notes.

4. Enter a **Note title** in the box.

5. Optional: Enter any **Details** about the note in the box.

6. Click **Save & close**. The note is saved and appears in the Notes section in the Organization details pane.


## 担当者の作成

注：新しい連絡先を作成する必要がある場合は、作成中の組織の進捗状況を保存するか、新しい連絡先のプロセスを開始する前に、すべての組織情報の入力が完了するまで待機する必要があります。新しい連絡先を作成すると、組織ウィンドウから外れます。

1. Click **Add contact**.

2. In the **Add contacts** dialog, click **New**. If you have not saved your organization information, you are prompted to do so before continuing.

3. In the **Create contact** window, fill in the fields in the Name, Emails, Phone numbers, URLs, and Addresses sections. See below for more information.

4. Click **Save & close**. A confirmation message appears and the contact is saved.


##### 名称



*   **プリフィクス。** 担当者の肩書き。
*   **姓。** 担当者の苗字。
*   **名。** 担当者の名前。
*   **ステータス。** ドロップダウン・リストから連絡先のステータスを選択します。「アクティブ」または「非アクティブ」を選択します。
*   **言語。** 担当者が主に話す言語。
*   **カテゴリー。** ドロップダウン・リストから、担当者を説明する任意のカテゴリーを選択します。カテゴリは、設定アプリで設定します。詳しくは、「設定」>「組織」を参照してください。
*   **ノート。** 担当者に関するノート。


##### Eメール


###### Adding an email address

1. Click **Add email**.

2. Enter the **Email address** in the box.

3. Optional: Enter a **Description** of the email in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed.The email address saves once you save the contact. Note: If you are adding multiple emails, click **Primary** to indicate the contact’s primary email address.


###### Deleting an email address

1. Find the email address you want to delete.

2. **ゴミ箱アイコン**をクリック。 The email address is removed and is deleted once you save the contact.


##### 電話番号


###### 電話番号の追加

1. Click **Add phone number**.

2. Enter the **Phone number** in the box.

3. Optional: Select the **Type** of number it is from the drop-down list: Office, Mobile, Fax, or Other.

4. Optional: Select the **Language** spoken at that number from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed. The phone number saves once you save the contact. Note: If you are adding multiple phone numbers, click **Primary** to indicate the contact’s primary phone number.


###### Deleting a phone number

1. Find the phone number you want to delete.

2. **ゴミ箱アイコン**をクリック。 The phone number is removed and is deleted once you save the contact.


##### URLs


###### URLの追加

The URL can be a website or FTP link.

1. Click **Add URL**.

2. Enter the **URL** in the box.

3. Optional: Enter a **Description** of the URL in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the URL.

6. Repeat steps 1-5 as needed. The URL saves once you save the contact. Note: If you are adding multiple URLs, click **Primary** to indicate the contact’s primary URL.


###### URLの削除

1. Find the URL you want to delete.

2. **ゴミ箱アイコン**をクリック。 The URL is removed and is deleted once you save the contact.


##### 住所


###### 住所の追加

1. Click **Add address**.

2. Fill in the address information.

3. Repeat steps 1-2 as needed. The address saves once you save the contact. Note: If you are adding multiple addresses, click **Primary** to indicate the contact’s primary address.


###### 住所の削除

1. Find the address you want to delete.

2. **ゴミ箱アイコン**をクリック。 The address is deleted and is removed from the record once you save the contact.


## 担当者の編集

注：連絡先を編集する必要がある場合、作成中の組織の進捗状況を保存するか、すべての組織情報の入力が完了するまで待ってから、新しい連絡先プロセスを開始する必要があります。連絡先を編集すると、組織ウィンドウから外れます。

1. [Add the contact you want to edit to Contact people](#adding-an-existing-contact) if you have not already.

2. Click the contact you want to edit. If you have not saved your organization information, you are prompted to do so before continuing.

3. In the contact window, click **Actions > Edit**.

4. Edit the contact.

5. Click **Save & close**. A confirmation message appears and the contact is updated.


## 担当者のコピー

ユーザーインターフェイスに表示されますが、連絡先のコピーはできません。

## 担当者の割り当て解除

See [Deleting a contact](#deleting-a-contact) for an alternate way to remove a contact from an organization.

1. [Add the contact you want to unassign to Contact people](#creating-a-contact-person) if you have not already.

2. Click the contact you want to unassign. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Unassign**.

4. In the **Unassign from organization** dialog, click **Confirm**. A confirmation message appears, the contact is removed from the organization, and the organization window appears.


## 担当者の削除

連絡先を削除すると、図書館の連絡先リストからその連絡先が削除されます。組織の記録から連絡先を削除する場合は、[連絡先の削除](#deleting-a-contact-person)を参照してください。

1. [Add the contact you want to delete to Contact people](#creating-a-contact-person) if you have not already.

2. Click the contact you want to delete. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Delete**.

4. In the **Delete contact** dialog, click **Confirm**. The contact is deleted and the organization window appears.


## インターフェイスの作成

注：新しいインターフェースを作成する必要がある場合、作成中の組織の進捗状況を保存するか、新しいインターフェースプロセスを開始する前に、すべての組織情報の入力が完了するまで待機する必要があります。インターフェイスを作成すると、組織ウィンドウから外れます。

1. Click **Add interface**.

2. In the **Add interfaces** dialog, click **New**. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the **Create interface** window, fill in the fields. See below for more information.

4. Click **Save**. A confirmation message appears and the interface is saved.


##### フィールド



*   **タイプ。** 追加するインターフェイスの種類。管理、エンドユーザー、レポート、発注、請求書、またはその他。
*   **名称。** インターフェイスの名前。
*   **URI。** インターフェイスのURI。
*   **ユーザー名。** インターフェイスへのログインに必要なユーザー名。
*   **パスワード。** インターフェイスへのログインに必要なパスワード。 **表示** をクリックしてパスワードを表示。**非表示** をクリックしてパスワードを非表示。
*   **ノート。** インターフェイスに関するノート。
*   **利用可能。** このインターフェイスで統計情報を利用できるかどうかを示す **利用可能** チェックボックスを選択します。
*   **配信方法。** 統計の**配信方法**をドロップダウンリストから選択します。オンライン、FTP、Eメール、その他から選択します。
*   **統計フォーマット。**  **統計情報のフォーマット** をドロップダウンリストから選択します。Counter、Delimited、Excel、PDF、ASCII、HTML、またはその他を選択します。
*   **ローカルに保存。** 統計情報がローカルに保存されているか？
*   **オンラインの場所。** 統計のオンラインの場所。例えば、ウェブサイト。
*   **統計ノート。** 統計情報に関するノート。


## Editing an interface

注：インターフェイスを編集する必要がある場合、作成中の組織の進捗状況を保存するか、すべての組織情報の入力が完了するまで待ってから、新しいインターフェイスのプロセスを開始する必要があります。インターフェイスを編集すると、組織ウィンドウから外れます。

1. [Add the interface you want to edit to the Interface section](#adding-an-existing-interface) if you have not already.

2. Click the interface you want to edit. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Edit**.

4. Edit the interface.

5. Click **Save**. A confirmation message appears and the interface is updated.


## Copying an interface

Although it appears in the user interface, copying an interface is not available.


## Unassigning an interface

See [Deleting an interface](#deleting-an-interface) for an alternate way to remove an interface from an organization.

1. [Add the interface you want to unassign to the Interface section](#adding-an-existing-interface) if you have not already.

2. Click the interface you want to unassign. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Unassign**.

4. In the **Unassign from organization** dialog, click **Confirm**. A confirmation message appears, the contact is removed from the organization, and the organization window appears.


## インターフェイスの削除

インターフェイスを削除すると、図書館のインターフェイスの一覧から削除されます。組織レコードからインターフェースを削除する必要がある場合は、インターフェースの削除を参照してください。

1. Add the interface you want to delete to the Interface section if you have not already.

2. Click the interface you want to delete. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Delete**.

4. In the **Delete interface** dialog, click **Confirm**. The contact is deleted and the organization window appears.
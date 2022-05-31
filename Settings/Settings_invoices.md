| ソース | 取得日 |
| ---- | ---- |
| [Settings](https://github.com/folio-org/docs/tree/master/content/en/docs/Settings) | 2022-03-28 |


設定アプリの請求書セクションは、ワンクリック承認の設定、プリセット調整金の作成、バッチグループの作成、バッチグループの設定、支払伝票番号の入力を行う場所です。

## Permissions

To interact with invoice settings, users need the following permission:



*   **Settings (Invoice): Can view and edit settings.** This permission lets you view and edit all of the Invoice settings.

Note: This is the only permission for invoice settings. You can assign permissions to users in the Users app.


## 設定 > 請求書 > 承認

請求書をワンクリックで承認できるようにする設定です。「承認と支払いをワンクリックで行う」を選択すると、請求書の承認と支払いの承認が一度に行えます。この設定を有効にした場合でも、請求書アプリは、送信前に承認の確認を求めます。


## 設定 > 請求書 > 調整金

この設定は、請求書にいつでも追加できるプリセット調整金を作成するために使用します。

### 調整金の作成



1. 「新規作成」をクリック。
2. ボックスに**説明**を入力してください。
3. リストから**タイプ**（パーセント、金額）を選択します。
4. 新しい請求書を作成する際に、自動的に調整金を表示させたい場合は、**常に表示** チェックボックスを選択します。注：このオプションを有効にしても、請求書から調整金を削除することはできます。
5. ボックスに **既定の金額** を入力します。
6.リストから **比例配分** （「明細行単位」「金額単位」「数量単位」「比例配分しない」）を選択します。
7. リストから**合計額との関係**を選択します：追加（In addition to）または分離（separate from）。
8. 外部の財務システムに調整金のコピーを送信する場合は、**会計にエクスポート** チェックボックスを選択します。
9. 「保存して閉じる」をクリックします。調整金が保存されます。


### 調整金の編集



1. Find the adjustment you want to edit and click it.
2. Click **Actions** > **Edit**.
3. Edit the adjustment.
4. Click **Save & close**.


### 調整金の削除

1. Select the adjustment you want to delete.
2. In the adjustment window, select **Actions** > **Delete**.
3. In the **Delete adjustment** dialog, click **Delete**. A confirmation message appears and the adjustment is deleted.


## 設定 > 請求書 > バッチグループ

この設定は、バッチグループの作成、編集、削除に使用されます。バッチグループは、特に外部の支払システムに支払伝票としてエクスポートするために請求書を整理するために使用されます。

### バッチグループの作成


1. 「新規作成」をクリック。
2. Enter a **Name** in the box.
3. Optional: Enter a **Description** in the box.
4. Click **Save.** The Batch group is saved.


### バッチグループの編集

1. Find the Batch group you want to edit and click the **pencil icon**.
2. Edit the **batch group**.
3. Click **Save**.


### バッチグループの削除

1. Find the Batch group you want to edit and click the **delete icon.**
2. In the **Delete Batch group** dialogue box, click **Delete**. A confirmation message appears and the Batch group is deleted.


## 設定 > 請求書 > バッチグループ設定

請求書の整理に使用する「バッチグループ」を構成する場合に使用します。この設定により、前回のエクスポート以降に作成されたすべての支払伝票を含むファイルをエクスポートすることができます。伝票の作成方法については、[請求書 > 請求書の承認](../Acquisitions/Invoices.md#インボイスの承認)を参照してください。
「会計にエクスポート」チェックボックスが選択されている支払伝票で、バッチグループの最後のエクスポート以降に作成されたものは、全てファイルにエクスポートされます。「会計にエクスポート」チェックボックスの詳細については、[請求書 > 調整金の作成](../Acquisitions/Invoices.md#請求書の作成)を参照してください。
各請求書は、すべてのファンドチャージがファンド外部アカウント番号でグループ化された一意の支払伝票を生成します。

### バッチグループの構成

1. 「バッチグループ」を選択します。
2. 「エクスポートのスケジュール」を選択します。**日時**を選択した場合、時間を入力します。**週次**を選択した場合、エクスポートを自動的に実行させたい曜日と時間を選択します
3. **アップロード場所**を入力します。 このボックスが空白のままであれば、エクスポートはあなたのコンピュータにファイルをダウンロードします。
4. **フォーマット**を選択します。 JSON または XMLです。
5. ファイルのアップロード場所に必要な場合は、**ユーザー名** を入力します。
6. ファイルのアップロード場所に必要であれば、**パスワード**を入力します。
7. 「保存」をクリック。

「資格情報の表示/資格情報の非表示」をクリックすると、パスワードの表示/非表示を切り替えることができます。アップロード先との接続をテストしたい場合は、「テスト接続」をクリックします。

### 手動エクスポートの実行

注：手動エクスポートを実行すると、バッチグループの最後のエクスポート以降に作成されたすべての支払伝票がエクスポートされ、この処理は元に戻すことができません。

1. 「手動エクスポートを実行する」をクリックします。
2. 手動エクスポート実行ダイアログで、確認メッセージの 「続ける」をクリックします。

## 設定 > 請求書 > 支払伝票番号

請求書に使用する支払伝票番号を作成することができるセクションです。

1. **プレフィックス**を入力します。
2. **開始番号**を入力します。
3. 伝票番号をリセットする必要がある場合は、**シーケンスのリセット**をクリックします。
4. 伝票番号の編集を許可する場合は、**支払伝票の編集を許可** のチェックボックスを選択します。
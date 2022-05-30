# 発注

発注アプリは、発注を作成・管理するためのアプリです。

受注アプリに関する用語の定義です。

* **収集ユニット(Acquisition units)**。購買の記録に追加できるレイヤーのことで、そのユニットに割り当てられているユーザー以外は、その記録を操作できないように制限されています。例えば、図書館システム内の異なる図書館を表すために、収集ユニットを作成することができます。ユニットは、設定アプリで図書館によって定義され、決定されます。詳しくは、「設定」＞「収集ユニット」を参照してください。
* **発注（Order）**。図書館がベンダーに発注するタイトルまたはパッケージ（物理的または電子的）のリストを特徴とする発注。
* **発注明細(Orderline)**。発注明細には、図書館が発注するタイトルまたはパッケージのいずれかが含まれます。発注明細は「発注」を構成します。「発注」には複数の発注明細が含まれることがあります。

# パーミッション

以下の権限により、発注アプリの操作が可能になり、アプリ内でできること、できないことが決定されます。「ユーザー」アプリでユーザーに権限を割り当てることができます。これらの権限がユーザーに割り当てられていない場合、そのユーザーは発注アプリや関連情報を見ることができません。

注：以下の権限は、発注アプリにのみ適用されます。アプリ内の発注は、「所蔵」や「受入」などの他のアプリのレコードにリンクしている場合があり、それらのレコードを操作するためには別のパーミッションが必要になる場合があります。

以下は、発注のすべての権限です：

* **Orders: Assign acquisition units to new order**. This permission allows the user to assign acquisition units to orders when creating a new order.
* **Orders: Create order lines**. This permission allows the user to create new order lines. With this permission, the user can also view and edit existing order lines. Additionally, they can view order settings.
* **Orders: Create orders**. This permission allows the user to create new orders. With this permission, the user can also view and edit existing orders. Additionally, they can view order settings.
* **Orders: Delete order lines**. This permission allows the user to delete order lines. With this permission, the user can also view and edit existing order lines. Additionally, they can view order settings.
* **Orders: Edit order lines**. This permission allows the user to view and edit order lines. Additionally, they can view order settings.
* **Orders: Edit orders**. This permission allows the user to view and edit orders. Additionally, they can view order settings.
* **Orders: Manage acquisition units**. This permission allows the user to change the assignment of acquisition units for an order or order line.
* **Orders: Remove orders**. This permission allows the user to delete orders. With this permission, the user can also view and edit existing orders**. Additionally, they can view order settings.
* **Orders: Reopen purchase orders**. This permission allows the user to reopen an order.
* **Orders: Unopen purchase orders**. This permission allows the user to unopen an order.
* **Orders: View order lines**. This permission allows the user to search for and view order lines. Additionally, they can view order settings.
* **Orders: View orders**. This permission allows the user to search for and view orders. Additionally, they can view order settings

## 発注（order）を作成する

発注には、図書館がベンダーに発注しているタイトルやパッケージ（物理的または電子的）のリストが含まれています。

FOLIOでは、1回限りの発注と継続的な発注のいずれかを作成することができます。単行本のように年内に納品されるものは、一回限りの発注とします。一方、継続発注は、通常、複数年にわたる発注となり、各品目を受け取るたびに支払いを行うことになります。例えば、雑誌の定期購読のために継続的な発注を作成することができます。

発注を作成したら、少なくとも1つの発注を追加して、発注を開き、取得プロセスを開始できるようにする必要があります。

## ワンタイムの発注の作成

1. 「検索とフィルタ」ペインで、「発注」をクリックします。

1. 「発注」 ペインで、「新規」 をクリックします。

1. 「発注を作成」ウィンドウで、「テンプレート名」ドロップダウン・リストからテンプレートを選択します（使用する場合）。発注には、テンプレートで設定された情報が入力されます。テンプレートは、設定アプリで作成されます。詳細については、「設定」 > 「発注」 > 「発注テンプレート」を参照してください。

1. 「発注タイプ」 ドロップダウンリストから「ワンタイム」 を選択します。

1. 発注と発注サマリーの下にある残りのフィールドを入力します。これらのセクションで利用可能なフィールドとアクションの詳細については、以下のセクションの説明を参照してください。

1. オプション：発注を承認する場合は、「承認」を選択します。注：発注を承認する必要があるのは、図書館で「承認が必要」の設定がオンになっている場合のみです。詳細については、「設定」 > 「発注」 > 「承認」を参照してください。

1. 「保存して閉じる」 をクリックします。確認メッセージが表示され、発注が「発注」ペインに表示されます。

### 発注(Purchase Order)

* **プリフィックス**。該当する場合、発注番号の接頭辞をドロップダウンリストから選択します。プリフィックスは、設定アプリで図書館によって設定されます。詳細については、「設定」>「発注」>「プリフィックス」を参照してください。
* **発注番号（PO number）**。発注の発注番号。発注番号を編集できるかどうかは、図書館の「発注番号の編集」設定に依存します。詳しくは、設定 > 発注 > 編集を参照してください。
* **サフィックス**。該当する場合は、ドロップダウン リストから発注番号のサフィックスを選択します。サフィックスは、図書館によって設定アプリで設定されます。詳しくは、「設定」>「発注」>「サフィックス」を参照してください。
* **ベンダー**。あなたの図書館が資料を購入する任意の機関。ベンダーを選択するには、「組織検索」をクリックします。「組織の選択」ダイアログで、検索ボックスおよび/またはフィルタを使用して組織を見つけます。組織をクリックして選択します。組織は、ベンダーのフィールドに追加されます。

* **発注タイプ**。発注の種類を選択します。「ワンタイム（1回限り）」または「継続」

* **収集ユニット**。発注を特定の収集ユニット内の特定のユーザーが利用できるようにしたい場合、収集ユニットを入力するか、ドロップダウンリストから選択します。複数の単位を選択することができます。収集ユニットについて詳しくは、「設定」>「収集ユニット」を参照してください。

* **割り当て先** 発注をユーザーに割り当てるには、[+]をクリックします。ユーザー選択ダイアログで、検索ボックスおよび/またはフィルターを使用してユーザーを見つけます。ユーザーをクリックして、選択します。そのユーザーが Assigned to ボックスに表示されます。ユーザーを削除する必要がある場合は、xをクリックします。発注を別のユーザーに割り当てる必要がある場合は、+をクリックし、上記の手順を繰り返します。
* **請求先** 「請求先」ドロップダウンリストで、発注の請求先住所を選択します。住所を選択すると、請求先が表示されます。住所は、設定アプリで設定します。詳しくは、［設定］＞［テナント］＞［住所］を参照してください。
* **配送先**。「配送先」 ドロップダウン リストで、発注商品の配送先の住所を選択します。住所を選択すると、発送先が表示されます。住所は、設定アプリで設定します。詳しくは、［設定］＞［テナント］＞［住所］を参照してください。
* **手動** 「手動」 チェックボックスを選択すると、発注を自動処理の対象から除外します。たとえば、EDIを設定しているが、ベンダーのサイトで発注を送信し、ベンダーに再送信したくない場合に選択します。
* **再支出準備**。再支出準備（Re-encumber）チェックボックスは、デフォルトで選択されています。このチェックボックスがオフの場合、発注が再支出準備（Re-encumber）の条件を満たしていても、会計年度のロールオーバー中に再支出準備（Re-encumber）すべきではないことを意味します。ただし、チェックボックスが選択されていて、ロールオーバーの設定により、この発注が再支出準備（Re-encumber）の基準を満たさないことが示された場合、この発注の資金は次の会計年度にはコミットされません。再支出準備（Re-encumber）のトグルは、発注がロールオーバーの基準を満たす場合にのみ考慮されます。チェックボックスが選択され、ロールオーバーの設定により、この発注が再支出準備（Re-encumber）の基準を満たしていることが示された場合、この発注の資金は次の会計年度にコミットされます。
* **タグ**。発注に適用するタグを入力またはドロップダウンリストから選択します。

### 発注サマリー

* **承認済み** 発注を承認する場合は、「承認済み」チェックボックスを選択します。注：発注を承認する必要があるのは、図書館で「承認が必要」という設定がオンになっている場合のみです。詳細については、「設定」 > 「発注」 > 「承認」を参照してください。


## 継続（ongoing）発注の作成

1. 「検索とフィルタ」ペインで、［発注］をクリックします。

1. 「発注」 ペインで、「新規作成」 をクリックします。

1. 「発注を作成」ウィンドウで、「テンプレート名」ドロップダウン・リストからテンプレートを選択します（使用する場合）。発注には、テンプレートで設定された情報が入力されます。テンプレートは、設定アプリで作成されます。詳細については、「設定」 > 「発注」 > 「発注テンプレート」を参照してください。

1. 「発注タイプ」 ドロップダウン リストから 「継続」 を選択します。

1. 「発注」「継続発注情報」「発注サマリー」の下にある残りのフィールドを入力します。これらのセクションで利用可能なフィールドとアクションの詳細については、以下のセクションの説明を参照してください。

1. オプション：発注を承認する場合は、「承認済み」 を選択します。注：発注を承認する必要があるのは、図書館で「承認が必要」の設定がオンになっている場合のみです。詳細については、「設定」 > 「発注」 > 「承認」を参照してください。

1. 「保存して閉じる」 をクリックします。確認メッセージが表示され、発注が「発注」ペインに表示されます。

## 継続的発注情報

* **サブスクリプション**。継続的な発注が定期購入（サブスクリプション）である場合、「サブスクリプション」チェックボックスを選択します。
* **更新間隔**。更新の間隔を日数で指定します。これは、図書館がこの資料にアクセスできる期間（日単位）です。その後、図書館は別の期間の更新が必要になります。このフィールドは、「サブスクリプション」を選択した場合のみ編集可能で、必須です。
* **更新日**。図書館が更新するかどうかを決定しなければならない日付で、解約期限と呼ばれることもあります。このフィールドは、「サブスクリプション」を選択した場合のみ編集可能であり、必須項目です。
* **レビュー期間**。更新日前に、サブスクリプションを再度購入するかどうかを決定することができる期間です。このフィールドは、「サブスクリプション」を選択した場合のみ編集できます。
* **手動更新（Manual renewal）**。「手動更新」 チェックボックスを選択すると、サブスクリプションを更新するためにベンダーに連絡する必要があることを示します (ベンダーは自動的に更新しません)。このフィールドは、「サブスクリプション」が選択されている場合にのみ編集可能です。
* **レビュー日**。レビューの日付です。このフィールドは、「サブスクリプション」が選択されていない場合にのみ編集可能です。
* **ノート**。進行中の発注に関するメモ。

## 発注の検索

## 発注の承認

発注を承認する必要があるのは、「承認が必要」という設定がオンになっている場合のみです。詳細については、「設定」>「発注」>「承認」を参照してください。この設定をオンにした場合、発注を承認するには、該当する権限も必要です。発注が承認されると、発注を「オープン」いすることができます。

発注を承認するには、2つの方法があります。発注を編集して、「発注サマリー」の 「承認済み」 チェックボックスを選択するか、次の手順を実行します。

1. 承認したい発注を検索し、選択します。

1. 「発注」 ペインで、「操作」 > 「承認」 を選択します。確認メッセージが表示され、発注書が「承認済み」としてマークされます。

## 発注の複製

1. 複製したい発注を検索し、選択します。

1. 「発注」 ペインで、「操作」 > 「複製」 を選択します。

1. 「発注の複製」 ダイアログで、「複製」 をクリックして複製/重複作成を確定します。確認メッセージが表示され、発注が複製/重複作成され、発注ペインに表示されます。

## 発注のオープン

発注を作成した後、その発注を開くまでは、ステータスが「保留」になっています。発注を「オープン」にすると、次のことが起こります。

* 支払準備金が作成されます。注: ファンドが発注明細に追加されている場合のみ、支払準備金（encumbrances）が作成されます。
* 所蔵の書誌が作成されます。注: 発注明細の「所蔵の作成」フィールドが「なし」に設定されている場合、所蔵レコードは作成されません。「所蔵の作成」フィールドの詳細については、以下の「電子資料の詳細」および「物理資料の詳細」セクションを参照してください。
* 「発注日」は本日の日付に設定されています。
* 発注明細を追加することはできません。
* 発注タイプ、タイトル、取得方法、発注フォーマットなどのフィールドは、一度発注をオープンにすると編集することができません。これらのフィールドを編集するには、発注を開いていない状態にする必要があります。詳しくは、「発注を非オープンにする」を参照してください。

1. オープンにしたい発注を検索して選択します。

1. 「発注」ペインで、[操作] > [オープン] を選択します。

1. 「オープン - 発注」ダイアログで、「送信」をクリックします。確認メッセージが表示され、発注のステータスが「オープン」に変更されます。

## 発注を非オープンにする

発注のオープンは最終的なものではなく、発注の「オープン」を解除することで、発注を保留状態に戻すことができます。

注: 発注の「オープン」を解除すると、発注中（On Order）のステータスを持つすべての支払準備金、および資料の資料のレコードが削除されます。ただし、受入済みの資料（item）、所蔵（holdings）、およびインスタンスは削除されません。

1. 非オープンにする発注を検索し、選択します。

1. 発注ペインで、「操作」 > 「オープン」を選択します。

1. 「非オープン - 発注」 ダイアログで、「送信」 をクリックします。確認メッセージが表示され、発注のステータスが「オープン」に変更されます。

## 発注をクローズする

発注が不要になったら、発注をクローズすることができます。発注をクローズすることができるのは、「オープン」の発注のみです。

1. クローズする発注を検索し、選択します。

1. 「発注」ペインで、「操作」>「発注をクローズ」を選択します。

1. 「クローズ - 発注」ダイアログで、ドロップダウン・リストから「クローズする理由」を選択します。クローズする理由は、[設定] アプリで設定します。詳細については、「設定」 > 「発注」 > 「発注をクローズする理由」を参照してください。

1. オプション：発注をクローズする理由についてのメモを入力します。

1. 発注をクローズするには、[送信]をクリックします。確認メッセージが表示され、発注のステータスが「クローズ」に変更されます。

## 発注を再オープンする

発注のクローズは最終的なものではなく、発注を再開することで発注の状態を「オープン」に戻すことができます。

1. 再開したい発注を検索し、選択します。

1. 「発注」ペインで、「操作」>「再オープン」を選択します。確認メッセージが表示され、発注のステータスが「オープン」に変更されます。

## 発注の受入
受入ができるのは、オープンになっている発注だけです。

1. [Search for the order you want to receive](#searching-for-an-order) and select it.

2. In the **Purchase order** pane, select **Actions > Receive.** The order line(s) open in the Receiving app.

3. Follow the steps as outlined in [Receiving > Receiving an order](/Acquisitions/Receiving.md#receiving-an-order").

## 発注の削除
Note: When you delete an order, received items remain in the system, but the receiving history is removed.

1. [Search for the order you want to delete](#searching-for-an-order) and select it.

2. In the **Purchase order** pane, select **Actions > Delete.**

3. In the Delete order dialog, click **Delete**. A confirmation message appears and the order is deleted.


## 発注にタグを追加する
1. [Search for the order you want to tag](#searching-for-an-order) and select it.

2. In the **Purchase order details** pane, click the **tag icon**.

3. In the **Tags** pane, either select a tag from the box or enter a tag.

4. Click the **X** on the Tags pane to close the pane and save the tag. The tag number updates to the number of tags applied to the order.

## 発注に発注明細を追加する
1. [Search for the order to which you want to add the PO line](#searching-for-an-order) and select it.

2. In the **Purchase order** pane, in the **PO lines** section, click **Add PO line**.

3. In the **Add PO line** window, fill in the fields in the [Item details](#item-details), [PO line details](#po-line-details), [Vendor](#vendor), [Cost details](#cost-details), and [Fund distribution](#fund-distribution) sections. For more information on the fields and actions available in these sections, see the section descriptions below.

4. Click **Save & close** or **Save & open order**, if applicable. For more information on saving and opening orders at the same time, see [Settings > Orders > Opening purchase orders](../Settings/Settings_orders.md#設定--発注--opening-purchase-orders)

### 項目の説明

*   **パッケージ。** パッケージを追加する場合は、**パッケージ**のチェックボックスを選択します。選択すると、「タイトル」が「パッケージ名」になります。
*   **タイトル/パッケージ名。** 資料のタイトル。その資料がすでに 所蔵アプリにある場合、タイトル検索を使用して、その資料を所蔵レコードにリンクさせることができます。これにより、該当するフィールドに自動的に入力されます。所蔵レコードにリンクするには、**タイトル検索**をクリックします。**インスタンスの選択**ダイアログで、検索ボックスやフィルターを使用してタイトルを見つけます。タイトルをクリックして選択します。タイトルがタイトルボックスに表示され、関連する項目フィールドが入力されます。
*   **受入ノート。** 資料の受入に関するノートを入力します。ノートは、この注文明細の「受入」アプリに表示されます。
*   **サブスクリプション開始日。** 資料がサブスクリプションの場合、サブスクリプションの開始時期を選択します。
*   **サブスクリプション終了日。** 資料がサブスクリプションの場合、サブスクリプションの終了時期を選択します。
*   **サブスクリプション間隔。** サブスクリプションの場合は、サブスクリプションの継続日数を入力または選択します。
*   **出版日。** 資料の出版日。 \
**出版者。** 資料の出版者。
*   **版。** 資料の版。
*   **リンクされたパッケージ。** パッケージと発注明細を紐付けるには、**パッケージ発注明細の検索**をクリックします。**発注明細の選択** ダイアログで、検索ボックスやフィルターを使用してパッケージを探します。パッケージをクリックして選択します。パッケージは、「リンクされたパッケージ」ボックスに表示されます。
*   **寄与者。** 資料の寄与者。
*   **製品ID。** ISBNのような資料の識別子。
*   **内部ノート。** 資料に関する内部向けのノート。

#### Adding a contributor

1. Click **Add contributor**.

2. Enter the **Contributor** in the box.

3. Select the **Contributor type** from the drop-down list. The Contributor saves once the order line is saved.


#### Deleting a contributor

1. Find the contributor you want to delete.

2. Click the **trash can icon**. The contributor is removed and is deleted once the order line is saved.


#### Adding a product ID and product ID type

1. Click **Add product ID and product ID type**.

2. Enter the **Product ID** in the box.

3. Optional: Enter a **Qualifier** in the box.

4. Select the **Product ID type** from the drop-down list. The product identifier saves once the order line is saved.


#### Deleting a product ID and product ID type

1. Find the product ID you want to delete.

2. Click the **trash can icon**. The product ID is removed and is deleted once the order line is saved.


### 発注明細の詳細

*   **購入方法。** 購入の際に利用した方法。
*   **発注フォーマット。** 発注する資料の形式を選択してください。電子リソース、物理リソース、物理と電子のミックス、その他のいずれかを選択します。発注フォーマットによって、[コストの詳細](#cost-details)セクションで必須のフィールドと、[物理リソースの詳細](#physical-resource-details)または[電子リソースの詳細](#e-resources-details)セクションが表示されるかどうかが決定されます。
*   **受入日。** 資料を受け入れた日。
*   **受入スタータス。** 資料の受入状況を選択します。「保留」または「受入不要」を選択します。
*   **支払ステータス。** 資料の支払い状況を選択します。「支払い不要」または「保留」を選択します。
*   **寄贈者。** 資料の寄贈者。
*   **選択者。** 資料を選んだ人。
*   **リクエスト者。** 資料をリクエストした人。
*   **キャンセル制限。** 資料にキャンセル制限がある場合は、**キャンセル制限**のチェックボックスを選択します。
*   **至急。** 急ぎの処理が必要な場合は、**至急**のチェックボックスを選択します。
*   **コレクション。** 資料がコレクションの一部である場合は、**コレクション**のチェックボックスを選択します。
*   **Manually add pieces for receiving.** 受入のために手動でピースを追加したい場合は、**Manually add pieces for receiving** チェックボックスを選択します。このチェックボックスが選択されている場合、システムは自動的に受入アプリに資料の受入レコードを作成しません。このチェックボックスを選択した場合、受入アプリでピースを手動で作成する必要があります。
*   **キャンセルの説明。** キャンセル制限についてのノート。
*   **明細の説明。** 発注明細の説明。
*   **タグ。** ボックス内の発注に割り当てるタグを選択または入力します。

### ベンダー



*   **ベンダー参照番号。** ベンダーが発注や発注された資料を特定するために使用する参照番号。例えば、移行されたオープンな発注の場合、ベンダーからの請求書と照合するために、オリジナルの発注番号をここに保存しておくと便利でしょう。
*   **ベンダー参照タイプ。** 前のボックスで入力された参照番号の種類を選択します。エージェント固有の契約参照番号、内部で利用しているベンダー番号、図書館の継続注文番号、サプライヤーの継続注文、またはサプライヤーの固有の注文明細参照番号のいずれかを選択します。
*   **アカウント番号。** ベンダーアカウント番号。[発注](#purchase-order)セクションで選択したベンダーについて、組織レコードに1つ以上のベンダーアカウントが存在する場合、最初のアカウントがデフォルト値としてこのフィールドに表示されます。このベンダーに別のアカウント番号を使用するには、ドロップダウン リストから **アカウント番号** を選択します (該当する場合)。
*   **ベンダーへの指示。** 発注がオープンになった時にベンダーに送信する指示があれば入力します。


### 費用詳細

注）[発注明細詳細](#po-line-details)で選択した[発注フォーマット](#発注フォーマットorder-format)によって、特定のフィールドのみ編集可能になります。また、発注フォーマットによっては、一部の項目が必須となります。


*   **物理単価。** 物理的な単位の価格。[発注フォーマット](#発注フォーマットorder-format)が物理、物理/電子のミックス、その他の場合、必須です。

*   **物理数量。** 注文している資料の数。 [発注フォーマット](#発注フォーマットorder-format)が物理、物理/電子のミックス、その他の場合、必須です。
*   **通貨。** 資料の **通貨** をドロップダウンリストから選択します。デフォルト値は、主要通貨としてテナント設定に保存されています。詳細については、「設定 > テナント > 言語とローカライズ」を参照してください。
*   **追加費用。** 資料の追加コスト。
*   **電子単価。** 電子資料の価格。[発注フォーマット](#発注フォーマットorder-format)が電子、または物理/電子のミックスの場合、必須です。
*   **電子数量** 注文している電子資料の数。 [発注フォーマット](#発注フォーマットorder-format)が電子、または物理/電子のミックスの場合、必須です。

*   **割引。** 割引率または価格。
*   **タイプ。** 割引の種類を示す **%** または **$** を選択します。
*   **見積価格。** 入力された値をもとに計算された価格です。見積価格＝単価×発注数＋追加費用-割引額です。

### ファンド分配

特定のファンドに支払準備金を割り当てる場合は、このセクションにファンドの分配金を入力してください。複数のファンドに支払準備金を割り当てられます。このファンド分配は、選択されたファンドの現在の会計年度予算に適用されます

#### Adding a fund distribution

1. Click **Add fund distribution**.

2. Select the **Fund ID** from the drop-down list.

3. Select the **Expense class** from the list.

4. Enter the **Value** of the fund to be distributed.

5. Select the **%** or **$** to indicate whether the value is a percentage or price. The fund distribution saves once you save the order line.


#### Deleting a fund distribution

1. Find the fund distribution you want to delete.

2. Click the **trash can icon** next to the fund. The fund distribution is removed and is deleted once the order line is saved.


### 場所

「場所」は、資料を受け取った後の有効な場所を定義します。複数の資料を注文する場合、それぞれを異なる場所に割り当てることができます。

#### Adding a location

1. Click **Add location**.

2. Select a **Name (code)** from the drop-down list.

3. Enter a **Quantity physical** in the box.

4. Enter a **Quantity electronic** in the box.

5. Repeat as needed. The location saves once the order line is saved.


#### Deleting a location

1. Find the location you want to delete.

2. Click the **trash can icon** next to the location. The location is removed and is deleted once the order line is saved.


### Physical resource details

This section only appears if you select Physical resource or P/E mix under [Order format](#order-format).



*   **Material supplier.** The supplier of the item. The field defaults to the name of the vendor associated with the vendor code selected for the order. For more information, see [Purchase order](#purchase-order). To change the supplier, click **Organization look-up** to select an organization. In the **Select Organization** dialog, find the organization using the search box and/or filters. Click the organization to select it. The organization is added to the Material supplier field.
*   **Receipt due.** The date that receipt of the material is due, or the date by which the material should be received.
*   **Expected receipt date.** The date the material is expected to be received. This date could fall before or after the Receipt due date.
*   **Create inventory.** Select the types of records you want to create in the Inventory app once the order is opened: Instance, holdings, items; Instance; Instance, holdings; None.  For information on configuring the default setting for this field, see [Settings > Orders > Inventory interactions](../Settings/Settings_orders.md#settings--orders--inventory-interactions").
*   **Material type.** The type of material.
*   **Volume.** A number to identify the specific volume being ordered within a series, set or collection.


### 電子リソース詳細

この項目は、[発注形式](#order-format)で電子リソースまたは物理/電子ミックスを選択した場合のみ表示されます。

*   **アクセスプロバイダー。**  電子リソースの提供元です。プロバイダーを変更するには、**組織検索**をクリックして、ベンダーを選択します。**組織の選択**ダイアログで、検索ボックスおよび/またはフィルターを使用して組織を見つけます。クリックして組織を選択します。組織は、アクセスプロバイダーフィールドに追加されます。
*   **アクティベーション ステータス。** 電子リソースがアクティベートされている場合は、 **アクティベーション ステータス**チェックボックスを選択します。
*   **アクティベーション期限。** アクティベーションの期限日。注：ベンダーレコードのベンダー情報セクションの「予定アクティベーション間隔」フィールドに間隔を入力した場合、間隔として入力した日数に基づいてアクティベーション期限が設定されます。たとえば、間隔を 365 に設定した場合、アクティベーション期限フィールドには、発注明細が作成された日から 1 年後の日付が入力されます。
*   **所蔵の作成。** 発注がオープンになった時点で、所蔵アプリに作成したいレコードの種類を選択します。[発注フォーマット](#発注フォーマットorder-format)に基づいて、このフィールドのデフォルト設定を構成する方法については、[設定 > 注文 > 所蔵とのインタラクション](../Settings/Settings_orders.md#settings--orders--inventory-interactions)をご覧ください。
*   **資料種別（Material Type）。** 資料のタイプ。
*   **トライアル。** 電子資料がトライアルの一部である場合は、**トライアル** チェックボックスを選択します。
*   **アクティベーション予定日。** アクティベーションの予定日。
*   **ユーザー数上限。** 電子リソースを一度に利用できるユーザー数。
*   **URL。** 電子リソースへのリンク。


#### 巻の追加

巻を追加するには、**巻を追加**をクリックし、巻番号を入力します。巻は、発注明細が保存された時点で保存されます。

#### 巻の削除

巻を削除するには、削除したい巻を探し、**ゴミ箱**のアイコンをクリックします。巻が削除され、発注明細が保存されると削除されます。

### その他のリソース詳細

この項目は、[発注形式](#order-format)で「その他」を選択した場合のみ表示されます。


*   **資料サプライヤー（Material Supplier）。** 資料の供給者です。初期値は、発注時に選択されたベンダーです。サプライヤーを変更するには、**組織検索**をクリックして、ベンダーを選択します。**組織の選択**ダイアログでは、検索ボックスおよび/またはフィルタを使用して、組織を見つける。それを選択する組織をクリックします。選択した組織が、資料サプライヤーフィールドに追加されます。
*   **受入期限。** 受け入れの期限日。
*   **受入予定日。** 資料の受入予定日。
*   **所蔵の作成。** 発注がオープンになった時点で、所蔵アプリに作成したいレコードの種類を選択します。[発注フォーマット](#発注フォーマットorder-format)に基づいて、このフィールドのデフォルト設定を構成する方法については、[設定 > 注文 > 所蔵とのインタラクション](../Settings/Settings_orders.md#settings--orders--inventory-interactions)をご覧ください。
*   **資料種別（Material Type）。** 資料のタイプ。


## 発注明細の検索

「検索とフィルター」ペインでは、発注明細を検索することができます。初期設定では、発注明細が選択されています。発注明細を検索するには、ボックスに検索語を入力します。「キーワード」ドロップダウンリストを選択し、以下のフィールドのいずれかを検索します。

*   **キーワード。** ドロップダウン・リストのすべてのフィールドを検索します。これはデフォルトの検索です。
*   **寄与者。** 資料の寄与者。
*   **発注明細番号。**　発注明細の番号。
*   **リクエスト者。** 資料のリクエスト者。
*   **タイトルまたはパッケージ名。** 資料のタイトルまたはパッケージ名。
*   **出版者。**　資料の出版者。
*   **ベンダーアカウント。** 図書館が資料の購入に使用しているベンダーアカウント。
*   **ベンダー参照番号。** ベンダーの参照番号。
*   **寄贈者。** 資料の寄贈者。
*   **選択者。** 資料の選択者。
*   **巻。** 資料の巻数。
*   **製品ID。** 資料の製品ID。
*   **製品ID ISBN。** 資料のISBN。

また、**検索とフィルター** ペインで任意のフィルターを選択することで、発注明細を検索することができます。さらに、検索を行った後にフィルターを適用して、検索結果を制限することもできます。詳しくは、以下のセクションをご覧ください。

### 受入ステータス

**検索とフィルター**ペインで、**受入ステータス**をクリックし、該当するフィルターを選択します。

*   **受入待ち。** 受入を待っている発注明細。
*   **キャンセル済。** キャンセルされた発注明細。
*   **すべて受入完了（Fully received）。** すべての受入が完了した発注明細。
*   **一部受入完了（Partially received）。** 一部の受入が完了した発注明細。
*   **保留（Pending）。** 保留になっている発注明細。
*   **受入不要。** 受入が不要な発注明細。


### 支払いステータス

**検索とフィルター**ペインで、**支払いステータス**をクリックし、該当するフィルターを選択します。

*   **支払い待ち。** 支払いを待っている発注明細。
*   **キャンセル済。** キャンセル済みの支払がある発注明細。
*   **すべて支払済。** すべて支払済みの発注明細。
*   **一部支払済** 一部が支払済みの発注明細。注：発注明細に紐づけられた1つ以上の請求書が「承認」されると、その発注明細の支払状況は「一部支払済」に変更されます。 詳しくは、[請求書 > 請求書の承認](./Invoices.md#請求書の承認)を参照してください。
*   **支払不要。** 支払いが必要ない発注明細。
*   **保留（Pending）。** 保留になっている支払がある発注明細。


### 購入方法（Acquisition method）

**検索とフィルター**ペインで、**購入方法**をクリックし、該当するフィルターを選択します。

*   **承認プラン（Approval plan）** 承認計画により取得した発注明細。
*   **需要駆動型購入（DDA）。** DDAにより取得した発注明細。
*   **寄託（Depository）。** 政府刊行物など、寄託制度により取得した発注明細。
*   **エビデンスに基づく購入 (EBA).** EBAにより取得した発注明細。
*   **交換（Exchange）。** 他の図書館や機関との交換で取得した発注明細。
*   **寄贈（Gift）。** 図書館に寄贈された資料の発注明細。
*   **ベンダーのシステムで購入。**　外部のベンダーシステムで購入した発注明細。 
*   **購入。** 電子メールやEDIなどの方法で購入した注文明細。
*   **テクニカル。** サービスオーダーやベンダーの処理費用など、技術的な経費の支払いを追跡するための発注明細。この値は、外部システムから移行した資料にも使用できるでしょう。

### 場所（Location）

To search for order lines in a specific permanent location, follow these steps:

1. **検索とフィルター** ペインで、click **Location**.

2. Click **Location look-up**.

3. In the **Select permanent location** dialog, select an **Institution**, **Campus**, **Library**, and **Location** using the drop-down lists.

4. Click **Save and close**. The search results appear in the Order lines pane.


### ファンドコード

特定のファンドコードを使用して発注明細を検索する場合は、以下の手順で行ってください。

1. **検索とフィルター** ペインで、**ファンドコード** をクリックします。

2. ドロップダウン・リストからファンド・コードを選択します。検索結果は、発注明細ペインに表示されます。


### 発注フォーマット（Order format）

**検索とフィルター**ペインで、**発注フォーマット**をクリックし、該当するフィルターを選択します。


*   **電子リソース。** 電子リソースを含む発注明細。
*   **物理リソース。** 物理リソースを含む発注明細。
*   **電子/物理ミックス。** 物理および電子の混合リソースを含む発注明細。
*   **その他。** 異なる種類のリソースを含む発注明細。


### 資料タイプ、電子（Material type, electronic）

電子リソース詳細セクションの電子資料タイプに基づく「発注フォーマット」が「電子リソース」または「物理/電子ミックス」である発注明細を検索するには、以下の手順で行います。

1. **検索とフィルター** ペインで、click **Material type, electronic**.

2. ドロップダウン・リストから資料タイプの種類を選択します。検索結果は、発注明細ペインに表示されます。


### Material type, physical

To search for order lines that have an Order format of Physical resource or P/E mix based on their physical material type in the physical details section, follow these steps:

1. **検索とフィルター** ペインで、click **Material type, physical**.

2. Select the material type from the drop-down list. The search results appear in the Order lines pane.


### 作成日

発注明細の作成日を基準に検索するには、以下の手順で行います。

1. **検索とフィルター** ペインで、 **作成日** をクリック。

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### ベンダー

To search for order lines from a specific vendor, follow these steps:

1. **検索とフィルター** ペインで、click **Vendor**.

2. Click **Organization look-up**.

3. In the **Select Organization** dialog, search for the vendor.

4. Select the vendor you want to filter by. The vendor filter is applied.


### タグ

To search for order lines assigned specific tags, follow these steps:

1. **検索とフィルター** ペインで、**タグ** をクリック。

2. Select the tag(s) from the drop-down list. The search results appear in the Order lines pane.


### ソース

**検索とフィルター** ペインで、**ソース** をクリックし、該当するフィルターを選択します：



*   **ユーザー。** FOLIOユーザーによって作成された発注明細。
*   **API。** Application Programming Interfaceによって作成された発注明細。
*   **EDI・** Electronic Data Interchangeによって作成された発注明細。
*   **MARC。** MAchine-Readable Cataloging形式のレコードインポートで取り込んだ発注明細。


### コレクション

**検索とフィルター** ペインで、**コレクション** をクリックし、該当するフィルターを選択します：



*   **Yes.** コレクションの一部である発注明細。
*   **No.** コレクションの一部ではない発注明細。


### 至急

**検索とフィルター** ペインで、**Order format** をクリックし、該当するフィルターを選択します：



*   **Yes.** 急ぎで処理をするフラグが立っている発注明細。
*   **No.** 急ぎの処理の必要が無い発注明細。


### アクセスプロバイダー

To search for order lines from a specific access provider, follow these steps:

1. **検索とフィルター** ペインで、**Access provider** をクリックします。

2. Click **Organization look-up**.

3. In the **Select Organization** dialog, search for the vendor.

4. Select the vendor you want to filter by. The search results appear in the Order lines pane.


### アクティベート済

**検索とフィルター** ペインで、**Activated** をクリックし、該当するフィルターを選択します：



*   **Yes.** Order lines that are activated.
*   **No.** Order lines that are not activated.


### アクティベーション予定日

To search for order lines based on their expected activation date, follow these steps:

1. **検索とフィルター** ペインで、click **Expected activation**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### トライアル

発注フォーマットが電子リソースまたは物理/電子ミックスで、「電子リソース詳細」に「トライアルリソース」のフラグが立っている発注明細を検索します。

**検索とフィルター** ペインで、click **Trial** and select any applicable filters:



*   **Yes.** Order lines for resources that are being evaluated on a trial basis.
*   **No.** Order lines for resources that are not trials.


### 契約開始日

To search for order lines based on their subscription from date, follow these steps:

1. **検索とフィルター** ペインで、click **Subscription from**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### 契約終了日

発注明細を契約期間の終了日に基づいて検索するには、次の手順に従います：

1. **検索とフィルター** ペインで、**Subscription to** をクリック。

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### 実際の受入日

発注明細を実際の受入日（発注明細が完全に受入された日）に基づいて検索するには、次の手順に従います：

1. **検索とフィルター** ペインで、**Actual receipt date** をクリック。

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### 受入予定日

To search for order lines based on their expected receipt date, follow these steps:

1. **検索とフィルター** ペインで、click **Subscription to**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


### 受入期限

To search for order lines based on their receipt due date, follow these steps:

1. **検索とフィルター** ペインで、click **Subscription to**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. **適用**をクリックします。検索結果は、発注明細ペインに表示されます。


## 発注明細詳細の表示

発注明細を検索すると、発注明細ペインに以下の情報が表示されます。


*   **発注明細番号。** 発注明細番号。
*   **更新日。** 発注明細が最後に更新された日付。
*   **タイトルもしくはパッケージ名。** 資料のタイトルもしくはパッケージ名。
*   **製品ID。** 資料の製品ID。
*   **ベンダー参照番号。** ベンダー参照番号。
*   **ファンドコード。** 資料の購入時に使用されるファンドコード。
*   **発注ステータス。** 発注のステータス。


検索結果で、発注明細をクリックして表示します。発注明細詳細ペインに、その発注明細に関する追加情報が表示されます。発注明細が契約アプリの契約明細にリンクされている場合、リンクされた契約明細に関する情報を含む、リンクされた契約明細セクションが発注明細の詳細ペインに表示されます。 詳細は、「Agreements > PO LineをAgreement Lineに追加する」を参照してください。


## 発注明細の編集

1. [Find the order line you want to edit](#searching-for-order-lines) and select it.

2. In the **PO Line details** pane, click **Actions > Edit**.

3. Edit the order line.

4. Click **Save & close**. A confirmation message appears and the order line is updated.


## 発注明細の受入

1. [Find the order line you want to receive](#searching-for-order-lines) and select it.

2. In the **PO Line details** pane, click **Actions > Receive.** The order line opens in the Receiving app.

3. Follow the steps as outlined in the [Receiving app documentation](/Acquisitions/Receiving.md).


## 発注明細の削除

1. [Find the order line you want to delete](#searching-for-order-lines) and select it.

2. In the **PO Line details** pane, click **Actions > Delete**.

3. In the Delete order line dialog, click **Delete**. A confirmation message appears and the order line is deleted.


## 発注明細にノートを追加する

1. [Find the order line to which you want to add a note](#searching-for-order-lines) and select it.

2. In the **PO Line details** pane, under **Notes**, click **New**.

3. In the **New note** window, select the **Note type** from the drop-down list. Note types are created in the Settings app. For more information, see Settings > Notes.

4. Enter a **Note title** in the box.

5. Optional: Enter any **Details** about the note in the box.

6. Click **Save & close**. The note is saved and appears in the Notes section in the PO Line details pane.


## 発注明細にタグを追加する

1. [Find the order line you want to tag](#searching-for-order-lines) and select it.

2. In the **PO Line details** pane, click the **tag icon**.

3. In the **Tags** pane, either select a tag from the box or enter a tag.

4. Click the **X** on the Tags pane to close the pane and save the tag. The tag number updates to the number of tags applied to the order line.


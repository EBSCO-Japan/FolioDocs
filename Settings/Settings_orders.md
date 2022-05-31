| ソース | 取得日 |
| ---- | ---- |
| [Settings](https://github.com/folio-org/docs/tree/master/content/en/docs/Settings) | 2022-03-28 |

「設定」アプリの「発注」セクションでは、発注をオープンにする際に承認を必要とするかどうか、発注をクローズする理由、発注とInventoryアプリの連動方法、発注テンプレート、発注明細の行数制限、発注番号設定などを設定できます。


## Permissions

In order to interact with order settings, a user needs to be assigned the following permission:



*   **Settings (Orders): Can view and edit settings.** This permission allows you to view all of the Order settings.

Note: This is the only permission available for order settings. You can assign permissions to users in the Users app.


## 設定 > 発注 > 承認

発注をオープンにする際に承認を必要とする場合は、**発注をオープンにするには "承認が必要"**を選択してください。選択すると、保留とオープンの間にステップが追加されます。適切な権限を持つユーザーが発注を承認する必要があります。注文が承認されると、承認された日時と、承認を行った人のユーザー名が記録されます。詳しくは、[注文の承認](../Acquisitions/Orders.md#発注の承認)を参照してください。

## 設定 > 発注  > 発注をクローズする理由

発注をクローズする理由を設定する場合に使用します。FOLIOはデフォルトで発注のクローズ理由を提供しており、編集や削除はできませんが、理由を追加して図書館固有のクローズ理由を追跡することができます。


### Creating a closing purchase order reason

1. Click **New**.

2. Enter a **Reason** in the box.

3. Click **Save**. The Reason is saved.


### Editing a closing purchase order reason

1. Find the Reason you want to edit and click the **pencil icon**.

2. Edit the **Reason**.

3. Click **Save**. The Reason is saved.


### Deleting a closing purchase order reason

1. Find the Reason you want to delete and click the **delete icon**.

2. In the **Delete Reason** dialog, click **Delete**. A confirmation message appears and the Reason is deleted.


## 設定 > 発注 > 所蔵インタラクションのデフォルト

この設定を使用して、発注する資料が所蔵アプリとどのように相互作用するかを決定します。ここで選択した設定は、発注明細の資料に選択した発注形式（電子、物理、物理/電子ミックス、その他）に基づくデフォルトの相互作用を決定します。選択した相互作用は、必要に応じて、発注明細の追加または編集時に、発注明細の物理リソースまたは電子リソースの詳細セクションの所蔵作成フィールドで変更することができます。

選択可能なデフォルトの相互作用は4つあります。


*   **Instance, holding, item.** Once the order is opened, an instance, holding, and item are found or created in the Inventory app.
*   **Instance.** Once the order is opened, an instance is found or created in the Inventory app.
*   **Instance, holding.** Once the order is opened, an instance and holding are found or created in the Inventory app.
*   **None.** Nothing is found or created in the Inventory app.


## 設定 > 発注 > Instance status

Use this setting to determine the instance status that is assigned to the instances that are created through opening an order. Note: If you have not selected a default, then you may encounter problems when trying to receive an item or when you close an order.

For information on managing instance status values, see Settings > Inventory > Instances > Instance status types.


## 設定 > 発注 > Instance type

Use this setting to determine the instance resource type that is assigned to the instances that are created through opening an order. Note: If you have not selected a default, then you may encounter problems when trying to receive an item or when you close an order.

For information on managing instance type values, see Settings > Inventory > Instances > Resource types.


## 設定 > 発注 > Loan type

Use this setting to determine the loan type that is assigned to the items that are created through opening an order. Note: If you have not selected a default, then you may encounter problems when trying to receive an item or when you close an order. For information on managing loan type values, see Settings > Inventory > Loan types.


## 設定 > 発注 > 発注テンプレート

Use this setting to configure your order templates. Order templates can be used to populate consistent information that you may always fill out when ordering from a specific vendor, for example. Note: Any order templates you create are shared among all users who have permission to create orders.

Order templates contain the same fields found in order records but also include order line information, which is automatically applied to any order lines added to the order record that uses the order template.

この設定は、注文テンプレートの設定に使用します。注文テンプレートは、例えば、特定のベンダーに注文する際に常に記入するような、一貫した情報を入力するために使用できます。注：作成された注文テンプレートは、注文を作成する権限を持つすべてのユーザー間で共有されます。

注文テンプレートには、注文レコードと同じフィールドが含まれますが、注文行情報も含まれ、注文テンプレートを使用する注文レコードに追加された注文行に自動的に適用されます。

### Creating an order template

Note: Template name is the only required field.

1. Click **New**.

2. Fill in the fields. Follow the instructions under [Creating an order](../Acquisitions/Orders.md#creating-an-order) for more information.

3. Click **Save**. A confirmation message appears and the template is saved.


### Editing an order template

1. Select the order template you want to edit.

2. In the order template window, select **Actions > Edit**.

3. Edit the order template.

4. Click **Save**. A confirmation message appears and the template is updated.


### Deleting an order template

1. Select the order template you want to delete.

2. In the order template window, select **Actions > Delete.**

3. In the **Delete template** dialog, click **Delete**. A confirmation message appears and the template is deleted.


## 設定 > 発注 > Purchase order lines limit

Use this setting to limit the number of order lines that you can add to an order. If you do not want to have a limit, enter **999**. The minimum order lines limit is 1.


## 設定 > 発注 > Opening purchase orders

If you want to allow users the option to save and open a purchase order in the same step, select **Allow save and open purchase order when creating or editing a purchase order line.**


## 設定 > 発注 > Edit

If you want users to be able to edit the PO number on an order, select **User can edit.** If this option is not selected, then the PO number is locked.


## 設定 > 発注 > Prefixes

Use this setting to configure prefixes, which are used in orders. You can add prefixes to orders to provide context.


### Creating a prefix

1. Click **New**.

2. Enter a **Name** in the box.

3. Optional: Enter a **Description** in the box.

3. Click **Save**. The Prefix is saved.


### Editing a prefix

1. Find the Prefix you want to edit and click the **pencil icon**.

2. Edit the **prefix**.

3. Click **Save**. The Prefix is updated.


### Deleting a prefix

1. Find the Prefix you want to delete and click the **delete icon**.

2. In the **Delete Prefix** dialog, click **Delete**. A confirmation message appears and the Prefix is deleted.


## 設定 > 発注 > Suffixes

Use this setting to configure suffixes, which are used in orders. You can add suffixes to orders to provide context.


### Creating a suffix

1. Click **New**.

2. Enter a **Name** in the box.

3. Optional: Enter a **Description** in the box.

3. Click **Save**. The Suffix is saved.


### Editing a suffix

1. Find the Suffix you want to edit and click the **pencil icon**.

2. Edit the suffix.

3. Click **Save**. The Suffix is updated.


### Deleting a suffix

1. Find the Suffix you want to delete and click the **delete icon**.

2. In the **Delete Suffix** dialog, click **Delete**. A confirmation message appears and the Suffix is deleted.
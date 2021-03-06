| ソース | 取得日 |
| ---- | ---- |
| [Receiving](https://github.com/folio-org/docs/tree/master/content/en/docs/Acquisitions/Receiving) | 2022-03-24 |

「受入」アプリを使うと、「発注」アプリで作成した発注明細を図書館が受入たことを示すことができます。

受入アプリに関する用語の定義です。


*   **パッケージ。** 複数のタイトルの取得を表す発注です。
*   **ピース。**  受入ることが予想される受入タイトルのサブセクション。例えば、注文されたタイトルが雑誌のサブスクリプションである場合、そのタイトルの「ピース」は雑誌の第1巻となる可能性がある。
*   **受入。** 注文品が図書館に届いたことを確認すること。
*   **受入タイトル。** 発注した資料の名称。これには1つまたは複数のピースが付属している場合がある。
*   **未受入（Unreceive）。** 以前「受入済」と表示された注文が、図書館に届いていなかったことを示すこと。


## Permissions

The permissions listed below allow you to interact with the Receiving app and determine what you can or cannot do within the app. You can assign permissions to users in the Users app. If none of these permissions are assigned to a user, they are unable to see the Receiving app or any related information.



*   **Receiving: View.** This permission allows the user to view receiving information for orders.
*   **Receiving: View, edit.** This permission allows the user to receive and edit pieces that are associated with a purchase order line.
*   **Receiving: View, edit, create.** This permission allows the user to view, edit, and create piece records. Note: Users can only create pieces if the related purchase order line has the [Manually add pieces for receiving](/Acquisitions/Orders.md#po-line-details") checkbox selected.
*   **Receiving: View, edit, delete.** This permission allows the user to view, edit and delete pieces in the Receiving app.
*   **Settings (Receiving): Can view and edit settings.** This permission allows the user to manage receiving settings.


## 受入タイトルの作成

通常、ある注文は受入タイトルで構成され、1つまたは複数のピースが含まれる場合があります。例えば、雑誌を注文する場合、受入タイトルは雑誌名となり、添付されるピースには雑誌の各号が含まれます。

発注明細は、パッケージを表すためにも使用することができます。パッケージの発注明細は、1つの発注明細として発注アプリで作成されますが、複数のタイトルの取得を表すため（例えば、モノグラフの継続注文）、受入アプリで場所を特定したり、受入を行うことはできません。パッケージに含まれるタイトルを受け入れるには、受入アプリで受入用のタイトルを作成し、パッケージPOLにリンクさせる必要があります。本バージョンのFOLIOでは、受入タイトルは、InventoryアプリのインスタンスとPOLに接続する必要があります。

「新規作成」機能を使用すると、パッケージに含まれる受入タイトルを図書館で受入できるように作成することができます。また、この機能では、インスタンスと注文の関係を作成したい場合、既存のインスタンスをパッケージのPOLにリンクさせることができます。この場合、受入タイトルはその関連するPOL番号で検索可能です。



1. Click **New**.
2. In the **New title** window, in the **PO line details** section, click **POL number look-up**. 
3. In the **Select order lines** dialog, in the **Search & filter** box, enter the Package POL number.
4. Optional: Filter results using the filters in the **Select order lines** dialog.
5. Click **Search** and select the Package from the Search results. The Package POL is linked to the new title. 
6. Enter a **Title** for the item in the Package. 
7. Fill in the rest of the fields under Item details and PO line details. For more information on the fields and actions available in these sections, see the section descriptions below.
8. Click **Save & close**. A confirmation message appears, and the new receiving title is created and appears in the Receiving pane. It can now be edited, expected pieces can be added to it, and it can be received. You can locate the title by searching for the PO or POL number, the Package Name, or the Title(s) within it. 


### Item details


*   **タイトル。** 受入資料のタイトルです。注：パッケージ以外のPOLの場合、受入タイトルは自動的に作成されます。パッケージ POL の場合は、ルックアップを使用してインベントリインスタンスをパッケージ POL にリンクし、受入タイトルを正常に追加します。
*   **出版者。** 資料の出版者。
*   **出版日。** 資料の出版日。
*   **版。** 資料の版。
*   **サブスクリプション開始日。** サブスクリプションの開始日（該当する場合）。
*   **サブスクリプション終了日。** サブスクリプションの終了日（該当する場合）。
*   **サブスクリプション間隔（interval）。** サブスクリプションの継続日数（該当する場合）。
*   **寄与者。** 資料の寄与者。
*   **製品ID。** ISBNやDOIなどの識別番号。


#### 寄与者の追加

Note: Adding a contributor is optional, but if you click **Add contributor**, you must enter an **Contributor** and **Contributor ID type** or delete the contributor in order to save the title.



1. Click **Add contributor**.
2. Enter the **Contributor**.
3. Select a **Contributor ID type** from the drop-down list. The Contributor is added once all changes are saved.


##### Deleting a contributor



1. Find the contributor you want to delete.
2. Click the **trash can icon**. The contributor is removed and is deleted once the changes are saved.


##### Adding a product ID and type

Note: Adding a product ID and type is optional, but if you click **Add product ID and type**, you must enter a **Product ID** and **Product ID type** or delete the product ID and type in order to save the title.



1. Click **Add product ID and type**.
2. Enter the **Product ID**.
3. Optional: Enter a **Qualifier**. For example, you may want to add _paperback_ as a Qualifier for an ISBN.
4. Select the **Product ID type** from the drop-down list. The product ID is added once all changes are saved.


##### Deleting a product ID and type



1. Find the product ID you want to delete.
2. Click the **trash can icon**. The product ID is removed and is deleted once the changes are saved.


#### PO line details



*   **POL number.** The purchase order line number. This can only be populated by using the **POL number look-up**. See [Creating a receiving title](#creating-a-receiving-title) for more information.
*   **Expected receipt date.** The date the material is expected to be received. This is automatically populated with information from Orders and cannot be modified.
*   **Receiving note.** Notes about receiving the material. This is automatically populated with information from Orders and cannot be modified. 
*   **Must acknowledge receiving note.** When this checkbox is selected, the **Receiving note** dialog appears when you attempt to receive the material. You must click **Continue** in order to receive the material.


### Linking an existing receiving title



1. Click **New**. 
2. In the **New title** window, click **Title look-up**.
3. In the **Select instance** dialog, in the **Search & filter** box, enter the title you want to link to the package.
4. Optional: Filter the results using the filters in the **Select instance** dialog.
5. Click **Search** and select the Title from the search results. This populates all of the fields that have already been filled out for the existing title.
6. Fill in the rest of the fields under **Item details**. See [Item details](#item-details) above for more information.
7. Click **POL number look-up**. 
8. In the **Select order lines** dialog, in the **Search & filter** box, enter the Package POL number. 
9. Optional: Filter the results using the filters in the **Select order lines** dialog.
10. Click **Search** and select the Package from the search results. 
11. Click **Save & close**. The existing title is now linked to the Package POL. It can be located by searching for its Title, original POL number, Package POL number, or Package name.


## Searching for a receiving title

You can search for orders in the **Search & filter** pane. To search for orders, enter your search terms into the box. Select the **Keyword** drop-down list to search through one of the following fields:



*   **Keyword.** Searches through all fields in the drop-down list. This is the default search.
*   **Title.** Title of the ordered material.
*   **Package.** The name of the package to which a receiving title is attached.
*   **Product ID.** Identifying number, typically assigned in Orders when the order was created.
*   **PO number.** The purchase order number.
*   **POL number.** The purchase order line number.

You can also search for orders by selecting any of the filters in the **Search & filter** pane. Additionally, you can apply the filters after you perform a search to limit your results. See the sections below for more information.


### Order status

In the **Search & filter** pane, click **Order status** and select any applicable filters:



*   **Closed.** Orders that are closed.
*   **Open.** Orders that are open.
*   **Pending.** Orders that are pending.

Only open orders can be received.


### Vendor

To search for orders from a specific vendor, follow these steps:



1. In the **Search & filter** pane, click **Vendor**.
2. Click **Organization look-up**.
3. In the **Select Organization** dialog, search for the vendor.
4. Select the vendor you want to filter by. The search results appear in the Receiving pane.


### Order type

In the **Search & filter** pane, click **Order type** and select any applicable filters:
 


*   **One-time.** One-time orders that are received within the year.
*   **Ongoing.** Ongoing orders that span multiple years.


### Material type

To search for orders of a specific material type, follow these steps:



1. In the **Search & filter** pane, click **Material type**.
2. Select the material type from the drop-down list. The search results appear in the Receiving pane. 


### Order format

In the **Search & filter** pane, click **Order format** and select any applicable filters:



*   **Electronic Resource.** Order lines containing an electronic resource.
*   **Physical Resource.** Order lines containing a physical resource.
*   **P/E Mix.** Order lines containing a physical and electronic mixed resource.
*   **Other.** Order lines containing a different type of resource.


### Tags

To search for orders assigned specific tags, follow these steps:



1. In the **Search & filter** pane, click **Tags**.
2. Select the tag(s) from the drop-down list. The search results appear in the Receiving pane.


### Location

To search for orders assigned to a specific permanent location, follow these steps:



1. In the **Search & filter** pane, click **Location**.
2. Click **Location look-up**.
3. In the **Select permanent location** dialog, select an **Institution**, **Campus**, **Library**, and **Location** using the drop-down lists.
4. Click **Save and close**. The search results appear in the Receiving pane.


### Receiving status

In the **Search & filter** pane, click **Receiving status** and select any applicable filters:



*   **Expected.** The order is expected to arrive.
*   **Received.** The order has arrived and been received. 


### Acquisition units

To search for orders assigned to a specific acquisition unit, follow these steps:



1. In the **Search & filter** pane, click **Acquisition units**.
2. Select the acquisition unit(s) from the drop-down list. The search results appear in the Receiving pane. 

To clear all filters, go to the **Search & filter** pane and click **Reset all**.


## Viewing receiving titles details

Receiving title details can be viewed by any user with the [Receiving: View permission](#permissions). 


### Search results

Once you search for a receiving title, the following information appears in the Receiving pane:



*   **Title.** The title of the material to be received.
*   **Expected receipt date.** The date the material is expected to be received.
*   **Package.** The name of the package the receiving title is associated with (if applicable).
*   **POL number.** The purchase order line number.
*   **Receiving note.** Notes about receiving the material.
*   **Locations.** The location(s) to which the order is assigned.
*   **Order status.** The status of the order, either open, closed, or pending.

In the search results, click on a receiving title to view it. The receiving title pane displays with additional information about the title.


### Title information

This section displays the material details defined under [Creating a receiving title](#creating-a-receiving-title). 


### POL details

This section displays the details of the purchase order lines.



*   **POL number.** The purchase order line number.
*   **Expected receipt date.** The date the piece is expected to be received.
*   **Receiving note.** Notes about receiving the material.
*   **Order type.** The type of order, either one-time or ongoing.
*   **Vendor.** The institution from which the material was purchased. 
*   **Material supplier.** The supplier of the material.


### Expected

This section displays the pieces of the order that are still expected to be received. See [Adding an expected piece](#adding-an-expected-piece) for more information.


### Received

This section displays the pieces of the order that have been received. See [Receiving an order](#receiving-an-order) for more information.


## Editing receiving title information



1. Find the receiving title you want to edit and select it.
2. In the receiving title pane, click **Edit**.
3. In the receiving title window, you can modify [Item details](#item-details) and [PO line details](#po-line-details). Note: The **Title look-up** and **POL number look-up** functions are different in editing mode. See details below.
4. Fill out the desired fields.
5. Click **Save & close.** A confirmation message appears and the receiving title is updated.


### Title look-up

The **Title look-up** function replaces the current title with a title that already exists as an instance in Inventory. This doesn't replace existing publishing or subscription details, but it does add any contributors or product IDs associated with the new title. Once you make this change, the material is longer be searchable by the original title.



1. Click **Title look-up**. 
2. In the **Select instance** dialog, in the **Search & filter** box, enter part or all of the title.
3. Optional: Filter your results using the filters in the **Select instance** dialog.
4. Click **Search** and select the title from your search results. The title updates once all changes are saved.


### POL number look-up

The **POL number look-up** function replaces the current POL number with a POL number that already exists in Inventory. This doesn't replace any item details, only the POL number. Once you make this change, the material is no longer be searchable by the original POL number.



1. Click **POL number look-up**.
2. In the **Select order lines** dialog, in the **Search & filter** box, enter the POL number.
3. Optional: Filter your results using the filters in the **Select order lines** dialog.
4. Click **Search** and select the POL number from your search results. The POL number updates once all changes are saved.


## Adding an expected piece

An expected piece is a part of an order you expect to receive. For example, if you order a magazine subscription, you might expect to receive 12 different pieces during the year. If you order a book that comes with supplemental materials such as a CD or map, you might expect to receive multiple pieces with the order. The order does not initially display each piece that comes with it. Adding expected pieces to an order allows you to track which pieces of the order have been received and which are still expected. 

Expected pieces can be found under the Expected section of an order. Expected pieces can also be received from this section. See [Quick receive](#quick-receive) for more information.

Note: To add an expected piece to an order, the **Manually add pieces for receiving** checkbox must have been selected in the [Order line](./Orders.md#po-line-details) when the order was created.



1. Find the receiving title to which you want to add a piece and select it.
2. In the **Expected** section, click **Add piece**.
3. In the **Add piece** dialog, fill out desired fields. See below for more information.
4. Click **Save & close**. The new piece is displayed under the Expected section.


### Add piece fields



*   **Caption.** Enter a caption for the piece. 
*   **Expected receipt date.** The date the piece is expected to be received.
*   **Select location.** This field is populated with the location selected in Orders. You can change the location by clicking [Assign a different location](#assign-a-different-location). 
*   **Piece format.** This field is populated with the format selected in Orders. It can not be modified. 
*   **Comment.** Enter any comments about the piece.
*   **Create item.** Selecting the **Create item** checkbox connects the new piece to an instance in Inventory. This option is not available for electronic resources. Note: In order to create an item, an [instance status](/Settings/Settings_orders.md#settings--orders--instance-status), [instance type](../Settings/Settings_orders.md#settings--orders--instance-type), and [loan type](../Settings/Settings_orders.md#settings--orders--loan-type) must be selected in Settings.
*   **Supplement.** Selecting the **Supplement** checkbox indicates that the piece is a supplementary material such as a CD or a map. 


#### Assign a different location

Note: When the system is told to create a holding, a holding is created for the chosen location. If the location is changed for a specific piece and no holding exists for that location already, a new holding is created.



1. In the **Add piece** dialog, click **Assign a different location**. 
2. In the **Select permanent location** dialog, select an **Institution**, **Campus**, **Library**, and **Location**.
3. Click **Save and close**. The changes appear in the **Select location** field of the **Add piece** dialog. The location is confirmed once the piece is saved. 


## Editing an expected or received piece

To edit an expected or received piece, make sure the correct receiving title is displayed by using the **Search & filter** pane and look under the Expected and Received sections of the title.


### Editing an expected piece



1. Select the piece you want to edit.
2. In the **Edit piece** dialog, the same fields as the [Add piece](#adding-an-expected-piece) dialog appear. See above for more information.
3. Fill out the desired fields.
4. Click **Save & close.** A confirmation message appears and the piece is updated.


### Editing a received piece



1. Select the piece you want to edit. 
2. In the **Edit piece** dialog, the same fields as the **Add piece** dialog appear. See above for more information. Note: You cannot make changes to **Location**, **Piece format**, or **Create item** when editing a received piece. If the **Create item** checkbox was selected, it says **Connected** in place of **Create item**. If the checkbox was cleared, it still displays the **Create item** box, but the checkbox will be grayed out.
3. Fill out the desired fields.
4. Click **Save & close**. A confirmation message appears and the piece is updated.


## Receiving an order

Receiving an order confirms that it has arrived at the library.

There are two ways to receive an order:



*   Quick Receive
*   Receive


### Quick receive

Quick receive can be used when you want to receive one piece of an order at a time.



1. Using the **Search & filter** pane, find the receiving title from which you want to receive pieces and select it.
2. In the Expected section of the order, click on the piece you want to receive. 
3. In the **Edit piece** dialog, make any necessary edits to the piece.
4. Click **Quick receive**. The piece is now displayed under the Received section. 


### Receive

The Receive function can be used to receive multiple pieces at once. 



1. Using the **Search & filter** pane, find the receiving title you want to receive and select it.
2. In the Expected section of the receiving title, click **Receive**.
3. In the receiving title window, all of the expected pieces are displayed. Here, you can make changes to the pieces. See below for more information.
4. Select the checkbox beside each piece you want to receive. Note: If you want to receive all of the pieces, click the top checkbox.
5. Click **Receive**. The selected pieces are now displayed under the Received section.


#### Receive fields



*   **Caption.** Create or change the caption of the piece. 
*   **Barcode.** Create a barcode for the piece. You can only add a barcode if the piece is already **Connected** to an instance in Inventory, or if the **Create item** checkbox is selected.
*   **Piece format.** This field is populated by the format selected in Orders. It can not be modified. 
*   **Request.** This field is populated with information from Requests. If there is a request open for the piece, this field says “Yes”. 
*   **Comment.** Enter any comments about the piece.
*   **Select location.** This field is populated with the location selected in Orders. You can change the location by clicking [Assign a different location](#assign-a-different-location).
*   **Item status.** This field is populated with the information that will appear in Inventory if the item is received. 
*   **Call number.** Enter the call number for the piece. You can only add a call number if the piece is already **Connected** to an instance in Inventory, or if the **Create item** checkbox is selected.
*   **Create item.** Selecting the **Create item** checkbox links the new piece to an instance in Inventory. This option is not available for electronic resources. Note: In order to create an item, a loan type must be selected in Settings.


## Unreceiving an order



1. In the Received section of the receiving title, click **Unreceive**.
2. In the receiving title window, all of the received pieces are displayed. 
3. Optional: Make changes to the **Comment** field.
4. Select the checkbox beside each piece you want to unreceive. Note: If you want to unreceive all of the received pieces, select the top checkbox.
5. Click **Unreceive**. The selected pieces are now displayed under the Expected section. 

You can also get to the Receiving app from the action menu of an open order by clicking **Receive**.

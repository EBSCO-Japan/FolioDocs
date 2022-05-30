# 設定 > 収集ユニット（Acquisition units）

設定アプリの「収集ユニット」では、収集ユニットの設定や、作成したユニットへのユーザーの割り当てを行うことができます。

収集ユニットとは、収集のレコード（acquisition records）に追加できるレイヤーで、そのユニットに割り当てられていない限り、ユーザーがそれらのレコードとやり取りする能力を制限するものです。収集（Acquisition）のパーミッションは、ユーザーが特定のアプリ内でそのアプリ内の任意のレコードに対して特定のアクションを実行することを許可しますが、収集ユニットはさらに、個々のレコードのみにユーザーのアクセスを制限することができます。

例えば、法学部図書館、医学部図書館、学部図書館など、複数の独立した図書館でFOLIOを共有している大学では、図書館ごとに個別の取得単位を設定し、各図書館のスタッフを適切な単位に割り当てることができます。取得単位が同じ注文、組織、請求書、資金については、割り当てられた取得単位内のスタッフのみが許可されたアクションを取ることができます。法律図書館のユーザーが財務アプリ内でレコードを作成および削除する権限を持っていたとしても、医療センター図書館の収集ユニットに割り当てられていなければ、医療センター図書館のファンドを作成または削除することが制限されます。

取得単位は、FOLIO の以下の種類のレコードに適用することができます。

* 会計年度
* 元帳
* グループ
* 資金
* 請求書
* 注文
* 組織

注：「財務」と「受入」アプリでは、収集ユニットによるユーザーの作業の制限は完全には機能しません。しかし、これらのアプリ内のレコードに収集ユニットを追加することは可能です。

## Creating an acquisition unit

1. In the **Acquisition units** pane, click **New**.

2. Enter the **Name** of the unit in the box.

3. Select the types of actions members in the unit can perform:



*   **View.** Users assigned to the unit are the only ones who can view records that have the unit assigned. If you want to allow all users to view the records that have this unit assigned, do not select this checkbox. 
*   **Edit.** Users assigned to the unit are the only ones who can edit records that have the unit assigned.
*   **Create.** Users assigned to the unit are the only ones who can add the unit to a record they are creating.
*   **Delete.** Users assigned to the unit are the only ones who can delete records that have the unit assigned.

4. Click **Save**. The unit is saved and appears in the Acquisition units pane.


## Assigning users to an acquisition unit

Note: Users can be assigned to more than one acquisition unit.

1. In the **Acquisition units** pane, find the acquisition unit you want to assign the user to and select it.

2. In the **Acquisition unit detail** pane, click **Assigned users > Assign users**.

3. In the **Select User** dialog, in the **User search** box, enter part or all of the user’s name.

4. Optional: Filter results by Status (Inactive/Active), or by Patron group.

5. Click **Search**.

6. Select the **checkbox** in the row of the users(s) you want to add to the unit and click **Save**. The Select User dialog closes and the user appears in the Assigned users section.


## Deleting a user from an acquisition unit

1. In the **Acquisition units** pane, find the acquisition unit you want to delete the user from and select it.

2. In the **Acquisition unit detail** pane, click **Assigned users > Assign users**.

3. Find the user you want to delete and click the **trash can icon** at the end of their row. The user is removed from the list and deleted from the unit.


## Editing an acquisition unit

1. In the **Acquisition units** pane, find the acquisition unit you want to edit and select it.

2. In the **Acquisition unit detail** pane, click **Actions > Edit**.

3. Edit the acquisition unit.

4. Click **Save**. The acquisition unit is updated.


## Deleting an acquisition unit

Note: You cannot delete acquisition units that have users assigned to them.

1. In the **Acquisition units** pane, find the acquisition unit you want to delete and select it.

2. In the **Acquisition unit detail** pane, click **Actions > Delete**.

3. In the **Delete acquisition unit** dialog, click **Confirm**. The acquisition unit is deleted and is removed from the Acquisition units pane.
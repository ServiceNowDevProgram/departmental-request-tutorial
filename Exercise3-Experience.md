## Exercise 3 - Create the Experiences

In this exercise you'll create a workspace and catalog experience for the application.

### Create a Workspace Experience

A workspace gives your fulfillers and approvers a way to interact with your application.

1. Go back to your App Home screen.

1. Click **+Add** next to experience.

    ![add experience](images/2021-10-06-14-33-16.png)

1. Choose **Workspace**.

    ![choose workspace](images/2021-10-06-14-33-41.png)

1. Click **Begin** in the modal that comes up.

1. Leave the form the way it is and click **Continue**.

1. The data screen should have the following values:

    * Primary Table: **Request**
    * Secondary Tables: **Type**

    ![data screen](images/2021-10-06-14-34-26.png)

1. Click **Done**.

### Create a Catalog Item

A catalog item will allow your requesters to open a request from your portal via an easy to use form.

1. Click **+Add** next to experience.

1. Choose **Catalog item**.

1. Click **Begin** in the modal that comes up to open Catalog Builder.

1. In the form that comes up enter:

    * Name: **Departmental Request**
    * Description: **Submit a departmental request**

    ![experience screen](images/2021-10-06-14-36-18.png)

1. Choose **Edit catalog item**.

1. The name and description should be shown on this screen. In the item details section, enter this _Description_:

    **Fill out the type of request and details about the request. Upon approval and fulfillment you will receive an email.**

1. Click **Continue to Destination** at the bottom right.

    ![continue to destination](images/2021-10-06-14-37-08.png)

1. Enter your request table as the _Record submission table_.

    ![record submission table](images/2021-10-06-14-38-03.png)

1. Click **Continue to Location**.

1. Now you'll need to choose where this catalog item will live. Click **Browse** under _Catalogs_.

1. Choose the **Service Catalog** and use the \> to move it to the right bucket.

    ![](images/2021-10-06-14-38-46.png)

1. Click **Save selections**.

1. Click **Browse** under _Categories_.

1. Choose the **Can we help you?** and use the \> to move it to the right bucket.

    ![](images/2021-10-06-14-39-14.png)

1. Click **Save selections**.

1. Click **Continue to Questions**.

1. Choose **Insert new question**.

    ![](images/2021-10-06-14-39-39.png)

1. Fill out the question form as follows:

    * Question type: **Choice**
    * Question subtype: **Record reference**

    ![](images/2021-10-06-14-41-21.png)

    * Map to a specific field on the table: **true** (checked)
    * Table field: **Type**
    * Question label: **Choose the type of request**
    * Mandatory: **true**

    ![](images/2021-10-06-14-40-53.png)

1. Click **Continue to Additional details**.

1. Set the _Source table_ to your **Type** table.

    ![](images/2021-10-06-14-44-11.png)

1. Click the **Insert Question** button at the bottom right of your screen under _Question Preview_.

    ![](images/2021-10-06-14-45-20.png)

1. Click the **Insert new question** button to insert another question.

1. Fill out the question form as follows:

    * Question type: **Test**
    * Question subtype: **Multi-line**

    ![](images/2021-10-06-14-45-54.png)

    * Map to a specific field on the table: **true** (checked)
    * Table field: **Description**
    * Question label: **Describe your request in as much detail as possible**
    * Mandatory: **true**

    ![](images/2021-10-06-14-47-13.png)

1. Click the **Insert Question** button at the bottom right of your screen under _Question Preview_.

1. Click **Continue to Settings**.

1. Click **Continue to Access**.

1. Click **Continue to Review and Submit**.

1. This shows you a full view of everything you've filled out. Click the **Submit** button at the top of this form to make this catalog item available.

    ![](images/2021-10-06-14-59-01.png)

1. Click **Return to my application**.

[Proceed to Exercise 4 - Add automation](Exercise4-Automation.md)
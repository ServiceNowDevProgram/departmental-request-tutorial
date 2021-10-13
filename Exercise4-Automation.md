## Exercise 4 - Add automation

In this exercise, you will use flow designer to add an approval and emails to your application.

### Create an Approval Flow

1. Click **+Add** next to _Logic and automation_.

    ![logic and automation](images/2021-10-06-15-08-02.png)

1. Select **Build from scratch**.

    ![scratch or template flow](images/2021-10-06-15-08-19.png)

1. Name your flow **Request Approval**, add a description, and click **Continue**.

    ![flow configuration](images/2021-10-06-15-09-15.png)

1. Choose **Edit this flow** to open the new flow in _Flow Designer_.

    ![flow is ready screen](images/2021-10-06-15-10-01.png)

1. Click **Add a trigger** in the _Trigger_ section of the flow canvas.

1. In the box that comes up choose **Created** under _Record_.

    ![trigger selection](images/2021-10-06-15-11-06.png)

1. Select your **Request** table as the table.

    ![table selection](images/2021-10-06-15-11-44.png)

1. Click **Add filters**.

1. Configure the _Condition_ **[Type] [is not empty]**.

    ![condition builder](images/2021-10-06-15-13-51.png)

1. Click **Done**.

1. Under _Actions_ click **+ Add an Action, Flow Logic, or Subflow**.

1. Choose **Action** and type **approval** into the search box.

1. Choose **Ask for Approval** under _Default_.

    ![ask for approval activity](images/2021-10-06-15-15-16.png)

1. Click the Data Pill Picker ![data pill picker icon](images/2021-10-06-15-16-22.png) to the right of the _Record_ field and choose **Trigger - Record Created**, then choose **Request Record**.

1. Under _Rules_ click the **-Choose approval rule** dropdown and select **Anyone approves**.

    ![configure approval](images/2021-10-06-15-17-17.png)

1. To the right of the empty field that comes up, click the data pill picker icon and choose **Trigger - Record Created**. Click the right arrow next to _Request Record_, then scroll down to **Type** and click the right arrow, then choose **Approval Group**.

    **Trigger - Record Created --> Request Record --> Type --> Approval Group**

    ![set approval group](images/2021-10-06-15-17-50.png)

1. Click the **Add another OR rule set** button.

    ![add another condition](images/2021-10-06-15-18-07.png)

1. Under _OR_ click **Approve** and change it to **Reject**.

    ![reject group](images/2021-10-06-15-18-29.png)

1. Choose the **-Choose approval rule** dropdown and select **Anyone rejects**.

    ![anyone rejects](images/2021-10-06-15-18-49.png)

1. Again, to the right of the empty field that comes up, click the data pill picker icon and choose **Trigger - Record Created**. Click the right arrow next to _Request Record_, then scroll down to **Type** and click the right arrow, then choose **Approval Group**.

    **Trigger - Record Created --> Request Record --> Type --> Approval Group**

    ![set approval group](images/2021-10-06-15-19-14.png)

1. Click **Done**.

1. Under _Actions_ click **+ Add an Action, Flow Logic, or Subflow**.

1. Click **Flow Logic** and choose **If**.

    ![flow logic](images/2021-10-06-15-19-48.png)

1. Click the data pill picker icon next to the Condition 1 field that comes up.

1. Choose **1 - Ask For Approval --> Approval State**.

    ![if dot walk](images/2021-10-06-15-20-20.png)

1. In the box next to _is_ choose **Approved**.

    ![set approved](images/2021-10-06-15-20-40.png)

1. Click the Action button that popped up under the _If_ action and choose **ServiceNow Core > Update Record**.

    ![add action](images/2021-10-06-15-21-15.png)

1. Use the data pill picker next to the _Record_ field to choose **Trigger - Record Created --> Request Record**.

    ![set value](images/2021-10-06-15-21-44.png)

1. Click **+ Add field value**.

1. Choose **State** and set its value to **Work in Progress**.

1. Click **+ Add field value**.

1. Choose **Assignment group**.

1. In the Select assignment group field use the data pill picker to choose **Trigger - Record Created --> Request Record --> Type --> Fulfillment Group**.

    ![set fulfillment group](images/2021-10-06-15-23-10.png)

1. Click **Done**.

1. Click **+ Add an Action, Flow Logic, or Subflow**.

1. Click **Flow Logic** and choose **Else**.

    ![add else logic](images/2021-10-06-15-24-15.png)

1. Use the **+** icon directly below the else to add another **Update Record** action.

    ![add update record activity](images/2021-10-06-15-24-59.png)

1. Use the data pill picker to choose **Trigger - Record Created --> Request Record**.

    ![add trigger](images/2021-10-06-15-25-28.png)

1. Use the **+Add field value** button to set the _State_ field to **Closed Incomplete**.

    ![set state field](images/2021-10-06-15-25-54.png)

1. Click **Done**.

1. Click **Save** at the top of the flow.

    ![save button](images/2021-10-06-15-26-11.png)

1. Click **Activate** at the top of the flow.

    ![activate button](images/2021-10-06-15-26-31.png)

### Create a Notification Flow

In this section, you will create a flow to send an email notification when the request is closed.

1. Back at your App Home click **+Add** next to _Logic and automation_.

1. Select **Build from scratch**.

1. Name your flow **Closed notification**, add a description, and click **Continue**.

    ![configure flow](images/2021-10-06-15-27-41.png)

1. Click **Edit this flow**.

1. Click **Add a trigger**.

1. Choose **Updated** under _Record_.

    ![record updated condition](images/2021-10-06-15-28-22.png)

1. Choose your request table as the table.

    ![request table choice](images/2021-10-06-15-28-49.png)

1. Click **Add filters**.

1. Add a filter for **[State] [Changes to] [Closed Complete]**

    ![condition filter](images/2021-10-06-15-29-17.png)

1. Click **Done**.

1. Click **+ Add an Action, Flow Logic, or Subflow**.

1. Choose **Send Email** under _ServiceNow Core_.

    ![choose send email activity](images/2021-10-06-15-29-52.png)

1. Use the data pill picker next to the _Target Record_ field to choose the **Request Record**.

    ![choose the target record](images/2021-10-06-15-31-34.png)

1. Use the data pill picker next to the _To_ field to choose **Trigger - Record Updated > Request Record > Opened by**.

    ![](images/2021-10-06-15-32-03.png)

1. In the Subject type **Your request has been completed** with the request number after _Your request_. Use the data pill picker to access the number field on the request table.

    ![request record number](images/2021-10-06-15-33-13.png)

1. Add a body to your email.

    ![entire email record](images/2021-10-06-15-34-36.png)

1. Click **Done**.

1. **Save** and **Activate** the flow.

[Proceed to Exercise 5 - Add security](Exercise5-Security.md)
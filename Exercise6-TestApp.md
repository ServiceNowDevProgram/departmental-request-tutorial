## Exercise 6 - Test your app

Now it's time to test your app. For this exercise you're going to test the app as an admin user in order to reduce the amount of role and group administration.

### Set up your test data

You'll need to add the admin user to the _Marketing_ and _Marketing Approval_ groups.

1. In the platform view, go to User Administration and click **Users**.

    ![](images/2021-10-06-16-35-10.png)

1. Find the _admin_ user in the list and click on in.

    ![](images/2021-10-06-16-35-54.png)

1. In the _Groups_ related list at the bottom of the form click **Edit**.

    ![](images/2021-10-06-16-36-41.png)

1. Move the _Marketing_ and _Marketing Approval_ groups from the left side of the slushbucket to the right and click **Save**.

    ![](images/2021-10-06-16-37-11.png)

### Testing - Submit a request

In this section you'll submit a request from the service portal like any employee in your company would do.

1. Navigate to your service portal by going to https://devXXXXXX.service-now.com/sp.

1. Search _departmental request_ under _How can we help?_.

    ![](images/2021-10-06-16-38-55.png)

1. Click the _Departmental Request_ catalog item when the search results come up.

    ![](images/2021-10-06-16-57-53.png)

1. In the form that comes up choose **Miscellaneous Marketing** as the request type and add a description.

    ![](images/2021-10-06-16-58-51.png)

1. Click **Submit** on the right.

1. Make a note of the request number that comes up.

### Testing -- Approve the request

Generally, approvals happen through email or mobile, but they can also happen through the portal.

1. Click **Home** in the breadcrumbs or the ServiceNow logo on the service portal to get back to the homepage. 

1. You should see the My Approvals section on the bottom right of the portal. Click **Approve**.

    ![](images/2021-10-06-17-02-20.png)

### Testing - Fulfill the request

1. Go back to your App Engine Studio tab.

1. In your Dept Request app, choose **PREVIEW** in the _Now Experience_ line under the _Experience_ section to open the workspace you created earlier.

    ![](images/2021-10-06-17-06-26.png)

1. In the new workspace tab that comes up, click the list icon in the left bar ![](images/2021-10-06-17-06-59.png).

1. On the screen that comes up choose the record that was just created and approved. It should be in the _Work in Progress_ state.

    ![](images/2021-10-06-17-07-54.png)

1. In the form that comes up, add a work note and change the state to Closed Complete.

    ![](images/2021-10-06-17-09-13.png)

1. Click **Save** at the top right of the form.

### Testing - Closed email

Now you'll make sure that the email flow ran and sent the email when you changed the state to closed complete.

1. Go back to the platform view of your instance with the left navigator and choose System Mailboxes > Outbound > Outbox.

1. Validate that you can see the record with the subject line _Your request DEPTREQXXXXXXX has been completed_.

    ![](images/2021-10-06-17-14-36.png)
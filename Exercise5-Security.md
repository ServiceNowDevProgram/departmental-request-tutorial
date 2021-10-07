## Exercise 5 - Security

In this exercise you'll create roles and add security to your tables.

### Elevate your privelges

1. Switch back to the platform view of your instance, the view you had when you first logged in. If you've closed that tab, open another tab with url: https://devXXXXXXX.service-now.com (replace XXXXXX with your instance number).

    ![](images/2021-10-06-15-58-39.png)

1. Click **System Administrator** at the top left and choose **Elevate Roles** from the dropdown.

    ![](images/2021-10-06-15-57-41.png)

1. Click the _security_admin_ checkbox and choose **OK**.

    ![](images/2021-10-06-15-59-30.png)

### Add Security

1. Click back to your app engine studio tab and refresh the page. The security section should now be clickable.

    ![](images/2021-10-06-16-00-41.png)

1. Click the **+Add** button in the Security section.

    ![](images/2021-10-06-16-23-46.png)

1. In the screen that comes up choose **Build a new role** then click **Continue**.

    ![](images/2021-10-06-16-24-46.png)

1. Fill out the form that comes up.

    * _Name_: **Fulfiller**
    * _Description_: **Users with this role will fulfill departmental requests**

    ![](images/2021-10-06-16-26-12.png)

1. Click **Continue**.

1. In the screen that comes up give the Fulfiller role Create, Read, and Write access to the Request table and Read access to the Type table.

    ![](images/2021-10-06-16-27-29.png)

1. Click the **Experience** tab and give the fulfiller role access to the Dept Request experience.

1. Click **Continue**.

1. Click **Done** on the screen that comes up.

1. Repeat the previous steps to add a role called _Admin_ that has full access to all tables and experiences.

[Proceed to Exercise 6 - Test your app](Exercise6-TestApp.md)
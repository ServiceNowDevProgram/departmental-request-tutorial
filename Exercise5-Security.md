## Exercise 5 - Security

In this exercise, you will create roles and add security to your tables.

### Demo Video

Click the thumbnail below to launch a YouTube video of someone working through this exercise. 

<!--[![Overall app build video](https://img.youtube.com/vi/inR4UIuVjBA/0.jpg)](https://www.youtube.com/watch?v=inR4UIuVjBA)-->

<iframe id="video" width="560" height="315" src="https://www.youtube.com/embed/inR4UIuVjBA/" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>

### Elevate your privelges

1. Switch back to the platform view of your instance, which was the view with the left hand navigation you had when you first logged in. If you've closed that tab, open another tab with url: https://devXXXXXXX.service-now.com (replace XXXXXX with your instance number).

    ![instance gome](images/2021-10-06-15-58-39.png)

1. Click **System Administrator** at the top left and choose **Elevate Roles** from the dropdown.

    ![user dropdown menu](images/2021-10-06-15-57-41.png)

1. Click the _security_admin_ checkbox and choose **OK**.

    ![elevated priveleges modal](images/2021-10-06-15-59-30.png)

### Add Security

1. Click back to your app engine studio tab and refresh _App Home_ page. The security section should now be clickable.

    ![app home](images/2021-10-06-16-00-41.png)

1. Click the **+Add** button in the Security section.

    ![security section](images/2021-10-06-16-23-46.png)

1. In the screen that comes up choose **Build a new role** then click **Continue**.

    ![add security screen](images/2021-10-06-16-24-46.png)

1. Configure the new role screen.

    * _Name_: **Fulfiller**
    * _Description_: **Users with this role will fulfill departmental requests**

    ![new role configuration](images/2021-10-06-16-26-12.png)

1. Click **Continue**.

1. In the screen that comes up give the Fulfiller role Create, Read, and Write access to the Request table and Read access to the Type table.

    ![table security](images/2021-10-06-16-27-29.png)

1. Click the **Experience** tab and give the fulfiller role access to the Dept Request experience.

1. Click **Continue**.

1. Click **Done** on the screen that comes up.

1. Repeat the previous steps to add a role called _Admin_ that has full access to all tables and experiences.

[Proceed to Exercise 6 - Test your app](Exercise6-TestApp.md)
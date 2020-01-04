# Jenkins Credentials Setup

Open your Jenkins instance.

## *To View Existing Credentials:*

In the left panel you will find **Credentials** options.  

<img src="../images/Jenkins_left_panel.png" alt="Jenkins_left_panel" style="width:140px;height:250px;"/>

Click on the **Credentials** option, then you will be able to see all the available credentials configured on the Jenkins instance as below:

<!-- <img src="../images/credentials_page.png" alt="credentials_page" style="height:200px;"/> -->

![credentials_page](../images/credentials_page.png)

You can use an existing **ID** from the available credentials in the Pipeline.

## *To Modify Existing / Add Credentials:*

As you have clicked on **Credentials** option earlier you can see **System** option under it in the left panel. Once you click on the **System** option you will be shown this page:

<!-- <img src="../images/System_creds.png" alt="System_creds" style="height:100px;"/> -->

![System_creds](../images/System_creds.png)

By clicking the **Global credentials** option under **Domain** column you will redirected to the following page:

<!-- <img src="../images/global_credentials_page.png" alt="global_credentials_page" style="height:200px;"/> -->

![global_credentials_page](../images/global_credentials_page.png)

By clicking on available credentials you will be able to `update, delete or move` the existing credentials.

You can create new set of credentials to be used in pipeline by clicking on **Add Credentials** option from left panel.

<!-- <img src="../images/options_for_credentials.png" alt="options_for_credentials" style="height:150px;"/> -->

![options_for_credentials](../images/options_for_credentials.png)

You can select type of credentials you want to create as shown above.
Here, we are selecting `Username with password` type for demonstration.
But you can explore all the other available options.

<!-- <img src="../images/add_credentials.png" alt="add_credentials" style="height:200px;"/> -->

![add_credentials](../images/add_credentials.png)

Here, you can select from **`Global or System`** scope for the credentials.

Provide `Username and Password` for the credential you want to create.

Provide `ID` for the credential this will be used as unique identifier to use the specified set of credentials that it points to.

Provide `Description` for the credential you are creating.

Once you fill all the required fields, click on `OK` button to save the credentials.

Now the `ID` you have provided while creating this set of credentials or an `ID` from available credentials can be used in the Pipeline.


# Jenkins Credentails Setup

Open your Jenkins instance.

## *To View Existing Credentials:*

In the left panel you will find **Credentials** options.  

<img src="../images/Jenkins_left_panel.png" alt="Jenkins_left_panel" style="width:140px;height:250px;"/>

Click on the Credentials option, then you will be able to see all the available credentials configured on the Jenkins instance as below:

<img src="../images/credentials_page.png" alt="credentials_page" style="height:200px;"/>

You can use an existing **ID** from the available credentials in the Pipeline.

## *To Modify Existing / Add Credentials:*

Click on global option under **Domain** column of the **Credentials** section to get redirected to **Global Credentials** page.

<img src="../images/global_credentials_page.png" alt="global_credentials_page" style="height:200px;"/>

By clicking on available credentials you will be able to `update, delete or move` the existing credentials.

You can create new set of credentials to be used in pipeline by clicking on **Add credentials** option from left panel.

<img src="../images/options_for_credentials.png" alt="options_for_credentials" style="height:150px;"/>

You can select from the following type of credentials you want to create.
Here, we are selecting `Username with password` type for demonstration.
But you can explore all the other available options as well.

<img src="../images/add_credentials.png" alt="add_credentials" style="height:200px;"/>

Here, you can select from **`Global or System`** scope for the credentials.

Provide `Username and Password` for the credential you want to create.

Provide `ID` for the credential this will be used as unique identifier to use the specified set of credentials that it points to.

Provide `Description` for the credential you are creating.

Once you filled out all the required fields click on `OK` button to save the credentials.

Now the `ID` you have provided while creating this set of credentials or an `ID` from available credentials can be used in the Pipeline.


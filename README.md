ConsoleApp-GraphAPI-DiffQuery-DotNet
====================================

This console application demonstrates how to make Differential Query calls to the Graph API, allowing applications to request only changed data from Azure AD tenants.

For more information about how the protocols work in this scenario and other scenarios, see the REST API and Authentication Scenarios on http://msdn.microsoft.com/aad.

## How To Run This Sample

To run this sample you will need:
- Visual 2013
- An Internet connection
- An Azure subscription (a free trial is sufficient)

Every Azure subscription has an associated Azure Active Directory tenant.  If you don't already have an Azure subscription, you can get a free subscription by signing up at [http://wwww.windowsazure.com](http://www.windowsazure.com).  All of the Azure AD features used by this sample are available free of charge.

### Step 1:  Clone or download this repository

From your shell or command line:

`git clone git@github.com:AzureADSamples/ConsoleApp-GraphAPI-DiffQuery-DotNet.git`

### Step 2:  Run the sample in Visual Studio 2013

The sample app is preconfigured to read data from a Demonstration company (GraphDir1.onMicrosoft.com) in Azure AD. Run the sample application, and from the main page, authenticate using this demo user account: demoUser@graphDir1.onMicrosoft.com   graphDem0

### Step 3:  Running this application with your Azure Active Directory tenant

#### Register the MVC Sample app for your own tenant

1. Sign in to the [Azure management portal](https://manage.windowsazure.com).
2. Click on Active Directory in the left hand nav.
3. Click the directory tenant where you wish to register the sample application.
4. Click the Applications tab.
5. In the drawer, click Add.
6. Click "Add an application my organization is developing".
7. Enter a friendly name for the application, for example "WebApp for Azure AD", select "Web Application and/or Web API", and click next.
8. For the sign-on URL, enter the base URL for the sample, which is by default `https://localhost:44322`.
9. For the App ID URI, enter `https://<your_tenant_name>/WebAppGraphAPI`, replacing `<your_tenant_name>` with the domain name of your Azure AD tenant. For Example "https://contoso.com/WebAppGraphAPI".  Click OK to complete the registration.
10. While still in the Azure portal, click the Configure tab of your application.
11. Find the Client ID value and copy it aside, you will need this later when configuring your application.
12. In the Reply URL, add the reply URL address used to return the authorization code returned during Authorization code flow.  For example: "https://localhost:44322/".
13. Configure Permissions - under the "Permissions to other applications" section, select application "Windows Azure Active Directory" (this is the Graph API), and under the second permission (Delegated permissions), select "Access your organization's directory" and "Enable sign-on and read users' profiles". Application Permission (the 2nd column is not needed for this demo app).
<TODO List information on each type of delegated permssion>

## How To Deploy This Sample to Azure

Coming soon.

## About The Code

Coming soon.

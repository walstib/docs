---
description: Information for Dynamics 365 courses
---

# Dynamics 365

## WWL Tenant Solution - October 2020

When, as an MCT, you launch a lab for the courses listed below, the class lab key must be added to your class in order to get access to the "Admin" user for the tenant provided for all students in that class.

{% hint style="danger" %}
**Note**: You are not redeeming the key, but instead simply aligning the key to your class.
{% endhint %}

MB-210   
MB-220  
MB-230   
MB-240  
MB-901  
  
Once logged into the LMS, click on the Instructor Home icon in the top right hand corner.

![](../.gitbook/assets/image%20%2832%29.png)

If this is the first time you have used the Instructor area then you will see the following screen:

![](../.gitbook/assets/image%20%283%29.png)

This is where you need to create a class. Click **Add One**. \(If you already used the instructor area before click **+ Create**\)

Enter the access key for your class.

{% hint style="warning" %}
**Note:** You are not redeeming the key here, you are associating the key with your instructor area.
{% endhint %}

Select the date the class/course will start.  
Enter any notes you may feel useful in the future then click the confirm check box and click **Create Class**.

![](../.gitbook/assets/image%20%28123%29.png)

Your live classes will now be presented to you. Click **Start**.

You will see a tenant will be assigned to you:

![](../.gitbook/assets/image%20%28122%29.png)

Return back to the LMS.[  
](../usinglabs/shadowing-users.md)  
Launch the lab you are teaching.  Once the lab has launched, locate the class key provided by the learning partner and enter it in the lookup box and click **Lookup**

![](../.gitbook/assets/image%20%28121%29.png)

You will now be able to see the admin credentials for the tenant.

If you receive the following error then you have not created a class correctly in the Instructor area:

![](../.gitbook/assets/image%20%28124%29.png)

  
_Due to this new solution, we are unable to provide 180 day access for the labs listed above._

## Subscription / Tenant issues

If there are any issues with Dynamics Tenants, this workaround should be used.

### Task 1 - Set up a trial of Microsoft Dynamics 365

1. Open a Browser and navigate to the following URL:  [https://trials.dynamics.com](https://trials.dynamics.com)

2. Click on the **Sign up here** link. 
3. Click on the **No, continue signing up** link.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/b1577903-3994-47cb-9a82-6eb24f083232.png)

4. Complete the **Welcome Form** with your details. Keep your location as the **USA**.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/13c14147-2d63-49d8-aa0c-637fc338646b.png)

5. Create a unique user by entering **admin@GDMB{your name}.onmicrosoft.com** and **Pa55w.rd**. Make sure you make a note of the username and password you create as this will be needed later.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/d6927b49-f2b6-4eec-9349-8c150d722f33.png)

6. In the **Verification Form**, enter your mobile phone number and validate using the verification code that is sent to you. @@@warning **Note:** Microsoft will not use your mobile number for any activities other than sending a verification code. @@@

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/2ca968d5-4e5c-4b57-a702-ec8fdf2f3b86.png)

7. When prompted, click the **Set Up** button.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/3299ca65-1d0e-4f3a-803e-b18ddb00e5cb.png)

8. When prompted, select **All of these - Show me everything!**

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/3f68a4e2-7ddb-459e-b63a-e88d32a4bf34.png)

9. Click the **Complete Set Up** button.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/0b36c725-72e3-4909-86f9-02831e81ea11.png)

10. Once setup has completed, close down your browser \(please close the browser even if you get a 'We are having trouble signing you in message'\)

### Task 2 - Sign in to Microsoft Dynamics 365

1. Open the browser and navigate to the following URL:

   ```text
   https://portal.office.com/
   ```

2. When prompted, sign in with the username and password you created above.
3. Close any Office 365 dialogs or popups that appear.
4. Click the **Dynamics 365 logo** button.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/ba1de471-44f9-411f-8653-d453ae42f1b8.png)

5. Click the **Dynamics 365 - custom App** to use for this course.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/9a48e7d6-0a92-4f40-bc70-d1e1fe776a08.png)

6. For Dynamics Sales courses select the **Sales Hub** app.

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/MB-900T01/All-Modules/cea048d0-9b8c-414c-b391-bef8db401abe.png)

**Congratulations! You now have your own instance of Microsoft Dynamics 365.** 

### Task 3 - Install Sample Data

1. In the top right-hand navigation select 'Advanced Settings'

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/M55250A/All-Labs/1025610c-e222-477b-9c79-0dccabe8841f.png)

2. Under Settings select Data Management

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/M55250A/All-Labs/1dc91f51-8bee-44e1-b2e8-96f00934c39c.png)

3. In the Data Management window navigate to 'Sample Data'

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/M55250A/All-Labs/0eb16e8a-3ebe-4ef5-b888-40bd25a4378c.png)

4. In the Sample Data dialog click the 'Install Sample Data' button

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/M55250A/All-Labs/5fdfceb0-8fca-4bbd-b207-6b406dbf239d.png)

5. Close the Sample Data dialog and navigate back to the Dynamics 365 home page
6. Refresh the browser until you see the charts on the home page dashboard come alive with data!

   ![Screenshot](https://godeployblob.blob.core.windows.net//labguideimages/M55250A/All-Labs/4011aa96-e750-427a-9ef1-b9a7ef46f33e.png)

## Finance and Operations Labs

FinOps labs have been very complex problem. However we are pleased we now have a solution.

This applies to courses MB-300, MB-310, MB-320, MB-330. These are Dynamics 365 for Finance and Operations courses.

These lab environments are wholly self-contained Windows machines, which contain an installation of Dynamics 365 apps and SQL Server with demo data.

### Lifecycle Services Labs

**Update: LCS exercises have now been removed from Dynamics Labs.**

~~Issue: There is as yet no solution for the Lifecycle Services labs.~~

~~These are:~~

* ~~MB-300T01 Module 2~~
* ~~MB-300T03 Module 3~~

~~A support plan may be needed for the LCS labs. “You cannot sign into Microsoft Dynamics Lifecycle Services because your account does not have the required associated CustomerSource or PartnerSource support plans. Microsoft Accounts \(MSA\) \(such as Live or Hotmail\) are not allowed to use Microsoft Dynamics Lifecycle Service without a support plan. For more information, please refer to this~~ [~~announcement~~](https://cloudblogs.microsoft.com/dynamics365/it/2018/03/14/upcoming-change-april-15-2018-only-azure-active-directory-users-will-be-allowed-to-create-prospective-presales-projects-in-lcs/?source=lcs)~~.”~~


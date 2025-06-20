# Microsoft-Entra-ID-Conditional-Access

This is a project on how to configure Entra ID Conditional Access through the admin center

To start you must have an account with Azure. Link >  https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account

Go to this link to access the admin center. Link > https://entra.microsoft.com/#home

Step 1: Click on 'Users' > 'all users' > 'new user'. 

![image](https://github.com/user-attachments/assets/18a8df8a-3110-46fa-8e90-1ee4fc72ae7e)

Step 2: Create 3 new users. You can also assign them a role if you want but it's not necessary for this project. After you're done, it should look like the screenshot below.

![image](https://github.com/user-attachments/assets/ec02214c-6b10-4160-9e11-70c090447b12)

Step 3: Click on 'Groups' > 'Overview' > 'New Group' 

![image](https://github.com/user-attachments/assets/8f9d579b-64f2-4ad7-b0c3-84088887c1fb)

Step 4: Create your new group. Give the group a name and a description. Select the three memebers you created before and add them to this group

![image](https://github.com/user-attachments/assets/1f478360-8dbf-4b06-a022-ff539babebf5)

Step 5: Go to 'Protection' > 'user risk policy' 

![image](https://github.com/user-attachments/assets/872f3b98-d35c-4e18-bc16-943ee45f8910)

Step 6: Click on 'all users' > 'select users and groups' > select the group you created previously. Then go 'User risk' below and click on 'High'. Below that on 'Access' > select 'Block access'. 

Why are we doing this? These employees have elevated privileges so that makes them a prime target for attackers. By placing them in this section, we can block all access if we see any suspicious activity. 

Step 7: Now we're going to go to the 'Sign in risk policy' category and do the exact same as before. The only difference will be the 'access' category. I'm going to change it to MFA

![image](https://github.com/user-attachments/assets/6aa1cf56-1727-474b-bbc2-7878b657e042)

Step 8: Go to 'Conditional Access' > 'Authenication Strengths' > 'new authentication strength' 

![image](https://github.com/user-attachments/assets/cde88c22-bd2f-45c7-a30b-f879f12cc4d2)

Step 9: Now we're going to create own rule. Give your new authentication strength a name, description, and select 'Phishing-resistant MFA, 'Passwordless MFA', and 'MFA'. You should see your new authenticatoin strength on the list. 

![image](https://github.com/user-attachments/assets/9b5fe41e-2ea4-4747-ad8a-d0c14dab78c8)

![image](https://github.com/user-attachments/assets/b84e01f3-403c-45e2-a4d5-9272ce267f2b)

Step 10: Go to 'Policies' and click on 'New policy' 

![image](https://github.com/user-attachments/assets/479fc5d5-d4ef-48fe-9556-0eb819029f72)

Step 11: Name your new policy and click on 'users' > 'select users and groups' > select the group you made previously

![image](https://github.com/user-attachments/assets/e62dd960-d3ec-437b-a8c9-2fe023d14405)

Step 12: For 'Target resources' we're going to select 'all resources'

![image](https://github.com/user-attachments/assets/dcb9ec01-890c-49d7-a2bd-e71de810ed39)

Step 13: For 'Network' I'm going to choose 'any network or location and all trusted locations exlcuded' 

![image](https://github.com/user-attachments/assets/d0c04f83-7f9f-47a6-90d7-2a4a4ad5a003)

Step 14: For 'Conditions', user risk will be 'high' > sign in risk will be 'high' > insider risk will be 'moderate' and 'elevated' > device platforms will be 'any device' > locations will be 'any network location and all trusted locations excluded' >  Client apps will be 'browser', 'mobile app', and 'Exchange'

![image](https://github.com/user-attachments/assets/6887b918-eb61-4b03-9092-c899dfdd0bb8)

Step 15: Go to 'Access Controls' and select 'Grant Access'. Select 'Require authentication stregnth' and select your custom authentication strength you made previously. 

![image](https://github.com/user-attachments/assets/87e862ba-54aa-4a2f-b931-49a3aa3c2c89)

Now you have made custom conditional access policy to a group!





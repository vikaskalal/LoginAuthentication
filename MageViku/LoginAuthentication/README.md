# LoginAuthentication
The Custom developed Magento Two Factor Authentication (2FA) gives you an opportunity to protect the Magento store from hackers, keyloggers, unauthorized logins, data sniffing tools, and other threats. Using the password and a security code from your smart-phone, you can easily enhance your Magento admin security. Also, keep it in mind that you only share the code with authorized users to access the Magento admin panel.

Install Manually using source code :

  Download zip from github. And paste downloaded code in<code> /var/www/html/[ProjectName]/app/code </code>Remove global readme.md files it's not needed.

Run the following command in Magento 2 root folder:
```
  php bin/magento setup:upgrade
  php bin/magento s:d:c
  php bin/magento setup:static-content:deploy
  ```

**User Guide**
  **How to config LoginAuthentication For admin**
  **Configuration**
  
  Log into the Magento administration panel, go to Stores > Configuration > MAGEVIKU > General Configuration

  Choose Yes to enable LoginAuthentication.

![image](https://user-images.githubusercontent.com/48544769/210317650-c35d22ee-7b62-4171-a0b3-471d7e17100f.png)

**NOTE** : Please check email sending functionality is enabled or not in local environment. Otherwise you will not get email with otp for further process and email not sending log will be generated in debug.log file.


1) Magento login first setp you have to login with submiting right credentials to admin login step.

![image](https://user-images.githubusercontent.com/48544769/210315851-b2a635e9-765f-4615-a914-c137e34053e8.png)

2)  When you hit sign in button you will get one email notification with 5 minutes valid otp.Which you need to fill in second step to continue login successfully.
		![image](https://user-images.githubusercontent.com/48544769/210315899-0b3868ea-98fb-440b-997e-419b32533ed5.png)

3) Here is the email with otp.  

    ![image](https://user-images.githubusercontent.com/48544769/210315969-1eecb63c-a4b6-4bcd-a8fc-2bf3c6dcb0a6.png)


4) Received email otp need to fill in authentication input box.if you enter invalid otp then it will throw the below error. 

![image](https://user-images.githubusercontent.com/48544769/210316132-b531a852-41a5-47d1-824a-8b0d166aa8b4.png)


5) When you enter valid otp. And hit the confirm button.The otp will be checked is valid or not.

![image](https://user-images.githubusercontent.com/48544769/210316171-285e3a08-43f8-4104-b7a9-f7f1900a49b6.png)


6) If otp is valid then you will be successfully logged in magento admin dashboard and it will keep alive session till you do not logout from admin or it’s get logged out it self.

![image](https://user-images.githubusercontent.com/48544769/210316426-36dd1b94-74c9-4174-a835-7a878680f3d3.png)

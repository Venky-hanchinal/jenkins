**E-mail Notifications Configuration in Jenkins**
https://www.youtube.com/watch?v=MFgbp00hbVI&list=PL6flErFppaj35spJjPy41-lruDjw2kRV-&index=5

1) Manage Jenkins > Configure System > E-mail Notification > SMTP server >
smtp.gmail.com (update it) > click on advance 

2) Selecte Use SMTP Authentication > User Name (mail ID) > Password > Selecte Use SSL > SMTP port (465) 

3) Click on Test configuration by sending test e-mails > update your mail id > click on test configuration > you will get one e-mail for confirmation.

**Need to below configuration in G-mail**

1) Disable 2 factor authenticaton
2) Allow less secure on

**Extended E-mail Notification**

1) SMTP server (smtp.gmail.com) > SMTP Port (465) > Click on Advance > select use SSL > Default content type - select HTML > Default Subject & Default content just check it no edit require. 

2) Default triggers > select which one you want - selecte always > click on apply and save.

**Jenkins Job level configuration for E-mail notification**

1) Jenkins job > configure > Post build actions > Editable email notification > Project recipient list - add mail ID > content type - HTML.

2) Click on advance settings > Triggers > untick the developer list > click on apply and save. 

3) Click on Build job once it built you will get e-mail with default subject and content of build status.

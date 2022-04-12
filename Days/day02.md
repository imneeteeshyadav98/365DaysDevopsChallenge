## Password based authentication  on AWS EC2 Machine
### Problem:- How to create Password based Ec2 machine?.
### Fallow Some basic steps to solve this use case........
#### step1:- Login with ec2 machine webbased or ssh based
#### step2:- Open sshd_config file.
        path:- sudo vi /etc/ssh/sshd_config
![ssh location](https://github.com/imneeteeshyadav98/365DaysDevopsChallenge/blob/main/Images/Day02/1.png)
#### step3:- Find the line containing “PasswordAuthentication” parameter and change its value from “no” to "yes"
        PasswordAuthentication yes
##### Note:-If you want to set up “root” ec2 user password, find  “PermitRootLogin” parameter and change its value from 
        "prohibit-password" to "yes"
##### Step4:- Setup ec2 user password using the "passwd" command along with the username.
##### You need to enter the password twice. For example, if you want to set up a password for “ubuntu” user, use the following command.
        sudo passwd root.
##### Step5: Now, restart the "sshd" service using the following command.
       sudo service sshd restart
       sudo systemctl restart sshd
##### step6:- Step 6: Now you can log out and log in using the password you set for the user. For example,
        ssh root@35.162.225.240

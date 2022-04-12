## Password based authentication  on AWS EC2 Machine
<h3>Problem:- How to create Password based Ec2 machine?.</h3>
<p>Fallow Some basic steps to solve this use case........
<h3>step1:- Login with ec2 machine webbased or ssh based</h3>
<h3>step2:- Open sshd_config file</h3>
        <h4>path:- sudo vi /etc/ssh/sshd_config</h4>
        <img src="images/Day02/1.png">
<h3>step3:- Find the line containing “PasswordAuthentication” parameter and change its value from “no” to “yes“</h3>
        <h4>PasswordAuthentication yes</h4>
        <h4>Note:-If you want to set up “root” ec2 user password, find  “PermitRootLogin” parameter and change its value from 
        "prohibit-password" to "yes"</h4>
<h3>Step4:- Setup ec2 user password using the "passwd" command along with the username.<h3>
        <h4>You need to enter the password twice. For example, if you want to set up a password for “ubuntu” user, use the following command.<h4>
        <h4>sudo passwd root</h4>
<h3>Step5: Now, restart the "sshd" service using the following command.<h3>
        <h4>sudo service sshd restart<h4>
        <h4>sudo systemctl restart sshd </h4>
<h3>step6:- Step 6: Now you can log out and log in using the password you set for the user. For example,<h3>
        <h4>ssh root@35.162.225.240</h4>
</p>
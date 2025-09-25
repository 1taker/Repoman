HOW TO MAKE AN EC2, Make security group, Copy DNS and make into useable link.

1.	Log into AWS and click EC2.
2.	click on security groups ( Don't touch/delete Security group) ( Don't touch out bound rules)
3.	Click on Instances.
4.	Click on Create new key pair and copy and paste security group name into it. ( a key pair allow you to connect to your instance.
5.	Scroll down to Firewall and click " select existing Security group" select default.
6.	scroll down to advance details. Open it and go down to user data.
7.	Go to Gethub and Copy MookieWaf EC2 script and paste it in Advance details.
8.	Click Launch instance, then click green link.
9.	Copy DNS link. http://ec2-54-144-24-121.compute-1.amazonaws.com
10.	Go to Instance then Instance state and click Terminate.

Make new security group

1.Click Security group and give it a name.(Tags are good for organizational purpose and the office)
2.Scroll down to Inbound rules. Select HTTP, Anywhere IP4
3.Click Create Security Group.
 
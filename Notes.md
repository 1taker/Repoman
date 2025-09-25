1 go to search and type in GITBASH

pwd- Print working directory 

Print- meanings displayed on screen

directory- folder

ls- allows you to few all files in that directory 

cd- change directory( all directories cd have a /

mkdir (Directory name)- make directory





In Terminal or Gitbash

To get to folders



Commands to Remember-



pwd- Print Working Directory/Folder

cd (directory name)- changes directory 





1.Build a security group port SSH 22 and HTTP 80

2.build an EC2 Instance (amazon Linux based 2023

3.build a key pair

4.copy and paste Theo's ec2 script 

5.lanch instance

6.copy and paste public dns 

7.paste http:public-dns- to sho EC2 script webserver created. 

8.SSH into ec2 instance as it's running 

9.modify ece script and refersh the webserver page 

10.ping IP address 8.8.8.8 

11.Complete



GitHub: 



Save new modified ec2 script







**Build a Security group port 22 and 80**

Security Groups:



1\. Build a Security Group (Ports 22 and 80)

\- Name: wolfpack-wednesday

\- Description: wolfpack-wednesday

\- VPC: Leave default



Inbound Rules

\- Add Rule

\- Type: SSH | Protocol: TCP | Port Range: 22 | Source Type: Anywhere IPv4 | Source: (Default 0.0.0.0) | Description: SSH

\- Add Rule

\- Type: HTTP | Protocol: TCP | Port Range: 80 | Source Type: Anywhere IPv4 | Source: (Default 0.0.0.0) | Description: HTTP



Outbound Rules

\- SKIP OUTBOUND RULES!!!! GO AROUND THEM OR SUFFER THE WRATH OF CHEWBACCA!!!!



Tags

\- Key: Name

\- Value: wolfpack-Wednesday



2\. **Build an EC2 Instance** (Amazon Linux based 2023)

\- Click the orange button "Launch instance"

\- Name: wolfpack-wednesday



Applications and OS Images (Amazon Machine Image)

\- Click the "Quick Start" tab

\- Ensure "Amazon Linux" icon is selected

\- Amazon Machine Image: "Amazon Linux 2023 kernel-6.1 AMI" (default)

Description: Leave as default

\- Instance Type: t3.micro



Key pair (login)

\- Click "Create new key pair"

\- Key pair name: wolfpack-wednesday

\- Key pair type: RSA (leave as default)

\- Private key file format: .pem (leave as default)

\- Click orange button (Create key pair)

\- Save your key pair in your DOWNLOADS folder on your computer

\- NOTE: Key pair name is now populated with "wolfpack-Wednesday"



Network Settings:

Network: leave as default

Subnet: leave as default

Auto-assign public IP: should be defaulted as "Enable"

Firewall Security groups: 

\- Click "Select existing security group"

\- Scroll down and click on "wolfpack-wednesday"



Configure storage: leave as default



Advanced details:

\- Scroll all the way down to user data (optional)

\- (SKIP EVERYTHING BEFORE IT)

\- Access the MookieWAF EC2script via GitHub: https://github.com/MookieWAF/bmc4/blob/main/ec2scrpit

\- Click the two boxes in the top right corner labeled as "Copy Raw File"

\- Look for the pop up box that indicated it was "Copied"

\- Go back to your EC2 Instance user data block and paste your script (Ensure the entire script was pasted correctly).

\- PRAY TO CHEWBACCA BEFORE YOU LAUNCH INSTANCE!!!

\- Click the orange button and Launch Instance at the bottom of the page.











**SSH into EC2 Instance as it's running**

\- Go back to your Instance summary page (the same page you copied and pasted your Public DNS)

\- Click the "Connect" button at the top of the page.

\- On the next page leave everything as default and click the orange "Connect" button at the bottom right of the page.

\- Look for the Black Bird and the "Amazon Linux 2023" logo at the top.



9\. **Modify EC2 Script and refresh the WebServer page**



On the command line type the following commands.



sudo vim /var/www/html/index.html



\- Press the letter "i" on your keyboard (lowercase i, NOT UPPERCASE I). This will change your script to INSERT MODE at the bottom left of the screen.

\- Using your keyboard arrows, move up, down, left, or right in the script to modify your script.


\- Check the line "Samurai Katana" and change to "Wolfpack Wednesday"

\- Remove the entire line "# insert an image or GIF"

\- Paste updated image file one the next line after `img src=<image-file-here`



Press the "Esc" button

Type the command :wq and Press Enter



**10. Ping IP address 8.8.8.8 (Google DNS) to show web connectivity**.



ping 8.8.8.8



\- Verify the connectivity is running to the internet.

\- Press either "CTRL+C" or "CTRL+Z" to stop the ping.



**11. Teardown**



\- Go to your EC2 Instance. Go to Action and click "Terminate Instance.

\- Go to your Security Group, click the Action button at the top and click "Delete Security Group"

\- Praise Chewbacca and Get this Money














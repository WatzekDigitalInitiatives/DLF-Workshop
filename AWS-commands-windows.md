## Login to AWS Console

---

#### Make a virtual computer (EC2 Instance)

1. Go to Watzek Digital Initiatives' [AWS account](https://watzekdi.signin.aws.amazon.com/console)
2. Login with the username and the password on your table. They should look like:
```
User Name: DLFUser#
Password: Qwnmzxop9
```
(when explaining dashboard check for N.Virginia)

3. Selecting Service
  - **Scroll** down to *AWS Services*
  - Under *Compute* section **click** *EC2* (screenshot, explain side bar)
4. **Click** the big blue `Launch Instance` button (explain all the available OS)
5. **Click** `My AMIs` (explain the image they are selecting, pre-installed software)
6. **Select** `dlf_agalma` image
7. Configure Instance Details
  - **Select** `c3.2xlarge`
  - **Click** `Next: Configure Instance Details`(explain different computer options, make them scroll through them)
8. Explain the Configure Instance Details page, explain spot, connect your s3 here
9. **Click** `Next: Add Storage` (explain the page, 20 GB is enough)
10. Tagging Instance:
  - **Click** `Next: Tag Instance`
  - **Name** your virtual computer here! Use your `lastname_firstname` for exmaple `Doe_Jane`
  - **Click** `Next: Configure Security Group`
11. Selecting Security Group:
  - **Select** `Select an existing security group`
  - **Click** on `dlf-workshop-security-group`
  - **Click** `Review and Launch`(explain the page)
12. Review page:
  - **Click** `Launch`
  - In **Select a key Pair** select `dlf-workshop-key`
  - **Select** the check-box `I acknowledge that I have access to the...`
  - **Click** `Launch Instances`
  - **Scroll** down to `View Instances`

---

#### Download Key

1. Download the key from <a href="http://tinyurl.com/dlf-ec2-key" target="_blank">here (http://tinyurl.com/dlf-ec2-key)</a>

---

#### Download mobaXterm (tool to access command line)

1. Download mobaXterm from <a href="http://tinyurl.com/dlf-mobaxterm" target="_blank">here (tinyurl.com/dlf-mobaxterm)</a>

---

#### Access your virtual computer

1. Run mobaXterm (software you downloaded earlier) and **click** `New session`
2. **Click** on your name from the list on AWS
3. **Copy** the `Public IP (xx.xx.xxx.xxx)` number under *Public IP* column of your row (might have to scroll right to see it)
4. Go to mobaXterm and **paste** this IP in the `Remote host` box
5. **Select** the check-box `Specify username` and **type** `ubuntu` in the box
6. **Click** `Advanced SSH settings` tab
7. **Select** check-box `Use private key`
8. **Click** the tiny *paper picture* and find and select the key downloaded earlier in the tutorial, the file should be named `dlf-workshop-key.pem` in *Downloads* folder
9. Click OK to connect to connect to your computer

#### Now go to [Agalma Commands page](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/Aglama-commands.md)

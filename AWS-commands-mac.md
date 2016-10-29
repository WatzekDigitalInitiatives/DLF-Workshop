## Login to AWS Console

---

#### Make a virtual computer (EC2 Instance)

1. Go to Watzek Digital Initiatives' <a href="https://watzekdi.signin.aws.amazon.com/console" target="_blank">AWS account</a> (tinyurl.com/watzek-aws-console)

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

1. Download the key from <a href="http://tinyurl.com/dlf-ec2-key" target="_blank">here</a> (tinyurl.com/dlf-ec2-key)
  - Note: Don't change the download destination, make sure it is in your `Downloads` folder

---

#### Access your virtual computer

1. Open spotlight by typing `cmd + space`
2. Type `terminal` and hit **return** key to open it
3. Change directory to Downloads folder by typing `cd Downloads` followed by a **return** on the terminal window
4. Give permission to your key to access your EC2-Instance by typing `chmod 400 dlf-workshop-key.pem` followed by a **return** on the terminal window
4. **Copy** the `Public IP (xx.xx.xxx.xxx)` number under *Public IP* column of your row (might have to scroll right to see it)
5. Go to terminal and access your EC2-Instance by typing `ssh -i dlf-workshop-key.pem ubuntu@xx.xx.xxx.xxx.`
  - Replace the `xx.xx.xxx.xxx` with your Public IP (use `cmd+v` to paste it)
  - Hit a **return** to connect
  - If it prompts you `Are you sure you want to continue connecting (yes/no)?` type `yes` and hit **return**
  - You should now be connected to your EC2-Instance

#### Now go to [Agalma Commands page](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/Aglama-commands.md)

## Login to AWS Console

---

#### Make a virtual computer (EC2 Instance)

1. Go to Watzek Digital Initiatives' <a href="https://watzekdi.signin.aws.amazon.com/console" target="\_blank">AWS account</a> **(NOTE: Open the link in a new tab)**

  Alternative URL: tinyurl.com/watzek-aws-console)

  ---

2. Login with the username and the password on your table. They should look like:
  ```
  User Name: DLFUser# (replace # with your respective number)
  Password: Qwnmzxop9
  ```

  ---

3. Selecting Service
  - Make sure you are in the right region. Your top bar should look like:

  ![navbar](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/navbar.png)

  with N.Virginia as your center option
  - **Scroll** down to *AWS Services*
  - Under *Compute* section **click** *EC2*

  ![EC2](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/select-ec2.png)

  ---

4. **Click** the big blue `Launch Instance` button

  ![Launch](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/launch_instance.png)

  ---

5. **Click** `My AMIs` from the left pane

  ![Select AMI](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/select_ami.png)

  ---

6. **Select** `dlf_agalma` image

  <!-- slect agalma image -->

  ---

7. Configure Instance Details
  - **Select** `c3.2xlarge`

  ![Use c3.2xlarge](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/c32xlarge.png)

  - **Click** `Next: Configure Instance Details`

  ---

8. **Click** `Next: Add Storage`

  ---

9. Tagging Instance:
  - **Click** `Next: Tag Instance`
  - **Name** your virtual computer here! Use your `lastname_firstname` for exmaple `Doe_Jane`  
  - **Click** `Next: Configure Security Group`

  ![Tag](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/tag.png)

  ---

10. Selecting Security Group:
  - **Select** `Select an existing security group`

  ![User Existing SG](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/select_existing_sg.png)

  - **Click** on `dlf-workshop-security-group`

  ![Select dlf workshop SG](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/sg.png)

  - **Click** `Review and Launch`

  ---

11. Review page:
  - **Click** `Launch`
  - In **Select a key Pair** select `dlf-workshop-key`
  - **Select** the check-box `I acknowledge that I have access to the...`

  ![Key](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/images/key.png)

  - **Click** `Launch Instances`
  - **Click** `View Instances` (might have to scroll down a bit)

---

#### Download Key

1. To download the key, right click on the *DLF Key* link and click `Save link as (Chrome)` or `Download Link Target (Firefox)` or `Download Linked File As (Safari)` 
2. And save the file in your **downloads** folder

  <a href="http://tinyurl.com/dlf-ec2-key" target="\_blank">DLF Key</a> (tinyurl.com/dlf-ec2-key)

  - Note: Don't change the download destination, make sure it is in your `Downloads` folder
  - Note: Don't change the name of the file

---

#### Access your virtual computer

1. Open spotlight by typing `cmd + space`
2. Type `terminal` and hit **return** key to open it
3. Change directory to Downloads folder by typing `cd Downloads` followed by a **return** on the terminal window
4. Give permission to your key to access your EC2-Instance by **typing** `chmod 400 dlf-workshop-key.pem` followed by a **return** on the terminal window
6. The next command to access your cloud computer is in two parts:
  1. **Type** `ssh -i dlf-workshop-key.pem ubuntu@` in your terminal window and **do not hit return yet**
  2. Go back to your Amazon Console and **select** the row with your name and scroll right till you see Public IP column (might have to scroll right and should be around 9th column)
    - **Copy** the `xx.xx.xx.xx` number under *Public IP* column of your row
    - **Paste** it at the end of the command you just typed
    - You command should look like: `ssh -i dlf-workshop-key.pem ubuntu@xx.xx.xx.xx`
    - Hit **return** to connect
    - If it prompts you `Are you sure you want to continue connecting (yes/no)?` type `yes` and hit **return**

You should now be connected to your EC2-Instance!

#### Now go to [Agalma Commands page](https://github.com/WatzekDigitalInitiatives/DLF-Workshop/blob/master/Aglama-commands.md)

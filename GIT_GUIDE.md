--------------------------------------------------
HOW TO DOWNLOAD THIS MOD (VERY BEGINNER FRIENDLY)
==================================================

This guide is written for people who have never worked with:
- Git
- Programming
- IT tools

We will download the files using SSH.
This is safe and works long-term.

--------------------------------------------------
STEP 1 — CREATE A GITHUB ACCOUNT
--------------------------------------------------
1. Open https://github.com
2. Click "Sign up"
3. Create a free account
4. Stay logged in

--------------------------------------------------
STEP 2 — INSTALL GIT
--------------------------------------------------

macOS:
1. Open your web browser
2. Go to https://git-scm.com
3. Click "Download for macOS"
4. Open the downloaded installer (.pkg file)
5. Install Git using default settings
6. After installation, open Terminal and run:
   git --version
7. If you see a version number, Git is installed

Windows:
1. Go to https://git-scm.com
2. Click "Download for Windows"
3. Run the installer
4. Install using default settings
5. Open "Git Bash" (NOT PowerShell)
6. Run:
   git --version

--------------------------------------------------
STEP 3 — CREATE AN SSH KEY (ONE TIME ONLY)
--------------------------------------------------

Run this command (in Terminal on macOS or Git Bash on Windows):  

ssh-keygen -t ed25519 -C "your_email@example.com"

When asked:
- Where to save the key → press ENTER
- Passphrase → press ENTER (simplest option)
- Repeat passphrase → press ENTER

--------------------------------------------------
STEP 4 — START SSH AND ADD THE KEY
--------------------------------------------------

macOS:  
eval "$(ssh-agent -s)"  
ssh-add --apple-use-keychain ~/.ssh/id_ed25519  

Windows (Git Bash):  
eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/id_ed25519  

--------------------------------------------------
STEP 5 — ADD SSH KEY TO GITHUB (ONE TIME ONLY)
--------------------------------------------------

Copy your public key:

macOS:  
pbcopy < ~/.ssh/id_ed25519.pub

Windows:  
cat ~/.ssh/id_ed25519.pub

Then:
1. Go to GitHub → Settings
2. SSH and GPG keys
3. New SSH key
4. Title: My Computer
5. Key type: Authentication Key
6. Paste the key and save

--------------------------------------------------
STEP 6 — TEST CONNECTION
--------------------------------------------------

Run this command (in Terminal on macOS or Git Bash on Windows):  
ssh -T git@github.com

You should see a success message.

--------------------------------------------------
STEP 7 — DOWNLOAD THE MOD
--------------------------------------------------

Choose a folder (example: Desktop):

cd ~/Desktop

Clone the repository:

git clone git@github.com:YOUR_GITHUB_USERNAME/arydia-tts-mod.git

After this, a folder named "arydia-tts-mod" will appear.

--------------------------------------------------
STEP 8 — UPDATE LATER
--------------------------------------------------

Run this command (in Terminal on macOS or Git Bash on Windows):  
cd ~/Desktop/arydia-tts-mod  
git pull

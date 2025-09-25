ls ~/.ssh

command to get the public and private key
here ~ means root directory which is /Users/arunj

ssh-keygen -t ed25519 -C "jaiswal.najafgarh@gmail.com"

It will ask for the file in which you want to save the key

/Users/arunj/.ssh/new_ssh

new_ssh will be the name of your new key
/Users/arunj/.ssh is the folder where your key will be generated.

Okay, now you can do cat command to see the key

cat /Users/arunj/.ssh/new_ssh to display private key
cat /Users/arunj/.ssh/new_ssh.pub to display public key

cat command has 3 uses.

# Displays the content of the file in the terminal

cat filename.txt -> display the content of the file.

# Displays the content of both files in the terminal

cat file1.txt file2.txt

# Combines both files into a new file called combined.txt

cat file1.txt file2.txt > combined.txt

# Create a new file 

cat > newfile.txt

#### This command waits for you to type

After running this, you can type your text, press Enter, and then use Ctrl + D to save and exit.

# Post creation of SSH key 

Copy the pub key that you've created and go to gihub account -> settings -> ssh and gpg keys -> add a new ssh key

Verify your identity

# Setting Your Terminal to Use Bash

If your VS Code terminal is opening with PowerShell or Command Prompt on Windows, you can easily switch the default to Git Bash.

Note: This requires you to have Git for Windows installed on your computer.

Open the Command Palette with the keyboard shortcut: Ctrl+Shift+P

Type "Terminal" and select the option Terminal: Select Default Profile.

Choose Your Shell. A list of available shells will appear. Select Git Bash.

Now, any new terminal you open in VS Code will automatically start with Git Bash. 👍

# Do the following steps in git bash only

eval "$(ssh-agent -s)"

o/p -> Agent pid 1234

ssh-add ~/.ssh/new_ssh

o/p -> Identity added: /c/Users/arunj/.ssh/new_ssh (jaiswal.najafgarh@gmail.com)

---

Create a new repository on git hub / make it public or private

Open the integrated termial as stated above in your code editor

Now change your directory to the project location

add .gitignore file in your project and mention the name of file which you don't want to publish and .means the hidden file e.g .env You can also add your database or login file which you don't want to add.

# Git Workflow

git init

// write some code or make some changes.

git add . ( in place of code you can write your file name as well )

git commit -m 'comments'

##### Above commands will add your file to .git ( hidden file ) which is your local repo. Remember, your project is added to local repo only not to the github profile.


## For the first time you have to do the following steps ::

git remote add origin https://github.com/ARUNJAISWAL1/practice_lumna.git

git branch -M main

git push -u origin main

#### Now the file is uploaded to your github profile and you have to do only these steps for making / uploading any changes

git init

git add .

git commit -m 'comm'

git push


# Deployment to Netlify

Login to Netlify using your github account

Click on <Add a new Project> -> Import an existing project

Deploy with github

Choose your github project

Type your project name

Deploy your project and you will get the link

In order to get the data from the form submission you have to add name attributes to the elements and add

form name="contact" method="POST" netlify

this attribute needs to be added to the form attribute

Post making any changes to the project. Go to deploys section on the website of nelify and press "triggerdeploy"

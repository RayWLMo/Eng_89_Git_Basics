# Git and GitHub Set up documentation
## Git installation
- To install Git, go to the [Git download page](https://git-scm.com/downloads) and download the Git for the appropiate operating system
[Git Download Page]("Git download page.png")
- This download includes Git Bash as well
## Creating an account on GitHub
- Go to the [GitHub homepage](https://github.com) and create an account using the sign up button in the top right hand corner
- This account will be used to link the account with the generated SSH Key
## Generating an SSH Key to use with GitHub
- To generate an SSH Key, Git Bash is needed
- On Windows, press the Windows key and type 'Git' and open Git Bash as an administrator by right clicking Git Bash
- On Mac, use spotlight to search for Git Bash and it should open as an administrator by default
- In the Git Bash console, enter `$ ssh-keygen -t ed25519 -C "your_email@example.com"` or `$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` if the first one doesn't work
	- make sure your_email@example.com is substituted with the email address used to create the GitHub account 
- Press `enter` a few times until Git Bash has confirmed that it has generated a SSH Key
- To access the SSH key, the system needs to be navigated to the .ssh folder
- To find which directory the system is currently in type `pwd` in the Git Bash terminal
- By Default, it should be in the User directory
- If not, enter `/c/Users/Your_UserName` into the Git Bash terminal, substiting 'Your_UserName' with your own
- Git Bash should now be in your user directory
- the .ssh folder should be located in the user directory
- In the Git Bash terminal enter `cd .ssh`
	- This should navigate Git Bash into the .ssh folder
- In the Git Bash terminal, enter `cat id_ed25519` or `cat id_rsa` for the first or second generation commands respectfully
- The console should now display your SSH key, which is a series of characters
- Copy all the text provided including `ssh-ed25519` or `ssh-rsa` and the email address provided
- On a browser, navigate to the [GitHub profile 'SSH key' settings page](https://github.com/settings/keys)
- Click `New SSH Key`
- Paste the SSH Key in the lower box titled 'Key' and give it a reasonable title i.e 'Windows SSH Key'
- Click Add SSH Key
- The SSH Key should now be added to your GitHub account and you will be able to add and edit files using Git

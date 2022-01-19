Cody Bradley

Ms. Kayleigh Duncan 

Intro to Design of Information Technology Systems

19 January 2021


Status - This shows the status of the local repository, which shows if files are removed, added, and changed! It basically lets you know what is going on your local system. Example: git status

Clone - This command will copy the info and files in your repository to your local computer! Example: git clone git@github.com

Add - The add command basically tells the system this file is ready for tracking to later be commited/pushed.                            Example: git add git-guide.md

Rm - rm commmand in short this removes the file from being tracked from the index. Example: git rm git-guide.md

Commit - This will change the commit of the file. I like to think of this as a file comment/message. Commit helps to keep track of the   changes made to the file. Example: git commit -m "Project 0 Cody Bradley"

Push - This command will sync your files with your repository. Example: git push

Fetch - The fetch command will download all changes to your remote repository. Example: git fetch

Pull - The pull command is the opposite of push, this will pull the files from your repository to your local system. Example: git pull

Branch - This will create a new branch for instance the branch main in our repository, you could make another main branch  but naming it something else. This keeps work more organised. Example: git branch codys-branch 

Checkout - This will change the branch you are wanting. Example: git checkout codys-branch 

.get folder - This folder can contain mainly information for version control and commits. Example: git init

.getignore - This is a folder that will hold files and directories that will be ignored, it basically hides the file.                    Example: vim .gitignore

GitHub Pull Request - You can vice versa here. Pull request from the github's UI rather than your command prompt.

SSH authentication to repo - If i'm answering this correctly, you are creating a public/private key to create a secure connection from   your computer to github. This is basically a encrypted keys to use for a secure connection to github!                                    Example: ssh-keygen -t ed25519 -C "Email"


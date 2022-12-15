# Git-tutorial
Learning Git and GitHub with Harry on his YouTube channel CodeWithHarry.

Git Commands
-------------
Clear the console:
clear

Logout from console:
logout
exit

Show the name of the Git user from Git configuration:
git config --global user.name

Set the name of the Git user in Git configuration:
git config --global user.name Zulfequar Ali

Show the email of the Git user from Git configuration:
git config --global user.email

Set the email of the Git user in Git configuration:
git config --global user.email develperzull@gmail.com

Open VS Code with the current directory open:
code .

Initialize a Git repository in the current directory:
git init

Show all the sub direcories in the current directory:
ls -lart

List all files in the current directory (using Unix command):
ls

Create a file in the current directory:
touch index.html

Get the current status of the repository:
git status

Show the current status of the repository in short:
git status -s


Add a single file to staging area:
git add index.html

Add mulitple files to staging area:
git add index.html about.html

Add all files to staging area:
git add --all
git add -A
git add .

Commit staged files:
git commit -m "Feature: Added a nav bar"

For a single, file restore changes from the last commit:
git checkout index.html

For all files, restore changes from the last commit:
git checkout -f
git checkout --force

Show all commits log:
git log

Show last 1 commit with changes:
git log -p -1
Hint: Press 'q' for quitting.

Show last 1 commit:
git log -1
git log -n 1
git log --max-count=1

Show differences between working tree files and staged files:
git diff

Show differences between staged files and last committed files:
git diff --staged

Directly commit all files without staging them:
git commit -a -m "Feature: Added new files and directly commited without staging."

Remove file from the working tree and from the index (i.e. local file is also deleted):
git rm waste.html

Move a staged or committed file to untracked area (file is first moved to staging area then deleted from there and moved to untracked area):
git rm --cached waste.html

Ignore some files and don't track them:
Create '.gitignore' file and list the files to be ignored.
Add '*.log' to the list to ingore all files with .log extension.
Add '<directory_name>/' to the list to ingnore the directory and its contents.
Add '<file_path>' to the list ingore a file at a specific folder.

Show all branches:
git branch

Create a branch from current branch:
git branch <branch_name>

Switch to a branch:
git checkout <branch_name>

Create a new branch and switch to it as well:
git checkout -b <branch_name>

Merge a branch to current branch:
git merge <branch_name>

Delete a branch:
git branch -d <branch_name>
git branch -D <branch_name>

Add a remote repository (remote):
git remote add <remote_name> <repository_url>

Show all remotes:
git remote

Show romtes with their URLs:
git remote -v
git remote -verbose

Push a (local) branch to a remote:
git push <remote_name> <branch_name>

Generate a new SSH key:
ssh-keygen -t ed25519 -C "your_email@example.com"
or,
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Start the ssh-agent in the background:
eval "$(ssh-agent -s)"

Add SSH key to ssh-agent:
ssh-add ~/.ssh/id_ed25519
[Note: If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.]
or,
ssh-add <ssh_key_file_address>
or,
ssh-add <local_repository_root_directory_address/ssh_key_filename>

Copy the SSH public key contents to your clipboard:
clip < <ssh_public_key_file_address>

Print the SSH public key contents on the terminal:
cat <ssh_public_key_file_address>

Show the current HTTPS of SSH URLs for a remote:
git remote get-url <remote_name>
git remote get-url --all <remote_name>

Change the URL for a remote:
git remote set-url <remote_name> <new_url>

Update the remote by pushing/uploading the local files of a branch and add the upstream (tracking) reference as well:
git push -u <remote_name> <branch_name>
or,
git push --set-upstream <remote_name> <branch_name>

Update the remote by pushing local files from the current branch (last pushed branch using -u or --set-upstream option):
git push

Clone/copy a public repository:
git clone <repository_url>

Clone a public repository into a new directory:
git clone <repository_url> <new_dictory_name>

# Git-tutorial
Learning Git and GitHub with Harry on his YouTube channel CodeWithHarry.

<h3>Git Commands</h3>
<hr />

<h6>1. Clear the console:</h6>
<pre>clear</pre>

<h6>2. Logout from console:</h6>
<pre>logout
or
exit</pre>

<h6>3. Show the name of the Git user from Git configuration:</h6>
<pre>git config --global user.name</pre>

<h6>4. Set the name of the Git user in Git configuration:</h6>
<pre>git config --global user.name Zulfequar Ali</pre>

<h6>5. Show the email of the Git user from Git configuration:</h6>
<pre>git config --global user.email</pre>

<h6>6. Set the email of the Git user in Git configuration:</h6>
<pre>git config --global user.email develperzull@gmail.com</pre>

<h6>7. Open VS Code with the current directory open:</h6>
<pre>code .</pre>

<h6>8. Initialize a Git repository in the current directory:</h6>
<pre>git init</pre>

<h6>9. Show all the sub direcories in the current directory:</h6>
<pre>ls -lart</pre>

<h6>10. List all files in the current directory (using Unix command):</h6>
<pre>ls</pre>

<h6>11. Create a file in the current directory:</h6>
<pre>touch index.html</pre>

<h6>12. Get the current status of the repository:</h6>
<pre>git status</pre>

<h6>13. Show the current status of the repository in short:</h6>
<pre>git status -s</pre>


<h6>14. Add a single file to staging area:</h6>
<pre>git add index.html</pre>

<h6>15. Add mulitple files to staging area:</h6>
<pre>git add index.html about.html</pre>

<h6>16. Add all files to staging area:</h6>
<pre>git add --all
or
git add -A
or
git add .</pre>

<h6>17. Commit staged files:</h6>
<pre>git commit -m "Feature: Added a nav bar"</pre>

<h6>18. For a single, file restore changes from the last commit:</h6>
<pre>git checkout index.html</pre>

<h6>19. For all files, restore changes from the last commit:</h6>
<pre>git checkout -f
or
git checkout --force</pre>

<h6>20. Show all commits log:</h6>
<pre>git log</pre>

<h6>21. Show last 1 commit with changes:</h6>
<pre>git log -p -1
Hint: Press 'q' for quitting.</pre>

<h6>22. Show last 1 commit:</h6>
<pre>git log -1
or
git log -n 1
or
git log --max-count=1</pre>

<h6>23. Show differences between working tree files and staged files:</h6>
<pre>git diff</pre>

<h6>24. Show differences between staged files and last committed files:</h6>
<pre>git diff --staged</pre>

<h6>25. Directly commit all files without staging them:</h6>
<pre>git commit -a -m "Feature: Added new files and directly commited without staging."</pre>

<h6>26. Remove file from the working tree and from the index (i.e. local file is also deleted):</h6>
<pre>git rm waste.html</pre>

<h6>27. Move a staged or committed file to untracked area (file is first moved to staging area then deleted from there and moved to untracked area):</h6>
<pre>git rm --cached waste.html</pre>

<h6>28. Ignore some files and don't track them:</h6>
<pre>Create '.gitignore' file in the root directory of the repository and list out the filenames to be ignored.
Add '*.log' to the list to ingore all files with .log extension.
Add '&lt;directory_name&gt;/' to the list to ingnore the directory and its contents.
Add '&lt;file_path&gt;' to the list ingore a file at a specific folder.</pre>

<h6>29. Show all branches:</h6>
<pre>git branch</pre>

<h6>30. Create a branch from current branch:</h6>
<pre>git branch &lt;branch_name&gt;</pre>

<h6>31. Switch to a branch:</h6>
<pre>git checkout &lt;branch_name&gt;</pre>

<h6>32. Create a new branch and switch to it as well:</h6>
<pre>git checkout -b &lt;branch_name&gt;</pre>

<h6>33. Merge a branch to current branch:</h6>
<pre>git merge &lt;branch_name&gt;</pre>

<h6>34. Delete a branch:</h6>
<pre>git branch -d &lt;branch_name&gt;
or
git branch -D &lt;branch_name&gt;</pre>

<h6>35. Add a remote repository (remote):</h6>
<pre>git remote add &lt;remote_name&gt; &lt;repository_url&gt;</pre>

<h6>36. Show all remotes:</h6>
<pre>git remote</pre>

<h6>37. Show romtes with their URLs:</h6>
<pre>git remote -v
or
git remote -verbose</pre>

<h6>38. Push a (local) branch to a remote:</h6>
<pre>git push &lt;remote_name&gt; &lt;branch_name&gt;</pre>

<h6>39. Generate a new SSH key:</h6>
<pre>ssh-keygen -t ed25519 -C "your_email@example.com"
or
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"</pre>

<h6>40. Start the ssh-agent in the background:</h6>
<pre>eval "$(ssh-agent -s)"</pre>

<h6>41. Add your SSH private key to ssh-agent:</h6>
<pre>ssh-add ~/.ssh/id_ed25519
[Note: If you created your key with a different name, or if you are adding an existing key that
has a different name, replace id_ed25519 in the command with the name of your private key file.]
or
ssh-add &lt;ssh_key_file_address&gt;
or
ssh-add &lt;local_repository_root_directory_address/ssh_key_filename&gt;</pre>

<h6>42. Copy the SSH public key contents to your clipboard:</h6>
<pre>clip &lt; ~/.ssh/id_ed25519.pub
or
clip &lt; &lt;ssh_public_key_file_address&gt;</pre>

<h6>43. Print the SSH public key contents on the terminal:</h6>
<pre>cat ~/.ssh/id_ed25519.pub
or
cat &lt;ssh_public_key_file_address&gt;</pre>

<h6>44. Test your SSH connection (attempts to ssh to GitHub):</h6>
<pre>ssh -T git@github.com

You may see a warning like this:
&gt; The authenticity of host 'github.com (IP ADDRESS)' can't be established.
&gt; RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
&gt; Are you sure you want to continue connecting (yes/no)?

Verify that the fingerprint in the message you see matches GitHub's public key fingerprint.
If it does, then type yes:
&gt; Hi USERNAME! You've successfully authenticated, but GitHub does not provide shell access.

Verify that the resulting message contains your username.</pre>

<h6>45. Show the current HTTPS of SSH URLs for a remote:</h6>
<pre>git remote get-url &lt;remote_name&gt;
or
git remote get-url --all &lt;remote_name&gt;</pre>

<h6>46. Change the URL for a remote:</h6>
<pre>git remote set-url &lt;remote_name&gt; &lt;new_url&gt;</pre>

<h6>47. Update the remote by pushing/uploading the local files of a branch and add the upstream (tracking) reference as well:</h6>
<pre>git push -u &lt;remote_name&gt; &lt;branch_name&gt;
or
git push --set-upstream &lt;remote_name&gt; &lt;branch_name&gt;</pre>

<h6>48. Update the remote by pushing local files from the current branch (last pushed branch using -u or --set-upstream option):</h6>
<pre>git push</pre>

<h6>49. Clone/copy a public repository:</h6>
<pre>git clone &lt;repository_url&gt;</pre>

<h6>50. Clone a public repository into a new directory:</h6>
<pre>git clone &lt;repository_url&gt; &lt;new_dictory_name&gt;</pre>

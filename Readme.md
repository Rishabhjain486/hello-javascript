# JavaScript Basics

This repo consists of code written while learning the basic JS conepts 


To run a specific JS concept code, replace _"xyz"_ with the file name in **"index.html"** - reference line below.

`<script src = "xyz.js"></script>`


### USING GIT WITH VSCODE: COMMANDS TO BE USED

### Working with an existing repo on GITHUB:

1. Open the git folder on the local machine
2. Cloning a repo
`git clone <SSH Link>`
3. See the files in the folder
`ls -la`
4. Change directory into the repo
`cd hello-javascript`
5. make the changes and save the file using cmd+s
6. Check the status of the files created, updated or deleted
`git status`
7. Make GIT track all the files
`git add .`
 * Make GIT track a specific file instead
`git add <name of new file created>`
8. Now check the status again and see that all files are green, ie, all files are tracked
`git status`
9. Now we will commit the changes to our repo
`git commit -m "message title" -m "description"`
 * The -m means message, and it should specify what and why the changes being commited were made
10. These changes are now saved locally, but still not saved on the github
11. Now we push these changes on the remote repository
`git push origin master`
 * Origin is the word that stands for our git repo
 * Master is the branch that we want to push to
12. After running the above command go to github and refresh the page to see the changes.


50. Run the
following command and follow the instructions in your editor to edit
your configuration file:
` git config --global --edit` 

After doing this, you may fix the identity used for this commit with:
` git commit --amend --reset-author`

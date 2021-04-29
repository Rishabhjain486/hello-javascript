# USING GIT WITH VSCODE: COMMANDS TO BE USED

## Working with an existing repo on GITHUB:

1. Open the git folder on the local machine
2. Cloning a repo:
`git clone <SSH Link>`
3. See the files in the folder:
`ls -la`
4. Change directory into the repo:
`cd hello-javascript`
5. make the changes and save the file using cmd+s
6. Check the status of the files created, updated or deleted:
`git status`
7. Make GIT track all the files:
`git add .`
 * Make GIT track a specific file instead:
`git add <name of new file created>`
8. Now check the status again and see that all files are green, ie, all files are tracked:
`git status`
9. Now we will commit the changes to our repo:
`git commit -m "message title" -m "description"`
 * The -m means message, and it should specify what and why the changes being commited were made
10. These changes are now saved locally, but still not saved on the github
11. Now we push these changes on the remote repository:
`git push origin master`
 * Origin is the word that stands for our git repo
 * Master is the branch that we want to push to
12. After running the above command go to github and refresh the page to see the changes
13. To clear the terminal:
`clear`
14. Update the local repo:
`git pull`
 * This will update the files on the local machine
 * We can clone a repo only once, thus this is used to update the repos


## Making a new repo on the local machine and pushing it onto GITHUB

1. go into the newly created repo:
`cd ../new_repo`
2. See the files in the folder:
`ls -la`
 * this will come as a blank till we add a file in the folder
3. To convert this folder into a git repo:
`git init`
4. Steps 2-10 above can now be used here as required
5. Running `git push origin master` will give an error
 * This is because we did not clone this repo from the GITHUB, we created it locally
 * Git doesnt know where to push it to since it is not connected to anything
 * We need to create this connection
6. Go to Github, and create a new repo, give it a name, save it and copy the SSH Link
7. Now run the command:
`git remote add origin <SSH Link>`
8. To verify the remote repository that we connected to this repo:
`git remote -v`
9. Now we can push:
`git push origin master`
 * If we use `git push -u origin master` we will define an upstream, ie, next time just typing `git push` will by default push it to origin master and we dont have to type it again and again
 * This will push the code on the master branch
 * to push on the other branch, replace master with the branch name: `git push origin branch-name`
10. Refresh the Github page and see the changes


## GIT Branching

1. To see the branches:
`git branch`
 * if there are no branches, it will just show master
 * in case of multiple branches, the branch with the `*` will show the branch we are in currently
 * If you are using terminal outside VSCode, you may need to press `Q` to gome back to terminal
2. To create a new branch:
`git checkout -b Branch-name`
3. Check branches:
`git branch`
4. Switch between branches:
`git checkout branch-name`
 * we can hit the `tab` button and it will autocomplete the branch name
 * we can type any part of the branch-name and it will autocomplete it
 * to switch to master branch: `git checkout master`
 * check which branch you are on: `git branch`
5. Now we can use the steps 6-9
6. To check the differences between the master and the new branch:
 * Save the changes and push
 * change the branch to the master branch
 * now type: `git diff branch-name`
7. To merge:
`git merge branch-name`



### Additional stuff
1. Run the
following command and follow the instructions in your editor to edit
your configuration file:
` git config --global --edit` 

After doing this, you may fix the identity used for this commit with:
` git commit --amend --reset-author`

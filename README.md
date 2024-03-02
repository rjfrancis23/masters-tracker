# masters-tracker
Tracking the Masters golf tournament ⛳️

## Instructions for set-up: 

### Git setup
1. Download Homebrew with this package installer: https://github.com/Homebrew/brew/releases/download/4.2.10/Homebrew-4.2.10.pkg
2. Open terminal and enter <code>brew install git</code>.
3. You can confirm the installation with <code>git --version</code>.

### GitHub setup
1. Navigate to https://github.com/.
2. Create an account and sign in. 
3. Open terminal and set your git username <br /><code>git config --global user.name "[USERNAME]"</code> <br />e.g. <code>git config --global user.name "rjfrancis23"</code>
4. Set your git email <br /><code>git config --global user.email "YOUR_EMAIL"</code> <br />e.g. <code>git config --global user.name "rebeccafrancis23@gmail.com"</code>


#### *Set up a personal access token for your first commit*
1. In GitHub, click on your profile in the upper right hand corner of the screen. Click on Settings near the bottom of the list.
2. Scroll down on the left hand side of the page and select Developer Settings.
3. On the left, select Personal Access Tokens, then Tokens (classic).
4. Select Generate new token > Generate new token (classic).
5. Enter a note to label the token, e.g. "Personal projects."
6. Change the expiration date to 90 days. 
7. Click the "repo" checkbox to ensure all the nested boxes in that section are selected, then scroll down and selected Generate token. 
8. Copy the token into a note for reference later. 


### Repository set up 

1. Navigate to the masters-tracker GitHub repository: https://github.com/rjfrancis23/masters-tracker.
2. In the top right corner, select the green "Code" button.
3. Copy the HTTPS link to your clipboard. 
4. Open terminal. Create a new folder to clone the respository into, then "cd" into the new folder.
<br /> <code>mkdir rebecca_git_projects</code><br /> <code>cd rebecca_git_projects</code>
5. Clone the repository into this folder. 
    <br /><code>git clone https://github.com/rjfrancis23/masters-tracker.git</code>
    <br /><code>ls</code> (this lists all the items in the folder)  
    *You should now see a new folder called "masters_tracker." This is the git repository.*
   <br /><code>cd masters_tracker</code><br /><code>ls</code> <br /> *You should now see this README.md file listed.*

### Making your first commit
1. Navigate to your git folder. 
   <br /><code>cd path/to/git/masters_tracker</code>
2. Check what branch you are on. You should see <code>* main</code> printed with a green asterisk.    <br /><code>git branch</code>
3. Check out a new branch to make your changes safely. <br /><code>git checkout -b marcos_branch</code>
4. In Visual Studio Code, open the entire <code>masters_tracker</code> folder. This will allow VS Code to track git changes for you. In the bottom left hand corner, you should see that you are on branch <code>marcos_branch</code>.
5. Open the README.md file in VS Code. Make a small change to the title. Save the changes. 
6. Go back to terminal and check your changes. You should see that the README.md file was modified. <br /><code>git status</code>
7. Add and commit your changes. <br /><code>git add README.md</code> <br /><code>git commit -am "Small change to the README title."</code>
8. Now we push! Have your personal access token ready. <br /><code>git push -u origin marcos_branch</code>
9. You should be prompted for your GitHub username. When you are prompted for the password, paste in the personal access token. Note: you won't see the characters print in terminal, but if you paste, they will be entered. 
10. You should see output similar to: 
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 646 bytes | 646.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'rebecca' on GitHub by visiting:
remote:      https://github.com/rjfrancis23/masters-tracker/pull/new/rebecca
remote: 
To https://github.com/rjfrancis23/masters-tracker.git
 * [new branch]      rebecca -> rebecca
branch 'rebecca' set up to track 'origin/rebecca'.
```
11. Copy and paste the pull request into your browser, fill out the information requested, and create the pull request! Then, tell Rebecca, and she will approve the merge to the main branch. Then you'll see your change reflected in the main version on GitHub. 
12. To pull down the new changes on the main branch, check out main and pull. <br /><code>git checkout main</code> <br /><code>git pull</code><br /><code>cat README.md</code>
13. The changes you made to the README.md file should now be reflected in the main version. Congratulations! You made your first successful PR. 

### What next? 
Any time you want to work on the project, you'll want to checkout a branch to make your changes on first, so that you don't "corrupt" the main branch with any unwanted changes. The workflow should always look like this: 
1. Make sure you're on main to start <code>git branch</code>.
2. Pull down new changes so you are branching off the most up-to-date version <code>git pull</code>.
3. Checkout a new branch <code>git checkout -b your_branch_name</code>.
4. Make your changes, and when you're ready to commit, go back to Step 6 in the section above. 
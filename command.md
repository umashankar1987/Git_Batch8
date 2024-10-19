 

Correct Workflow with Explanations:
Set Global User Name and Email:
---------------------------------------------------------------------------------------------------------
You set your Git username twice, but your email command is missing an extension.
 
git config --global user.name "umashankar1987"
git config --global user.email "umashankar1987@gmail.com"

---------------------------------------------------------------------------------------------------------
Initialize a Repository: You initialized a new Git repository and created a file named git_initialization.txt.

git init
vi git_initialization.txt  # Create and edit the file
git add git_initialization.txt  # Add the file to staging area
git status  # Check status

---------------------------------------------------------------------------------------------------------
Correct Commands: You used git stastu and git logs, which are typos. The correct commands are:

git status
git log  # View commit history
Add and Commit Files: You modified git_initialization.txt and used git add multiple times. You can use the following flow:
 
---------------------------------------------------------------------------------------------------------
vi git_initialization.txt  # Make changes to the file
git add git_initialization.txt  # Stage the changes
git commit -m "Updated initialization file"  # Commit the changes
Remove a File from Staging and Delete: You removed a file (git_initialization_1.txt) from the Git staging area and deleted it from the working directory:

 
---------------------------------------------------------------------------------------------------------
git rm --cached git_initialization_1.txt  # Remove from staging
rm -rf git_initialization_1.txt  # Remove from the working directory
git status
Restoring a File: You tried to restore git_initialization_1.txt, but it doesn't exist anymore since you deleted it. If a file is deleted and committed, it can't be restored unless it exists in the Git history.

However, for staged files, you can use:

 
---------------------------------------------------------------------------------------------------------
git restore --staged git_initialization_1.txt  # Unstage the file
git restore git_initialization_1.txt  # Restore working copy from the previous version (if it exists)


Branching: You created a branch dev, switched between branches, and checked their statuses:
---------------------------------------------------------------------------------------------------------
git checkout -b dev  # Create and switch to the dev branch
git checkout master  # Switch back to the master branch

Committing and Viewing Logs: You committed updates and wanted to see a compact log of commits:
---------------------------------------------------------------------------------------------------------
git log --oneline  # View concise log history

Switching Between Branches: You used git switch, which is an alternative to git checkout for switching branches:
---------------------------------------------------------------------------------------------------------
git switch dev  # Switch to dev branch
git switch master  # Switch back to master
Commit in a New Branch: You created and committed a new file head.txt in the dev branch:
 
---------------------------------------------------------------------------------------------------------
git add head.txt  # Add the new file
git commit -m "New file head created in DEV branch"
Branch Commands: To view the list of branches, use:
 
---------------------------------------------------------------------------------------------------------
git branch  # List all branches
git branch -a  # List local and remote branches
Viewing Detailed Information: To view detailed information about a branch or a commit, you can use:
 
---------------------------------------------------------------------------------------------------------
git show  # Show details about the last commit or a specific one
Summary of Corrections and Notes:
Make sure to use the correct commands: git status, git log, git checkout, etc.
Ensure you are setting up your Git user email properly: git config --global user.email "your-email@gmail.com".
Always check the status with git status to confirm what changes are staged, modified, or untracked.
When viewing logs, git log --oneline is useful for concise history.




---------------------------------------------------------------------------------------------------------
# Git Command Cheat Sheet

This document contains a list of Git commands with their explanations to help you understand and use Git effectively.

---

### 1. Set Global Username and Email

``` 
git config --global user.name "umashankar1987"
git config --global user.email "umashankar1987@gmail.com"
Explanation: These commands configure the global Git username and email address, which will be used for every commit you make from your machine unless overridden for a specific repository.

2. Initialize a Git Repository
---------------------------------------------------------------------------------------------------------
git init
Explanation: Initializes a new Git repository in the current directory, setting up the necessary files and structure for version control.
3. Create and Edit a File
 
---------------------------------------------------------------------------------------------------------
vi git_initialization.txt
Explanation: Opens the vi text editor to create or edit the file git_initialization.txt.
4. Check Repository Status
 
---------------------------------------------------------------------------------------------------------
git status
Explanation: Displays the current status of the repository, including staged, modified, and untracked files.
5. Stage a File
 
---------------------------------------------------------------------------------------------------------
git add git_initialization.txt
Explanation: Stages git_initialization.txt for the next commit. This means Git will track changes made to this file and include it in the next commit.
6. Commit Changes
 
---------------------------------------------------------------------------------------------------------
git commit -m "git class started on 19th OCT 2024"
Explanation: Commits the staged changes to the repository with the message "git class started on 19th OCT 2024". The -m flag allows you to write a commit message.

7. Remove a File from Staging
 ---------------------------------------------------------------------------------------------------------
git rm --cached git_initialization_1.txt
Explanation: Removes the file git_initialization_1.txt from the staging area (but not the working directory), so it will not be included in the next commit.

8. Delete a File
 --------------------------------------------------------------------------------------------------------
rm -rf git_initialization_1.txt
Explanation: Permanently deletes the file git_initialization_1.txt from the working directory.

9. Create and Switch to a New Branch
 ---------------------------------------------------------------------------------------------------------
git checkout -b dev
Explanation: Creates a new branch called dev and switches to it. Branching allows you to work on different features or tasks in isolation from the main project.
10. Switch Between Branches
 
---------------------------------------------------------------------------------------------------------
git checkout master
git checkout dev
Explanation: Switches between the master branch and the dev branch. Use this to switch between different branches of your project.
11. View Commit History
 
---------------------------------------------------------------------------------------------------------
git log
Explanation: Shows the full commit history of the repository, including commit IDs, author names, dates, and commit messages.
 
---------------------------------------------------------------------------------------------------------
git log --oneline
Explanation: Displays a concise log of commits, showing only commit IDs and messages in a single line per commit.
12. Add and Commit a New File
 
---------------------------------------------------------------------------------------------------------
git add head.txt
git commit -m "new file head created in DEV branch"
Explanation: Adds head.txt to the staging area and commits it with the message "new file head created in DEV branch". This is done while in the dev branch.

13. View List of Branches
---------------------------------------------------------------------------------------------------------
git branch
Explanation: Lists all the local branches in the repository. The currently active branch will be marked with an asterisk (*).

git branch -a
Explanation: Lists all branches, including local and remote branches.

14. View Detailed Information of Last Commit
 ---------------------------------------------------------------------------------------------------------
git show
Explanation: Displays detailed information about the last commit, including changes made, commit message, and more.

15. Check Git Help
 ---------------------------------------------------------------------------------------------------------
git --help
Explanation: Opens the Git help documentation, providing a detailed list of all available Git commands and their usage.
Summary
This document contains a sequence of commonly used Git commands along with brief explanations. It covers everything from setting up Git to working with branches, committing changes, and managing files.

yaml
---------------------------------------------------------------------------------------------------------

### How to Create and Edit `command.md`:

1. **Create the File**:
   You can create the `command.md` file using `vi` or any other text editor on Linux:

   ``` 
   vi command.md
Paste the Content: Copy the above Markdown content into your file and save it.

Preview the File: To preview the file in Markdown, you can open it in a Markdown viewer (such as GitHub or any Markdown editor).

This file serves as a helpful Git cheat sheet, guiding you through the most important Git operations.

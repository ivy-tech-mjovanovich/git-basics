# Git and GitHub Fundamentals Assignment

This assignment will guide you through the basic operations of Git and GitHub. Follow these steps carefully to complete the assignment.

Consistency in commit messages and file contents is crucial for this assignment. Follow the instructions exactly as written.

## 1. Create a New Repository

1. Go to GitHub.com and log in to your account.
2. Click on the '+' icon in the top right corner and select 'New repository'.
3. Name your repository "git-fundamentals-yourname" (replace 'yourname' with your Ivy Tech username).
4. Make sure it's set to Public.
5. Leave all options at the defaults. Do not initialize the repository with a README, .gitignore, or license.
6. Click 'Create repository'.

## 2. Create a New File Locally

1. On your local machine, create a new file named "hello.txt".
2. In the file contents, type exactly: "Hello, Git!".
3. Save and close the file.

## 3. Add a File via GitHub UI

1. In your new repository, click on 'uploading an existing file'. _Note: once you have files in your repository, you will not see this option again - it will be replaced with an "Add file" button._
2. Click 'Drag files here to upload' or 'Choose your files' and select the "hello.txt" file you created in the previous step.
3. In the 'Commit changes' section, type the commit message "Initial commit".
4. Click 'Commit changes'.

## 4. Clone the Repository

1. On your repository page, click the 'Code' button and copy the HTTPS URL.
2. Open your terminal or command prompt.
3. Navigate to where you want to clone the repository.
4. Run: `git clone <paste-your-repository-url-here>`
5. Change into the new directory: `cd git-fundamentals-yourname`

## 5. Check Status

Run: `git status`

You should see something like:

```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

## 6. Modify Existing File

1. Open "hello.txt" in a text editor.
2. Change the contents to exactly: "Hello, Git and GitHub!".
3. Save and close the file.

## 7. Check Status

Run: `git status`

This time you should see the hello.txt file listed as modified.

## 8. Create a New File

1. Create a new file named "git-commands.txt".
2. In this file, type exactly: "git status, git add, git commit, git push".
3. Save and close the file.

## 9. Check Status

Run: `git status`

Note that the new file is _untracked_, so it does not show up in the output. Git only keeps track of changes to files that it has been told to track.

## 10. Stage the Modified File

Run: `git add hello.txt`

## 11. Stage the New File

Run: `git add git-commands.txt`

_Note: you can also stage multiple files at once by running `git add file1.txt file2.txt`, or by using wildcards like `git add *.txt`._

## 12. Check Status

Run: `git status`

You should now see the new and modified files listed in the output as "Changes to be committed".

## 13. Commit the Changes

Remember that the commit command requires a commit message. We add this in the text after the `-m` flag.

Run: `git commit -m "Modified hello. Added new git commands file."`

In professional practice, we would strive to write messages that are not redundant, but this is just an exercise.

## 14. Check Status

Run: `git status`

We now see "Your branch is ahead of 'origin/main' by 1 commit". Let's see what that means.

Go back to your repository on GitHub.com. Note that your changes are not yet pushed to the remote repository.

## 15. Push to Remote

Run: `git push`

Refresh your repository on GitHub.com. Note that your local changes have been pushed to the remote repository.

You can see the actual file contents by clicking on the file names. Click on the "hello.txt" file, then click the "History" tab. Click on your commit comment to see the changes for that commit.

## Side Note: Credentials

If this is your first time using Git on your machine, you may need to configure some global settings.

1. Set your name. This is not your GitHub username, it is the name that will appear in the commit history:

   `git config --global user.name "Your Name"`

2. Set your email:

   `git config --global user.email "your.email@example.com"`

_Caching: Windows_

Git for Windows includes caching of your credentials, so you will not be prompted for your password again. If you need to run this manually:

```
git config --global credential.helper wincred
```

_Caching: macOS_

Git for macOS uses the macOS keychain to cache your credentials. You will not be prompted for your password again. If you need to run this manually:

```
git config --global credential.helper osxkeychain
```

## Submission

After completing all steps, submit the URL of your GitHub repository. The commit history should reflect the steps you've taken in this assignment.

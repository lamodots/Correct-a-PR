# Correct-a-PR
How revert a pull request made with the wrong GitHub account, you can follow these steps:
## Option 1: Close the Pull Request

    1. Close the Pull Request:
        Go to the GitHub repository where the pull request was made.
        Navigate to the "Pull Requests" tab.
        Find the pull request made with the wrong account.
        Click on the pull request, then click on the "Close pull request" button.

    2. Re-create the Pull Request:
        Ensure you're using the correct GitHub account on your work computer.
        Switch to the correct branch in your local repository.
        Make any necessary changes or commits.
        Push the branch to the remote repository.
        Create a new pull request from the correct branch and account.

## Option 2: Amend the Commit and Force Push

If the pull request has been merged or you want to change the author of the commits, you can amend the commit history:
1. Set Up Git to Use the Correct User:
```bash
git config --global user.name "Your Correct Name"
git config --global user.email "your_correct_email@example.com"
```
2. Rebase Interactive:

    Start an interactive rebase:


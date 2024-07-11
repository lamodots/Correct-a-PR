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
```bash
git rebase -i HEAD~n
```
Replace n with the number of commits you want to change.

3. Change the Commit Author:

    For each commit you want to change, replace pick with edit.
    with steps bellow
    a. Entering Insert Mode:

    To start editing the file, you need to enter Insert mode. Press i to insert text at the cursor.
    You can also use a to start inserting text after the cursor or o to open a new line below the cursor.

    b. Making Changes:

    Type your text or make changes as needed.
    Use the arrow keys to move the cursor around.

    c. Exiting Insert Mode:

    Press Esc to return to Normal mode.

    d. Saving Changes:

    In Normal mode, type :w to save the file.

    e. Saving and Exiting Vim:

    In Normal mode, type :wq and press Enter to save and exit.
    Alternatively, you can type :x and press Enter to save and exit.

4. Amend the Commit:

    For each commit marked for editing, change the author:
   ```bash
git commit --amend --author="Your Correct Name <your_correct_email@example.com>"
```
Continue the rebase process:
```bash
git rebase --continue
```
5. Force Push the Changes:

    Force push the changes to the remote repository:
   ```bash
git push --force

   ```

Create a New Pull Request:

    If necessary, create a new pull request with the corrected commits.

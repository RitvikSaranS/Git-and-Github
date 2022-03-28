- Creating a folder
```
$mkdir learningit
```
- Initializing an empty git repository to catch all the changes that will be brought to this folder.
```
$git init
```
Returns the msg, 
```
Initialized empty Git repository in [path till learningit]learningit/.git/
```
- The folder .git is the git repository that would be recording the changes made in this folder. To record a change say, creating a file.
```
$touch sample.txt
```
- To view these unsaved changes use the command,
```
$git status
```
which returns the message,
```On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        sample.txt

nothing added to commit but untracked files present (use "git add" to track)
```
sample.txt would be in red colour, meaning it is not staged to save.
- To add the changes to staging area use the command,
```
$git add .
```
here '.' means every changes in the current directory. Instead of all changes we can provide a file name for specific changes too. Now use the git status command to see that the unsaved chnages are moved to staging area ready to commit. git status returns the message,
```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   sample.txt
```
new file: sample.txt would be green colour meaning it is staged to be committed.
- To save or commit these changes use the command,
```
$git commit -m "[any message]"
```
gives a message identical to,
```
[master (root-commit) df4745f] Creating-a-repository
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sample.txt
```
- To view the commit history use the command,
```
$git log
```
which returns something like,
```
commit a0dfa6e0540314819297b418ed288febf7535820 (HEAD -> master)
Author: [name] <[mail-id]>
Date:   Mon Mar 28 18:11:57 2022 +0530

    [message you typed]
```

- By default the HEAD will be pointing to main branch. If we are making any changes to a repository, do not make it in main branch. Make a new branch and make changes then merge the changes to the main after confirming. To start a new branch use the command,
```
$git branch newfeature
```
move the HEAD pointer to the new branch by,
```
$git checkout newfeature
```
then merge to the main branch by,
```
$git merge newfeature
```
- To contribute to a project, first fork that project then take its url from the code option. Use the command,
```
$git clone [url]
```
to download the copy to local system and make the contributions.
- The url of the repository from which the local copy was cloned is upstream url. Set the upstream url by,
```
$git remote add upstream [url]
```
to view all the linked urls use the command,
```
$git remote -v
```
we cannot directly push to the upstream url so push the contributions to the new branch.
- To merge this with the main project make a pull request, this option will pop up in the remote repository after pushing the contributions. Preferably make new pull request for each change, for this make new branch for before adding say a new feature. If we push all changes to a single branch, it will only make a single pull request and it would be difficult to compare and merge.
- To delete a commit from remote repository, we should forcefully do it,
```
$git reset commithash -f
```

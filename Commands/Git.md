Useful [link](https://github.blog/2015-06-08-how-to-undo-almost-anything-with-git/)

## Delete an untracked file

	git stash 
	

## Get the deleted file back

	git stash pop stash@{1}



## Undo git add 

How to undo a "git add ."
for preserving the local changes and discarding the commit use
	
	git reset <file>

or 

	git reset

if you do not want to preserve the changes and want to go back to the last comitted then use

```git reset --hard <last good SHA>```

The First option is the safest option, but often, you’ll want to “undo” the commits and the changes in one move—that’s what --hard does.

## Undo commits

Command for undo git commit saving changes

	git reset HEAD~

or 

if don't want to save changes

   ```git reset --hard HEAD~```

## Command for undo git push 
as if the commit never really existed (dangerous if others are working with you and might have pulled changes from your wrongly pushed ones)

	git reset --hard HEAD~	
	git push -f origin master

if adding another commit but reverting the changes instead in the last commit (useful while working in collaboration)

	git revert
	git push -f origin master
# Git reset

git reset <filename>
or
git reset -A

git reset when performed in this way will simply remove items from staging. If you accidentally staged something you didn't mean to, you can remove it with a git reset <filename>.

If it is a file you don't want to use long-term, then I suggest throwing a 
.gitignore file into your repo.

When you use git reset <commit hash> or git reset HEAD~1 (to remove the previous commit) you are asking to remove the last commit and throw all of the files that those commits changed into a modified state (which will contain the changes there were in those commits for those files).

<i>This is an unsafe command when used to target another commit and you can absolutely lose work and git history by doing this.</i>

Sometimes you make mistakes committing and either want to rewrite your git history or just undo the last commit.  

You can use git reset to undo commits. By default when you do a git reset, you are using --mixed mode. What mixed mode does is you keep the changes that were in your commits that you reset, but they're unstaged.  

If you want to keep your changes and throw the files into staging to make a quick change, then you can use the --soft command so you can immediately make a commit without having to add again.




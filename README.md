# stash-feature

## Part - 1 Without conflicts
$ git stash save "added formulas"

$ git stash list
stash@{0}: On feature-1: added formulas

$ git stash apply stash@{0}

$ git stash pop
On branch feature-1
Your branch is up to date with 'origin/feature-1'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.txt

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (42f3094b5a194bf4fa7e2cbdea67b4010959c58c)

$ git stash drop

## Part - 2 With conflicts

Created branch add-square from main <br>
Made changes in add-square main.txt and saved a stash from it <br>
Made changes in main main.txt and commited those <br>
Tried to apply the stash to main <br>
Got merge conflict as both stash and main had made changes starting from same point in time to main.txt <br>
Opened main.txt and resolved the conflicts <br>
git add .           ---------> while on main branch in git bash <br>
git commit -m "resolved conflicts"           ---------> while on main branch in git bash <br>
git stash apply stash@{0} <br>
<br>
stash applied successfully

# git

[Oh Shit, Git!?!][2.1]

[2.1]: https://ohshitgit.com/

```js
git remote prune origin // prune remote list
git reset --hard HEAD~1 // go back a commit, good for reverse merge.
git reset --hard origin/<branch> // reset to origin/branch

git config --global core.editor "vim"
git config --global user.name "coriandar"
git config --global user.email "xxx"
git config --global color.ui auto
git config --global pull.rebase false
ssh-keygen -t ed25519 -C <youremail>
cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com

git log --oneline -- <filename>
git branch <branch-name>
git diff // can add <filename> / <branch-name>

git stash // stash temporarily
git stash pop // remove and re-apply most recent to chosen branch
git stash list

git checkout HEAD <filename> // discard changes, revert back to head
git checkout <hash> // HEAD points at commit, detached, can make new branch
git restore --staged <filename> // unstage file

git tag // list tags
git tag -l *beta* // wildcard search
git tag <label> commitHash -f // move existing tag
git push --tags // Pushed all to remote, can specify

git commit -am "message" // commit existing only
git push origin <branch> // specific branch

git rebase -i HEAD~5 //Need specify how far back.
git rebase -i --root
git push -f // force push

git reflog show // show log, defaults to HEAD
git checkout HEAD@{2}
git diff HEAD@{2} HEAD@{5}
git reflog diff main@{0} main@{yesterday}

git reset <commitHash> // undo commit to specific branch, moves branch pointer backwards
git reset --hard <commitHash> // undo commit and changes
git revert <commitHash> // for collab, creates commit with undos

git switch -c <branch-name> // branch & switch
git merge <branch-name> // switch to receiving first
```

---

# regex

```js
g //global
i //case insensitive
m //multiline
s //sinlge line
u //unicode
y //sticky

\s // any whitespace
\r // carriage return
^  // start of line
$  // end of line
.  // any except newline
?  // zero or one, optional
*  // zero or more
```

```js
//js
/^.{20,}(\r?\n|$)/gm // match greater than 20
/^\s*(\r?\n|$)/gm // match empty lines

// npp
^.*center;> // up to center
^.{20,} // match length greater than
^.{0,10}$ // match length less than
```

---

# grep

```js
// recursive sub-dir, -l only matching filenames
// piped to xargs, -I specify placeholder {}
grep -Rl --include={*.mkv,*.mp4} . | xargs -I {} mv {} /mnt/path/
```

---

# shell

```js
cd - // toggle previous directory
ctrl + l //clear terminal
echo hello > hello.txt // stream hello' into txt
cat < hello.txt // stream input from hello.txt
echo hello >> hello.txt // append
curl... | grep... // pipe, output from left, input to right
```

---

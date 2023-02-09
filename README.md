# Quick Vim
```js
:set nu // line number
:set rnu // relative line number

ctrl + o // jumplist prev
ctrl + i // jumplist next
```

-----------------------------------------------------------------------------------------

# Quick Regex
```js
^.*center;> // up to center
^.{50,} // match length greater than
^.{0,10}$ // match length less than
```

-----------------------------------------------------------------------------------------

# Quick Express
```js
npm init -y // create JSON, skip prompts
npm i express // install express

const express = require('express');
const app = express();
const port = 3000; // localhost:3000
const path = require('path');

app.set('views', path.join(__dirname, '/views')) // absolute path
app.use(express.static(path.join(__dirname, '/public'))); // use executes on every request

app.listen(port, () => {
    console.log(`Listen on port ${port}`);
})
```

-----------------------------------------------------------------------------------------

# Quick Git
[Oh Shit, Git!?!][2.1]

[2.1]: <https://ohshitgit.com/>

```js
git config --global core.editor "vim"
git config --global user.name "coriandar"
git config --global user.email "xxx"

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

-----------------------------------------------------------------------------------------

# Quick JS

-----------------------------------------------------------------------------------------

# Quick CSS

-----------------------------------------------------------------------------------------

# Quick HTML

-----------------------------------------------------------------------------------------

This is a git practice with mosh 
---
# Git commands used in windows bash terminal
### Global config
- git config --global user.name "username"
- git config --global user.email xxx@gmail.com
- git config --global core.editor "code --wait"
- git config --global -e
- git config --global core.autocrlf true 
  - this is for windows (if mac there is input instead of true)
### Initial workflow
- git init  
- ls -a 
- open .git
- echo hello >file1.txt
- echo hello >file2.txt
- git status
- git add *.txt  / git add . 
- git status
- echo world >>file1.txt
- git status
- git commit -m "Initial commit"
- git status
- echo test >> file1.txt
- git commit -am "Fix the bug that prevented the users for signing up."

  ### Remove a file
- rm file2.txt
- git status
- git ls-files
- git add file2.txt
- git ls-files
- git status
- git commit -m "Remove unused code"
- git rm file2.txt

### Renaming or Moving Files
- mv file1.txt main.js
- git status
- git add file1.txt
- git add main.js
- git mv main.js file1.js
- git status
- git commit -m "Refactor code"

### Ignoring Files
- mkdir logs
- echo hello >logs/dev.log
- git status
- echo logs/ >> .gitignore
- git status
- git add .gitignore
- git commit -m "Change gitignore"
- mkdir bin 
- echo hello >bin/app.bin
- git add .
- git commit -m "Add bin."
  - add bin/ in the gitignore
- git status
- git add .gitignore
- git commit -m "Include bin/ in gitignore"
- echo helloworld >bin/app.bin
- git ls-files
- git rm -h
- git rm --cached -r bin/
- git ls-files
- git status
- git commit -m "Remove the bin directory that was accidentally committed"
###  Short Status
- git status -s 
- echo sky >> file1.js
- echo sky > file2.js
- git status
- git status -s 
  - M README.md
  - M file1.js
  - ?? file2.js
- git add file1.js
- git status -s 
- git add file2.js
- git status -s 
- git add README.md
- git status -s 
- echo ocean >>file1.js
- git status -s 
  - M  README.md
  - MM file1.js
  - A  file2.js
### Veiwing the Staged and Unstaged Changes
- 
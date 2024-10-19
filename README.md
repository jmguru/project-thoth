# Lesson Summary for 10/17

## Visual Code
* Summarized some basic features
* Talked a little about MarkDown
## Github operations
### Cloning
#### This clones the repo and the 'main' branch to a directory called 'Project0-OOP'
  ```
  git clone git@github.com:bellag10/Project0-OOP.git
  ```
#### This clones the repo and 'main' branch to directory called 'MyProject'
  ```
  git clone git@github.com:bellag10/Project0-OOP.git MyProject
  ```
#### This clones the repo and a branch called 'BGProject' into directory BGProject
  ```
  git clone -b BGProject git@github.com:bellag10/Project0-OOP.git BGProject
  ```
  Be sure to change into the cloned repo directory. When your doing git commands, be sure to be at the top directory of the clone. 
  ```
  cd BGProject
  ```
### Making changes directly to the `main` branch
#### Add the files that need to be committed to main
This shows three different ways to add files. One, multiple in different directories, and all contents in a specific directory, respectively
  ```
  git add src/main/app.py
  git add src/datastore/dbdriver.py data/konkkonk.csv
  git add docs/
  ```
Note: There's a way to tell git to ignore certain files using `.gitignore` file which just is a text file with a list of file paths. 

This shows how to remove files. Don't use shell command `rm`. Use the `git rm`. It will delete the files and mark them as deleted in git.
  ```
  git rm src/main/crud.py
  ```
Remove an entire directory using the recursive flag
  ```
  git rm -r junk/
  ```
This shows how to move files
 ```
 git mv src/main/gigi.py src/data/store/gigi.py
 ```
#### Check the state your your git ops. This will show you what's not tracked, what's tracked, and new files. It will also show you what branch you are in. 
  ```
  git status
  ```
This shows how to reset all of your changes to start again. Check the status afterwards. 
  ```
  git reset
  git status
  ```
#### Commit your changes and a comment using -m and append the command like so
  ```
  git commit -m 'Making changes for issue 1223'
  ```
#### Push your changes to main
  ```
  git push
  ```
### Making changes directly to specific branch for a pull request (most common use case)
  Change directory into cloned repository and run git command to 'checkout' or create a new branch called 'Changes-for-issue1223'
  ```
  cd BGProject
  git checkout -b 'Changes-for-issue1223'
  ```
  Now add and commit your files
  ```
  git add src/datastore/dbdriver.py data/konkkonk.csv docs/
  git status
  ...
  git commit -m 'Making changes for issue 1223'
  ```
  Now push to the files to the new branch. If you forget, use `git status` to see what branch you're on. 
  ```
  git push origin Changes-for-issue1223
  ```
## Home work
  - Create a new branch copy of datathon in the same repository
  - Practice create a mock PR or an actual change to our copy of datathon.
## Next time:
- More practice of command line

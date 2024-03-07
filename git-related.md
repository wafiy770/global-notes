
```
git --version
```

--> common terms
- repositories
- clone
- staging
- commit
- branch
- merge
- pull
- push

initialize git on a folder --> repositories
modified files --> stage --> commit (commit: git store permanent snapshots of the files)

--> configure git
```
git config --global user.name "yourusername"
git config --global user.email "your@email.mail"
```

use global to set for every repository on local
remove global to set ONLY for current repository

--> initialize git
```
mkdir <your_folder>
cd your_folder
git init
```

--> git status

tracked files: files already added inside repo
untracked files: files in working directory but not yet added inside repo

adding, editing and removing files
--> after finish a specific milestone
	--> should add the files to Staging Environment

staged files: READY to be committed to the repo
```
git add filename.file
```

all changed/added/deleted files
```
git add --all
```

committed files as in a save point
```
git commit -m "Your message that should be very descriptive"
```

```
git status --short
```

?? / A / M / D filename.file
- ??: untracked files
- A:  files added to stage
- M:  modified files
- D:  deleted files

see the logs
```
git log
```

```
git help --all
```
very long list, instead use
```
git -help
```
eg: 
```
git status -help
```

navigating the list view

shift + G --> jump to end of list
q --> to exit view

--> create a new branch
```
git branch <your_branch_name>
```

--> list out the branches and where you at
```
git branch
```

--> to move between branches
```
git checkout <branch_name_you_want_to_move_into>
```

--> switch to and create a new branch straightaway
```
git checkout -b <move_into_this_newly_created_branch>
```

--> for merging
- always to to the master first
- and then only,
```
git merge <branch_name_you_want_to_merge>
```

but make sure the changes inside the branch are already committed

--> delete unrequired branch afer merging
```
git branch -d <branch_name_you_want_to_delete>
```

- fetch: updates to see what has changed on GitHub
- merge: merge the changes
- pull: fetch then merge

but need to set the origin url first?

- origin/master: web version of master
- master: local version of master

--> to pull
```
git pull origin
```

--> to push (after the changes have been committed
```
git push origin 
```

local git and github
--> to see all local and remote branches
```
git branch -a
```

--> to see remote only
```
git branch -r
```

--> to pull the branch
```
git checkout <branch_you_want_to_pull_into_local>
git pull <branch_you_want_to_pull_into_local>
```

--> to push a local branch to github
be on the branch
```
git push origin <branch_name_you_want_to_push>
```

--> compare & pull requests
- to go through the changes made

--> pull request
- review changes, so others can pull your branch and merge into theirs

general flow
1. create a new branch
2. make changes and add commits
3. open a pull request
4. review
5. deploy
	 github allows you to deploy from a branch for final testing in production before merging with the master branch
6. merge

#### Create git folder

if from portal
- create folder from portal
- copy url link
```
git clone <url_link>
cd local_path/<folder_name_created_in_portal>
git add.
```
- check the added files
```
git status
```

```
git commit "<write_your_comments>"
```









synapse pipeline
-----------------

parameterized --> opposite of hardcoding something aka dynamic

wildcard file path
--> 

copy method
--> polybase: parallel
--> copy command: 


pre-copy script
--> sql commands that runs before the activity runs

debug
--> runs the pipeline currently on modification not what's published
--> to run the last published pipeline use add trigger --> trigger now
--> the red circle that if you clicked becomes full circle is called breakpoint
	--> run the pipeline until the activity that is marked as breakpoint


--> azure devops homepage
https://dev.azure.com/4fingersmy/



* */5 * * * *


0 0 17 * * *

rymnetafter
0 10 18 * * *




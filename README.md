#GIT summary
working directory	||	staging area	|| Local repo 	|| 	remote repo
					=>					=>				=>
				  git add 			git commit 		 git push
					<=					<=				<=
				  git reset 						 git pull
									 git pull		 git fetch

https://ohshitgit.com/


# generate & test public key
## Generate Key
ssh-keygen -t rsa -b 4096 -C "Your GitHub Email Here"

# Get Key To Copy
cat ~/.ssh/id_rsa.pub

# Same Command Example in Windows
cat C:/Users/elmog/.ssh/id_rsa.pub

# Test Key And Connection
ssh -T git@github.com

# .gitignore & Show All Configurations
*.log
!vip.log
node_packs/
text.txt

# Show User Email
git config --global user.email

# Change User Email
git config --global user.email "Your Github Email Here"

# Edit Configuration
git config --global --edit

# Create New File
touch "File Name Here"


# install github cli for cmd line

# basics
## create a new repository on the command line
# Initialize & create Empty Git Repository
touch README.md
git init
git add *
# commit to local repo
git commit -m "first commit"
# change main/master branch name to main instead of master "optional"
git branch -M main
# create repo on my github
gh repo create "repo-name" --public
# specify the origin as a target remote
git remote add origin https://github.com/elmoghany/"repo-name".git
Or
git remote set-url origin git@github.com:elmoghany/css-refresher.git
# debug addition status of git remote in case of failure "optional"
git remote -v
# upload to my new repo
git push -u origin main

# cloning a project from git
git clone https:// ...

# Add Files
git add <File> <File>
git add *.extension
git add *

# Show Status
git status

# remove things added by git add
git reset
git reset <file>

# Show Log File
git log
git log tofile

# Commit File
git commit -m "Your Commit Message Here"
git commit --amend	#modify latest commit instead of new one

# set the remote repo you wroking with
git branch --set-upstream-to <origin>

# Add Repository
git remote add origin "SSH Repository URL"

# Example
git remote add origin "git@github.com:elmoghany/Course.git"

# Push Data to repo
git push
git push <repo> <branch>	
git push -u origin master
git push origin main

# Pull Changes From Remote Repository
git pull origin
git pull	
git pull <repo> <branch>	

git fetch	#does not do any change ... only get changes
git pull does the change

# Show All Tags
git tag

# Add New Lightweight Tag
git tag "Version Name Or Tag Name Here"

# Add New Annotated Tag
git tag -a "Version Name Or Tag Name Here" -m "Description Or Message"

# Push Tag To Remote
git push origin "Tag Name Here"

# List All Tags Starting With v1.
git tag -l "v1.*"

# Delete Tag
git tag -d "Version Name Or Tag Name Here"

# Delete Tag From Remote
git push origin --delete "Version Name Or Tag Name Here"

# Create Branch And Switch To It
git checkout -b "Branch Name"

# Move / Rename Branch
git branch -m "New Branch Name"

# Merge Branch With Current Branch
git merge "Branch Name You Need To Merge"

# Switch To Branch
git checkout "Branch Name"

# branches
# Show Log File
git log

# Reset Head
git reset --hard "Commit Hash Here"

# Push Edits From Local To Remote With Force Flag
git push origin main --force

# Show Branches
git branch
git remote -v

# Switch To Branch
git checkout "Branch Name"

# Delete Branch
git branch -d "Branch Name"

# Create Branch And Switch To It
git checkout -b "Branch Name"

# Move / Rename Branch
git branch -m "New Branch Name"

# Merge Branch With Current Branch
git merge "Branch Name You Need To Merge"

# delete
# Show Files That Will Be Cleaned
git clean -n

# Remove Un Needed Files
git clean -f

# stash
# Create Text File With "Hello World" String Inside It
echo "Hello World" > about_readme.txt

# Save Work To Stash
git stash

# List Items in Stash
git stash list

# Get Work From Stash
git stash pop

# Save Work To Stash
git stash

# List Items in Stash
git stash list

# Get Work From Stash
git stash pop

# Save Work To Stash With Description
git stash save "Description Here"

# Get Specific Stash
git stash pop stash@{2}

# Delete Stash
git stash drop stash@{1}

# Show Lastest Added Stash Content
git stash show

# Show Specific Stash Content
git stash show stash@{1}

# Empty The Stash
git stash clear

# Restore Staged Files
git restore --staged "File Name Here"

# Show Files That Will Be Cleaned
git clean -n

# Remove Un Needed Files
git clean -f

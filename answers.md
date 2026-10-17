# Git Assignment — Answers

# 1. What is a terminal? How is it different from clicking through folders in a file explorer?
terminal lets us control the computer by typing commands instead of clicking buttons
File Explorer lets us open and manage files and folders by clicking while terminal gives us commands to manager files

# 2. Write the terminal command to:
 (a) list all files including hidden ones, 
ls -a

 (b) create a folder called project , 
mkdir project

 (c) move into that folder.
 cd project


# 3. What does the cd .. command do? What about cd ~ ?
cd .. takes us one folder back or to the parent folder
cd ~ moves to the home folder

# 4. Explain what version control is in your own words. Give one real-world analogy (not Google Docs — pick your own).
version control tracks changes in the files and lets us restore an older version if needed
example analogy: canva

# 5. What is the difference between Git and GitHub? Can you use Git without GitHub?
git is a tool to track files in our computer while github is the platform where we can use it to collaborate with others
we can use git without github on our computer

# 6. Name three features GitHub provides that Git alone does not.
1. pull requests
2. collaboration
3. resolve conflicts

# 7. What is a repository? What is the difference between a local repository and a remote repository?
repository is where project and history is stored
local repository is tored on our computer
remote repo is stored on platform like github

# 8. Explain what HEAD means in Git. What happens to HEAD when you switch branches?
head points to current commit we are working on
when we switch branch, head points to the new branch's commit

# 9. What is a .gitignore file? Write a .gitignore that ignores: all .log files, a folder called node_modules/ , and any file ending in .env .
.gitignore file tells git which files and folders to ignore so they are not tracked
*.log
node_modules/
*.env

# 2.2.6. In answers.md , explain: Why did we commit A+B separately from C? When would you want to split commits this way?
we commit features A+B separately from C beacuse these are different features and we want to keep the commit history clean for later cleaning or debugging purposes

# 2.3.6. In answers.md , answer: What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
my local and remote branch would cause merge conflict
use git fetch to check remote changes before pushing

# 2.2.9. In answers.md : Did this merge create a merge commit or was it a fast-forward? How can you tell?
it created fast forward, I can tell because there is no extra merge commit on log

# Why did this conflict happen? (Reference the rule: same file, same line) Would there have been a conflict if the two branches edited different lines of team.txt ? Would there have been a conflict if one branch edited team.txt and the other edited about.md ?
The conflict happened because both branches edited the line 2 in team.txt

No there would be no conflict if the branches edited different lines of team.txt

No there would be no conflict if one branch edited team.txt and the other edited about.md



# What is the purpose of a pull request? Why not just merge directly? Name two things a reviewer should check in a pull request. What is the difference between a merge commit and a fast-forward merge?
A pull request lets others review changes before merging

Whether the code works correctly.
Whether the code is readable and has no obvious errors.

A merge commit creates a new commit to combine two branches. A fast-forward merge simply moves the branch forward without creating a new commit.

# Part 5 — Merge Conflict Scenarios (10 marks)
No coding here — read each scenario and write your answers in answers.md . 2 marks per
question.

# Scenario A. Ahmed creates a branch and changes line 10 of index.html . Sara creates a different branch and changes line 1 of the same index.html . Both merge into main . Will there be a conflict? Why or why not?

No there will be no conflict if ahmed and sara changed different lines in the same file

# Scenario B. Ali edits style.css on his branch. Fatima edits app.js on her branch. Both merge into main . Will there be a conflict? Why or why not?
No beacuse ali and fatima changed different files


# Scenario C. DevA changes line 5 of config.py to DEBUG = True . Dev B changes line 5 of config.py to DEBUG = False . Both merge into main . Will there be a conflict? If yes, show exactly what the conflict markers would look like in the file.
yes there will be a conflict because both changed same lines


# Scenario D. You run git merge feature/new-ui and see this output:
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
Write out the exact steps (commands included) you would take to resolve this conflict
and finish the merge.

open index.html and find conflict markers
edit file to keep correct changes
remove conflict markers and save
then stage and commit and check status

we can also do it by checking conflicts on github, ask any ai model to rewrite the correct code resolve conflicts and merge again


# Scenario E. Your teammate says: "I always do git pull before I start working every morning." Is this a good practice? Explain why or why not, and what could go wrong if they skip it.
yes it is a good practice beacuse it gets the latest changes from remote if avaialable
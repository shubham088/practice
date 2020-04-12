This is just for practicing git commands.

1} create a git repo using :   git init

2} add some files in the project and check : git status
   it will show us tracked and untracked files
   
3} if untracked.... : git add .   => adds all the files 
                      git add filenames   => to add individually
                      
4}  commit the changes    : git commit -m"commit message"

5}  git remote add origin git@github.com:username/new_repo

6}  git push -u origin master

Now the files will be added to branch master.

to list all the branches we can check : git branch

Now, if we want to make new branch and work on it to make some modification we need to take all the files present in master to new branch.
so, we will do 

git checkout -b <new_branch_name>

eg. git checkout -b branch1

Now, we will be switched to branch branch1 with all the files in master.

Now we will add some files in the branch branch1.
again we will repeat the process of 

git add

git commit

git push origin branch1

Similarly we can create more branches like branch2, demo.

Suppose somebody else is also working on branch1 and he/she updated the files. But on my local machine that updation is not present.
So, to pull the changes from server(github repo) to our local system we will do

  -> we will checkout to branch1 first if we are at some other branch
  
    git checkout branch1
    
    then, 
    
  ->git pull origin branch1

Suppose we have updated the branch branch1 and branch2 with all the modifications.Now, its time to test . so , we could merge the 
files to demo branch for testing.
so what we will do is:

-> git checkout demo 

will move to the branch where we need to merge

-> git merge branch1

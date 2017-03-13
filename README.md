# Use-Git

Untrack Files In Git Repos Without Deleting Them

1. Do this on all machines

    echo "FILE_NAME" >> .gitignore

    git rm --cached FILE_NAME

    git add -u

    git commit -m "removing files from version control"

2. Sync with your git server, pull to sync and push to register your local change

    git pull

    git push
    
Merge changes from other to master
    
    #set new branch and change to this new branch
    git checkout -b new-branch
     
    #merge the changes in new-branch to master 
    git merge --no-off new-branch
 
    #change branch
    git checkout -b bioinformatics-gao-patch-1 master
    git pull https://github.com/bioinformatics-gao/PathwaySplice.git patch-1    
    
    #Change back to master
    git checkout master    
    git merge --no-ff bioinformatics-gao-patch-1
    git push origin master

Others
http://www.interviewadda.com/shortest-path-nodes-binary-search-tree-bst/



#Rename a local and remote branch in git

1. Rename your local branch.
If you are on the branch you want to rename:

git branch -m new-name

#If you are on a different branch:

git branch -m old-name new-name

2. Delete the old-name remote branch and push the new-name local branch.

git push origin :old-name new-name
3. Reset the upstream branch for the new-name local branch.
Switch to the branch and then:

git push origin -u new-name

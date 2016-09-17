# Use-Git

Untrack Files In Git Repos Without Deleting Them

## Do this on all machines

echo "FILE_NAME" >> .gitignore

git rm --cached FILE_NAME

git add -u

git commit -m "removing files from version control"

## Sync with your git server, pull to sync and push to register your local change

git pull

git push

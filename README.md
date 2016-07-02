# Something about github and jekyll
collected knowledge about github and jekyll

## Github commands for terminal

* Clone a git repo to desktop in the selected directory
```
git clone https://github.com/tranzexact/landing-page.git
```
* Compare status between local repo and git repo
```
git status
```
* Add any changes or new file by name (waiting to be committed) or use "-A" for all files
```
git add index.html
git add -A
```
* Commit the new changes into the repo
```
git commit -m "added index.html"
```
* Push any new commit to github.com
```
git push
```
* Pull the latest version of the repo from github.com
```
git pull
```
### Daily workflow
1. Use git pull to get all the latest changes
2. Make changes you need to on the local file
3. Add > Commit with comments after every major changes
4. Use git pull every couple of hours each day to stay update

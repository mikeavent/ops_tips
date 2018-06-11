----------------------
Notes, Tips and Tricks
----------------------

# Command Line Keyboard Shortcuts

- crtl a = back to beginning
- crtl e = back to end
- crtl k = deletes everything in front of the cursor
- crtl u = deletes everything behind the cursor
- crtl l = clears everything but the line you're on
- crtl w = deletes one word at a time
- crtl t = switches spots
- crtl d = deletes one spot in front of cursor
- crtl h = deletes one spot behind the cursor
- crtl p = show last command (same as up arrow)
- alt f = skip on word forward
- alt b = skip on word backword
- cat /etc/passwd = view all users
- cat /etc/group = view all groups
- pushd /directory_to_go_to
- popd (to go back)
- usermod -a -G groupname username = add user to group
- bash -x whatever_script.sh = for debugging scripts
- du -sh
- df -i
- date +%s = unix timestamp 
- ps -aux = list all processes

# SFTP
- sftp -o "IdentityFile=keyname" some@server.com

# Resize command line
- stty -a = to check current size
- stty rows 136 cols 152 (Portrait screen) 
- stty rows 76 cols 272 (Landscape screen)

view process history
- sudo vim /var/log/syslog (ubuntu)
- sudo vim /var/log/messages (centos)

# VIM
- : se nu (set number) = see line numbers
- : ctrl f = page forward
- : ctrl b = page backward
- : set paste = paste without it going crazy
- : set nopaste = go back to normal
- : / "keyword" n to go to next
- : se ru (set ruler = line number, column number (and more)

# Docker
docker ps -a = view docker containers on instance
docker exec -it c9ce21e003fc bash = login to container
docker system prune

# AWS CLI 
copy s3
aws s3 cp --recursive ~/Documents/someplace/ ~/tosomeplace

netstat -tulpn
AWS CLI 
If on root and you want to see other cronjobs
$ cronjob -e -u "name of user"ls

-------
GIT
-------
# Git commands for migration to AWS CodeCommit:

$ git branch -a
$ git checkout (each branch)
$ git fetch --tags
$ git remote rename origin upstream
$ git remote add origin url_of_new_repo
$ git remote rm upstream
$ git push origin --all (pushes all branches)
$ git push --tags

# Remove upstream:
$ git remote rm upstream

$ git remote add upstream url_of_repo

To view origin and upstream:
$ git remote -v

# List all tags
$ git tag

$ git fetch --all
$ git branch -u origin/<branch>

# See log history:
$ git log -- "filename"


- git reset head~
- git branch -d the_branch
- git ls-tree -r --name-only <branch> (list how many files)
or
- git ls-files


git branch --set-upstream-to=origin/<branch>

# Reset to a specific branch
$ git reset --hard "commit_number"

# Force push to origin
$ git push origin +"branch"

# Crontab
as root view other user crontabs:

$ crontab -l -u "user"

# Links to docs and tutorials
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/set-time.html


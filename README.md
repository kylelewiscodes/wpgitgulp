# wpgitgulp
My Wordpress Git/Gulp Set-up that works.

New Project:
Remote Server/Host:
SSH into server/host and cd to remote wp install
Git init
Git config receive.denyCurrentBranch ignore
cd .git/hooks/
nano post-receive
type #!/bin/sh
	GIT_WORK_TREE=../ git checkout -f
	Ctrl+x
	Y to save
	Enter
 chmod +x ~/public_html/REPO-NAME/.git/hooks/post-receive
 Copy of .gitignore files to both the local and remote server before doing any adds or commits.
    !SERVER IS DONE!

Local Host(Main Owner of Project):
Create Database (if only you working on this project same prefix as remote)
Create Folder for site on local host (i.e. www for WAMP, htdocs for XAMP)
Install Wordpress (for us it’s wp core download from git bash)
Drag over base framework and gulp files
From inside the base framework/theme folder run npm install gulp
npm install
Load wp_db_sync Plugins (only if you are the only one doing dev on the site)
Open git bash in the main wp install folder
git init
git remote add origin ssh://username@host:port/~/public_html/REPO-NAME/
git add -A
git commit -am ‘Initial Commit’
git push origin master



Local Host(Other Dev):
git clone
Create Database (if only you working on this project same prefix as remote)
Create Folder for site on local host (i.e. www for WAMP, htdocs for XAMP)
Install Wordpress (for us it’s wp core download from git bash)
Run WP install by visiting the local directory OR import the database from the remote

Active Project:
Remote Server/Host:
SSH into server/host and cd to remote wp install
Git init
Git config receive.denyCurrentBranch ignore
Cd .git/hooks/
Nano post-receive
type #!/bin/sh
GIT_WORK_TREE=../ git checkout -f
Ctrl+x
Y to save
Enter
Chmod +x ~/public_html/REPO-NAME/.git/hooks/post-receive
Copy of .gitignore files to both the local and remote server before doing any adds or commits.
Git config user.name and email (git will prompt you do this otherwise)
Git add -A
Git commit -am ‘Initial Commit’


Local Host(Main Owner of Project):
Create Database (if only you working on this project same prefix as remote)
Create Folder for site on local host (i.e. www for WAMP, htdocs for XAMP)
Git clone ssh://username@host:port/~/public_html/REPO-NAME/
Install Wordpress (for us it’s wp core download from git bash)
Drag over base framework and gulp files
Npm install gulp
Npm install
Load wp_db_sync Plugins (only if you are the only one doing dev on the site)

The wp.rar file is wp_cli (this is opitional).
I just have it ready to use on windows.

The Git and Gulp should be universal it's tested and working on Windows as that's what I use.

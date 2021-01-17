# redirects-cli
CLI Tool for Creating Redirects

How does it work

## Setup

Create a repo from this template
[template coming soon]

Go to index.html and replace {githubUsrName} with whatever name you want

```
$ redirects link [github repo]
```

For example
```
$ redirects link okistuff/redirects
Linking to okistuff/redirects
Link Complete!
```

Now time for setup
```
$ redirects setup
(Leave Answer Field Blank to use the Default answer if there is one)
Where would be a good place for me to use as a Temp Folder? [Default: C:/Program Files/okistuff/redirects-cli/temp/]: 
Where would be a good place for me to use as a Backup Folder? [Default: C:/Program Files/okistuff/redirects-cli/backup/]:
Where would be a good place for me to use as a Data Folder? [Default: C:/Program Files/okistuff/redirects-cli/data/]:
Do you want your redirect files to be backed up? [Y/N, Default: Y]:
Do you want a redirects directory viewer be created in index.html? [Y/N, Default: Y]:
Do you have git installed. [Y/N, If N(O) then setup will stop]: Y
Cloning [githubUsername]/[githubRepoName] into my Temporary Folder (git)
{response goes here}
Updating Files
Cleaning Temporary Folder
Saving Settings into my data folder
Complete!
```

## How to use

```
$ redirects new [public/priavte] [name] [link]
Creating .redirect file
Complete, Please Run redirects gen to generate the web page files!
```

For Example:

```
$ redirects new public Example_Webpage https://example.com
Creating .redirect file
Complete, Please Run redirects gen to generate the web page files!
```

You can use _ instead of spaces! redirects-cli will convert them to spaces

Then, Generate the files

```
$ redirects gen
(Leave Answer Field Blank to use the Default answer if there is one)
Cloning okistuff/redirects into my Temporary Folder (git)
{git response goes here}
Scanning for .redirect files
FOUND [1] REDIRECT FILE
Copying Example_Webpage.redirect => /backup/ as Example_Webpage.redirect.old
Backing up Complete!
Generating files for Example_Webpage.redirect...
Generated redirect.js
Generated index.html
Generated info.html
Generated info.css
Generated sleep.js
Complete!
Would you like to push now or push later with redirects push? [Y/N, Default: Y]:
Cleaning up my Temporary Folder
Staging Changes
Commiting Changes with Message "Generated 1 Redirect"
Pushing Changes
{git response goes here}
Complete!
```

You can answer N to pushing now if you want to create more redirects before pushing
if you do when you are complete run
```
$ redirects push
Cleaning up my Temporary Folder
Staging Changes
Commiting Changes with Message "Generated Redirect Files"
Pushing Changes
{git response goes here}
Complete!
```


Thats basically it!!!!

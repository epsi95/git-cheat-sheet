### Git clone
`$ git clone https://github.com/libgit2/libgit2 <destination directory, optional(it will create a directory named libgit2 if not specifies)>`

---

### Lifecycle of a file in git
Remember that each file in your working directory can be in one of two states: tracked or untracked. Tracked files are files that were in the last snapshot; they can be unmodified, modified, or staged. In short, tracked files are files that Git knows about.

Untracked files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area. When you first clone a repository, all of your files will be tracked and unmodified because Git just checked them out and you haven’t edited anything.

As you edit files, Git sees them as modified, because you’ve changed them since your last commit. As you work, you selectively stage these modified files and then commit all those staged changes, and the cycle repeats.
![lifecycle](../images/lifecycle.png "lifecycle")

---

### Git Status
`$ git status`

### Git short status notation
`$ git status -s`\
`?? means files that are not tracked`\
`A means file that has been added to the staging area`
`M means modified file`

---
### Ignoring files using gitignore
comprehensive list
https://github.com/github/gitignore

add then to `.gitignore` file

---

### Git status shows generic status to see specific status use
`$ git diff`

That command compares what is in your working directory with what is in your staging area. The result tells you the changes you’ve made that you haven’t yet staged.

---
### If you want to see what you’ve staged that will go into your next commit, you can use 
`$ git diff --staged`

 This command compares your staged changes to your last commit. git diff --cached to see what you’ve staged so far (--staged and --cached are synonyms)

 ---
### To use a diff tool use
`$ git difftool`

It wil launch a tool based on os

---

### Commit the staged files
`$ git commit`

It will start vim editor with git status message as message. To add differences additionally use

`$ git commit -v`

---

### Skipping the Staging Area
`$ git commit -a -m "commit message"`
It remove the need to `git add`

---

### Removing Files
`$ git rm <file_name>`

The next time you commit, the file will be gone and no longer tracked. If you modified the file or had already added it to the staging area, you must force the removal with the -f option. This is a safety feature to prevent accidental removal of data that hasn’t yet been recorded in a snapshot and that can’t be recovered from Git.

Another useful thing you may want to do is to keep the file in your working tree but remove it from your staging area. In other words, you may want to keep the file on your hard drive but not have Git track it anymore. This is particularly useful if you forgot to add something to your .gitignore file and accidentally staged it, like a large log file or a bunch of .a compiled files. To do this, use the --cached option:

`$ git rm --cached <file name>`

---

### Moving Files

`$ git mv file_from file_to`

---











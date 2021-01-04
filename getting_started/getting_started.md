### 3 Stages of git
Git has three main states that your files can reside in: modified, staged, and committed:

`Modified` means that you have changed the file but have not committed it to your database yet.

`Staged` means that you have marked a modified file in its current version to go into your next commit snapshot.

`Committed` means that the data is safely stored in your local database.

![3 stages of git](../images/areas.png "3 stages of git")

* Git does include for each commit a full copy of all the files, except that, for the content already present in the Git repo, the snapshot will simply point to said content rather than duplicate it.
That also means that several files with the same content are stored only once.

---

### You can view all of your settings and where they are coming from using:
`$ git config --list --show-origin`

---

### See all global configs
`$ git config --global --list`\
`http.proxy= <proxy>`\
`user.name=Probhakar Sarkar`\
`user.email=<email>`\
`core.editor=emacs`\
`init.defaultbranch=main`

### Set a global config
`$ git config --global core.editor vim`

---

### Set your identity
`$ git config --global user.name "Probhakar Sarkar"`\
`$ git config --global user.email <email>`

*  If you want to override this with a different name or email address for specific projects, you can run the command without the --global option when you’re in that project.

---
### To set main as the default branch name do:
`git config --global init.defaultBranch main`

---

### To get help documentation
`$ git help <verb>`

---




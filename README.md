# git for dummies

```
$ git clone [url]
```

download a copy of a git project that already exists, using the url of a github repository <br/>

<details>
<summary>see: what is difference between git clone and git init?</summary>

git clone is basically a combination of:

- `$ git init` (create the local repository)
- `$ git remote add` (add the URL to that repository)
- `$ git fetch` (fetch all branches from that URL to your local repository)
- `$ git checkout` (create all the files of the main branch in your working tree)
</details>

<hr>

```
$ git status
```

show the working tree status (if there's a new file or a modified one, and if it's already added or not, etc)

<hr>

```
$ git add
```

prepare the file to be commited

<details>
<summary>see: adding multiple files</summary>

- `git add [file]` (add a particular file to index)
- `git add [directory]` (add an entire directory to index)
- `git add .` (indexes all the new and modified files, except for the files that have been removed)
- `git add –u` (indexes all modified and removed files, except for the new files created)
- `git add –all` (indexes all new, modified and removed files, it is a combination of both `git add .` & `git add -u`)
</details>

<hr>

```
$ git commit -m "[descriptive message]"
```

make a commit with a message.

<details>
<summary>see: commit message conventions</summary>

```
[type][optional scope]: [description]

example:
  feat: add login-page.html
```

Allowed [type] values:

- **feat:** for a new feature for the user, not a new feature for build script. [✨]
- **fix:** for a bug fix for the user, not a fix to a build script. [🐛]
- **perf:** for performance improvements. [⚡]
- **docs:** for changes to the documentation. [📝]
- **style:** for formatting changes, missing semicolons, etc. [🎨]
- **refactor:** for refactoring production code, e.g. renaming a variable. [♻️]
- **test:** for adding missing tests, refactoring tests; no production code change. [🧪]
- **build:** for updating build configuration, development tools or other changes irrelevant to the user. [📦️]

for more emojis, see: https://gitmoji.dev/

</details>
  
<hr>

```
$ git push
```

send the commits to a github repository

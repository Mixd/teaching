# Version Control

## [GitHub Student Pack](https://education.github.com/pack)
A great __FREE__ pack from GitHub, that gives you some great stuff for web development (amongst other industries). We'd suggest getting it for:

* [Sublime Text](http://www.sublimetext.com/): technically free, because there isn't a time limit on the trial
* [Atom](https://atom.io/): Still in its infancy, but a solid IDE for web development. Unlike other IDEs, it's __FREE__.
* [Digital Ocean](https://www.digitalocean.com/): A solid hosting company for web developers. With the student pack, you'd get $100 credit; which depending on the package you choose is between 10-20 months free hosting!
* [GitHub Micro](https://github.com/): Gives you unlimited private repositories for free; which would usually cost £4 a month.

## Version Control / Git GUI's
Interacting with Version Control typically works best straight from terminal / commandline, but to get started you might be more comfortable using one of the following apps.

* [SourceTree](http://www.sourcetreeapp.com/) (Windows + Mac)
* [Tower](https://www.git-tower.com/) (Windows + Mac)
* [GitHub Desktop](https://desktop.github.com/) (Windows + Mac)
* [Cornerstone](https://cornerstone.assembla.com/) (Mac)

## Tutorials
* [Try](https://try.github.io/levels/1/challenges/1): from GitHub themselves...a good basic introduction to interacting via. command line.
* [CodeSchool](https://www.codeschool.com/courses/git-real): Nice step-by-step tutorial
* [Codeacademy](https://www.codecademy.com/learn/learn-git)

## Interacting with Git...commandline

GitHub have a really useful [cheat sheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)that lists the most commonly used commands. Below is a few specific tips to highlight them even more.

### [`git clone --recursive [url] [folder]`](https://git-scm.com/docs/git-clone)

eg. `git clone --recursive https://github.com/Mixd/teaching witw`

Above example will clone our [teaching repo](https://github.com/Mixd/teaching) into a new folder called __witw__. The `--recursive` flag is a good habit to get into, as it will make sure that any included submodules are also cloned down.

You'd most likely use this when you've been asked to work on a pre-existing project for the first time.

### [`git checkout [branch]`](https://git-scm.com/docs/git-checkout)

eg. `git checkout development`

This is the command that allows you switch between branches. Your local repo will need to mirror branches that already exist...the above example would only work if a branch exists called __development__.

It's mentioned this early on purpose, because you always want to make sure you're doing your work on the correct branch: typically a 'feature' branch or __development__.

### [`git pull`](https://git-scm.com/docs/git-pull)

A command to get into good habits with. It will pull down any changes that others have made.

If you've already got a repo locally, it's smart to do a pull before you start any work...just to make sure you've got every commit since you last worked on it.

### [`git status`](https://git-scm.com/docs/git-status)

Another good habit. Run to be told which files have been changed. It'll tell you (in red) files that have been modified, added, deleted or renamed. It'll also tell you (in green) of files you've already staged.

### [`git diff [file]`](https://git-scm.com/docs/git-add)

eg. `git diff /content/themes/mixd/header.php`

A command that'll give a crude output of what has changed in a file. Typically, plugins like [GitGutter](https://github.com/jisaacks/GitGutter) for Sublime Text can give you better visual cues as to what's changed.


### [`git add -A [file]`](https://git-scm.com/docs/git-add)

eg. `git add -A content/themes/mixd/header.php`

You can run `git add -A` without specifying a file to just add everything you saw in `git status`. Or you can start typing something – eg. `cont` – and tab for it to auto-complete.

The `-A` flag is important as using it will ensure that added, deleted and renamed files are included in the add, not just the modified files.

### [`git commit -m "[message]"`](https://git-scm.com/docs/git-commit)

eg. `git commit -m "update header with more vertical padding"`

Whatever files you've included using `git add`, this is you committing them. Use the message (in quotes) to give a meaningful message of what you commit does. Doesn't have to be an essay, but you want to properly explain things.

### [`git push`](https://git-scm.com/docs/git-push)

Any commits you've yet to push to the remote repo, will now be sent.

### [`git merge [branch]`](https://git-scm.com/docs/git-merge)

eg. __whilst in master__ `git merge development`

Providing that there is no conflicts – eg. same line of same file edited – this will pull in any commits that one branch has but your current one doesn't. 

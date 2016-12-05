---
title: "Source- and File-sharing"
layout: page
---

When working together, we will sooner or later produce something
(hopefully). In the case of computer science, this usually means files
(duh!). Several improvements have been suggested over
[filenames-with-counter-via-email-attachment](http://www.phdcomics.com/comics/archive.php?comicid=1531).

# Filesharing

- centralized (DEPRECATED): owncloud, Dropbox (~5 GB), Google Drive (~15 GB), Novell Filr
  via UPassau's ZIM (~600 MB, mounted as `H:/`)
- distributed: [Resilio Sync](http://getsync.com) (formerly: Bittorrent
  Sync), [Syncthing](https://syncthing.net/)

# Sourcesharing

- public: [Github](https://github.com),
  [Bitbucket](https://bitbucket.com), [Gitlab](https://gitlab.com) (?),
  [Savannah](https://savannah.gnu.org) (?); TODO do the latter two offer
  public/private repositories?
- private: [local gitlab](https://gitlab.dimis.uni-passau.de)

## Setup

Github has its own
[tutorial](https://guides.github.com/activities/hello-world/).

1. Get a bitbucket/github/gitlab-account. In the latter case, send and
email to your adivsor, because he has to manually "activate" your
account. (The notification system for this is broken.)
2. Install the necessary software on your local computer (usually
`git`, `ssh`, and optionally some GUI).
3. Link your local machine with your bitbucket/github/gitlab-account. (You need to generate an SSH-key and
copy it to the settings.)
4. Clone your project.

### GUIs for git


If you don't want/like to interact via the command line, the git-webpage maintains an extensive list of [GUI
clients](https://git-scm.com/downloads/guis).

- [SourceTree](https://www.sourcetreeapp.com/) (Mac & Windows)
- [Github Desktop](https://desktop.github.com/) (Mac & Windows)
- [TortoiseGit](https://tortoisegit.org/) (Windows)

Field Report (git with gui on windows): Tried SourceTree at first and it
worked reasonably well, but I found the interface bloated (for our
purposes). Tried Windows on Git + TortoiseGit next (trade real GUI for
context-menu) and found that the
[instructions](https://blog.assembla.com/AssemblaBlog/tabid/12618/bid/77264/Setting-Up-Git-on-Windows-in-Four-Easy-Steps.aspx)
by Adam Feber worked almost out of the box. Thanks. I just had to
Shift-Right-Click to actually get/find the `clone` command, but that's
hopefully a one-time thing.

## Production Workflow

After the setup, your production workflow has three parts

1. Get the changes from the repository. (see "Pull" below)
2. Do the work
3. Copy your changes to the repository so that everybody else can see
them. (see "Commit & Push" below)


### Pull (before editing)

0. don't touch/open the project files yet
1. pull (and then close/minimize sourcetree)
2. OPTIONAL read log messages
3. browse with filemanager to the directory of your project and work
there

In the case of TortoiseGit, this is a right-click on the top-level
folder of your project and then "Pull"


### Commit & Push (after editing)

1. after you're done working, save and close all project files
2. if necessary open SourceTree
3. "Vormerken": mark all (changed) files that you want to upload
(exclude temporary files like Apples ... or auto-generated files like
'Thumbs.db')
3. "Commit" with a meaningful message
4. Push

In the case of TortoiseGit, this is a right-click on the top-level
folder of your project, then "Commit" -> "Msg" -> "Commit". Followed by
"Push" (and "Close").y

Q: Why are `commit` and `push` two separate steps?
A: There's a logical and a technical reason: maybe you want to
commit not all of your changes (but only some who fit logically well
together); maybe you're without internet connection (and thus can't push), but still want to "freeze" the current
state.

## Further Reading

- Read the [intro of the
  documentation](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
- Do this [tutorial](https://try.github.io/levels/1/challenges/1)
- Here's an exemplary
  [workflow](http://nvie.com/posts/a-successful-git-branching-model/)

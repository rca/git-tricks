git-tricks
==========

random things to make git work for you


Know where you are
------------------

```bash
export PS1='[\u@\h \W$(__git_ps1 " (%s)")]\$ '
```

https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh



Selectively pick parts of a file to commit
------------------------------------------

```bash
git add --patch
```


Interactive Rebase
------------------

```bash
git rebase -i
```

* Shuffle around commits to a more meaningful order
* "squash" commits together
* Change commit messages
* ...


The reflog is your safety net
-----------------------------

```bash
git reflog
```

This gives you an "out-of-band" history of every revision your
local repo has been in.  If a merge goes bad, or you accidentally
overwrite a commit, bad rebase, etc. you can always get back to
the last state.


The index / staging area
------------------------

It's not that magical; think about it as BEGIN / QUERY / COMMIT for version control.



## Git rebase and commit squashing exercise

### Objective

In this exercise we will practice how to squash incomplete commits into one
nice commit and replay it on top of the master branch.


### Motivation

This technique is useful in situations where you need to make changes to a pull
request before it can be integrated.


### Exercise

Start the exercise by forking and cloning the repository.

The `haiku` branch represents a feature branch that is to be rebased (moved) and squashed.

On the `haiku` branch you find a script that prints a haiku:

```shell
$ python main.py

This is our haiku:

On a branch ...
                  by Kobayashi Issa

              On a branch
              floating downriver
              a cricket, singing.
```

The haiku is great but the
commit history on
the `haiku` branch is not (on purpose):

```shell
$ git log --oneline

65870f9 fix a copy-paste error
47a007d completed the haiku
a3278e3 another incomplete commit
54fba21 startign to work on it (commit with a typo)
3ff39a1 forgot to add a file
7e1f903 starting working on the haiku
c50a463 initial commit
```

Your task is to rebase the `haiku` branch on top
of `master` and squash the several small "incomplete" commits into one single
self-contained cherry-pickable commit.

In other words instead of this history:

![alt text](https://github.com/bast/git-rebase-squash-exercise/raw/master/img/rebase-exercise-1.jpg "Exercise step 1")

we wish to arrive at this history:

![alt text](https://github.com/bast/git-rebase-squash-exercise/raw/master/img/rebase-exercise-3.jpg "Exercise step 3")

by first rebasing the commits:

![alt text](https://github.com/bast/git-rebase-squash-exercise/raw/master/img/rebase-exercise-2.jpg "Exercise step 2")

and later squashing them.

Verify the history and also that the script still works after the operation.

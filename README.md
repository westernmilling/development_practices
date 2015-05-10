# Western Milling Development Practices

First, read the [thoughtbot Guides](https://github.com/thoughtbot/guides/tree/master/best-practices).

These are pretty exhaustive and you shouldn't go wrong if you follow them.

In this repository you will find configuration files for the following tools:

- hound
- js-lint
- [rubocop](.rubocop.yml) ([repo](https://github.com/bbatsov/rubocop))
- scss_lint

## rubocop

The rubocop configuration comes straight from [hound](https://houndci.com/configuration).

There have been some changes, such as preferring hash rockets over Ruby 1.9
hash syntax.

You can download the YAML file [here](.rubocop.yml)

All pull requests must pass rubocop before merging, hound is used to validate
this during the `branch > pull request > review > rebase > merge` workflow.

## GitHub

We use GitHub for version control and follow these general good practices.

- [4 Ways to Avoid Merge Commits in Git (or How to Stop Being a Git Tit)](http://kernowsoul.com/blog/2012/06/20/4-ways-to-avoid-merge-commits-in-git/)
- [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
- [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/)
- [Git Interactive Rebase, Squash, Amend and Other Ways of Rewriting History](https://robots.thoughtbot.com/git-interactive-rebase-squash-amend-rewriting-history)

When working on a new branch you should make all of your regular commits as
additions (no `git commit --amend`) for greater visibility of changes during the review
process.

Once the review has been complete you must use `git rebase -i HEAD~#` and
squash all commits into a single commit using a good commit message using
the guidelines above.

## Workflow

We use the GitHub flow workflow, you can read more here:

- [GitHub Flow](https://guides.github.com/introduction/flow/)

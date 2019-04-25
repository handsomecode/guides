# Git Protocol

A guide for programming within version control.

Maintain a Repo
---------------

* Use [GitFlow] as a branch management strategy.
* Avoid including files in source control that are specific to your
  development machine or process.
* Delete local and remote feature branches after merging.
* Perform work in a feature branch.
* Merge frequently to incorporate upstream changes.
* Use a [pull request] for code reviews.

[GitFlow]: https://nvie.com/posts/a-successful-git-branching-model/
[pull request]: https://help.github.com/articles/using-pull-requests/

Write a Feature
---------------

Create a local feature branch based off `develop`.

	
*Branch Names*

Branch naming style varies slightly depending on the ticketing system we're using:

*Jira*: `feature/<ticket id>-human-readable-reminder, e.g. `feature/HG-123-update-readme`.

*Trello*: `feature/<issue ID from link>`, e.g. `feature/51-share-handsome-pov-via-social-media`.

*Other*: `feature/<short description>`, e.g. `feature/remove-obsolete-links`.

    git checkout develop
    git pull
    git checkout -b <branch-name>

Merge frequently to incorporate upstream changes.

    git fetch origin
    git merge origin/develop

Resolve conflicts. When feature is complete and tests pass, stage the changes.

    git add --all

When you've staged the changes, commit them.

    git status
    git commit --verbose

Write a [good commit message]. Example format:

    Present-tense summary under 50 characters

    * More information about commit (under 72 characters).
    * More information about commit (under 72 characters).

    http://project.management-system.com/ticket/123

When the feature is complete, share your branch.

    git push origin <branch-name>

Submit a [GitHub pull request].

Assign reviewers. Ask for a code review in the project's chat room.

[good commit message]: https://chris.beams.io/posts/git-commit/
[GitHub pull request]: https://help.github.com/articles/using-pull-requests/

Review Code
-----------

A team member other than the author reviews the pull request. They follow
[Code Review](https://github.com/thoughtbot/guides/tree/master/code-review) guidelines to avoid
miscommunication.

They make comments and ask questions directly on lines of code in the GitHub
web interface or in the project's chat room.

When satisfied, they mark the PR approved and comment `Ready to merge.`

Merge
-----

The developer who submitted the PR should merge it using the merge button on Github. Once the merge is completed, they should use the delete branch button that appears.
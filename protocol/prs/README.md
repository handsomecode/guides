# Pull Requests

How we do Pull Requests and Code Reviews at Handsome.

## Submitting a Pull Request

While it feels a litte scary if you're not used to it, getting focused feedback from other developers is one of the best ways we can continuously improve our craft and skills. Make the most of the opportunity and help your reviewers do the same. Here's how:

1.  Using Github's web interface, create a new PR using the "New Pull Request" button. This will generally go from your feature branch to `develop`.
2.  Use the "Files Changed" tab to be sure you're only changing what you intend to. If there are changes in your PR that you didn't intend, undo them or change your merge targets until the changes reflect only the work you've done. If there are sections of code that aren't clear, refactor them before submitting the PR.
3.  Make sure the code builds and runs correctly on your machine and that all unity and functional tests still pass.
4.  Use the "Create Pull Request" button to create a PR with the changes you've specified.
5.  Enter a meaningful title and a short description of the work. Include the ticket where the work is specified and brief instructions for QA and other reviewers on how to see your work in action and test it.
6.  Choose who to review the changes using the `Reviewers` list. Generally, you'll want this to include all the other developers on the team, or perhaps just those who have knowledge of the section of code you're working on.
7.  Start the review with the "Create pull request" button.

### Submission Pro Tips

-   Keep your PRs small and focused. By only including changes that are relevant to the feature you're working on, you make it easier for reviewers to understand your PR.
-   Make sure your code is as clear as you can make it. This helps reviewers and will help you when you come back to this same section of code in two months.
-   Be sure any given set of changes only goes into one PR so that your team doesn't have to read through the same code changes repeatedly. Keeping feature branches clean and independent is helpful for this.
-   If your project is using unit or functional tests, include them with the functionality that they're testing.
-   Don't include any commented out code. If feel you need to hang on inactive code, check it into source control somewhere; don't make your team look at it every time they open this file.
-   Make sure you've updated the README and any other documentation that may be affected by your commit.

## Managing an Open Pull Request

Once you've opened a PR, you'll be getting input from different directions, having conversations about the best way to do things, and making changes to your code accordingly. These are best practices for this phase:

1.  As new comments and questions come in, reply to all of them on github to make sure that the author knows you've read and understood their comments. (Responses can be as simple as "done" or "ACK".) Mark comments as resolved once you've addressed the authors concerns.
2.  If review shows areas of the code that need improvement, make the changes in your existing branch in a new commit and push them up to Github. The PR will be updated with the new code.
3.  Once you've received the required numers of approvals, use GitHub's "Merge Pull Request" button to close the PR and merge your code into the target branch. Then use the "Delete Branch" button to remove the branch from the serve.

## Reviewing Others' Pull Requests

Reviewing others' code helps us to share knowledge and and improve our craft. Here's how to do it well:

1.  Use Github's "Start Review" button to begin a review.
2.  Add comments to the appropriate lines of code where a problem occurs or you have a question. Having those comments in context makes them easier for the submitter to understand and process.
3.  PRs aren't only for criticism. Call out places where the code is especially well done or uses a technique that's new to you.
4.  When you've reviewed the entire PR, mark it approved or request changes so that the submitter is clear that you're done with your review. (If changes are trivial, e.g. spelling errors, feel free to leave a comment asking for the change but mark the PR as approved so the submitter doesn't need to wait for you to come review the PR again.)

### Review Pro Tips

-   Keep it constructive! It's often best to make suggestions as questions: e.g. "Would this be easier to read with a ternary operator rather than an if/then?" (No.)
-   Keep in mind any style guides or coding standards that the team has agreed on. It may feel picky to call violations of these out, but ultimately it helps everyone to be able to move easily through the project. (Or better, set up linting tools for the project to call these out automatically.)
-   Look for and call out spelling errors, both in documentation and in function and variable names. While it can feel petty to point these out, fixing them is important for readability.
-   Run the code! Just because it looks good doesn't mean that it works correctly. Give it a try.
-   Take your time reviewing. This is the cheapest place for us to improve our code quality, so let's not waste the opportunity.
-   Don't do PRs for more than 30 minutes at a time. If you've got more than that lined up, take a break in the middle.

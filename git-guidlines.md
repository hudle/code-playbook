# Git Usage Hudle
## 1. How to create branches

 * Always create a new branch from `dev` or `master` for every new feature you are working on. Please make sure you have pulled latest dev/master before creating a branch.
* Bug fixes should always be in new branches and those branches should be created from dev/master.
* One branch should do just one thing. Please do not mix many features in one branch.
* Never create nested branches. ALWAYS create a new branch from `dev` or `master`. If you need to use a code in other branches please use cherry-pick instead of making a nested branch.
* Never mix code refactoring and feature in one branch. Please create a separate branch for code refactoring.
* When working on a feature, Please try to finish that feature in the branch you have created. That branch should contain production ready code always.
Code commits in a branch should always be related to what the name of the branch is. For example, never mix two features in a branch and name it based on one feature.


## 2. How to name branches

We use `feature/`,`bug/` and `refactor/`as a prefix in the name to suggest what is the purpose of a branch. After the prefix comes the name of the branch which reveals its intent. For example here are some use cases.

        feature/new-feature
        bug/make-it-work
        refactor/make-it-awesom

## 3. How to write good commit message:

    ADD: (Your commit messages of new functionality/feature added)
    UPDATE: (Your commit messages of functionality/feature is changed or updated)
    REFACTOR: (Your commit messages of ode formatted/ Package moved/ Conflicts Resolved)
    FIX: (Your commit message what you have fixed)

* Every commit should start with keywords like "Refactor:, Bug:, Feature:, Chore:", followed by name feature/bug you are working on. Something like that "Bug:  Fix crash on home button click"
*  Commits should be small and should only do what its commit message says. For example, If it says that it fixes crash on home button click, it should only fix crash on Home button click and nothing more. Not even a small change needs to be done here.
* Never mix refactor commit with something else. And refractor commit format should be like this "Refactor: removed redundant function from HomeActivity"
*  Please always try to create a clean commit history and do not add nonsense commits.
* Commits should be done in such a way that they can be reverted quickly when a need comes in future.
* When the project is in starting phase and you are writing code/files from scratch, do not make small-small commits. Make sure commits are big and contain that one feature you are working on.

## 4. How to create a pull request

* Please give Title to pull request.
* Please provide a description in pull request about what a pull request does.
* Pull request descriptions should be concise and well written
* If it's a static UI, a screenshot would do. Can be ignored.
* If it's an interaction, a gif would help a lot. A good tool to make gifs is Licecap. Can be ignored.
* If it's a bug, steps to reproduce are very useful to help understanding context. Can be ignored.
* If your project is in the initial state and you are pushing the code first time for a particular, Please squash your commits into one. Therefore you are going to push one commit for the whole feature for the very first time.
* Please make sure there are no conflicts in the pull request.

## My pull request depends on another pending pull request. What to do?
    If your next pull request is really that intimately related to your last, consider continuing working on it instead of opening another.
    If it really makes sense to open another, see if you can use cherry-pick, if not, it's okay to base your next pull request on your unmerged branch, just make sure to make it clear in the PR description. Finally, make sure to merge any changes you've made to its parent during its review.
    
    Before merging a pull request, your code has to be reviewed, so that we can learn from you, point out your silly mistakes, and/or post a sufficient amount of gifs. The reviewing process is important. It is better for you to have another person backing you up. More eyes can mean fewer bugs and more consistency throughout.

# Release Process
### Steps for releasing a new version of your app:
* Switch to the `master` branch
* Bump the project's version number (make sure to use semantic versioning)
* Create and upload the archive to FAD (can be ignored)
* Commit and push your changes to the `master` branch
* Create a release on GitHub. If the release uses the staging server, mark it as pre-release

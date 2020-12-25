*Phases of Git

Git has four main phases that should be executed linearly.

The following example demonstrates the workflow of git:
Working Directory > Stagging Area > Local Repository > Remote Repository (GitHub)

1. Working Directory 

Working directory would be your files in realtime, files that you are currently working on.

2. Stagging Area

Adding files to the stagging area prepares them for commits in to the local repository.
They remain in the stagging area before being commited in to the local repository.

3. Local Repository

This is your local storage for version control, after the files are commited they end up here.
The Local Repository contains a copy of your latest commits or your working directory.

4. Remote Repository

Once the files in your local repository are in order, you can push them to the remote repository.
Files from the remote repository can be accessed from anywhere since they are on a remote location(online).


*Branching in git

Branch is just a timeline of commits

Types of Merges: Fast-Forward, Automatic

1. Fast-Forward

Fast-Forward is the simplest case when no additional work has been detected on the parent branch (usually master).
It will apply all of the commits directly onto the parent branch.

2. Automatic

Automatic merging happens when git detects non-conflicting changes in the parent branch, git automatically resolves conflicts.
The old branch timeline is preserved and a merge commit is made in the parent branch.

3. Manual

Happens when git is not able to resolve any merge conflicts. Git enters in a conflicting merge state, which means all conflicts must be resolved.
Once all the conflicts are resolved the changes are saved as a merge commit and the child branch preserved.

IMPORTANT: Once a branch has been merged there is no need for it anymore and we can simply delete the branch.
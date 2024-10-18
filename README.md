# <div align="center"> Git </div>
<p align="center">
  <img src="https://github.com/user-attachments/assets/00ed15fe-6e4d-4514-b438-2bbc1a811131"/>
</p>

## What is Git?
Git is a free and open-source version control system that helps developers manage changes to their code. It was created by Linus Torvalds in 2005 for developing the Linux kernel, and it has since become the most widely used version control system in the world.

## Key concept 
**1.Repository:** A Git repository (or repo) is a directory that contains all the project files and the entire history of changes made to those files. Repositories can be local (on your machine) or remote (on a server).<br>
**2.Commit:** A commit is a snapshot of your changes at a specific point in time. Each commit has a unique identifier (a hash) and contains information about what changes were made, who made them, and when.<br>
**3.Branch:** A branch is a parallel version of the repository. By default, Git creates a branch called main (or master), but you can create new branches for features or bug fixes. Branching allows developers to work on different tasks without interfering with each other.<br>
**4.Merge:** Merging is the process of integrating changes from one branch into another. When a feature is complete, it can be merged back into the main branch. Git can often automatically resolve conflicts, but manual intervention may be needed in complex cases.<br>
**5.Clone:** Cloning is creating a local copy of a remote repository. This allows developers to work on the code locally and push changes back to the remote repo when they’re ready.<br>
**6.Push and Pull:**<br>
  **- Push:** Sending your commits from your local repository to a remote repository.<br>
  **- Pull:** Fetching and integrating changes from a remote repository into your local repository.<br>
**7.Remote Repository:** A remote repository is hosted on a server (like GitHub, GitLab, or Bitbucket) and can be accessed by multiple developers. It serves as a central hub for collaboration.

## Advantages of Using Git
**1.Collaboration:** Multiple developers can work on the same project simultaneously without overwriting each other's work. Branching and merging facilitate this collaboration.<br>
**2.History Tracking:** Git maintains a detailed history of changes, allowing developers to review past modifications, understand who made changes, and revert to earlier states if necessary.<br>
**3.Flexibility:** Git supports various workflows (like Git Flow) and can be adapted to fit different project needs and team structures.<br>
**4.Performance:** Git is designed for speed, with operations like commits, branches, and merges being extremely fast, even for large projects.<br>
**5.Data Integrity:** Git uses a hashing algorithm (SHA-1) to ensure data integrity. Every change is cryptographically secured, making it difficult to alter history without detection.<br>
**6.Offline Work:** Since every developer has a full copy of the repository, they can work offline and sync changes when they’re back online.

## Common Commands
**- git init:** Initializes a new Git repository.<br>
**- git clone <repo-url>:** Clones a remote repository to your local machine.<br>
**- git add <file>:** Stages changes for the next commit.<br>
**- git commit -m "message":** Commits the staged changes with a message.<br>
**- git push:** Pushes local changes to a remote repository.<br>
**- git pull:** Fetches changes from a remote repository and merges them into your local branch.<br>
**- git branch:** Lists all branches or creates a new branch.<br>
**- git checkout <branch>:** Switches to a different branch.

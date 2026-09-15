# A02: Git, GitHub, and WebStorm Tutorial

This document is a step-by-step tutorial for using **Git**, **GitHub**, and **WebStorm** together in a typical development workflow. It is written so that someone with no prior experience could follow it from start to finish.

---

## Part 1: Directions on Using Git, GitHub, and WebStorm

### Step 1: Install Git

1. Go to the official Git website: [https://git-scm.com/downloads](https://git-scm.com/downloads)
2. Download the installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and accept the default settings unless you have a specific reason to change them.
4. Verify the installation by opening a terminal (or Git Bash on Windows) and typing:

git --version

If a version number appears, Git is installed correctly.

### Step 2: Create a GitHub Account

1. Go to [https://github.com](https://github.com).
2. Click **Sign up** and follow the prompts to create a free account using your school or personal email.
3. Verify your email address when prompted.

### Step 3: Configure Git with Your Identity

Open a terminal and run the following commands, replacing the placeholders with your own information:

git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

This tells Git who is making the commits so they show up correctly on GitHub.

### Step 4: Install WebStorm

1. Go to the official JetBrains WebStorm page: [https://www.jetbrains.com/webstorm/download/](https://www.jetbrains.com/webstorm/download/)
2. Download the installer for your operating system.
3. Run the installer and follow the setup wizard, accepting the default options.
4. Launch WebStorm. Students can activate a free license through the [JetBrains Student Pack](https://www.jetbrains.com/community/education/#students) using a valid school email address.

### Step 5: Create a New Repository on GitHub

1. Log into GitHub and click the **+** icon in the top-right corner, then select **New repository**.
2. Name the repository **A02** (capitalization matters).
3. Choose whether the repository is public or private, then click **Create repository**.

### Step 6: Clone the Repository

1. On the repository page, click the green **Code** button and copy the HTTPS URL.
2. In WebStorm, select **Get from VCS** on the welcome screen (or **File > New > Project from Version Control**).
3. Paste the repository URL and choose a local folder, then click **Clone**.
4. Alternatively, from a terminal you can run:

git clone https://github.com/yourUCID/A02


### Step 7: Make Changes and Track Them

1. Open the project folder in WebStorm and create or edit a file (for example, this `README.md`).
2. In WebStorm's **Git** tab (or via terminal with `git status`), you will see the file listed as changed/untracked.
3. Stage the change:

git add README.md


### Step 8: Commit the Change

Commit the staged change with a clear, descriptive message:

git commit -m "Task: Create Repository"

Additional example commit messages used throughout this project:

git commit -m "Feature: added workflow for using github"
git commit -m "Fix: changed readme.md for definition of terms"


### Step 9: Push the Change to GitHub

Upload your local commits to the remote repository on GitHub:

git push origin main

WebStorm users can also click the green **Push** (up-arrow) icon in the toolbar.

### Step 10: Pull and Fetch Updates

If working across multiple machines or collaborators, keep your local copy up to date:

git fetch origin
git pull origin main


### Step 11: Working with Branches

1. Create a new branch for a feature or fix so the `main` branch stays stable:

git branch new-feature
git checkout new-feature

or in one step:

git checkout -b new-feature

2. Make changes, then add, commit, and push the branch as shown above.
3. On GitHub, open a **Pull Request** to merge the branch back into `main`.
4. Once approved, click **Merge pull request** on GitHub, or merge locally with:

git checkout main
git merge new-feature


### Step 12: Submit the Repository Link

Copy the repository URL in the form `https://github.com/yourUCID/A02` and submit it to Canvas.

---

## Part 2: Glossary

- **Branch**: A parallel, independent line of development within a repository, allowing work to happen without affecting the main codebase until it is merged.
- **Clone**: The act of creating a local copy of a remote repository, including its full history.
- **Commit**: A saved snapshot of staged changes in a repository's history, recorded with a descriptive message.
- **Fetch**: Downloading the latest changes, branches, and history from a remote repository without merging them into the local working copy.
- **GIT**: A distributed version control system used to track changes to files over time.
- **GitHub**: A web-based hosting platform for Git repositories that adds collaboration features such as pull requests, issues, and project management tools.
- **Merge**: The process of combining changes from one branch into another.
- **Merge Conflict**: A situation that occurs when Git cannot automatically reconcile differences between two branches because the same lines of a file were changed differently, requiring manual resolution.
- **Push**: Uploading local commits to a remote repository so others can access them.
- **Pull**: Fetching changes from a remote repository and immediately merging them into the current local branch.
- **Remote**: A version of a repository hosted on a server (such as GitHub) that a local repository can push to or pull from.
- **Repository**: A storage location, either local or remote, that contains a project's files along with the full history of changes tracked by Git.

---

## References

- Git. (n.d.). *Git documentation*. Retrieved from https://git-scm.com/doc
- GitHub. (n.d.). *GitHub Docs*. Retrieved from https://docs.github.com/en
- JetBrains. (n.d.). *WebStorm documentation*. Retrieved from https://www.jetbrains.com/webstorm/documentation/
- JetBrains. (n.d.). *JetBrains Student Pack*. Retrieved from https://www.jetbrains.com/community/education/#students
- IS 117 Course PowerPoint Presentations. NJIT.
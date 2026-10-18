# Publish this Playbook to GitHub

This package is prepared locally. These steps create the single GitHub repository that will hold the Playbook. They do not create repositories for each project type; project-specific material stays in this one handbook repository.

## Recommended repository settings

- **Repository name:** `github-standard-playbook`
- **Description:** `A free-first, beginner-friendly handbook and template library for standardizing software repositories.`
- **Visibility:** Public if you want anyone to read and reuse the Playbook. Choose private if you are not ready to publish it.
- **Initialize with README / license / .gitignore:** Off, because those files are already in this package.

Do not put credentials, private project details, or company-confidential policies into a public Playbook repository.

## Option A: Git command line

### 1. Prepare the folder

Download `github-standard-playbook.zip` and extract it. Open a terminal in the extracted `github-standard-playbook` folder (the folder containing `README.md` and `LICENSE`). Make sure Git is installed:

```bash
git --version
```

### 2. Create an empty repository on GitHub

On GitHub, choose **New repository**, enter the name above, choose visibility, and create it without adding a README, license, or `.gitignore`.

### 3. Initialize and push

Replace `<YOUR-USERNAME>` with your GitHub username. Run these commands from the extracted folder:

```bash
git init -b main
git add .
git commit -m "chore: initialize GitHub Standard Playbook"
git remote add origin https://github.com/<YOUR-USERNAME>/github-standard-playbook.git
git push -u origin main
```

GitHub may ask you to authenticate through your configured credential manager or browser. Do not put a password or personal access token directly in these commands.

If Git says `remote origin already exists`, inspect it with `git remote -v` before changing it. If the remote repository was initialized with files, resolve the histories rather than force-pushing blindly.

## Option B: GitHub Desktop

1. Extract the ZIP.
2. In GitHub Desktop, choose **File → Add Local Repository** and select the extracted folder. If it is not a repository yet, choose the option to create a repository there.
3. Create the initial commit.
4. Publish the repository to GitHub using the name and visibility you chose above.
5. Verify the README, `.github/`, `docs/`, and `templates/` folders are present on GitHub.

## After the first push

- [ ] Open `README.md` on GitHub and click several internal links.
- [ ] Check the **Actions** tab for the Markdown lint workflow.
- [ ] Check the **Security** settings and enable available Dependabot alerts/security updates.
- [ ] Review the default branch and configure protection/rules where your plan supports it.
- [ ] Replace the placeholder security-reporting instructions with an actual private reporting path you can maintain.
- [ ] Add a short release tag when you are ready to publish a named version of the Playbook.

## Keep this repository useful

Use issues and pull requests to evolve the standards. Every rule should explain its purpose, how to apply it, and whether it is required, recommended, or optional. Avoid making paid tooling a prerequisite for the baseline.

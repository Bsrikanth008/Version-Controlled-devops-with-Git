
# DevOps Project: Git Version Control Workflow

## Overview
This project demonstrates Git best practices in a DevOps environment. It includes branching, pull requests, tagging, clean commits, and collaboration workflow.

---

## File & Folder Structure

```
devops-git-project/
│
├── .gitignore             # Git ignored files list
├── README.md              # Project documentation
├── deploy.sh              # Sample deployment script
├── docs/                  # Documentation in markdown
│   └── task1.md           # Task descriptions
└── scripts/               # DevOps related shell scripts
    └── setup.sh           # Sample setup script
```

---

## Git Branching Strategy

| Branch        | Purpose                     |
|---------------|-----------------------------|
| `main`        | Production-ready code       |
| `dev`         | Integration of all features |
| `feature/*`   | New features or tasks       |

---

## Git Setup Instructions

### 1. Initialize a Git Repository
```bash
git init
```

### 2. Add Remote Repository
```bash
git remote add origin https://github.com/Bsrikanth008/Version-Controlled-devops-with-Git.git
```

### 3. Add & Commit Files
```bash
git add .
git commit -m "Initial commit"
```

### 4. Create and Switch to Branches
```bash
git checkout -b dev                   # Create dev branch
git checkout -b feature/add-readme   # Create feature branch
```

### 5. Push Branches to GitHub
```bash
git push origin dev
git push origin feature/add-readme
```

### 6. Create a Pull Request
- Go to GitHub
- Open a pull request from `feature/*` → `dev` or `main`
- Get it reviewed and merge

### 7. Merge Branches
```bash
git checkout dev
git merge feature/add-readme
```

### 8. Tag a Release
```bash
git tag -a v1.0 -m "First stable release"
git push origin v1.0
```

### 9. Delete Feature Branch After Merge
```bash
git branch -d feature/add-readme                # Local
git push origin --delete feature/add-readme     # Remote
```

---

## .gitignore Sample

```
*.log
*.tmp
__pycache__/
node_modules/
.env
```

---

## Author
Created as part of the **Elevate Labs DevOps Internship** by [Srikanth Berla](https://www.linkedin.com/in/srikanth-berla-9bb743266)

---

## License

This project is intended for educational purposes.


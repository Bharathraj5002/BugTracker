# 🐛 BugTracker Setup & Git Workflow

This project uses Git and GitHub for version control. Follow the steps below to set up and work with the `BugTracker` repository.

---

## 1. Install Git

```bash
brew install git
git --version
```

---

## 2. Configure Git

```bash
git config --global user.name "Bharathraj5002"
git config --global user.email "mail@gmail.com"
```

---

## 3. Create GitHub Repository

- Name: `BugTracker`
- No README/license
- Private or public as needed

---

## 4. Clone the Repository

```bash
git clone https://github.com/your-username/BugTracker.git
cd BugTracker
```

---

## 5. Verify Git Initialization

```bash
ls -a   # Look for .git folder
```

---

## 6. Create Project Files

Create:

- `README.md`
- `index.html`
- `style.css`
- `app.js` / `main.java` / `Program.cs`

---

## 7. Add & Commit Files

```bash
git add .
git commit -m "feat: initial layout for BugTracker"
git commit -m "style: basic styles for homepage"
```

---

## 8. Push to GitHub

```bash
git push origin main
```

---

## 9. Remote Edit (Conflict Setup)

- Edit `index.html` on GitHub (`<h1>` tag)
- Commit: `fix: updated heading remotely`

---

## 10. Local Edit Same Line

- Change the same `<h1>` line in your local `index.html`

---

## 11. Trigger Merge Conflict

```bash
git add index.html
git commit -m "fix: updated heading locally"
git push origin main  # Merge conflict error expected
```

---

## 12. Resolve Conflict

```bash
git pull origin main  # Pull and resolve conflict in editor
git add index.html
git commit -m "fix: resolved heading conflict"
```

---

## 13. Create Frontend Branch

```bash
git checkout -b frontend
# Edit index.html/style.css
git add .
git commit -m "feat: improved UI"
git push origin frontend
```

---

## 14. Create Backend Branch

```bash
git checkout main
git checkout -b backend
# Add backend logic
git add .
git commit -m "feat: added backend logic"
git push origin backend
```

---

## 15. Add `.gitignore`

```text
node_modules/
*.log
.env
```

```bash
git add .gitignore
git commit -m "chore: add .gitignore"
```

---

## 16. Git Stash Scenario

```bash
# Edit a file, don't commit
git stash
git pull
git stash pop
```

---

## 17. Reset & Restore

```bash
echo "test" > debug.txt
git add debug.txt
git reset debug.txt
git restore index.html
```

---

## 18. Rename Branch

```bash
git branch -m main dev-main
git push origin dev-main
git push origin --delete main  # Optional
```

---

## 19. View Commit History

```bash
git log --oneline --graph --decorate
```

Look for commits with types like: `feat`, `fix`, `style`, `chore`.

---

You're ready to track bugs and collaborate! 🚀

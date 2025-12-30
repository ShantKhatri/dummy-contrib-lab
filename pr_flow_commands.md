# Pull Request Flow — STARTING WITH FORKING

## 1. Fork the repository (GitHub UI)
- Go to the original repo.  
- Click **Fork** (top-right).  
- This creates your own copy under your account.  

**Reality check:**  
You cannot push to the original repo. Forking is mandatory. **No fork = no PR.**

---

## 2. Clone your fork (not the original repo)
This is where beginners already mess up.

```
git clone https://github.com/YOUR_USERNAME/REPO.git
cd REPO
```

---

## 3. Add the original repo as upstream (one-time, mandatory)
Without this, your fork will rot.

```
git remote add upstream https://github.com/ORIGINAL_OWNER/REPO.git
```

**Verify:**
```
git remote -v
```

You should see:
```
origin   → your fork
upstream → original repo
```

---

## 4. Sync your fork with upstream (before starting)
Always start clean.

```
git checkout main
git pull upstream main
git push origin main
```

If you skip this, your PR may conflict and get rejected.

---

## 5. Create a feature branch (never touch main)
```
git checkout -b feature/short-description
```

**Example:**
```
git checkout -b fix-navbar-overflow
```

---

## 6. Make changes
Keep changes focused.  
**One feature = one PR.** Anything else is sloppy.

---

## 7. Inspect changes (non-negotiable)
```
git status
git diff
```
If this output surprises you, you’re not ready to commit.

---

## 8. Stage changes
Add everything:
```
git add .
```

Or be selective if you’re not careless:
```
git add src/Navbar.jsx
```

---

## 9. Commit with a serious message
```
git commit -m "Fix navbar overflow on small screens"
```
If your commit message is vague, reviewers assume your code is too.

---

## 10. Push branch to your fork
```
git push origin feature/short-description
```

---

## 11. Open the Pull Request
On GitHub:
1. Go to **your fork**.  
2. Click **Compare & pull request**.  
3. Set:
   - **Base repo:** `ORIGINAL_OWNER/REPO`
   - **Base branch:** `main`
   - **Compare branch:** `YOUR_USERNAME:feature/short-description`
4. Write a real description:
   - What changed  
   - Why it matters  
   - How to test  

Click **Create Pull Request**.

---

## Updating Your PR (after review feedback)
Don’t open a new PR. Fix the same one.

```
# make changes
git add .
git commit -m "Address PR review feedback"
git push origin feature/short-description
```

The PR updates automatically — that’s the whole point.

---

## Absolute Rules (Break these = rejection)
❌ Never push to main  
❌ Never fork and forget upstream  
❌ Never mix unrelated changes  
❌ Never submit untested code


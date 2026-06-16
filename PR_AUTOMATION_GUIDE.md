# 🚀 PR Creation and Decoration Automation Setup

This repository has been set up with automated PR creation and decoration workflows.

## ✨ What's Included

### 1. **Automatic PR Creation** 
PRs are automatically created when you push to:
- `develop` branch
- Any `feature/**` branches (e.g., `feature/my-feature`)

### 2. **Automatic PR Decoration**
Each PR gets automatically:
- **Labels** based on branch name:
  - `feature/**` → `enhancement`, `feature`
  - `bugfix/**` → `bug`, `bugfix`
  - `docs/**` → `documentation`
  - Others → `pending-review`
- **Reviewers** assigned
- **Assignees** configured
- **Standard template** with description, testing checklist, and more

### 3. **PR Template**
Every PR includes a structured template:
- Description section
- Type of change selection
- Related issues linking
- Testing details
- Code review checklist

## 🔄 How to Use

### Automatic Workflow
1. Create a new branch: `git checkout -b feature/my-feature`
2. Make your changes and commit
3. Push to GitHub: `git push origin feature/my-feature`
4. **PR is automatically created!** ✨

### Manual Trigger
1. Go to **Actions** tab in GitHub
2. Select **PR Automation - Creation and Decoration**
3. Click **Run workflow**
4. Select your branch and confirm

## 📝 File Structure

```
.github/
├── workflows/
│   └── pr-automation.yml          # Main automation workflow
├── pull_request_template.md       # PR template for new PRs
├── pr-template.md                 # Auto-generated PR content
└── CODEOWNERS                     # Auto-reviewer assignment

PR_AUTOMATION_GUIDE.md             # This guide
```

## 🎯 Branch Naming Convention

Follow these patterns for best results:

```
feature/short-description    # New features
bugfix/short-description     # Bug fixes
docs/short-description       # Documentation
develop                      # Main dev branch
```

## 🔧 Customization

You can easily customize:

### Change Labels
Edit `.github/workflows/pr-automation.yml` → "Add labels" section

### Change Reviewers/Assignees
Edit `.github/CODEOWNERS` or `.github/workflows/pr-automation.yml`

### Change PR Template
Edit `.github/pull_request_template.md` or `.github/pr-template.md`

### Change Trigger Branches
Edit `.github/workflows/pr-automation.yml` → `on.push.branches`

## 📋 What to Customize with Your Files

When you have your own files, replace:
1. **PR Template** - Update `.github/pull_request_template.md` with your template
2. **Automation Rules** - Customize labels, reviewers in workflow file
3. **Code Owners** - Update `.github/CODEOWNERS` with your team
4. **Workflows** - Modify `.github/workflows/pr-automation.yml` as needed

## ✅ Best Practices

1. ✓ Use descriptive branch names
2. ✓ Fill in PR details completely
3. ✓ Link related issues with `#issue-number`
4. ✓ Keep PRs focused on one feature/fix
5. ✓ Request reviews promptly

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| PR not created | Check branch name matches pattern, verify push permissions |
| Labels not applied | Ensure branch follows naming convention, verify labels exist |
| Reviewers not assigned | Check usernames are correct, verify token permissions |
| Workflow fails | Check Actions tab for error logs |

## 📚 Learn More

- [GitHub Actions Documentation](https://docs.github.com/actions)
- [Pull Request Templates](https://docs.github.com/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
- [CODEOWNERS File](https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

---

**Your PR automation is ready!** 🎉

When you have your own files and configurations, simply update the files listed above.

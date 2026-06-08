Push to your own GitHub fork
# Fork ERPGulf/changai on GitHub, then:
git remote add origin https://github.com/YOUR_USER/changai.git
git push -u origin lm-studio-frappe-v16
Remotes would look like:

Remote	Purpose
upstream
Official ERPGulf/changai
origin
Your fork (your saved changes)
When official changai updates
cd /home/user/frappe-bench/apps/changai
# 1. Update clean main from official
git fetch upstream
git checkout main
git merge upstream/main
# 2. Re-apply your patches on top
git checkout lm-studio-frappe-v16
git rebase main    # or: git merge main
If there are conflicts, fix them, then:

git add .
git rebase --continue   # if you used rebase
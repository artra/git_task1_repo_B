git init  /* repo A */
git add * /* repo A */
git commit -m "initial commit" /* repo A */
git branch branch1 /* repo A */
git clone repo_A/ repo_B /* repo A parent directory */
git checkout branch1 /* repo B */
git add file_C /* repo B */
git commit -m "file_C in repo_B is born" /* repo B */
git push /* repo B */
git checkout branch1 /* repo A */
git add file_C /* repo A */
git commit -m "file_C modified in repo A" /* repo A */
git add file_C /* repo B */
git commit -m "file C modified in repo B" /* repo B */
git fetch /* repo B */
git mergetool --tool-vimdiff /* repo B */
git commit -m "conflict in file_C resolved" /* repo B */
git remote add repo_B ../repo_B /* repo A */
git fetch repo_B /* repo A*/
git branch -f branch1 remotes/repo_B/branch1 /* repo A */
git remote add origin https://github.com/Baras/git_task1_repo_A.git /* repo A */
git push -u origin branch1 /* repo A */
git remote add origin2 https://github.com/Baras/git_task1_repo_B.git /* repo B */
git add README.md /* repo B */
git commit -m "README.md added" /* repo B */
git push -u origin2 branch1 /* repo B */

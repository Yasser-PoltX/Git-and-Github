````markdown
# 🧠 Git & GitHub Comprehensive Guide

## 🏁 Introduction
This README provides a complete overview of essential **Git** and **GitHub** commands for version control, collaboration, and efficient project management.  
الملف ده فيه شرح كامل لكل أوامر **Git** و **GitHub** اللي بتحتاجها علشان تدير الكود، ترجع للتعديلات القديمة، وتشتغل في تيم باحترافية.

---

## ⚙️ Basic Commands (الأوامر الأساسية)

- `git init` — Initializes a new Git repository.  
  ينشئ مستودع (Repository) جديد في المجلد الحالي.  
  ```bash
  git init
````

* `git clone <repository-url>` — Clones an existing repository.
  بينسخ مشروع من الإنترنت أو من جهاز تاني.

  ```bash
  git clone https://github.com/user/repo.git
  ```

* `git add <file>` — Stages changes for the next commit.
  بيضيف الملفات اللي اتعدلت علشان تتحفظ في الـ commit الجاي.

  ```bash
  git add index.html
  ```

* `git add .` — Stages all modified files.
  بيضيف كل التعديلات مرة واحدة.

  ```bash
  git add .
  ```

* `git commit -m "message"` — Records changes to the repository.
  بيحفظ التعديلات في المشروع مع رسالة توضح اللي اتعمل.

  ```bash
  git commit -m "Added homepage section"
  ```

* `git status` — Shows the state of the working directory and staging area.
  بيعرض الملفات اللي اتعدلت ولسه متعملهاش commit.

  ```bash
  git status
  ```

* `git log` — Displays the commit history.
  بيعرض سجل كل الـ commits اللي حصلت.

  ```bash
  git log
  ```

* `git diff` — Shows the difference between file versions.
  بيقارن بين التغييرات اللي حصلت في الملفات.

  ```bash
  git diff
  ```

---

## 🌿 Branching (الفروع)

* `git branch` — Lists all branches.
  بيعرض كل الفروع الموجودة.

  ```bash
  git branch
  ```

* `git branch <branch-name>` — Creates a new branch.
  بيعمل فرع جديد للتعديلات.

  ```bash
  git branch feature-login
  ```

* `git checkout <branch-name>` — Switches to another branch.
  بينقلك لفرع تاني.

  ```bash
  git checkout feature-login
  ```

* `git checkout -b <branch-name>` — Creates and switches to a new branch.
  بيعمل فرع جديد ويدخلك عليه على طول.

  ```bash
  git checkout -b feature-signup
  ```

* `git branch -d <branch-name>` — Deletes a branch.
  بيحذف الفرع بعد ما تخلص منه.

  ```bash
  git branch -d feature-login
  ```

---

## 🔀 Merging (دمج الفروع)

* `git merge <branch-name>` — Merges another branch into the current one.
  بيضم التعديلات من فرع تاني للفرع الحالي.

  ```bash
  git merge feature-login
  ```

🧠 **Tip:** لو حصل تعارض (Conflict)، Git هيطلب منك تحله يدويًا قبل ما تكمل الدمج.

---

## 💥 Undoing Changes (التراجع عن التغييرات)

* `git reset <commit-id>` — Moves the branch pointer to an older commit.
  بيرجع المشروع لحالة commit معين وبيمسح اللي بعده.

  ```bash
  git reset 1a2b3c4
  ```

* `git reset --hard <commit-id>` — Completely resets and removes all changes.
  بيرجع المشروع زي commit معين ويمسح أي تعديل بعده.

  ```bash
  git reset --hard HEAD~1
  ```

* `git revert <commit-id>` — Creates a new commit that undoes a previous one safely.
  بيرجع التغيير اللي حصل في commit معين لكن بطريقة آمنة بدون حذف التاريخ.

  ```bash
  git revert 1a2b3c4
  ```

🧠 **Note:**

* `reset` يغيّر تاريخ المشروع ويمسح commits.
* `revert` يضيف commit جديد للتراجع بدون حذف أي حاجة.

---

## 📤 Stashing Changes (تخزين التعديلات مؤقتًا)

* `git stash` — Saves uncommitted changes temporarily.
  بيخزن التعديلات مؤقتًا علشان تقدر ترجع لها بعدين.

  ```bash
  git stash
  ```

* `git stash list` — Shows saved stashes.

  ```bash
  git stash list
  ```

* `git stash pop` — Restores the most recent stash.
  بيرجع التعديلات اللي كنت مخزنها.

  ```bash
  git stash pop
  ```

---

## 🤝 Collaboration (التعاون على GitHub)

* `git remote add origin <url>` — Links your local repo to a remote one.
  بيربط المشروع المحلي بالمستودع على GitHub.

  ```bash
  git remote add origin https://github.com/user/repo.git
  ```

* `git push -u origin main` — Pushes your local commits to GitHub.
  بيرفع التغييرات للمستودع على GitHub.

  ```bash
  git push -u origin main
  ```

* `git pull` — Fetches and merges changes from the remote repository.
  بيجلب آخر تحديثات المشروع من GitHub.

  ```bash
  git pull
  ```

* `git fetch` — Downloads updates without merging.
  بيحمل التحديثات من غير دمج.

  ```bash
  git fetch
  ```

* `git clone` — Downloads a copy of a remote repo.

  ```bash
  git clone https://github.com/user/project.git
  ```

---

## ⚡ Aliases (اختصارات الأوامر)

Git allows you to create shortcuts for common commands to save time.
تقدر تعمل اختصارات للأوامر اللي بتستخدمها كتير لتسهيل الشغل.

### 🔹 Examples:

```bash
git config --global alias.st status
git config --global alias.cm "commit -m"
git config --global alias.br branch
git config --global alias.co checkout
git config --global alias.lg "log --oneline --graph --decorate --all"
```

Then you can simply use:

```bash
git st
git cm "quick fix"
git lg
```

---

## 🧩 Extra Useful Commands (أوامر إضافية)

* `git rm <file>` — Removes a file from tracking.
  بيحذف ملف من Git.

  ```bash
  git rm old_file.txt
  ```

* `git mv <old> <new>` — Renames or moves a file.
  بيغير اسم أو مكان ملف.

  ```bash
  git mv old.txt new.txt
  ```

* `git show <commit-id>` — Displays details of a specific commit.
  بيعرض محتوى commit معين.

  ```bash
  git show 1a2b3c4
  ```

* `git tag <tag-name>` — Adds a tag to a commit (useful for releases).
  بيضيف علامة أو إصدار معين للكود.

  ```bash
  git tag v1.0
  ```

---

## 🧭 Common Issues & Tips (مشاكل ونصائح)

* لو نسيت تعمل `commit` قبل الـ `push` → Git هيقولك *“nothing to push”*.
* لو حصل conflict → افتح الملفات المتعارضة، اختار التعديلات اللي عايزها، وبعدها اعمل:

  ```bash
  git add .
  git commit -m "Resolved merge conflict"
  ```
* دايمًا اعمل `git pull` قبل ما تبدأ شغلك اليومي علشان تاخد آخر التحديثات من الفريق.

---

## 📚 Conclusion

Git and GitHub are powerful tools that help you manage, track, and collaborate on code efficiently.
استخدام Git وGitHub بيساعدك تدير مشروعك بطريقة منظمة، خصوصًا في المشاريع الكبيرة أو وقت الشغل الجماعي.

For further learning and practice:

* [📘 Git Official Docs](https://git-scm.com/doc)
* [🐙 GitHub Guides](https://guides.github.com)
* [🧩 Try Git Interactive Tutorial](https://try.github.io/)

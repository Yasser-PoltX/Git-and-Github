````markdown
# 🧠 Git & GitHub Comprehensive Guide

## 🏁 Introduction
This README provides a complete overview of essential **Git** and **GitHub** commands for version control and collaboration.  
الملف ده فيه كل أوامر **Git** و **GitHub** الأساسية اللي هتحتاجها عشان تقدر تتحكم في الكود وتشتغل في فريق بشكل احترافي.

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

* `git commit -m "message"` — Records changes to the repository.
  بيحفظ التعديلات في المشروع مع رسالة توضح اللي اتعمل.

  ```bash
  git commit -m "Added homepage section"
  ```

* `git status` — Shows the state of the working directory and staging area.
  بيعرض الملفات اللي اتعدلت ولسه متعملهاش commit.

* `git log` — Displays the commit history.
  بيعرض سجل كل الـ commits اللي حصلت.

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

---

## 🔀 Merging (دمج الفروع)

* `git merge <branch-name>` — Merges another branch into the current one.
  بيضم التعديلات من فرع تاني للفرع الحالي.

  ```bash
  git merge feature-login
  ```

* **Tip:** لو حصل تعارض (Conflict)، Git هيطلب منك تحله يدويًا قبل ما تكمل الدمج.

---

## 💥 Undoing Changes (التراجع عن التغييرات)

* `git reset <commit-id>` — Moves the branch pointer to an older commit (removes newer ones).
  بيرجع المشروع لحالة commit معين، وبيمسح التغييرات بعده.

  ```bash
  git reset 1a2b3c4
  ```

* `git reset --hard <commit-id>` — Completely resets the repo and deletes all changes.
  بيرجع المشروع زي ما كان في commit معين ويمسح كل حاجة بعده.

* `git revert <commit-id>` — Creates a new commit that undoes a previous one.
  بيرجع التغيير اللي حصل في commit معين بس بطريقة آمنة بدون حذف التاريخ.

  ```bash
  git revert 1a2b3c4
  ```

🧠 **Note:**

* `reset` بيغير تاريخ المشروع وبيمسح commits.
* `revert` بيضيف commit جديد للتراجع بدون حذف أي تاريخ.

---

## 🤝 Collaboration (التعاون على GitHub)

* `git remote add origin <url>` — Links your local repo to a remote one.
  بيربط المشروع المحلي بالمستودع على GitHub.

  ```bash
  git remote add origin https://github.com/user/repo.git
  ```

* `git push -u origin main` — Pushes your local commits to the main branch online.
  بيرفع التغييرات إلى GitHub.

  ```bash
  git push -u origin main
  ```

* `git pull` — Fetches and merges changes from the remote repository.
  بيجلب آخر تحديثات المشروع من GitHub.

* `git fetch` — Gets updates without merging them.
  بيحمل التحديثات من غير ما يدمجها.

---

## ⚡ Alias Commands (الأسماء المختصرة للأوامر)

Git allows you to create **shortcuts** for long commands.
تقدر تعمل اختصارات للأوامر اللي بتستخدمها كتير لتسهيل الشغل.

### Examples:

```bash
git config --global alias.st status
git config --global alias.cm "commit -m"
git config --global alias.br branch
git config --global alias.co checkout
git config --global alias.lg "log --oneline --graph --decorate --all"
```

Then you can type:

```bash
git st
git cm "quick message"
git lg
```

---

## 🧩 Extra Useful Commands

* `git diff` — Shows what’s changed between commits or files.
  بيقارن بين النسخ المختلفة من الملفات.

* `git stash` — Temporarily saves uncommitted changes.
  بيخزن التعديلات مؤقتًا علشان تقدر ترجع لها بعدين.

  ```bash
  git stash
  git stash pop
  ```

* `git rm <file>` — Removes a file from the repository.
  بيحذف ملف من المشروع ومن Git.

---

## 📚 Conclusion

Git and GitHub are powerful tools for tracking code history and collaborating efficiently.
أوامر Git و GitHub هتساعدك تدير مشروعك بطريقة منظمة، خاصة لما تشتغل ضمن فريق.

For more learning:

* [Git Official Docs](https://git-scm.com/doc)
* [GitHub Guides](https://guides.github.com)
* [Try Git (Interactive Tutorial)](https://try.github.io/)

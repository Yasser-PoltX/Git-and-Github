````markdown
# 🧭 Git & GitHub Commands Guide

## 🧩 Introduction
Git هو نظام لإدارة الإصدارات (Version Control System) يُستخدم لتتبع التغييرات في الملفات والمشاريع البرمجية.  
GitHub هو منصة لاستضافة مشاريع Git على الإنترنت لتسهيل التعاون بين المطورين.  
هذا الدليل يشرح أهم أوامر Git وGitHub مع أمثلة بسيطة وواضحة.

---

## ⚙️ Basic Commands — الأوامر الأساسية

- **`git init`**  
  Initializes a new Git repository in the current folder.  
  يقوم بإنشاء مستودع Git جديد في المجلد الحالي.  
  ```bash
  git init
````

* **`git clone <repository-url>`**
  Clones an existing repository from a remote source (e.g., GitHub).
  يقوم بنسخ مستودع موجود من الإنترنت إلى جهازك المحلي.

  ```bash
  git clone https://github.com/user/repo.git
  ```

* **`git status`**
  Shows the current state of the repository (changes, untracked files, etc.).
  يعرض حالة المشروع الحالية مثل الملفات المعدلة وغير المضافة.

  ```bash
  git status
  ```

* **`git add <file>`**
  Adds a file to the staging area for the next commit.
  يضيف الملفات التي تم تعديلها إلى قائمة الملفات الجاهزة للحفظ.

  ```bash
  git add index.html
  ```

* **`git commit -m "message"`**
  Saves your changes in the repository with a descriptive message.
  يقوم بحفظ التعديلات مع رسالة توضح ما تم تغييره.

  ```bash
  git commit -m "Added homepage"
  ```

* **`git log`**
  Displays a history of all commits.
  يعرض سجل جميع عمليات الحفظ (commits).

  ```bash
  git log
  ```

---

## 🌿 Branching — الفروع

* **`git branch`**
  Lists all branches in the repository.
  يعرض جميع الفروع الموجودة في المشروع.

  ```bash
  git branch
  ```

* **`git branch <branch-name>`**
  Creates a new branch.
  ينشئ فرعًا جديدًا لتجربة تغييرات دون التأثير على الكود الأساسي.

  ```bash
  git branch testing
  ```

* **`git checkout <branch-name>`**
  Switches to another branch.
  يقوم بالانتقال إلى فرع آخر.

  ```bash
  git checkout testing
  ```

* **`git switch <branch-name>`**
  An alternative modern command to switch branches.
  طريقة حديثة للانتقال بين الفروع.

  ```bash
  git switch main
  ```

* **`git branch -d <branch-name>`**
  Deletes a branch.
  يحذف فرعًا غير مطلوب بعد الدمج.

  ```bash
  git branch -d testing
  ```

---

## 🔀 Merging — الدمج

* **`git merge <branch-name>`**
  Merges the specified branch into the current branch.
  يقوم بدمج التغييرات من فرع آخر في الفرع الحالي.

  ```bash
  git merge testing
  ```

* **`git rebase <branch-name>`**
  Reapplies commits on top of another base branch.
  يستخدم لإعادة ترتيب تاريخ المشروع بطريقة منظمة.

  ```bash
  git rebase main
  ```

🧠 **Tip:** إذا ظهرت رسالة دمج في محرر النص (مثل الصورة التي رأيتها)، يمكنك الحفظ والخروج باستخدام:

```
:wq
```

في محرر Vim.

---

## 🤝 Collaboration — التعاون باستخدام GitHub

* **`git remote add origin <url>`**
  Links your local repository to a remote one (e.g., GitHub).
  يربط المستودع المحلي بمستودع GitHub.

  ```bash
  git remote add origin https://github.com/user/repo.git
  ```

* **`git push -u origin <branch>`**
  Uploads local commits to the remote repository.
  يرسل التعديلات إلى المستودع على GitHub.

  ```bash
  git push -u origin main
  ```

* **`git pull`**
  Fetches and merges changes from the remote repository.
  يقوم بجلب التحديثات من GitHub ودمجها مع المشروع المحلي.

  ```bash
  git pull
  ```

* **`git fetch`**
  Downloads updates from the remote repository without merging.
  يجلب التحديثات فقط دون دمجها.

  ```bash
  git fetch
  ```

* **`git clone <repository-url>`**
  Clones a repository to start collaborating.
  يقوم بنسخ مشروع من GitHub للعمل عليه محليًا.

  ```bash
  git clone https://github.com/example/repo.git
  ```

---

## 🧰 Troubleshooting — نصائح لحل المشاكل

* **Merge Conflicts** — تعارضات الدمج
  تحدث عندما يتم تعديل نفس السطر في ملفين مختلفين.
  استخدم أدوات مثل:

  ```bash
  git status
  git diff
  ```

  ثم عدّل الملف يدويًا لحل التعارض، وبعدها:

  ```bash
  git add <file>
  git commit
  ```

---

## 🏁 Conclusion — الخاتمة

Git و GitHub أدوات قوية لإدارة المشاريع البرمجية، تساعدك على تتبع التغييرات، التعاون مع الآخرين، وتجنب فقدان الكود.
للتعلم أكثر:

* [Official Git Documentation](https://git-scm.com/doc)
* [GitHub Guides](https://guides.github.com/)
* [Learn Git Branching (Interactive)](https://learngitbranching.js.org/)

> ✨ تذكّر: كل commit هو خطوة صغيرة نحو مشروع أكثر استقرارًا وتنظيمًا.



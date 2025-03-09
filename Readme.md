
# دليل استخدام GitHub - رفع المشاريع وإدارتها

> إعداد بواسطة: **أحمد سامي ذكي (Ahmed Samy Zaky)**  
> حساب GitHub: [AhmedSamy98](https://github.com/AhmedSamy98)  
> البريد الإلكتروني: **ahmed1samy1998@gmail.com**

---

## 1. متطلبات حساب GitHub
1. **حساب على GitHub**  
   - يمكنك إنشاؤه مجانًا عبر [GitHub.com](https://github.com/).
2. **برنامج Git** مثبت على جهازك  
   - قم بتنزيله من [git-scm.com](https://git-scm.com/) وتثبيته.
3. (اختياري) **GitHub CLI**  
   - يسمح بإدارة المستودعات من خلال أوامر CLI.  
   - يمكن تنزيله من [cli.github.com](https://cli.github.com/).

---

## 2. متطلبات الأدوات على الكمبيوتر
- **Git**: للتعامل مع الأوامر وإدارة الإصدارات.
- محرر أكواد (مثل **VS Code**): يُفضل استخدامه مع إضافة Git لسهولة العمل.
- نظام تشغيل يدعم سطر الأوامر (Terminal) مثل **Windows PowerShell** أو **Git Bash** أو **macOS Terminal** أو **Linux Terminal**.

---

## 3. كيفية إنشاء مستودع (Repository) جديد على GitHub
1. سجِّل الدخول إلى [GitHub](https://github.com/).
2. انقر على زر الـ `+` في أعلى الصفحة واختر **New repository**.
3. أدخل اسم المستودع، مثلاً: `testproject1`.
4. حدد ما إذا كان المستودع **Public** (عام) أو **Private** (خاص).
5. (اختياري) أضف وصفًا للمستودع.
6. لا تقم بتحديد مربع **Initialize this repository with a README** إذا كنت تريد رفعه من جهازك مباشرةً.
7. انسخ رابط HTTPS أو SSH الخاص بالمستودع، مثلاً:
   ```
   https://github.com/AhmedSamy98/testproject1.git
   ```

---

## 4. كيفية إضافة مشروع إلى الريبو
### 4.1 إذا كان المشروع موجودًا على جهازك (ولم يكن مربوطًا بـ Git)
لنفترض أن اسم مشروعك هو `testproject1` وموجود في مسار محدد.

1. افتح **Terminal** وانتقل إلى مجلد المشروع:
   ```bash
   cd path/to/testproject1
   ```
2. قم بتهيئة المشروع للاستخدام مع Git:
   ```bash
   git init
   ```
3. أضف جميع الملفات إلى Git:
   ```bash
   git add .
   ```
4. أنشئ أول نقطة حفظ (**Commit**):
   ```bash
   git commit -m "Initial commit"
   ```
5. اربط المشروع بالمستودع على GitHub:
   ```bash
   git remote add origin https://github.com/AhmedSamy98/testproject1.git
   ```
6. حدد الفرع الرئيسي ليكون `master` أو `main` (حسب رغبتك):
   ```bash
   git branch -M master
   ```
7. ادفع المشروع إلى GitHub:
   ```bash
   git push -u origin master
   ```

---

### 4.2 إذا كان لديك ريبو GitHub موجود بالفعل وتريد إضافة ملفات جديدة
1. انتقل إلى مجلد المشروع:
   ```bash
   cd path/to/testproject1
   ```
2. تأكد من وجود الارتباط بالمستودع (`git remote -v`) وأنك على الفرع الصحيح:
   ```bash
   git checkout master
   ```
3. أضف الملفات الجديدة أو المعدلة:
   ```bash
   git add .
   ```
4. أنشئ **Commit** جديد:
   ```bash
   git commit -m "Add new files/features"
   ```
5. ادفع التعديلات:
   ```bash
   git push origin master
   ```

---

## 5. كيفية رفع مشروع إلى مستودع في حساب GitHub آخر
إذا أردت رفع مشروعك إلى ريبو ليس في حسابك، يلزمك:
- أن تكون لديك صلاحيات Collaborator أو Contributor في مستودع الشخص الآخر.
- أو عمل Fork وإرسال Pull Request.

#### الحالة الأولى: لديك صلاحيات مباشرة في مستودعه
1. احصل على رابط المستودع من صاحب الحساب.
2. افتح المشروع على جهازك:
   ```bash
   cd path/to/testproject1
   ```
3. أضف remote جديد:
   ```bash
   git remote add other-origin https://github.com/OtherUser/their-repo.git
   ```
4. ادفع مشروعك إلى ذلك المستودع:
   ```bash
   git push -u other-origin master
   ```

#### الحالة الثانية: عمل Fork
1. قم بعمل **Fork** للمستودع على حسابك.
2. ارفع التعديلات على الفورك.
3. أرسل **Pull Request** إلى المستودع الأصلي.

---

## 6. أهم 20 أمر للتعامل مع Git وGitHub
فيما يلي مجموعة من الأوامر المفيدة للعمل اليومي والاحترافي مع Git:

| الأمر                              | الوصف                                                             |
|------------------------------------|-------------------------------------------------------------------|
| `git init`                         | تهيئة مشروع ليكون مستودع Git.                                     |
| `git clone <repo-url>`            | استنساخ مستودع GitHub إلى جهازك.                                  |
| `git add .`                        | إضافة جميع الملفات الجديدة والمعدلة إلى Git.                     |
| `git commit -m "رسالة"`           | حفظ التعديلات محليًا في المستودع مع رسالة توضيحية.                |
| `git push origin master`          | رفع التعديلات إلى المستودع على الفرع `master`.                    |
| `git pull origin master`          | جلب آخر التحديثات من المستودع البعيد.                             |
| `git status`                      | عرض حالة المستودع والملفات المعدلة.                              |
| `git log --oneline`               | عرض تاريخ التعديلات بشكل مختصر.                                   |
| `git branch`                      | عرض جميع الفروع.                                                  |
| `git checkout -b new-branch`      | إنشاء فرع جديد والتبديل إليه.                                     |
| `git merge branch-name`           | دمج فرع محدد مع الفرع الحالي.                                     |
| `git remote -v`                   | عرض المستودعات البعيدة المرتبطة بالمشروع.                        |
| `git reset --hard HEAD~1`         | التراجع عن آخر Commit بشكل كامل.                                 |
| `git stash`                       | حفظ التعديلات مؤقتًا دون عمل Commit.                             |
| `git stash pop`                   | استعادة التعديلات التي تم حفظها بـ `git stash`.                    |
| `git rebase main`                 | إعادة بناء الكوميتات لتتماشى مع الفرع `main` بدون دمج.            |
| `git fetch --all`                 | جلب التحديثات من جميع الفروع البعيدة بدون دمج.                     |
| `git cherry-pick <commit-id>`     | تطبيق تغييرات Commit معين على الفرع الحالي.                       |
| `git log --graph --all`           | عرض تاريخ التعديلات بشكل رسومي (شجري).                           |
| `git tag -a v1.0 -m "إصدار أول"`  | إنشاء Tag (إصدار) مميز للتعديلات.                               |

---

## ملاحظات إضافية
- **GitHub** اعتمدت الفرع الافتراضي باسم `main` بدلًا من `master` في المستودعات الجديدة؛ يمكنك التبديل بينهما أو التمسك بـ `master` إذا رغبت.
- يفضل استخدام **SSH Key** أو **Personal Access Token** بدلًا من كلمة المرور مع HTTPS.
- احرص على التحكم في **صلاحيات المشاركين** إن كنت تعمل ضمن فريق أو تقدم على ريبو تابع لشخص آخر.

---

### تم بحمد الله
إذا واجهتك أي مشكلة، لا تتردد في التواصل عبر البريد الإلكتروني:  
**ahmed1samy1998@gmail.com**  
أو زيارة حسابي على GitHub: [AhmedSamy98](https://github.com/AhmedSamy98).  


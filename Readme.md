### 📌 **GitHub Guide - كيفية استخدام GitHub لرفع المشاريع وإدارتها**
> إعداد بواسطة: **أحمد سامي ذكي (Ahmed Samy Zaky)**  
> حساب GitHub: [AhmedSamy98](https://github.com/AhmedSamy98)  
> البريد الإلكتروني: **ahmed1samy1998@gmail.com**

---

## 🟢 **1. متطلبات حساب GitHub**
قبل أن تبدأ في استخدام **GitHub**، تحتاج إلى:
1. **حساب على GitHub** – يمكنك إنشاؤه مجانًا عبر [GitHub.com](https://github.com/).
2. **برنامج Git** مثبت على جهازك – وهو المسؤول عن إدارة الإصدارات ومزامنة الأكواد بين جهازك و GitHub.

### **🔹 كيفية التحقق مما إذا كان Git مثبتًا لديك**
افتح **Terminal** (أو Git Bash على Windows) ونفذ الأمر:

```bash
git --version
```

إذا كان **Git** مثبتًا، فسيظهر لك رقم الإصدار. أما إذا لم يكن مثبتًا، فقم بتنزيله من [git-scm.com](https://git-scm.com/) وتثبيته.

---

## 🔵 **2. متطلبات الأدوات على الكمبيوتر**
1. **Git** – الأداة الأساسية لإدارة المشاريع والاتصال بـ GitHub.
2. **GitHub CLI (اختياري)** – أداة إضافية لإدارة المستودعات بسهولة عبر الأوامر.
3. **VS Code أو أي محرر كود** – يُفضل استخدامه مع **Git Integration** لتسهيل العمل.

---

## 🔴 **3. كيفية إنشاء مستودع (Repository) جديد على GitHub**
1. انتقل إلى **[GitHub.com](https://github.com/)** وسجل الدخول إلى حسابك.
2. اضغط على زر `+` في الزاوية العلوية اليمنى، ثم اختر **New repository**.
3. أدخل اسم الريبو، مثلاً: **testproject1**.
4. اختر نوع الريبو:
   - `Public` إذا كنت تريد أن يكون مرئيًا للجميع.
   - `Private` إذا كنت تريده خاصًا.
5. لا تحدد **Initialize this repository with a README** لأننا سنقوم بذلك لاحقًا يدويًا.
6. انسخ رابط المستودع، مثلاً:
   ```
   https://github.com/AhmedSamy98/testproject1.git
   ```

---

## 🟠 **4. كيفية إضافة مشروع إلى الريبو على GitHub**
### 🟣 **(1) إذا كان المشروع موجودًا على جهازك ولم يكن مربوطًا بـ Git بعد**
إذا كنت قد بدأت العمل على مشروع **بدون استخدام Git**، وترغب في رفعه إلى المستودع على GitHub، اتبع التالي:

#### ✅ **الخطوات**
1. افتح **Terminal** وانتقل إلى مجلد المشروع:
   ```bash
   cd path/to/testproject1
   ```
2. قم بتهيئة المشروع ليكون مستودع Git:
   ```bash
   git init
   ```
3. أضف جميع الملفات إلى Git:
   ```bash
   git add .
   ```
4. قم بإنشاء أول **commit** لحفظ التعديلات:
   ```bash
   git commit -m "Initial commit"
   ```
5. اربط المستودع المحلي بالمستودع الموجود على GitHub:
   ```bash
   git remote add origin https://github.com/AhmedSamy98/testproject1.git
   ```
6. قم برفع المشروع لأول مرة:
   ```bash
   git branch -M master  # استخدم master أو main حسب إعدادات Git لديك
   git push -u origin master
   ```

---

### 🟣 **(2) إذا كان لديك ريبو GitHub بالفعل وتريد إضافة ملفات جديدة إليه**
إذا كان لديك مستودع **GitHub موجود** بالفعل، وترغب في **إضافة ملفات جديدة** إليه، اتبع الخطوات التالية:

#### ✅ **الخطوات**
1. انتقل إلى مجلد المشروع عبر **Terminal**:
   ```bash
   cd path/to/testproject1
   ```
2. تأكد من أنك في الفرع الصحيح:
   ```bash
   git checkout master
   ```
3. أضف الملفات الجديدة:
   ```bash
   git add .
   ```
4. أنشئ **commit** لحفظ التعديلات:
   ```bash
   git commit -m "Added new features"
   ```
5. ادفع التعديلات إلى GitHub:
   ```bash
   git push origin master
   ```

---

## 🟢 **5. كيفية رفع مشروع من جهازك إلى مستودع شخص آخر على GitHub**
### **🔹 المتطلبات:**
- يجب أن يكون لديك **صلاحية الوصول (Collaborator)** إلى الريبو الخاص بالشخص الآخر.
- يجب أن تحصل على رابط الريبو الخاص به.

### ✅ **الخطوات**
1. انتقل إلى مجلد مشروعك:
   ```bash
   cd path/to/testproject1
   ```
2. اربط المشروع بالمستودع الخاص بالشخص الآخر:
   ```bash
   git remote add other-origin https://github.com/OtherUser/otherproject.git
   ```
3. قم برفع المشروع إلى المستودع الخاص به:
   ```bash
   git push -u other-origin master
   ```

> **💡 ملاحظة**: إذا لم يكن لديك صلاحيات على المستودع، يمكنك **عمل Fork** وإرسال **Pull Request** لصاحب المشروع.

---

## 🟠 **6. أهم 20 أمرًا لاستخدام Git وGitHub باحترافية**
| الأمر | الوصف |
|-------|-------|
| `git init` | تهيئة مشروع ليكون مستودع Git |
| `git clone <repo-url>` | استنساخ مستودع GitHub إلى جهازك |
| `git add .` | إضافة جميع الملفات الجديدة والمعدلة إلى Git |
| `git commit -m "رسالة"` | حفظ التعديلات في المستودع المحلي |
| `git push origin master` | رفع التعديلات إلى GitHub |
| `git pull origin master` | جلب آخر التحديثات من GitHub |
| `git status` | عرض حالة المستودع والملفات المعدلة |
| `git log --oneline` | عرض تاريخ التعديلات بشكل مختصر |
| `git branch` | عرض جميع الفروع المتاحة |
| `git checkout -b new-branch` | إنشاء فرع جديد والتبديل إليه |
| `git merge branch-name` | دمج فرع معين مع الفرع الحالي |
| `git remote -v` | عرض المستودعات البعيدة المرتبطة بالمشروع |
| `git reset --hard HEAD~1` | التراجع عن آخر Commit |
| `git stash` | حفظ التعديلات مؤقتًا دون Commit |
| `git stash pop` | استعادة التعديلات المحفوظة باستخدام `stash` |
| `git rebase main` | دمج الفرع الحالي مع `main` بدون Merge |
| `git fetch --all` | جلب جميع التعديلات من الفروع البعيدة |
| `git cherry-pick <commit-id>` | تطبيق تغييرات Commit محدد على الفرع الحالي |
| `git log --graph --all` | عرض تاريخ التعديلات بشكل رسومي |
| `git tag -a v1.0 -m "إصدار أول"` | إنشاء Tag لإصدار معين |

---

## 🚀 **الختام**
تهانينا! 🎉 أنت الآن تمتلك دليلًا متكاملًا للتعامل مع **Git و GitHub**.  
إذا كنت بحاجة إلى أي مساعدة إضافية، يمكنك التواصل معي على **ahmed1samy1998@gmail.com** أو زيارة حسابي على GitHub: [AhmedSamy98](https://github.com/AhmedSamy98). 😃
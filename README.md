<رأسية.>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Code with GitHub Copilot

_GitHub Copilot can help you code by offering autocomplete-style suggestions right in VS Code and Codespaces._

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Leverage Codespaces with VS Code for Copilot

_مرحبًا بكم في "تطوير اقتراحات الكود المزود بالذكاء الاصطناعي باستخدام GitHub Copilot و VS Code"! _

GitHub Copilot هو مبرمج زوج AI يساعدك على كتابة التعليمات البرمجية بشكل أسرع وبعمل أقل. وهو يستمد السياق من التعليقات والرمز لاقتراح خطوط فردية ووظائف كاملة على الفور. يتم تشغيل GitHub Copilot بواسطة OpenAI Codex، وهو نموذج لغوي مولد تم تدريبه مسبقًا تم إنشاؤه بواسطة OpenAI.هو مبرمج زوج AI يساعدك على كتابة التعليمات البرمجية بشكل أسرع وبعمل أقل. وهو يستمد السياق من التعليقات والرمز لاقتراح خطوط فردية ووظائف كاملة على الفور. يتم تشغيل GitHub Copilot بواسطة OpenAI Codex، وهو نموذج لغوي مولد تم تدريبه مسبقًا تم إنشاؤه بواسطة OpenAI.

**Copilot works with many code editors including VS Code, Visual Studio, JetBrains IDE, and Neovim.**

Additionally, GitHub Copilot is trained on all languages that appear in public repositories. For each language, the quality of suggestions you receive may depend on the volume and diversity of training data for that language.

يُظهر استخدام Copilot داخل Codespace مدى سهولة النهوض والتشغيل مع مجموعة GitHub من [الترميز التعاوني] (https://github.com/features#features-collaboration) .[الترميز التعاوني.](https://github.com/features#features-collaboration) الأدوات.

>>>   **ملاحظة ** **ملاحظة.**
>  سيركز تمرين المهارات هذا على الاستفادة من GitHub Codespace. يوصى بإكمال مهارة GitHub،  [كود سبيس.]   (https://github.com/skills/code-with-codespaces) ، قبل المضي قدمًا في هذا التمرين. [كود سبيس.](https://github.com/skills/code-with-codespaces)قبل المضي قدما في هذا التمرين.

### :لوحة المفاتيح: Activity: Enable Copilot inside a Codespace

**We recommend opening another browser tab to work through the following activities so you can keep these instructions open for reference.**

Before you open up a codespace on a repository, you can create a development container and define specific extensions or configurations that will be used or installed in your codespace. Let's create this development container and add copilot to the list of extensions.

   1.1.الانتقال مرة أخرى إلى علامة التبويب     1.1.الانتقال مرة أخرى إلى علامة التبويب      **كود.**   التنقل مرة أخرى إلى الخاص بك.   **إضافة ملف.**، ثم انقر فوق "إنشاء ملف جديد".**كود.**  علامة التبويب من مستودع الخاص بك، انقر فوق  **إضافة ملف.**  الزر المنسدلة، ثم انقر فوق.  
  اكتب أو لصق ما يلي في مطالبة حقل النص الفارغ لتسمية ملفك.
 "' 
 .devcontainer/devcontainer.json 
 "' 
1.1.في نص ملف  **.devcontainer/devcontainer.json**   الجديد، أضف المحتوى التالي: **.devcontainer/devcontainer.json** file, add the following content:
 "' 
 { 
  // اسم هذا التكوين   
 "الاسم": "Codespace for Skills!"، 
 "التخصيصات": { 
 "vscode": { 
  "الامتدادات": [ [
                   "GitHub.copilot"
               ]
 } 
 } 
 } 
 "' 
       1.1.حدد خيار  ** الالتزام مباشرة بالفرع "الرئيسي"   ** ، ثم انقر فوق الزر        **ملف الالتزام.**       حدد الخيار إلى...     ** الالتزام مباشرة إلى   'main` فرع** main' branch** ، ثم انقر فوق **الالتزام بملف جديد.** زر.
 1.1.التنقل مرة أخرى إلى الصفحة الرئيسية من المستودع الخاص بك عن طريق النقر على   **كود.**  انتقل مرة أخرى إلى الصفحة الرئيسية لمستودعك بالنقر فوق  **كود.** علامة التبويب الموجودة في أعلى يسار الشاشة.
 1.1.انقر على الزر   **كود.**  انقر فوق  **كود.** زر موجود في منتصف الصفحة.
 1.1.انقر على   **كود سبيس.**  انقر فوق  **كود سبيس.** علامة التبويب على المربع الذي ينبثق.
1.1.انقر على **Create codespace على الزر الرئيسي **.**إنشاء مساحة رمزية على Main.** زر.

   **Wait about 2 minutes for the codespace to spin itself up.**

1. Verify your codespace is running. The browser should contain a VS Code web-based editor and a terminal should be present such as the below:
   ![لقطة شاشة 2023-03-09 في 9 09 07 صباحًا](https://user-images.githubusercontent.com/26442605/224102962-d0222578-3f10-4566-856d-8d59f28fcf2e.png)
1. ... 'copilot` يجب أن يظهر التمديد في قائمة ملحقات رمز VS. انقر فوق الإضافات الشريط الجانبي علامة التبويب.يجب أن ترى ما يلي:
   ![لقطة شاشة 2023-03-09 في الساعة 9 04 13 صباحًا](https://user-images.githubusercontent.com/26442605/224102514-7d6d2f51-f435-401d-a529-7bae3ae3e511.png)

**Wait about 60 seconds then refresh your repository landing page for the next step.**

<تذييل.>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

الحصول على المساعدة: [انشر في لوحة المناقشة الخاصة بنا.](https://github.com/orgs/skills/discussions/categories/code-with-copilot) &الثور; [مراجعة صفحة حالة GitHub](https://www.githubstatus.com/)

 2023 GitHub &الثور; [مدونة قواعد السلوك](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &الثور; [ترخيص معهد ماساتشوستس للتكنولوجيا](https://gh.io/mit)

</تذييل.>
<meta name="google-site-verification" content="AaDyuL5y_aCkRs1QVJrZNb56sVc55Ee_RWHVQLOTg2Y" />

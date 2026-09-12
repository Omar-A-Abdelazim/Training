# رود ماب الباك اند الكامل: Node.js و .NET

> ملحوظة: الملف ده مقسم لجزئين منفصلين تماماً. الجزء الأول رود ماب Node.js لوحده بكل تفاصيله، والجزء التاني رود ماب .NET لوحده بكل تفاصيله. مفيش مقارنة بينهم هنا خالص، كل واحد ماشي لوحده من الصفر لغاية الاحتراف.

---

# 🟢 الجزء الأول: رود ماب Node.js الكامل

المرجع البصري الرسمي والمعتمد لهذا الرود ماب: **[roadmap.sh/nodejs](https://roadmap.sh/nodejs)** - ده رود ماب مجتمعي محدث باستمرار وهيفيدك تراجع بيه كل فترة عشان تشوف مكانك.

## المرحلة صفر: قبل ما تلمس Node.js خالص

قبل ما تفتح أي فيديو عن Node، لازم يكون عندك الأساس ده:

### 1. أساسيات الإنترنت والويب
- إزاي المتصفح بيتكلم مع السيرفر (HTTP/HTTPS Protocol)
- دورة حياة الطلب: Client يبعت Request، السيرفر بيرد بـ Response
- إيه هو الـ DNS وإزاي بيحول اسم الدومين لـ IP
- الفرق بين Client-side وServer-side

### 2. HTML/CSS الأساسيات
مش هتبني بيهم حاجة كباك اند، لكن لازم تفهمهم عشان تفهم إيه اللي السيرفر بيبعته للمتصفح أصلاً، وإزاي الـ Templates بتشتغل لو استخدمتها.

### 3. JavaScript - وده أهم جزء في المرحلة دي كلها
لازم تاخد وقتك فيه صح، لأن Node.js أساسه JavaScript بالكامل:

**الأساسيات:**
- Variables (var, let, const) والفرق بينهم
- Data Types: String, Number, Boolean, Null, Undefined, Object, Array
- Operators (Arithmetic, Comparison, Logical)
- Conditionals (if/else, switch)
- Loops (for, while, for...of, for...in)
- Functions (Regular functions, Arrow functions, Default parameters)
- Arrays وكل الـ methods بتاعتها (map, filter, reduce, forEach, find, some, every)
- Objects وإزاي تتعامل معاهم (Object.keys, Object.values, Object.entries)

**المفاهيم المتوسطة (لازم تتقنها كويس):**
- Scope (Global, Function, Block scope) والفرق بين var وlet في السكوب
- Hoisting
- Closures - ده مفهوم أساسي جداً في JS ومحتاج تفهمه صح
- `this` keyword وإزاي بيتغير معناه حسب السياق
- Template Literals
- Destructuring (Arrays and Objects)
- Spread و Rest operators
- ES6 Modules (import/export)

**المفاهيم المتقدمة (دي أساس شغل Node بالكامل):**
- Event Loop - افهمها كويس جداً جداً، هي أساس فلسفة Node كلها
- Synchronous vs Asynchronous code
- Callbacks
- Callback Hell ومشاكله
- Promises (then, catch, finally, Promise.all, Promise.race)
- Async/Await
- Error Handling (try/catch, custom errors)

**وقت مقترح للمرحلة دي:** من 3 لـ 6 أسابيع حسب مستواك الحالي، ومتستعجلش فيها لأن أي ثغرة هنا هتضرك بعدين.

---

## المرحلة الأولى: Node.js نفسه (الـ Runtime)

### 1. إزاي Node.js شغال من جوه
- إيه هو الـ V8 Engine
- إزاي Node بيدير الـ Single Thread بتاعه مع الـ Event Loop
- الفرق بين Node.js والمتصفح في تشغيل JavaScript
- الـ libuv library ودورها في العمليات الغير متزامنة

### 2. الـ Built-in Modules
- `fs` (File System) - قراءة وكتابة الملفات، Sync vs Async methods
- `path` - التعامل مع مسارات الملفات
- `http`/`https` - إنشاء سيرفر بسيط من غير أي framework
- `os` - معلومات عن نظام التشغيل
- `events` - الـ EventEmitter class
- `stream` - التعامل مع البيانات الكبيرة (Streams: Readable, Writable, Duplex, Transform)
- `buffer` - التعامل مع البيانات الثنائية

### 3. نظام إدارة الـ Packages
- npm (Node Package Manager): install, uninstall, update
- الفرق بين dependencies و devDependencies
- ملف package.json وإيه معنى كل حقل فيه
- ملف package-lock.json وأهميته
- Semantic Versioning (^, ~, والأرقام)
- npm scripts
- بديل npm: pnpm و yarn - ليه الناس بتستخدمهم بدل npm أحياناً

### 4. إدارة الإعدادات
- Environment Variables وإزاي تستخدمها
- مكتبة dotenv
- الفرق بين بيئة Development وProduction وStaging

**وقت مقترح:** أسبوعين لـ 3 أسابيع.

---

## المرحلة الثانية: بناء الـ Backend والـ APIs

### 1. Express.js (الفريم وورك الأساسي - لازم تتقنه كويس أوي)
- إزاي تعمل سيرفر Express بسيط
- الـ Routing (GET, POST, PUT, PATCH, DELETE)
- الـ Route Parameters والـ Query Strings
- الـ Request و Response objects وكل الـ methods بتاعتهم
- الـ Middleware - إزاي تكتب middleware بنفسك، وإزاي تستخدم الجاهز
- Middleware شهيرة: cors, helmet, morgan, body-parser (بقى مدمج في Express نفسه دلوقتي)
- الـ Error Handling Middleware
- تنظيم المشروع: فصل الـ Routes عن الـ Controllers عن الـ Services (Layered Architecture)
- الـ Router الفرعي (express.Router())

### 2. بدائل Express (اختياري لكن مهم تعرف عنها)
- **NestJS**: framework متقدم مبني على TypeScript، بياخد فلسفة قريبة من Angular، منظم جداً ومناسب للمشاريع الكبيرة
- **Fastify**: أسرع من Express في الأداء، بيستخدم في المشاريع اللي محتاجة سرعة عالية
- **Koa.js**: من نفس فريق Express لكن أخف وأحدث في الفلسفة

### 3. مفاهيم REST API
- إيه هو الـ REST وقواعده الأساسية
- HTTP Status Codes وإمتى تستخدم كل واحد (200, 201, 400, 401, 403, 404, 500 وغيرهم)
- تصميم الـ Endpoints بشكل صحيح (naming conventions)
- Versioning للـ API (v1, v2)
- Pagination, Filtering, Sorting
- الفرق بين REST و GraphQL (اتعلم GraphQL بعدين لو حبيت)

**وقت مقترح:** 4 لـ 6 أسابيع.

---

## المرحلة الثالثة: قواعد البيانات

### 1. قواعد البيانات العلائقية (SQL)
- اختار واحدة: PostgreSQL (الأكتر انتشاراً وقوة حالياً) أو MySQL
- أساسيات SQL: SELECT, INSERT, UPDATE, DELETE
- الـ Joins (INNER, LEFT, RIGHT, FULL)
- Indexes وإزاي بتسرّع الاستعلامات
- Transactions
- Normalization (تصميم الجداول بشكل صحيح)

### 2. الـ ORMs للـ SQL
- **Prisma** - الأحدث والأكتر شعبية دلوقتي، بيدّيك type-safety ممتازة خصوصاً لو بتستخدم TypeScript
- **TypeORM** - قديم أكتر لكن لسه مستخدم بكثرة
- **Sequelize** - من أقدم الحلول، لسه موجود في مشاريع كتير

### 3. قواعد البيانات الغير علائقية (NoSQL)
- **MongoDB** - الأشهر مع Node.js
- **Mongoose** (ORM/ODM بتاع MongoDB) - Schemas, Models, Validation
- امتى تستخدم NoSQL بدل SQL وامتى العكس

### 4. Redis
- إزاي تستخدمه للـ Caching
- إزاي تستخدمه للـ Sessions
- إزاي تستخدمه في الـ Rate Limiting

**وقت مقترح:** 4 لـ 6 أسابيع.

---

## المرحلة الرابعة: الأمان (Security) والـ Authentication

### 1. أساسيات الأمان
- تشفير الباسورد بـ bcrypt أو argon2 (متسيبش الباسورد plain text أبداً)
- Input Validation (مكتبات Joi أو Zod)
- SQL Injection وإزاي تتجنبه
- XSS (Cross-Site Scripting)
- CSRF (Cross-Site Request Forgery)
- CORS وإزاي تظبطها صح

### 2. Authentication (التحقق من هوية المستخدم)
- Sessions & Cookies
- JWT (JSON Web Tokens) - إزاي بتشتغل، Access Token و Refresh Token
- OAuth 2.0 (تسجيل الدخول بجوجل/فيسبوك/جيت هاب)
- Passport.js (مكتبة شهيرة لإدارة الـ Authentication)

### 3. Authorization (التحقق من الصلاحيات)
- Role-Based Access Control (RBAC)
- Permission-based systems

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة الخامسة: اختبار الكود (Testing)

- **Unit Testing** بمكتبة Jest أو Vitest
- **Integration Testing** بمكتبة Supertest
- Mocking و Stubbing
- Test Coverage
- TDD (Test-Driven Development) كمفهوم عام

**وقت مقترح:** أسبوعين لـ 3 أسابيع.

---

## المرحلة السادسة: مواضيع لازم تعرفها قبل ما تقول أنا جاهز للشغل

- **Caching Strategies** (Redis بشكل متقدم)
- **Rate Limiting** (حماية الـ API من الإساءة)
- **Logging** بمكتبة Winston أو Pino
- **WebSockets** بمكتبة Socket.io - للـ Real-time features (شات، إشعارات لحظية)
- **Message Queues**: RabbitMQ أو Kafka أو BullMQ - للمهام اللي محتاجة تتنفذ في الخلفية (Background Jobs)
- **Cron Jobs** بمكتبة node-cron
- **File Uploads** (Multer)
- **Email Sending** (Nodemailer)

**وقت مقترح:** 3 لـ 5 أسابيع حسب عمق كل موضوع.

---

## المرحلة السابعة: DevOps والـ Deployment

- **Git & GitHub**: Branching, Merging, Pull Requests, Rebasing
- **Docker**: Dockerfile, Docker Compose، إزاي تحول تطبيقك لـ container
- **CI/CD** بسيط: GitHub Actions
- **الـ Deployment**: Render, Railway, DigitalOcean, أو AWS/Azure للمستوى المتقدم
- **Nginx** كـ Reverse Proxy (أساسيات فقط)
- **PM2** لإدارة الـ Node processes في الـ production

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة الثامنة: حاجات إضافية لو عايز تتميز عن غيرك

- **TypeScript** - بقى شبه إجباري في سوق الشغل دلوقتي، اتعلمه بعد ما تتقن JavaScript الأساسي كويس. بيدّيك Type Safety ويقلل الأخطاء بشكل كبير.
- **GraphQL** كبديل لـ REST APIs (مكتبة Apollo Server)
- **Microservices Architecture** - تقسيم التطبيق الكبير لخدمات صغيرة مستقلة
- **gRPC** للتواصل بين الخدمات الداخلية بسرعة عالية
- **Serverless** (AWS Lambda, Vercel Functions)

---

## ملخص خط سير Node.js الزمني التقريبي
مجموع الوقت من الصفر لغاية مستوى Junior قادر يشتغل: تقريباً **6 لـ 9 شهور** بمذاكرة منتظمة (3-4 ساعات يومياً)، مع بناء مشاريع حقيقية موازية للمذاكرة مش بس نظري.

---
---

# 🔵 الجزء الثاني: رود ماب .NET الكامل

المرجع البصري الرسمي والمعتمد لهذا الرود ماب: **[roadmap.sh/aspnet-core](https://roadmap.sh/aspnet-core)** - نفس فكرة الرود ماب اللي فوق بالظبط، بس لعالم .NET، وهيفيدك تتابعه بصرياً وانت بتذاكر.

## المرحلة صفر: فهم البيئة قبل ما تبدأ

### 1. إيه هو .NET أصلاً (لازم تفهم التاريخ عشان متتلخبطش)
- **.NET Framework**: النسخة القديمة، شغالة على Windows بس، مايكروسوفت مش بتطورها تاني (بس فيها تطبيقات قديمة لسه شغالة)
- **.NET Core**: النسخة اللي اتعملت من الصفر عشان تبقى Cross-platform (تشتغل على Windows, Linux, Mac)
- **.NET (الموحد)**: من إصدار .NET 5 لغاية دلوقتي (.NET 10)، مايكروسوفت وحدت كل حاجة تحت اسم واحد وقفت استخدام كلمة "Core"
- **النصيحة المهمة:** ابدأ على طول بأحدث نسخة LTS (Long Term Support) - دلوقتي .NET 10 هي الـ LTS الحالية المدعومة لغاية 2028. متبدأش بحاجة قديمة زي .NET Framework خالص.

### 2. الأدوات اللي هتحتاجها
- Visual Studio (الأقوى والأشمل، خصوصاً على Windows)
- Visual Studio Code + C# Dev Kit extension (أخف، شغال على أي نظام تشغيل)
- .NET CLI (dotnet command) - أوامر إنشاء وتشغيل وبناء المشاريع

**وقت مقترح:** أسبوع واحد بس عشان تفهم الصورة وتظبط بيئة الشغل.

---

## المرحلة الأولى: لغة C# (خد وقتك هنا، دي أهم مرحلة في الرود ماب كله)

النصيحة اللي الناس بتاخدها في سوق .NET: ذاكر C# لوحدها لحد ما تتقنها كويس قبل ما تفتح ASP.NET، عشان متلخبطش بين مشكلة في اللغة ومشكلة في الفريم وورك.

### الأساسيات
- Variables و Data Types (int, string, bool, double, decimal, char..)
- Operators
- Conditionals (if/else, switch expressions)
- Loops (for, foreach, while, do-while)
- Methods (Parameters, Return types, Overloading)
- Arrays و Lists

### الـ OOP (Object-Oriented Programming) - ده قلب فلسفة C# كلها
- Classes و Objects
- Constructors
- Encapsulation (Access Modifiers: public, private, protected, internal)
- Inheritance (الوراثة)
- Polymorphism (Method Overriding, Virtual/Override keywords)
- Interfaces
- Abstract Classes
- Static members
- Properties (get, set) والفرق بينها وبين الـ fields العادية

### مفاهيم متوسطة ومتقدمة
- Collections (List, Dictionary, HashSet, Queue, Stack)
- Generics
- LINQ (Language Integrated Query) - ده حاجة مميزة جداً في C# ولازم تتقنها، بتخليك تتعامل مع المجموعات بطريقة أنيقة جداً (Where, Select, OrderBy, GroupBy..)
- Exception Handling (try/catch/finally, custom exceptions)
- Delegates و Events
- Async/Await و Task-based programming (Task, Task\<T>)
- Nullable types (?)
- Records (نوع بيانات حديث في C#)
- Pattern Matching

**وقت مقترح:** 6 لـ 8 أسابيع، ومتستعجلش. الأساس ده هيفرق معاك في كل حاجة جاية بعدين.

---

## المرحلة الثانية: SQL وقواعد البيانات

- SQL Server (الافتراضي في عالم .NET، لكن تقدر تستخدم PostgreSQL أو MySQL برضو)
- أساسيات SQL: SELECT, INSERT, UPDATE, DELETE, Joins
- Stored Procedures
- Indexes و Transactions
- Database Design و Normalization

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة الثالثة: ASP.NET Core (الفريم وورك نفسه)

### 1. أساسيات بناء المشروع
- ملف Program.cs وإزاي بيتم تشغيل التطبيق منه
- ملف appsettings.json لإدارة الإعدادات
- الفرق بين appsettings.json و appsettings.Development.json

### 2. Web API Development
- Controllers و Actions
- Routing (Attribute Routing و Convention-based Routing)
- Model Binding
- Action Results (Ok, NotFound, BadRequest, وغيرهم)
- Data Transfer Objects (DTOs) وليه بنستخدمها بدل الـ Models مباشرة

### 3. Dependency Injection - مفهوم أساسي جداً في .NET
- إيه هي فلسفة الـ DI ولية .NET مبني عليها بالكامل
- Service Lifetimes: Transient, Scoped, Singleton
- إزاي تسجل الـ Services في الـ Program.cs

### 4. Middleware Pipeline
- إزاي الـ Request بيمشي في الـ Pipeline
- كتابة Middleware مخصص
- Middleware جاهزة: Authentication, Authorization, CORS, Exception Handling

### 5. SOLID Principles - .NET بتدي اهتمام كبير جداً بيها
- Single Responsibility Principle
- Open/Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependency Inversion Principle

### 6. Design Patterns الشائعة في .NET
- Repository Pattern
- Unit of Work Pattern
- Factory Pattern
- Singleton Pattern

**وقت مقترح:** 6 لـ 8 أسابيع.

---

## المرحلة الرابعة: الوصول لقواعد البيانات من الكود

### 1. Entity Framework Core (الـ ORM الرسمي - لازم تتقنه)
- Code-First Approach
- DbContext و DbSet
- Migrations (إزاي تحدث قاعدة البيانات من الكود)
- Relationships (One-to-One, One-to-Many, Many-to-Many)
- Lazy Loading vs Eager Loading vs Explicit Loading
- LINQ to Entities (استخدام LINQ مع قاعدة البيانات)

### 2. Dapper (بديل أخف لو المشروع محتاج أداء أعلى)
- Micro-ORM بيدّيك تحكم أكتر في الـ SQL مقابل سرعة أعلى

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة الخامسة: الأمان والـ Authentication

### 1. أساسيات الأمان
- تشفير الباسورد (BCrypt.Net أو الـ Identity المدمج)
- Input Validation (FluentValidation أو Data Annotations)
- HTTPS و SSL/TLS
- CORS Configuration

### 2. ASP.NET Core Identity
- نظام الـ Identity الجاهز من مايكروسوفت لإدارة المستخدمين
- Users, Roles, Claims

### 3. JWT Authentication
- إزاي تولد وتتحقق من الـ Tokens
- Refresh Tokens

### 4. Authorization
- Role-based Authorization
- Policy-based Authorization
- Claims-based Authorization

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة السادسة: اختبار الكود (Testing)

- **xUnit** أو **NUnit** (أشهر أدوات الـ Unit Testing في .NET)
- **Moq** لعمل Mocking
- **Integration Testing** باستخدام WebApplicationFactory
- Test-Driven Development كمفهوم عام

**وقت مقترح:** أسبوعين لـ 3 أسابيع.

---

## المرحلة السابعة: مواضيع متقدمة قبل ما تقول أنا جاهز للشغل

- **Caching**: Memory Cache و Distributed Cache (Redis)
- **Logging**: Serilog أو NLog
- **API Versioning**
- **Background Jobs**: Hangfire أو BackgroundService المدمج
- **SignalR** - للـ Real-time communication (بديل .NET لـ Socket.io)
- **gRPC** كبديل لـ REST في بعض السيناريوهات
- **Health Checks** لمراقبة حالة التطبيق
- **Rate Limiting** المدمج في ASP.NET Core

**وقت مقترح:** 3 لـ 5 أسابيع.

---

## المرحلة الثامنة: DevOps والـ Deployment

- **Git & GitHub**: نفس المفاهيم بغض النظر عن اللغة
- **Docker**: تحويل تطبيق .NET لـ container
- **CI/CD**: Azure DevOps Pipelines أو GitHub Actions
- **الـ Deployment**: Azure (البيت الطبيعي لـ .NET) أو أي VPS تاني
- **IIS** كـ Web Server (لو الديبلوي على Windows Server)

**وقت مقترح:** 3 لـ 4 أسابيع.

---

## المرحلة التاسعة: لو عايز تتخصص أكتر

- **Microservices Architecture** مع .NET - فيه اهتمام كبير بيها في عالم .NET تحديداً، وفيه أدوات ناضجة جداً لدعمها (MassTransit, gRPC, API Gateways زي Ocelot أو YARP)
- **Clean Architecture** و **Domain-Driven Design (DDD)** - فلسفات معمارية شائعة جداً في مشاريع .NET الكبيرة
- **Blazor** - لو حابب تعمل فرونت اند بلغة C# نفسها من غير JavaScript خالص
- **.NET MAUI** لو عايز تعمل تطبيقات موبايل/ديسكتوب بنفس اللغة
- **CQRS Pattern** (Command Query Responsibility Segregation) - منتشر جداً في مشاريع .NET المؤسسية الكبيرة (مع مكتبة MediatR)

---

## ملخص خط سير .NET الزمني التقريبي
مجموع الوقت من الصفر لغاية مستوى Junior قادر يشتغل: تقريباً **7 لـ 10 شهور** بمذاكرة منتظمة (3-4 ساعات يومياً)، وده أطول شوية من Node.js بسبب الوقت الإضافي المطلوب لإتقان C# نفسها قبل الفريم وورك، مع بناء مشاريع حقيقية موازية للمذاكرة مش بس نظري.

---

## مرجعين مهمين تحتفظ بيهم

- **[Node.js Roadmap - roadmap.sh](https://roadmap.sh/nodejs)** - الرود ماب البصري الرسمي لـ Node.js، مرجع تراجع بيه باستمرار
- **[ASP.NET Core Roadmap - roadmap.sh](https://roadmap.sh/aspnet-core)** - الرود ماب البصري الرسمي لـ .NET، مرجع تراجع بيه باستمرار


MID-STUDIOS · GeoSeeker & 360° Panorama Studio
تطبيق تفاعلي يجمع بين استوديو لمعاينة المشاهد البانورامية بزاوية 360° ولعبة GeoSeeker؛ استكشف المشهد، افحصه في عرض بانورامي، ثم خمّن موقع الاختباء على الخريطة.
English · الميزات · التشغيل · الإعداد
لمحة عن التطبيق
يوفّر التطبيق وضعين رئيسيين:
استوديو البانوراما: استعراض مجموعة من 10 مشاهد ساحلية، والتنقل داخل المشهد بزاوية 360°، ثم بدء جولة GeoSeeker باستخدام المشهد المختار.
لعبة GeoSeeker: ابحث عن موقع الاختباء باستخدام الخريطة وإشارات اللعبة، وقدّم تخميناتك للوصول إلى الموقع.
تلميحات ذكية: عند إعداد مفتاح Gemini، يمكن للتطبيق إنشاء مواقع اختباء وتلميحات ووصف للمشاهد. يعمل التطبيق أيضًا بإجابات احتياطية عند عدم إعداد المفتاح.
تكامل الخرائط: يعتمد عرض الخريطة وبيانات Street View على Google Maps Platform.
التقنيات
React 19 وTypeScript
Vite 6
Express
Google Maps Platform (@vis.gl/react-google-maps)
Google Gemini (@google/genai)
Three.js لعرض المشاهد ثلاثية الأبعاد
Tailwind CSS 4
متطلبات التشغيل
Node.js 20 أو أحدث
npm أو Bun
مفتاح Google Maps API لتفعيل وظائف الخرائط وStreet View
مفتاح Gemini API اختياري للميزات المدعومة بالذكاء الاصطناعي
التشغيل محليًا
استنسخ المستودع وانتقل إلى مجلده:
git clone https://github.com/bymidstudios/remix-geoseeker_Ft_-MID-STUDIOS-001.git
cd remix-geoseeker_Ft_-MID-STUDIOS-001
ثبّت الاعتماديات:
npm install
أو باستخدام Bun:
bun install
أنشئ ملف البيئة المحلي من النموذج:
cp .env.example .env
أضف مفاتيح الخدمات في .env وفق قسم إعداد مفاتيح الخدمات.
شغّل التطبيق في وضع التطوير:
npm run dev
افتح العنوان الذي يظهر في الطرفية (المنفذ الافتراضي 3000).
إعداد مفاتيح الخدمات
أنشئ مفاتيح API من لوحتي Google Maps Platform وGoogle AI Studio، ثم أضفها إلى ملف .env في جذر المشروع:
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
GEMINI_API_KEY=your_gemini_api_key
VITE_GOOGLE_MAPS_API_KEY: مطلوب لعرض خرائط Google وميزات Street View. فعّل واجهات Google Maps اللازمة للمشروع، واضبط قيود المفتاح بما يناسب بيئة التشغيل.
GEMINI_API_KEY: اختياري، ويُستخدم على الخادم لميزات توليد موقع الاختباء والتلميحات وتحليل المشاهد. يقبل الخادم أيضًا متغير API_KEY كبديل.
لا تضع GEMINI_API_KEY في متغير يبدأ بـ VITE_؛ متغيرات VITE_ تُضمّن في حزمة الواجهة الأمامية.
لا ترفع ملف .env أو مفاتيح حقيقية إلى المستودع.
أوامر المشروع
الأمر
الوصف
npm run dev
تشغيل خادم التطوير والواجهة
npm run build
بناء الواجهة وتجهيز خادم الإنتاج داخل dist/
npm start
تشغيل خادم الإنتاج بعد البناء
npm run preview
معاينة بناء Vite محليًا
npm run lint
فحص أنواع TypeScript باستخدام tsc --noEmit
npm run clean
حذف مجلد dist/
لبناء التطبيق وتشغيله بوضع الإنتاج:
npm run build
npm start
بنية المشروع
.
├── src/
│   ├── components/   # الخريطة، الشريط الجانبي، الاستوديو وعارض البانوراما
│   ├── context/      # حالة اللعبة
│   ├── services/     # خدمات التطبيق
│   ├── utils/        # أدوات مساعدة
│   ├── App.tsx       # واجهة التطبيق والتنقل بين الوضعين
│   └── constants.ts  # المشاهد والمناطق والإعدادات الثابتة
├── public/           # الملفات الثابتة
├── server.ts         # خادم Express وواجهات API
├── .env.example      # نموذج متغيرات البيئة
└── package.json      # الاعتماديات والأوامر
المساهمة
نرحّب بالمساهمات. افتح Issue لاقتراح ميزة أو الإبلاغ عن مشكلة، أو أرسل Pull Request يشرح التغيير بوضوح.
الجهة المطوّرة
MID-STUDIOS FOR VISUALIZATION IMAGINATION


MID-STUDIOS · GeoSeeker & 360° Panorama Studio
An interactive application combining a 360° panorama studio with GeoSeeker, a map-based hide-and-seek game. Explore a scene, inspect its panorama, and then guess the hiding location on the map.
Overview
Panorama Studio: Browse 10 coastal scenes, explore them in a 360° viewer, and launch a GeoSeeker round from a selected scene.
GeoSeeker Game: Search for the hiding location using the map and in-game clues, then submit guesses.
AI-assisted clues: With a Gemini API key configured, the app can generate hiding locations, hints, and scene descriptions. Fallback responses are available when the key is not configured.
Maps integration: Map and Street View features use Google Maps Platform.
Tech stack
React 19, TypeScript, Vite 6, Express, Google Maps Platform, Google Gemini, Three.js, and Tailwind CSS 4.
Requirements
Node.js 20 or later
npm or Bun
A Google Maps API key for maps and Street View
A Gemini API key is optional for AI-powered features
Getting started
git clone https://github.com/bymidstudios/remix-geoseeker_Ft_-MID-STUDIOS-001.git
cd remix-geoseeker_Ft_-MID-STUDIOS-001
npm install
cp .env.example .env
Add your API keys to .env (see Service API keys), then start the development server:
npm run dev
Open the URL printed in the terminal. The default port is 3000.
Service API keys
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
GEMINI_API_KEY=your_gemini_api_key
VITE_GOOGLE_MAPS_API_KEY is required for Google Maps and Street View. GEMINI_API_KEY is optional and is used by the server for AI-powered features; the server also accepts API_KEY as a fallback. Never expose the Gemini key through a VITE_ variable or commit real credentials.
Scripts
Command
Description
npm run dev
Start the development server and app
npm run build
Build the frontend and production server into dist/
npm start
Run the production server after building
npm run preview
Preview the Vite build locally
npm run lint
Type-check with tsc --noEmit
npm run clean
Remove the dist/ directory
Build and run for production with npm run build followed by npm start.
Project structure
src/components/  UI components, map, studio, and panorama viewer
src/context/     Game state
src/services/    Application services
src/utils/       Utilities
public/          Static assets
server.ts        Express server and API routes
Contributing
Issues and pull requests are welcome. Please describe bug reports, proposals, and code changes clearly.
Team
MID-STUDIOS FOR VISUALIZATION IMAGINATION

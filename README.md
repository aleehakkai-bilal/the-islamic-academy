# The Islamic Academy — Android V2

یہ V2 prototype اصل ایپ کے اگلے مرحلے کے لیے تیار کیا گیا ہے۔

## شامل فیچرز
- Public/Guest access
- Student / Teacher / Parent / Principal / Admin login flows
- Bilingual Urdu + English labels
- Quran, Salah, Wudu, Duas, Ahadith, Seerah
- Educational Videos
- Quiz
- Gallery
- Library
- News
- Notifications / Alerts
- Student classes, homework, exams, results, attendance
- Parent → Teacher/Principal note/complaint
- Teacher → Parent note
- Urgent/private alert concept: پیغام صرف متعلقہ وصول کنندہ کے لیے

## اہم وضاحت
یہ ابھی UI/functional prototype ہے۔ حقیقی login، database اور push notifications کے لیے
Firebase project/configuration درکار ہوگی۔

## Firebase production implementation
اگلے production مرحلے میں:
1. Firebase Authentication
2. Cloud Firestore
3. Firebase Cloud Messaging (FCM)
4. Firebase Storage
5. Role-based Security Rules

استعمال ہوں گے۔

## Push Alert design
ہر message document میں recipientUserId رکھا جائے گا۔ Cloud Function/FCM صرف
اسی user/device token کو notification بھیجے گا۔ اس طرح والدین کا نوٹ دوسرے والدین
یا اساتذہ کو نہیں جائے گا۔

## Build
Flutter SDK کے بعد:
flutter pub get
flutter run

Release APK:
flutter build apk --release

## اگلا مرحلہ
Firebase credentials/configuration شامل کرکے حقیقی authentication، database،
private messaging اور recipient-only push notifications کو live کرنا ہے۔

[README.md](https://github.com/user-attachments/files/26061316/README.md)
# מי אתה מול הכותרת? — הוראות העלאה

## שלב 1 — צור חשבון GitHub

1. היכנסי לאתר [github.com](https://github.com)
2. לחצי על **Sign up** וצרי חשבון חינמי
3. אמתי את כתובת המייל שלך

---

## שלב 2 — צרי Repository חדש

1. לאחר ההתחברות, לחצי על הכפתור הירוק **New** (בצד שמאל למעלה)
2. מלאי:
   - **Repository name**: `news-sensitivity-quiz` (או כל שם שתרצי)
   - בחרי **Public**
   - סמני את ✅ **Add a README file**
3. לחצי על **Create repository**

---

## שלב 3 — העלי את קובץ index.html

1. בתוך ה-Repository שיצרת, לחצי על **Add file** ← **Upload files**
2. גרري את קובץ `index.html` לחלון או לחצי **choose your files**
3. למטה, לחצי על **Commit changes**

---

## שלב 4 — הפעילי GitHub Pages

1. לחצי על **Settings** (בתפריט העליון של ה-Repository)
2. בצד שמאל, לחצי על **Pages**
3. תחת **Branch**, בחרי **main** ולחצי **Save**
4. תוך כמה שניות תקבלי כתובת URL כמו:
   `https://שם-המשתמש-שלך.github.io/news-sensitivity-quiz/`

🎉 **האפליקציה עכשיו אונליין!**

---

## שלב 5 — הגדרת מאגר הנתונים (Firebase)

כדי שהנתונים של המשתמשים יישמרו, צריך להגדיר Firebase חינמי.

### 5א — צרי פרויקט Firebase

1. היכנסי ל-[console.firebase.google.com](https://console.firebase.google.com)
2. לחצי על **Add project**
3. תני שם לפרויקט (למשל `news-quiz`)
4. לחצי **Continue** עד לסיום

### 5ב — הפעילי Firestore

1. בתפריט שמאל, לחצי על **Firestore Database**
2. לחצי **Create database**
3. בחרי **Start in test mode** (לעכשיו, זה מספיק)
4. בחרי אזור (למשל `europe-west`) ולחצי **Enable**

### 5ג — קבלי את פרטי ה-Config

1. לחצי על גלגל השיניים ⚙️ ← **Project settings**
2. גלגלי למטה עד **Your apps**
3. לחצי על הכפתור `</>` (Web)
4. תני שם לאפליקציה ולחצי **Register app**
5. תראי קוד כזה — **שמרי אותו**:

```javascript
const firebaseConfig = {
  apiKey: "AIza...",
  authDomain: "news-quiz.firebaseapp.com",
  projectId: "news-quiz",
  storageBucket: "news-quiz.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```

### 5ד — עדכני את קובץ index.html

פתחי את `index.html` בעורך טקסט (Notepad, TextEdit וכו').

חפשי את הקטע:
```javascript
const FIREBASE_CONFIG = {
  apiKey: "YOUR_API_KEY",
  ...
```

והחליפי את הערכים עם הפרטים שקיבלת בשלב 5ג.

לאחר מכן העלי שוב את הקובץ ל-GitHub (שלב 3) — GitHub Pages יתעדכן אוטומטית תוך דקה.

---

## סיכום

| מה | איפה |
|---|---|
| האפליקציה | `https://שם-משתמש.github.io/news-sensitivity-quiz/` |
| נתוני משתמשים | Firebase Console ← Firestore ← collection `responses` |

שאלות? אפשר לשאול את Claude 😊

# אפליקציית תורים — דביר יחיאל ספר

## קישורים

| מה | כתובת |
|---|---|
| האפליקציה החיה | https://naorat888-hash.github.io/dvir-barber-app |
| קוד ב-GitHub | https://github.com/naorat888-hash/dvir-barber-app |
| Firebase Console | https://console.firebase.google.com → פרויקט dvir-barber |

---

## גישה לחשבונות

| שירות | בעלים | חשבון |
|---|---|---|
| GitHub | נאור (המפתח) | naorat888 |
| Firebase | דביר (הלקוח) | חשבון Gmail של דביר |

---

## Firebase Config

נמצא בתוך `index.html` בשורות 69-76.
לגיבוי — ניתן לייצא מחדש מ: console.firebase.google.com → dvir-barber → Project Settings → Your apps

---

## תיקון ועדכון קוד

### להוריד את הקוד למחשב:
```
git clone https://github.com/naorat888-hash/dvir-barber-app
```

### לעלות שינוי:
```
git add .
git commit -m "תיאור השינוי"
git push origin main
```

### האפליקציה מתעדכנת תוך 2-3 דקות אחרי push.

---

## משימה פתוחה — לפני 4 יולי 2026

**לנעול חוקי Firestore:**

1. console.firebase.google.com → dvir-barber → Firestore Database → Rules
2. להחליף הכל ב:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```
3. לחץ Publish

אם לא נעשה → האפליקציה תפסיק לעבוד ב-4 יולי.

---

## מבנה הפרויקט

```
barber-app/
├── index.html      ← כל הקוד — React + Firebase + עיצוב
├── logo.jpg        ← לוגו דביר יחיאל
└── PROJECT_INFO.md ← המסמך הזה
```

---

## טכנולוגיות

| טכנולוגיה | שימוש |
|---|---|
| React 18 (CDN) | ממשק משתמש |
| Firebase Firestore | שמירת תורים בענן |
| GitHub Pages | אחסון האפליקציה (חינם) |
| Babel Standalone | הרצת JSX בדפדפן |

---

## תכונות האפליקציה

- יומן יומי שעות 8:00–20:00 (כל 20 דקות)
- הוספה / עריכה / מחיקה של תורים
- 7 סוגי שירות עם מחיר ומשך אוטומטי
- השלמה אוטומטית של שם לקוח
- שמירת מחיר לפי לקוח
- סטטיסטיקות יומיות (תורים, זמן, הכנסות)
- שמירה בענן + גיבוי מקומי
- ממשק עברית RTL מלא

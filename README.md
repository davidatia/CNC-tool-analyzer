# CNC Tool Analyzer

ניתוח שרטוטים הנדסיים ויצירת רשימת כלים אוטומטית.
Developed by [DAVID:ATIA](https://davidatia.com)

---

## התקנה והרצה

### דרישות מקדימות
- Node.js (גרסה 14 ומעלה)
- מפתח API של Anthropic

### שלב 1 — הורד את הקבצים
```
cnc-tool-analyzer/
├── index.html
├── server.js
├── package.json
└── README.md
```

### שלב 2 — הגדר את מפתח ה-API

**Windows (CMD):**
```cmd
set ANTHROPIC_API_KEY=sk-ant-xxxxxxxxxxxxxxxx
```

**Windows (PowerShell):**
```powershell
$env:ANTHROPIC_API_KEY="sk-ant-xxxxxxxxxxxxxxxx"
```

**Linux / Mac:**
```bash
export ANTHROPIC_API_KEY=sk-ant-xxxxxxxxxxxxxxxx
```

### שלב 3 — הפעל את השרת
```bash
node server.js
```

### שלב 4 — פתח בדפדפן
```
http://localhost:3000
```

---

## הרצה על שרת (Production)

ניתן להשתמש ב-PM2 להרצה רציפה:
```bash
npm install -g pm2
ANTHROPIC_API_KEY=sk-ant-xxx pm2 start server.js --name cnc-analyzer
pm2 save
```

לשינוי הפורט:
```bash
PORT=8080 node server.js
```

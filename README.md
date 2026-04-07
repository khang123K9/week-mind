# Week Mind

Website `Week Mind` dung `Node.js + Express` de phuc vu giao dien va cac API AI:

- Phan tich du lieu nguoi dung
- Tao cau hoi khao sat
- Lap ke hoach tuan bang AI
- Goi coach AI

Project nay da duoc rut gon de deploy len `Render` bang `Web Service`.

## Cai dat local

1. Cai `Node.js`
2. Mo terminal trong thu muc project
3. Cai dependency

```powershell
npm install
```

4. Tao file `.env` tu `.env.example`
5. Dien API key that

## Chay local

```powershell
npm start
```

Sau do mo `http://localhost:3000`

## Deploy len Render

Tao `Web Service` moi tren Render va dung:

- Build Command: `npm install`
- Start Command: `npm start`

Them cac bien moi truong sau trong Render:

```env
AI_PROVIDER=gemini
GEMINI_MODEL=gemini-2.5-flash
GEMINI_SURVEY_MODEL=gemini-2.5-flash-lite
GEMINI_API_KEY=your_gemini_api_key_here
AI_TIMEOUT_MS=20000
SURVEY_TIMEOUT_MS=25000
ANALYZE_TIMEOUT_MS=22000
PLAN_TIMEOUT_MS=18000
COACH_TIMEOUT_MS=20000
```

Neu Render yeu cau `PORT`, app da tu doc `process.env.PORT`.

## Luong API

- `POST /api/survey`
- `POST /api/analyze`
- `POST /api/plan`
- `POST /api/coach`

## Luu y

- Khong mo `index.html` bang `file://`
- Render phai deploy dang `Web Service`, khong phai `Static Site`
- Du lieu tai khoan/noi dung dang duoc luu bang `localStorage` tren trinh duyet
- File `api/_lib/openai.js` giu ten cu de tranh vo import, nhung hien dang dung Gemini

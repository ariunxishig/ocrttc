# Зураг → Текст → Дуу апп

Зураг оруулахад Claude API ашиглан текст гаргаж аваад, браузерийн TTS-ээр уншуулна.

## Байрлуулах заавар (Vercel)

### 1. GitHub repo үүсгэх
```bash
git init
git add .
git commit -m "first commit"
gh repo create ocr-tts-app --public --push
```

### 2. Vercel-д байрлуулах
```bash
npm i -g vercel
vercel
```

Эсвэл [vercel.com](https://vercel.com) руу орж GitHub repo-оо холбоно.

### 3. Anthropic API key тохируулах
Vercel dashboard → Project → Settings → Environment Variables:
```
ANTHROPIC_API_KEY = sk-ant-xxxxxx
```

Дараа нь **Redeploy** хийнэ.

### 4. Утсандаа ашиглах
Vercel өгсөн URL-ийг утасны браузерт нээнэ (жнь: https://ocr-tts-app.vercel.app)

📷 товч дарж зураг авах → Текст гаргаж, уншуулах → автоматаар уншина!

## Файлын бүтэц
```
├── api/
│   └── extract.js      # Anthropic API endpoint
├── public/
│   └── index.html      # Үндсэн хуудас
└── vercel.json         # Vercel тохиргоо
```

## Тэмдэглэл
- Монгол дуу хоолой байхгүй бол Казак (kk) эсвэл Орос (ru) хоолой сонгоорой
- API key-ийг хэзээ ч public-д оруулж болохгүй — зөвхөн Vercel environment variable-д тохируулна

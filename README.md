# 글뽐 · Geulppom

**Will I be able to read my notes later?** / **내 필기, 나중에 읽을 수 있을까?**

A web app that evaluates the **readability** of your handwriting using AI, designed with college students' note-taking habits in mind.
카메라로 노트를 비추면 **필기 가독성**을 AI가 평가해주는 웹 앱입니다. 대학생의 필기 특성에 맞춰 "흘려 써도 읽히기만 하면 OK!"를 모토로 합니다.

![Version](https://img.shields.io/badge/version-v26.04.18.1430-c8362a)
![Platform](https://img.shields.io/badge/platform-Web-green)
![Korean](https://img.shields.io/badge/lang-KO%20%2F%20EN-blue)

---

## ✨ Features / 주요 기능

- 📷 **Real-time camera capture** / **실시간 카메라 촬영** — Point at your notes to start
- 🤖 **AI handwriting recognition** / **AI 글자 인식** — Powered by Tesseract.js OCR
- 📊 **3 evaluation metrics** / **3단계 평가 지표** — Clarity · Structure · Readability
- 🎓 **Grade system (A+ to F)** / **학점 스타일 등급** — Fun and intuitive feedback
- 📱 **Fully responsive** / **완전 반응형** — Mobile-first design
- 🔒 **Privacy-first** / **프라이버시 보장** — Everything runs in your browser

---

## 🏆 How It Works / 평가 방식

### Metrics / 세부 지표

| Metric / 지표 | Meaning / 의미 | Measured by / 측정 방법 |
|:---:|:---|:---|
| **Clarity / 선명도** | Are individual letters crisp? <br/> 각 글자가 또렷한가 | OCR confidence score <br/> OCR 인식 신뢰도 |
| **Structure / 구조감** | Are lines well-spaced? <br/> 줄이 겹치지 않고 정돈되었나 | Line spacing consistency <br/> 줄 간격·높이 일관성 |
| **Readability / 판독성** | Can you read it later? <br/> 시간 지나도 읽을 수 있나 | Alignment & bbox analysis <br/> 경계 박스 정렬도 |

### Grading Scale / 등급 체계

| Score | Grade | Message |
|:---:|:---:|:---|
| 95~100 | **A+ · 완벽 가독 / Perfect** | 시험 때 시간 절약 1등급 필기예요 <br/> *Top-tier notes — saves exam time* |
| 85~94 | **A · 잘 읽힘 / Clear** | 친구도 빌려봐도 문제없어요 <br/> *Clear enough for a friend to borrow* |
| 75~84 | **B · 본인만 OK / Personal-use** | 본인 복습용으론 충분 <br/> *Good for your own review* |
| 65~74 | **C · 흐릿함 / Blurry** | 시간 지나면 헷갈릴 듯 <br/> *May confuse even you later* |
| 55~64 | **D · 암호 수준 / Cryptic** | 교수님 필체보다 어려울 수 있어요 <br/> *Harder to read than the professor's* |
| ~54 | **F · 미래의 나에게 / Dear Future Me** | 시험 전날 후회하지 말아요 <br/> *You'll regret this the night before the exam* |

---

## 🚀 Deployment (GitHub Pages) / 배포 방법

### Step 1. Create Repository / 저장소 생성

1. Login to [GitHub](https://github.com) → Click **`+` → New repository**
2. Name it (e.g., `handwriting-app`) / 이름 입력 (예: `handwriting-app`)
3. Select **Public** (required for free Pages) / **Public** 선택 (무료 Pages는 Public만 가능)
4. Click **Create repository**

### Step 2. Upload Files / 파일 업로드

Upload these two files to the repository root:
저장소 루트에 아래 두 파일을 업로드하세요:

- `index.html` — The app itself / 앱 본체
- `.nojekyll` — Empty file, disables Jekyll / 빈 파일, Jekyll 비활성화용

> 💡 If `.nojekyll` isn't visible in Finder, press `Cmd + Shift + .` (Mac) to show hidden files.
> `.nojekyll` 파일이 Finder에서 안 보이면 `Cmd + Shift + .` (Mac)으로 숨김 파일을 표시하세요.

### Step 3. Enable GitHub Pages / Pages 활성화

1. Repository → **Settings** → **Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main` / **Folder**: `/ (root)`
4. Click **Save**

### Step 4. Access / 접속

Wait 1–2 minutes, then open the generated URL:
1~2분 뒤 배포 완료, 아래 URL로 접속:

```
https://사용자명.github.io/저장소명/
```

---

## 📱 How to Use / 사용 방법

1. **Open the URL in Safari (iPhone) or Chrome (Android)**
   Safari(아이폰)나 Chrome(안드로이드)에서 URL 접속
2. **Tap "Camera On" and allow camera access**
   **카메라 켜기** 탭 → 권한 허용
3. **Fit your handwritten page into the frame**
   필기한 노트 한 페이지를 프레임에 맞추기
4. **Tap "Evaluate" and wait a moment**
   **평가하기** 탭 → 잠시 대기
5. **See your score, grade, and detailed metrics**
   점수·등급·세부 지표 확인!

> ⏱ The first evaluation may take 10–20 seconds (loading Korean OCR model ~10MB).
> Subsequent evaluations take only 2–5 seconds.
>
> 첫 평가는 **10~20초** 걸립니다 (한글 OCR 모델 약 10MB 다운로드).
> 두 번째 평가부터는 **2~5초**로 빨라집니다.

---

## 📁 File Structure / 파일 구조

```
handwriting-app/
├── index.html    # Main app (HTML + CSS + JS integrated)
│                 # 앱 본체 (HTML·CSS·JS 통합 단일 파일)
├── .nojekyll     # Disables Jekyll processing (empty file)
│                 # Jekyll 프로세싱 비활성화 (빈 파일)
└── README.md     # This document / 이 문서
```

---

## 🛠️ Tech Stack / 기술 스택

- **Vanilla HTML + CSS + JS** — No frameworks, no build step
  바닐라 JS, 프레임워크 없음, 빌드 과정 없음
- **Tesseract.js 5** — In-browser OCR (Korean language pack)
  브라우저 내 OCR (한글 언어팩)
- **MediaDevices API** — Real-time camera access
  실시간 카메라 접근
- **Canvas API** — Image capture and pixel analysis
  이미지 캡처 및 픽셀 분석
- **Google Fonts** — Nanum Myeongjo (Korean serif display)
  나눔명조 (한국어 세리프체)

---

## 🎨 Design Philosophy / 디자인 컨셉

- **Color Palette**: Ink black + Cinnabar red (朱墨) + Gold accents
  색상: 먹색 + 주묵 + 금니 포인트
- **Typography**: Mixing Korean serif display with sans-serif body
  한국어 세리프 디스플레이 + 산세리프 본문 조합
- **Motion**: Subtle pulse and float animations, scan line effect
  은은한 펄스·플로팅·스캔라인 애니메이션
- **Tone**: Friendly, encouraging, with a hint of humor
  친근하고 격려하는 톤, 재치 살짝

---

## 🌐 Browser Compatibility / 브라우저 호환성

| Browser / 브라우저 | Support / 지원 |
|:---|:---:|
| iOS Safari 14.3+ | ✅ |
| Android Chrome | ✅ |
| Desktop Chrome / Edge / Firefox | ✅ |
| Desktop Safari | ✅ |

⚠️ **HTTPS required for camera access** (GitHub Pages provides HTTPS by default).
⚠️ **카메라 사용은 HTTPS에서만 가능** (GitHub Pages는 자동 HTTPS 제공).

---

## 🆘 Troubleshooting / 문제 해결

### Camera permission popup doesn't appear / 카메라 권한 팝업이 안 뜸
→ Settings → Safari → Camera → "Allow", then reload
→ 설정 → Safari → 카메라 → "허용" 선택 후 새로고침

### "This browser doesn't support camera" / "이 브라우저는 카메라를 지원하지 않아요"
→ Update to iOS 14.3+ or use Safari
→ iOS 14.3 이상으로 업데이트하거나 Safari 사용

### Scores seem too low / 점수가 너무 낮게 나옴
→ Make sure the paper fills the frame in bright light
→ 밝은 조명에서 A4 용지가 프레임에 꽉 차도록 촬영

### First evaluation takes forever / 첫 평가가 너무 오래 걸림
→ Korean OCR model is loading (~10MB, first time only)
→ 한글 OCR 모델 다운로드 중 (~10MB, 첫 실행만)

---

## 📝 License / 라이선스

MIT License — Free to use, modify, and distribute.
자유롭게 사용·수정·배포 가능합니다.

---

## 🙏 Credits / 크레딧

- **OCR Engine**: [Tesseract.js](https://tesseract.projectnaptha.com/)
- **Fonts**: [Google Fonts](https://fonts.google.com) (Nanum Myeongjo, Noto Sans KR)
- **Icons**: Custom SVG illustrations
- **Inspiration**: Every college student who regretted their messy notes on exam day ✍️
  시험 전날 자기 필기를 후회한 모든 대학생들에게서 영감을 얻었습니다 ✍️

---

<p align="center">
  Made with ☕ for students who want to know<br>
  "Can future me actually read this?"<br>
  <br>
  "미래의 내가 이걸 읽을 수 있을까?"<br>
  궁금한 모든 학생을 위해 ☕ 만들었습니다
</p>

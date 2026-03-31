# 진삼가 웹폰트 가이드

### 추천 조합: Gowun Batang + Gowun Dodum

---

<br>

## 1. 폰트 개요

| 구분 | 타이틀용 | 본문용 |
|---|---|---|
| **폰트명** | Gowun Batang (고운 바탕) | Gowun Dodum (고운 돋움) |
| **유형** | 세리프 (명조) | 산세리프 (고딕) |
| **굵기** | Regular 400, Bold 700 | Regular 400 |
| **라이선스** | SIL Open Font License 1.1 (무료, 상업용 가능) | SIL Open Font License 1.1 (무료, 상업용 가능) |
| **제공처** | Google Fonts | Google Fonts |
| **한글 지원** | 11,172자 (현대 한글 완성형 전체) | 11,172자 (현대 한글 완성형 전체) |
| **한자 지원** | 지원 | 지원 |

<br>

## 2. 이 조합을 선택한 이유

**"고운" 시리즈**는 한글 서예의 전통적 아름다움을 현대 디지털 환경에 맞게 재해석한 서체 패밀리입니다. 같은 디자인 철학에서 탄생한 명조(Batang)와 고딕(Dodum)이기 때문에, 함께 사용했을 때 시각적 톤이 자연스럽게 어우러집니다.

**진삼가 브랜드와의 적합성:**

| 브랜드 키워드 | 폰트가 전달하는 느낌 |
|---|---|
| 전통 · 정성 | Gowun Batang의 명조 획이 전통 홍삼의 격조와 9증9포의 정성을 시각화 |
| 따뜻함 · 자연 | 두 폰트 모두 붓글씨에서 영감받은 부드러운 곡선으로 자연친화적 온기 전달 |
| 진정성 · 신뢰 | 과하지 않은 절제된 디자인이 "진짜"라는 브랜드 메시지와 정합 |
| 건강 · 웰빙 | 둥글고 부드러운 Gowun Dodum이 건강식품 브랜드의 친근함을 보완 |
| 프리미엄 · 고급 | 명조 타이틀의 세리프가 대중 브랜드와 차별화되는 프리미엄 인상 부여 |

<br>

## 3. 사용 가이드

### 3-1. 역할 분담

| 용도 | 폰트 | 굵기 | 크기 (권장) |
|---|---|---|---|
| 메인 슬로건 / 히어로 타이틀 | Gowun Batang | Bold 700 | 36~48px |
| 섹션 제목 (H1) | Gowun Batang | Bold 700 | 28~32px |
| 서브 타이틀 (H2) | Gowun Batang | Regular 400 | 22~26px |
| 강조 인용문 / 캡션 | Gowun Batang | Regular 400 | 16~20px |
| 본문 텍스트 | Gowun Dodum | Regular 400 | 15~16px |
| 네비게이션 / 버튼 | Gowun Dodum | Regular 400 | 14~15px |
| 부가 정보 / 풋터 | Gowun Dodum | Regular 400 | 12~13px |

### 3-2. 줄간격 (line-height) 권장값

| 용도 | line-height |
|---|---|
| 타이틀 (Gowun Batang) | 1.4 ~ 1.5 |
| 본문 (Gowun Dodum) | 1.7 ~ 1.8 |
| 캡션 / 부가정보 | 1.5 ~ 1.6 |

### 3-3. 자간 (letter-spacing) 권장값

| 용도 | letter-spacing |
|---|---|
| 타이틀 (큰 크기) | -0.02em ~ -0.01em (약간 좁게) |
| 본문 (일반 크기) | 0 ~ 0.01em (기본값 유지) |
| 영문 소문자 보조 텍스트 | 0.02em ~ 0.05em (약간 넓게) |

<br>

## 4. 웹 적용 코드

### 4-1. HTML (Google Fonts CDN)

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Gowun+Batang:wght@400;700&family=Gowun+Dodum&display=swap" rel="stylesheet">
```

### 4-2. CSS @import (대안)

```css
@import url('https://fonts.googleapis.com/css2?family=Gowun+Batang:wght@400;700&family=Gowun+Dodum&display=swap');
```

### 4-3. CSS 변수 설정 (권장)

```css
:root {
  /* 진삼가 폰트 시스템 */
  --font-title: 'Gowun Batang', 'Noto Serif KR', serif;
  --font-body: 'Gowun Dodum', 'Noto Sans KR', sans-serif;

  /* 진삼가 브랜드 컬러 (참고) */
  --color-brand-dark: #8B0000;
  --color-brand-gold: #B8860B;
  --color-text-main: #333333;
  --color-text-sub: #666666;
  --color-bg-warm: #F5F5F0;
}
```

### 4-4. CSS 적용 예시

```css
/* 타이틀 */
h1, h2, .hero-title, .section-title {
  font-family: var(--font-title);
  font-weight: 700;
  line-height: 1.4;
  letter-spacing: -0.01em;
  color: var(--color-brand-dark);
}

/* 서브 타이틀 */
h3, .sub-title, blockquote {
  font-family: var(--font-title);
  font-weight: 400;
  line-height: 1.5;
  color: var(--color-text-main);
}

/* 본문 */
body, p, li, .body-text {
  font-family: var(--font-body);
  font-weight: 400;
  font-size: 15px;
  line-height: 1.75;
  color: var(--color-text-main);
}

/* 네비게이션 / 버튼 */
nav, .nav-link, .btn {
  font-family: var(--font-body);
  font-weight: 400;
  font-size: 14px;
  letter-spacing: 0.01em;
}

/* 캡션 / 부가정보 */
.caption, footer, .meta {
  font-family: var(--font-body);
  font-size: 13px;
  line-height: 1.6;
  color: var(--color-text-sub);
}
```

<br>

## 5. 적용 예시 (진삼가 실제 문구)

### 메인 히어로

```
[Gowun Batang Bold 48px]
9번의 정성으로 홍삼에 진심을 담다

[Gowun Batang Regular 20px]
眞蔘家 — 모두 담은 홍삼, 진삼

[Gowun Dodum Regular 15px]
풍기 6년근 인삼 · 세계 최초 전자동 9증9포 · 합성첨가물 제로
```

### 섹션 제목 + 본문

```
[Gowun Batang Bold 28px]
오직 9증9포만을 고집합니다

[Gowun Dodum Regular 15px]
인삼을 9번 찌고 9번 말리는 전통 제법. 진삼가는 0.1도 단위의
정밀 온도 제어로 진세노사이드와 홍삼다당체의 유실을 원천
차단합니다. 일반 제품 대비 5~12배 높은 진세노사이드 함유량,
이것이 진삼가의 차이입니다.
```

### 인용문

```
[Gowun Batang Regular 18px, italic color: #8B0000]
"홍삼을 아는 사람이 먹는 홍삼, 진삼가"
```

<br>

## 6. 대체 폰트 (Fallback) 전략

웹폰트 로딩 실패 시를 대비한 폰트 스택입니다.

```css
/* 타이틀 fallback */
font-family: 'Gowun Batang', 'Noto Serif KR', '바탕', 'Batang', Georgia, serif;

/* 본문 fallback */
font-family: 'Gowun Dodum', 'Noto Sans KR', '맑은 고딕', 'Malgun Gothic', sans-serif;
```

| 순서 | 타이틀 Fallback | 본문 Fallback |
|---|---|---|
| 1순위 | Gowun Batang | Gowun Dodum |
| 2순위 | Noto Serif KR | Noto Sans KR |
| 3순위 | 바탕 (Windows) | 맑은 고딕 (Windows) |
| 4순위 | Georgia (범용) | sans-serif (범용) |

<br>

## 7. 성능 최적화 팁

### font-display: swap

Google Fonts URL에 `&display=swap`이 포함되어 있어, 폰트 로딩 전에는 시스템 폰트로 먼저 텍스트를 표시한 후 웹폰트가 로딩되면 교체됩니다. 이미 위 코드에 적용되어 있습니다.

### 필요한 굵기만 로드

Gowun Batang은 400과 700 두 가지, Gowun Dodum은 400 하나만 로드합니다. 불필요한 굵기를 추가하지 않아 로딩 속도를 최적화합니다.

### preconnect 사용

HTML `<head>` 상단에 `preconnect`를 넣으면 DNS 조회 시간을 단축할 수 있습니다.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
```

<br>

## 8. 참고 링크

| 항목 | URL |
|---|---|
| Gowun Batang (Google Fonts) | https://fonts.google.com/specimen/Gowun+Batang |
| Gowun Dodum (Google Fonts) | https://fonts.google.com/specimen/Gowun+Dodum |
| Google Fonts 한국어 쇼케이스 | https://googlefonts.github.io/korean/ |
| 눈누 (무료 한글 폰트 모음) | https://noonnu.cc/ |

---

> **문서 용도:** 진삼가 홈페이지 리뉴얼 시 프론트엔드 개발자 및 디자이너 참고용
>
> **브랜드:** 진삼가(眞蔘家) | 주식회사 진삼 | www.jinsamga.co.kr

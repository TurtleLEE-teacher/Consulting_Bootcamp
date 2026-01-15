# Design System v2.0 - MBB Consulting Level

## 개선 목표

**현재 문제점:**
- 텍스트 중심 레이아웃 (70% 텍스트 + 30% 장식)
- 낮은 비주얼 임팩트
- 일반적인 색상 사용
- "So What?" 불명확

**목표 수준:**
- MBB (McKinsey, BCG, Bain) 수준의 프로페셔널한 비주얼
- 다이어그램 60% + 데이터 시각화 20% + 텍스트 20%
- 명확한 메시지 전달
- 실전 적용 가능한 인사이트

---

## 1. 컬러 시스템

### 1.1 McKinsey 스타일 컬러 팔레트

```css
/* Primary Colors - 신뢰와 권위 */
--mbb-navy: #003d5c;           /* 진한 Navy - 메인 컬러 */
--mbb-navy-light: #005a82;     /* 밝은 Navy - 호버 상태 */
--mbb-navy-dark: #002942;      /* 어두운 Navy - 강조 */

/* Accent Colors - 액션과 하이라이트 */
--mbb-teal: #00a4a6;           /* Teal - Call-to-action */
--mbb-teal-light: #33b8ba;     /* 밝은 Teal */

/* Data Visualization */
--mbb-data-positive: #4fb3d9;  /* Sky Blue - 긍정 데이터 */
--mbb-data-negative: #ff6b6b;  /* Coral - 부정 데이터, 경고 */
--mbb-data-neutral: #a0a0a0;   /* Gray - 중립 데이터 */
--mbb-data-highlight: #ffd700; /* Gold - 핵심 강조 */

/* Neutral Colors */
--mbb-text-primary: #1a1a1a;   /* 메인 텍스트 */
--mbb-text-secondary: #556270; /* 보조 텍스트 */
--mbb-bg-white: #ffffff;       /* 배경 */
--mbb-bg-light: #f8f9fa;       /* 서브 배경 */
--mbb-border: #e0e0e0;         /* 경계선 */

/* Semantic Colors */
--mbb-success: #00b894;        /* 성공, 완료 */
--mbb-warning: #fdcb6e;        /* 주의 */
--mbb-error: #d63031;          /* 오류, 위험 */
--mbb-info: #74b9ff;           /* 정보 */
```

### 1.2 색상 사용 원칙

| 요소 | 색상 | 사용 목적 |
|------|------|----------|
| **제목/헤더** | Navy (#003d5c) | 권위, 신뢰감 |
| **액션 버튼/CTA** | Teal (#00a4a6) | 주목, 행동 유도 |
| **긍정 데이터** | Sky Blue (#4fb3d9) | 개선, 증가 |
| **부정 데이터** | Coral (#ff6b6b) | 문제, 감소 |
| **핵심 인사이트** | Gold (#ffd700) | 최우선 메시지 |
| **본문 텍스트** | Dark Gray (#1a1a1a) | 가독성 |

---

## 2. 타이포그래피 시스템

### 2.1 폰트 계층

```css
/* 폰트 패밀리 */
--font-display: 'Pretendard', -apple-system, sans-serif;  /* 제목용 */
--font-body: 'Pretendard', -apple-system, sans-serif;     /* 본문용 */
--font-mono: 'JetBrains Mono', monospace;                 /* 코드/숫자 */

/* 폰트 사이즈 (16:9 기준 1920x1080) */
--text-hero: 72px;      /* 타이틀 슬라이드 */
--text-h1: 56px;        /* 섹션 타이틀 */
--text-h2: 48px;        /* 슬라이드 제목 */
--text-h3: 36px;        /* 서브 제목 */
--text-body-large: 28px;/* 강조 본문 */
--text-body: 24px;      /* 일반 본문 */
--text-small: 20px;     /* 캡션, 주석 */
--text-tiny: 16px;      /* 각주 */

/* 폰트 웨이트 */
--weight-black: 900;    /* 초강조 */
--weight-bold: 700;     /* 제목 */
--weight-semibold: 600; /* 서브 제목 */
--weight-medium: 500;   /* 강조 본문 */
--weight-regular: 400;  /* 일반 본문 */
--weight-light: 300;    /* 보조 정보 */

/* 행간 (Line Height) */
--leading-tight: 1.2;   /* 제목 */
--leading-normal: 1.5;  /* 본문 */
--leading-loose: 1.8;   /* 여유로운 본문 */
```

### 2.2 타이포그래피 규칙

| 요소 | 크기 | 굵기 | 색상 | 용도 |
|------|------|------|------|------|
| **Hero Title** | 72px | Bold (700) | Navy | 타이틀 슬라이드 |
| **Section Title** | 56px | Bold (700) | Navy | 섹션 구분 |
| **Slide Title** | 48px | Semibold (600) | Navy | 슬라이드 제목 |
| **Subtitle** | 36px | Medium (500) | Gray | 부제목 |
| **Body Large** | 28px | Regular (400) | Dark Gray | 핵심 메시지 |
| **Body** | 24px | Regular (400) | Dark Gray | 일반 텍스트 |
| **Caption** | 20px | Light (300) | Gray | 설명, 주석 |
| **Number (Big)** | 64px | Bold (700) | Teal/Coral | 통계 강조 |

---

## 3. 레이아웃 시스템

### 3.1 그리드 시스템

```
슬라이드 크기: 1920px × 1080px (16:9)

Safe Zone (컨텐츠 영역):
- 좌우 여백: 120px (각 측면)
- 상하 여백: 80px (각 측면)
- 실제 컨텐츠 영역: 1680px × 920px

12 컬럼 그리드:
- 컬럼 너비: 115px
- 거터(Gutter): 24px
```

### 3.2 여백 시스템

```css
/* Spacing Scale (8px 기반) */
--space-xs: 8px;      /* 아주 작은 간격 */
--space-sm: 16px;     /* 작은 간격 */
--space-md: 24px;     /* 중간 간격 */
--space-lg: 32px;     /* 큰 간격 */
--space-xl: 48px;     /* 아주 큰 간격 */
--space-2xl: 64px;    /* 초대형 간격 */
--space-3xl: 96px;    /* 섹션 간격 */
```

### 3.3 화이트스페이스 원칙

- **60/40 법칙**: 컨텐츠 60%, 여백 40%
- **집중 영역**: 슬라이드당 시선 집중 영역 1개
- **호흡 공간**: 요소 간 최소 24px 간격

---

## 4. 슬라이드 타입 시스템

### Type 1: Hero Slide (타이틀 슬라이드)

**구조:**
```
+------------------------------------------+
|                                          |
|                                          |
|          [Big Visual/Icon]               |
|                                          |
|          HERO TITLE (72px)               |
|          Subtitle (36px)                 |
|                                          |
|                                          |
+------------------------------------------+
```

**특징:**
- 중앙 정렬
- 대형 타이포그래피
- 미니멀한 비주얼
- 배경: Navy 그라디언트 또는 화이트

---

### Type 2: One Big Visual (메인 다이어그램)

**구조:**
```
+------------------------------------------+
| Slide Title (48px)                       |
+------------------------------------------+
|                                          |
|                                          |
|      [Main Diagram/Chart]                |
|        (화면의 70%)                       |
|                                          |
|                                          |
+------------------------------------------+
| 💡 So What: 핵심 인사이트 (28px)          |
+------------------------------------------+
```

**특징:**
- 제목은 간결하게 (최대 10자)
- 다이어그램이 메인
- 하단에 So What 박스 필수
- 텍스트 최소화

---

### Type 3: Data Visualization (수치 강조)

**구조:**
```
+------------------------------------------+
| Slide Title (48px)                       |
+------------------------------------------+
|                                          |
|   [Big Number]     [Big Number]          |
|      64px             64px               |
|    Label (24px)    Label (24px)          |
|                                          |
|   [Chart/Graph - 중앙 배치]               |
|                                          |
+------------------------------------------+
| 📊 Insight: 데이터가 말하는 것 (24px)     |
+------------------------------------------+
```

**특징:**
- 핵심 수치를 크게 (64px)
- 차트는 심플하게 (최대 5개 데이터 포인트)
- 색상으로 긍정/부정 구분
- 인사이트 박스 필수

---

### Type 4: Framework (2x2, 3x3 등)

**구조:**
```
+------------------------------------------+
| Framework Title (48px)                   |
+------------------------------------------+
|                                          |
|    [2x2 Matrix or Framework]             |
|     - 축 라벨 명확                        |
|     - 각 사분면 예시 1개씩                |
|     - 색상으로 구분                       |
|                                          |
+------------------------------------------+
| ⚠️ 적용 시 주의점 (20px)                  |
+------------------------------------------+
```

**특징:**
- 프레임워크가 중앙
- 축 라벨은 굵게
- 각 영역마다 실제 예시
- 하단에 실무 팁

---

### Type 5: Process Flow (프로세스 흐름)

**구조:**
```
+------------------------------------------+
| Process Title (48px)                     |
+------------------------------------------+
|                                          |
| [Step 1] → [Step 2] → [Step 3] → [Step 4]
|   Icon      Icon       Icon       Icon  |
|   Label     Label      Label      Label |
|                                          |
| Current: Step 2 (하이라이트)              |
+------------------------------------------+
| ⏱️ 소요시간: X일 | 📋 산출물: Y          |
+------------------------------------------+
```

**특징:**
- 최대 5단계
- 각 단계 아이콘 필수
- 현재 단계 강조 (Teal 색상)
- 소요시간/산출물 표기

---

## 5. 비주얼 요소 가이드

### 5.1 아이콘 스타일

**기본 원칙:**
- 스타일: Line icons (2px stroke)
- 크기: 48px (표준), 64px (강조), 96px (Hero)
- 색상: Navy (기본), Teal (액션), Coral (경고)
- 소스: Heroicons, Lucide, Font Awesome

**사용 예:**
- ✅ 완료, 성공
- ⚠️ 주의, 경고
- 💡 인사이트, 아이디어
- 📊 데이터, 차트
- 🎯 목표, 타겟
- ⏱️ 시간, 기한

### 5.2 차트 스타일 가이드

**Bar Chart (막대 그래프):**
- 막대 두께: 60px
- 간격: 40px
- 색상: 긍정(Sky Blue), 부정(Coral)
- 라벨: 막대 상단에 수치

**Line Chart (선 그래프):**
- 선 두께: 4px
- 포인트 크기: 12px
- 그리드: 얇은 회색 (1px)
- 추세선: Teal

**Pie Chart (파이 차트):**
- 최대 5개 세그먼트
- 가장 큰 세그먼트부터 시계방향
- 라벨: 세그먼트 외부
- 퍼센트: 세그먼트 내부

### 5.3 다이어그램 스타일

**플로우차트:**
- 박스: 둥근 모서리 (12px radius)
- 선: 2px, Navy
- 화살표: 실선, 끝에 삼각형
- 간격: 최소 48px

**Issue Tree:**
- 루트: Navy 배경, 화이트 텍스트
- 브랜치: 화이트 배경, Navy 테두리
- 연결선: 2px, Gray
- 레벨별 들여쓰기: 48px

---

## 6. 인터랙티브 요소

### 6.1 하이라이트 박스

**So What 박스:**
```css
배경: Gold gradient
텍스트: Navy (Bold)
아이콘: 💡
패딩: 24px 32px
둥근 모서리: 12px
그림자: 0 4px 12px rgba(0,0,0,0.1)
```

**Insight 박스:**
```css
배경: Teal gradient
텍스트: White (Semibold)
아이콘: 📊 또는 🎯
패딩: 24px 32px
둥근 모서리: 12px
```

**Warning 박스:**
```css
배경: Coral gradient
텍스트: White (Semibold)
아이콘: ⚠️
패딩: 24px 32px
둥근 모서리: 12px
```

### 6.2 버튼 스타일

**Primary Button:**
```css
배경: Teal (#00a4a6)
텍스트: White (Semibold)
패딩: 16px 32px
둥근 모서리: 8px
호버: Teal Light (#33b8ba)
```

**Secondary Button:**
```css
배경: Transparent
텍스트: Navy (Semibold)
테두리: 2px Navy
패딩: 16px 32px
둥근 모서리: 8px
호버: Navy 배경, White 텍스트
```

---

## 7. 애니메이션 & 트랜지션

### 7.1 슬라이드 전환

```css
transition: slide (기본)
duration: 600ms
easing: cubic-bezier(0.4, 0.0, 0.2, 1)
```

### 7.2 요소 등장

**Fade In:**
- 제목: 200ms delay
- 본문: 400ms delay
- 다이어그램: 600ms delay

**Slide In:**
- 왼쪽에서: 리스트 아이템
- 아래에서: 통계 숫자
- 오른쪽에서: 인사이트 박스

---

## 8. 실전 적용 체크리스트

### 슬라이드 제작 전

- [ ] 이 슬라이드의 "So What?"은 무엇인가?
- [ ] 텍스트 없이 다이어그램만으로 이해 가능한가?
- [ ] 3초 안에 핵심 메시지를 파악할 수 있는가?

### 슬라이드 제작 중

- [ ] 텍스트는 3줄 이하인가?
- [ ] 불릿 포인트는 5개 이하인가?
- [ ] 메인 비주얼이 화면의 60% 이상인가?
- [ ] 색상 사용이 의미를 전달하는가?
- [ ] 여백이 충분한가? (60/40 법칙)

### 슬라이드 완성 후

- [ ] 인사이트 박스가 있는가?
- [ ] 데이터가 있다면 출처가 명시되었는가?
- [ ] 이전 슬라이드와 논리적으로 연결되는가?
- [ ] 다음 슬라이드로 자연스럽게 전환되는가?

---

## 9. Before & After 예시

### Before (현재)

```
제목: 컨설팅의 정의

"전문 지식으로 고객의 문제를 해결"

• 전문성: 특정 분야의 깊은 지식과 경험
• 문제 해결: 고객이 직면한 과제를 분석하고 해결
• 가치 창출: 측정 가능한 성과와 변화
```

**문제점:**
- 텍스트만 나열
- 비주얼 없음
- So What 불명확
- 데이터 없음

### After (개선)

```
제목: 컨설팅 = 6개월에 3년치 성과

[중앙 대형 다이어그램]
        전문지식 × 외부시각 × 실행력
               ↓
           10배 ROI

[3개 통계 박스]
  300%              6개월            $2.5M
평균 투자수익률    평균 프로젝트    평균 프로젝트
                   기간             규모

💡 내부 인력으로 3년 걸릴 일을 6개월에 끝내는 비결
```

**개선점:**
- 제목에 구체적 수치
- 대형 다이어그램으로 개념 시각화
- 실제 데이터로 신뢰성 확보
- So What 명확

---

## 10. CSS 변수 전체 요약

```css
:root {
  /* Colors */
  --mbb-navy: #003d5c;
  --mbb-teal: #00a4a6;
  --mbb-data-positive: #4fb3d9;
  --mbb-data-negative: #ff6b6b;
  --mbb-text-primary: #1a1a1a;
  --mbb-bg-white: #ffffff;

  /* Typography */
  --text-hero: 72px;
  --text-h2: 48px;
  --text-body: 24px;
  --weight-bold: 700;
  --weight-regular: 400;

  /* Spacing */
  --space-xs: 8px;
  --space-md: 24px;
  --space-xl: 48px;

  /* Effects */
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.1);
  --shadow-md: 0 4px 16px rgba(0,0,0,0.15);
  --radius-sm: 8px;
  --radius-md: 12px;
}
```

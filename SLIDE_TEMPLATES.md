# MBB 스타일 슬라이드 템플릿 가이드

## 사용 방법

1. 필요한 슬라이드 타입 선택
2. 해당 템플릿 HTML 복사
3. `index.html`에 붙여넣기
4. 내용 수정

---

## Type 1: Hero Slide (타이틀/섹션 구분)

**용도**: 타이틀, 섹션 전환, Part 구분
**특징**: 중앙 정렬, 대형 타이포그래피, 임팩트

### 템플릿 코드

```html
<!-- Type 1: Hero Slide -->
<section class="hero-slide">
    <!-- 선택사항: 아이콘/비주얼 -->
    <div class="visual">🎯</div>

    <!-- 메인 타이틀 -->
    <h1>컨설팅펌 직무부트캠프</h1>

    <!-- 부제목 -->
    <p class="subtitle">6개월에 3년치 성과를 만드는 방법</p>
</section>
```

### 사용 예시

```html
<!-- 예시 1: Part 타이틀 -->
<section class="hero-slide">
    <div class="visual">📊</div>
    <h1>Part 1</h1>
    <p class="subtitle">컨설팅과 컨설턴트</p>
</section>

<!-- 예시 2: 섹션 타이틀 -->
<section class="hero-slide">
    <h1>5C 역량 모델</h1>
    <p class="subtitle">McKinsey가 뽑는 사람의 기준</p>
</section>
```

---

## Type 2: Big Visual (메인 다이어그램 중심)

**용도**: 프레임워크, 다이어그램, 개념 시각화
**특징**: 비주얼 70%, 텍스트 최소화, So What 박스

### 템플릿 코드

```html
<!-- Type 2: Big Visual -->
<section class="big-visual-slide">
    <!-- 슬라이드 제목 (간결하게, 최대 10자) -->
    <h2>컨설팅 가치 공식</h2>

    <!-- 메인 비주얼 영역 -->
    <div class="main-visual">
        <!-- SVG, 다이어그램, 또는 이미지 삽입 -->
        <div style="text-align: center; font-size: 48px; line-height: 1.8;">
            <div style="color: #003d5c; font-weight: 700;">전문 지식 × 외부 시각 × 실행력</div>
            <div style="font-size: 64px; margin: 32px 0;">↓</div>
            <div style="color: #00a4a6; font-weight: 900; font-size: 72px;">10배 ROI</div>
        </div>
    </div>

    <!-- So What 박스 (필수) -->
    <div class="so-what">
        내부 인력으로 3년 걸릴 일을 6개월에 끝내는 비결
    </div>
</section>
```

### 사용 예시

```html
<!-- 예시: A-E-D-B-D 프로세스 -->
<section class="big-visual-slide">
    <h2>A-E-D-B-D 프로세스</h2>

    <div class="main-visual">
        <div class="process-flow">
            <div class="process-step">
                <div class="step-icon">A</div>
                <div class="step-name">ASSESS</div>
                <div class="step-desc">현황 분석</div>
            </div>
            <div class="process-arrow">→</div>
            <div class="process-step active">
                <div class="step-number">2</div>
                <div class="step-name">ENVISION</div>
                <div class="step-desc">방향 수립</div>
            </div>
            <div class="process-arrow">→</div>
            <div class="process-step">
                <div class="step-icon">D</div>
                <div class="step-name">DESIGN</div>
                <div class="step-desc">상세 설계</div>
            </div>
            <div class="process-arrow">→</div>
            <div class="process-step">
                <div class="step-icon">B</div>
                <div class="step-name">BUILD</div>
                <div class="step-desc">구축</div>
            </div>
            <div class="process-arrow">→</div>
            <div class="process-step">
                <div class="step-icon">D</div>
                <div class="step-name">DEPLOY</div>
                <div class="step-desc">실행</div>
            </div>
        </div>
    </div>

    <div class="so-what">
        모든 컨설팅 프로젝트는 이 5단계를 따라 진행돼요
    </div>
</section>
```

---

## Type 3: Data Visualization (수치 강조)

**용도**: 통계, KPI, 비교 데이터, 성과
**특징**: 대형 숫자, 차트, Insight 박스

### 템플릿 코드

```html
<!-- Type 3: Data Visualization -->
<section class="data-slide">
    <!-- 슬라이드 제목 -->
    <h2>컨설팅의 임팩트</h2>

    <!-- 핵심 수치 (2-3개) -->
    <div class="big-numbers">
        <div class="number-card">
            <div class="big-number">300%</div>
            <div class="number-label">평균 투자 대비<br>수익률</div>
        </div>
        <div class="number-card">
            <div class="big-number">6개월</div>
            <div class="number-label">평균 프로젝트<br>기간</div>
        </div>
        <div class="number-card">
            <div class="big-number">$2.5M</div>
            <div class="number-label">평균 프로젝트<br>규모</div>
        </div>
    </div>

    <!-- 인사이트 박스 (필수) -->
    <div class="insight-box">
        Fortune 500 기업의 80%가 연 1회 이상 컨설팅 활용
    </div>
</section>
```

### 차트 포함 예시

```html
<!-- 예시: Before/After 비교 -->
<section class="data-slide">
    <h2>BPR 프로젝트 성과</h2>

    <div class="big-numbers">
        <div class="number-card" style="border-top-color: #ff6b6b;">
            <div class="big-number" style="color: #ff6b6b;">80일</div>
            <div class="number-label">Before<br>재고 회전일</div>
        </div>
        <div class="number-card" style="border-top-color: #4fb3d9;">
            <div class="big-number" style="color: #4fb3d9;">30일</div>
            <div class="number-label">After<br>재고 회전일</div>
        </div>
        <div class="number-card" style="border-top-color: #00b894;">
            <div class="big-number" style="color: #00b894;">-62%</div>
            <div class="number-label">개선율</div>
        </div>
    </div>

    <div class="insight-box">
        프로세스 재설계로 6개월 만에 운전자본 40% 절감
    </div>
</section>
```

---

## Type 4: Framework (2x2 매트릭스)

**용도**: 우선순위화, 포지셔닝, 분류 프레임워크
**특징**: 2x2 또는 3x3, 사분면별 예시, 주의사항

### 템플릿 코드

```html
<!-- Type 4: Framework (2x2 Matrix) -->
<section class="framework-slide">
    <!-- 슬라이드 제목 -->
    <h2>이슈 우선순위화 매트릭스</h2>

    <!-- 프레임워크 컨테이너 -->
    <div class="framework-container">
        <div class="matrix-2x2">
            <!-- Q1: 영향도 높음, 실행 쉬움 -->
            <div class="matrix-cell q1">
                <h4>Quick Win</h4>
                <p>즉시 실행</p>
                <ul>
                    <li>수작업 자동화</li>
                    <li>승인 단계 간소화</li>
                    <li>중복 업무 제거</li>
                </ul>
            </div>

            <!-- Q2: 영향도 높음, 실행 어려움 -->
            <div class="matrix-cell q2">
                <h4>Major Project</h4>
                <p>별도 프로젝트화</p>
                <ul>
                    <li>ERP 고도화</li>
                    <li>조직 개편</li>
                    <li>프로세스 재설계</li>
                </ul>
            </div>

            <!-- Q3: 영향도 낮음, 실행 쉬움 -->
            <div class="matrix-cell q3">
                <h4>Fill-in</h4>
                <p>여유 시 실행</p>
                <ul>
                    <li>리포트 개선</li>
                    <li>매뉴얼 정비</li>
                    <li>교육 자료 보완</li>
                </ul>
            </div>

            <!-- Q4: 영향도 낮음, 실행 어려움 -->
            <div class="matrix-cell q4">
                <h4>Deprioritize</h4>
                <p>보류/제외</p>
                <ul>
                    <li>부가 기능</li>
                    <li>Nice-to-have</li>
                    <li>장기 검토</li>
                </ul>
            </div>
        </div>
    </div>

    <!-- 축 라벨 -->
    <div class="matrix-axes">
        <div>← 실행 용이 | 실행 어려움 →</div>
        <div>↑ 영향도 高 | 영향도 低 ↓</div>
    </div>

    <!-- 주의사항 (선택) -->
    <div class="framework-note">
        Quick Win부터 시작해 신뢰 확보 → Major Project 추진
    </div>
</section>
```

### 3x3 매트릭스 예시

```html
<!-- 예시: 시장 포지셔닝 -->
<section class="framework-slide">
    <h2>컨설팅 펌 포지셔닝</h2>

    <div class="framework-container">
        <table style="width: 100%; border-collapse: collapse;">
            <thead>
                <tr>
                    <th style="background: #003d5c; color: white; padding: 16px;">가격/전문성</th>
                    <th style="background: #003d5c; color: white; padding: 16px;">전략</th>
                    <th style="background: #003d5c; color: white; padding: 16px;">운영</th>
                    <th style="background: #003d5c; color: white; padding: 16px;">IT</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td style="padding: 16px; font-weight: 700; background: #f8f9fa;">프리미엄</td>
                    <td style="padding: 16px; background: #4fb3d9; color: white;">MBB</td>
                    <td style="padding: 16px; background: #f8f9fa;">-</td>
                    <td style="padding: 16px; background: #f8f9fa;">-</td>
                </tr>
                <tr>
                    <td style="padding: 16px; font-weight: 700; background: #f8f9fa;">미드티어</td>
                    <td style="padding: 16px; background: #00a4a6; color: white;">Big 4</td>
                    <td style="padding: 16px; background: #00a4a6; color: white;">Big 4</td>
                    <td style="padding: 16px; background: #00a4a6; color: white;">Big 4</td>
                </tr>
                <tr>
                    <td style="padding: 16px; font-weight: 700; background: #f8f9fa;">부티크</td>
                    <td style="padding: 16px; background: #fdcb6e;">특화 펌</td>
                    <td style="padding: 16px; background: #fdcb6e;">특화 펌</td>
                    <td style="padding: 16px; background: #fdcb6e;">SI 업체</td>
                </tr>
            </tbody>
        </table>
    </div>

    <div class="framework-note">
        포지셔닝에 따라 프로젝트 유형, 고객사, 보수 체계가 달라져요
    </div>
</section>
```

---

## Type 5: Process Flow (단계별 프로세스)

**용도**: 워크플로우, 단계별 가이드, 방법론
**특징**: 최대 5단계, 아이콘, 현재 단계 강조

### 템플릿 코드

```html
<!-- Type 5: Process Flow -->
<section>
    <!-- 슬라이드 제목 -->
    <h2>인터뷰 프로세스</h2>

    <!-- 프로세스 플로우 -->
    <div class="process-flow">
        <!-- Step 1 -->
        <div class="process-step">
            <div class="step-number">1</div>
            <div class="step-name">준비</div>
            <div class="step-desc">대상자 선정<br>질문지 작성</div>
        </div>

        <div class="process-arrow">→</div>

        <!-- Step 2 (현재 단계) -->
        <div class="process-step active">
            <div class="step-number">2</div>
            <div class="step-name">실행</div>
            <div class="step-desc">개방형 질문<br>적극적 경청</div>
        </div>

        <div class="process-arrow">→</div>

        <!-- Step 3 -->
        <div class="process-step">
            <div class="step-number">3</div>
            <div class="step-name">분석</div>
            <div class="step-desc">인사이트 추출<br>패턴 파악</div>
        </div>

        <div class="process-arrow">→</div>

        <!-- Step 4 -->
        <div class="process-step">
            <div class="step-number">4</div>
            <div class="step-name">검증</div>
            <div class="step-desc">교차 확인<br>추가 인터뷰</div>
        </div>

        <div class="process-arrow">→</div>

        <!-- Step 5 -->
        <div class="process-step">
            <div class="step-number">5</div>
            <div class="step-name">문서화</div>
            <div class="step-desc">보고서 작성<br>공유</div>
        </div>
    </div>

    <!-- 메타 정보 (선택) -->
    <div class="process-meta">
        <div class="meta-item">
            <span class="meta-icon">⏱️</span>
            <span>총 소요시간: 2-3주</span>
        </div>
        <div class="meta-item">
            <span class="meta-icon">📋</span>
            <span>산출물: 인터뷰 요약서</span>
        </div>
    </div>
</section>
```

### 아이콘 사용 예시

```html
<!-- 예시: A-E-D-B-D 프로세스 -->
<section>
    <h2>컨설팅 프로젝트 라이프사이클</h2>

    <div class="process-flow">
        <div class="process-step">
            <div class="step-icon">🔍</div>
            <div class="step-name">ASSESS</div>
            <div class="step-desc">3-4주</div>
        </div>
        <div class="process-arrow">→</div>
        <div class="process-step">
            <div class="step-icon">🎯</div>
            <div class="step-name">ENVISION</div>
            <div class="step-desc">2-3주</div>
        </div>
        <div class="process-arrow">→</div>
        <div class="process-step active">
            <div class="step-icon">📐</div>
            <div class="step-name">DESIGN</div>
            <div class="step-desc">4-6주</div>
        </div>
        <div class="process-arrow">→</div>
        <div class="process-step">
            <div class="step-icon">🔨</div>
            <div class="step-name">BUILD</div>
            <div class="step-desc">8-12주</div>
        </div>
        <div class="process-arrow">→</div>
        <div class="process-step">
            <div class="step-icon">🚀</div>
            <div class="step-name">DEPLOY</div>
            <div class="step-desc">2-4주</div>
        </div>
    </div>

    <div class="so-what-box">
        전체 프로젝트는 평균 6개월, 팀 규모 3-5명으로 진행돼요
    </div>
</section>
```

---

## 보너스: 인사이트 박스 종류

### So What Box (핵심 메시지)

```html
<div class="so-what-box">
    💡 핵심: 여기에 핵심 메시지를 작성하세요
</div>
```

### Insight Box (데이터 인사이트)

```html
<div class="insight-box-teal">
    데이터가 말하는 인사이트를 작성하세요
</div>
```

### Warning Box (주의사항)

```html
<div class="warning-box">
    함정, 주의사항, 피해야 할 것을 작성하세요
</div>
```

### Tip Box (실무 팁)

```html
<div class="tip-box">
    시니어 컨설턴트들이 쓰는 비법을 작성하세요
</div>
```

---

## 체크리스트

슬라이드 제작 전:
- [ ] 이 슬라이드의 "So What?"은 무엇인가?
- [ ] 어떤 타입이 가장 적합한가?
- [ ] 텍스트 없이 비주얼만으로 이해 가능한가?

슬라이드 제작 후:
- [ ] 텍스트는 3줄 이하인가?
- [ ] 메인 비주얼이 화면의 60% 이상인가?
- [ ] So What/Insight 박스가 있는가?
- [ ] 색상 사용이 의미를 전달하는가?

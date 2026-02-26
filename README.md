# 만세력 달력 (Manseryeok Calendar)

한국 전통 사주명리학 기반의 일진 조회 웹 애플리케이션입니다.

## 📌 프로젝트 소개

만세력은 한국의 전통 역법으로, 날짜별 천간지지(天干地支)와 각종 길흉신살을 조회할 수 있는 시스템입니다. 
본 프로젝트는 다음 요소들을 통합하여 제공합니다:

- **일진(日辰)**: 매일의 간지 정보
- **12신살**: 천살, 지살, 재살 등 12가지 신살
- **12운성**: 장생, 목욕, 관대 등 생명 주기 단계
- **자미두수**: 12궁위 기반 운세 해석

## 🤖 AI 협업 개발 방식

본 프로젝트는 **3가지 AI 도구를 활용한 협업 개발**의 사례입니다.

```
┌─────────────────┐
│   GitHub Copilot  │ → 계산 로직 개발
│                   │   (12신살/12운성 알고리즘)
└─────────┬─────────┘
          │
          ↓
┌─────────────────┐
│   ChatGPT       │ → 만세력 데이터 생성
│   Gemini        │ → 자미두수 궁위 해석
└─────────┬─────────┘
          │
          ↓
┌─────────────────┐
│   Claude        │ → 시스템 통합 & 디버깅
│                 │   (HTML/JSON 연동)
└─────────────────┘
```

### 역할 분담

1. **GitHub Copilot**
   - 순수 계산 로직 개발
   - 간지 계산, 12신살/12운성 매칭 알고리즘
   - 제약사항: "미래 예측 서비스" 정책으로 해석 생성 불가

2. **ChatGPT & Gemini**
   - 날짜별 만세력 데이터 생성
   - 자미두수 12궁위 해석 텍스트
   - 십성, 28수, 길흉 판단 컨텐츠

3. **Claude**
   - 전체 시스템 통합
   - HTML/CSS/JavaScript 구조 설계
   - 버그 수정 및 데이터 검증
   - 사용자 인터페이스 최적화

## 🛠️ 기술 스택

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Data Format**: JSON
- **Styling**: Custom CSS (Apple Design Guidelines 참고)
- **No Dependencies**: 외부 라이브러리 없이 순수 웹 기술만 사용

## ✨ 주요 기능

### 1. 달력 인터페이스
- 월별 달력 뷰
- 각 날짜별 간지 표시
- 날짜 클릭 시 상세 정보 표시

### 2. 일진 정보
- 십성(十星): 편재, 정재, 비견 등
- 28수(宿): 각, 항, 저, 방, 심, 미, 기 등
- 지지 관계: 충, 형, 합, 파, 해
- 테마, 조언, 메시지

### 3. 12신살/12운성
- **12신살**: 천살, 지살, 재살, 년살, 월살, 화개살, 귀문살, 반안살
- **12운성**: 장생, 목욕, 관대, 건록, 제왕, 쇠, 병, 사, 묘, 절, 태, 양

### 4. 자미두수 12궁위
- 명궁, 형제궁, 부부궁, 자녀궁
- 재백궁, 질액궁, 천이궁, 노복궁
- 관록궁, 전택궁, 복덕궁, 부모궁

## 📂 프로젝트 구조

```
manseryeok-demo/
├── index_sample.html          # 메인 HTML 파일
├── korea_data_sample.json     # 2026년 3월 만세력 데이터
├── dictionary_FINAL.json      # 용어 사전
├── jami_data.json            # 자미두수 궁위 데이터
└── README.md                 # 본 문서
```

## 🚀 로컬 실행 방법

1. **저장소 클론**
```bash
git clone https://github.com/yourusername/manseryeok-demo.git
cd manseryeok-demo
```

2. **로컬 서버 실행**
```bash
# Python 3
python -m http.server 8000

# Node.js (http-server)
npx http-server
```

3. **브라우저 접속**
```
http://localhost:8000
```

## ⚠️ 데모 안내

**본 애플리케이션은 데모 버전입니다.**

- 샘플 데이터: 2026년 3월 (31일)
- 가상 인물 사주: 1991년 4월 22일 21시 출생 (임자일주)
- 실제 사용자 데이터가 아닌 데모용 데이터입니다

## 📊 데이터 구조

### korea_data_sample.json
```json
{
  "YYYY-MM-DD": {
    "date": "날짜",
    "day_ganzhi": "일진 간지",
    "ten_god": "십성",
    "twelve_woonsung": "12운성",
    "twelve_shinsal": "12신살",
    "theme": "테마",
    "advice": "조언",
    "message": "메시지"
  }
}
```

### jami_data.json
```json
{
  "궁위명": {
    "subtitle": "궁위 설명",
    "stars": "주요 성",
    "details": [...],
    "summary": "요약"
  }
}
```

## 🔄 향후 계획

- [ ] 모바일 앱 버전 (APK)
- [ ] 개인화 데이터 입력 기능
- [ ] 추가 날짜 범위 확장
- [ ] PWA(Progressive Web App) 지원

## 📝 라이선스

MIT License

## 👤 개발자

- **포지션**: PM (3년차)
- **목표**: Growth PM 전환
- **특기**: AI 도구 활용 프로젝트 매니징

## 🙏 감사

- Copilot: 핵심 계산 로직
- OpenAI ChatGPT: 데이터 생성
- Google Gemini: 자미두수 해석
- Anthropic Claude: 시스템 통합

---

**⭐ 이 프로젝트가 마음에 드셨다면 Star를 눌러주세요** 

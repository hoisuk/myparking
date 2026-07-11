# 🅿️ 내 차 어디있지? (MyParking)

지하 다층 주차장에서 **내가 몇 층에 주차했는지** 한 번의 탭으로 기록하고, 다음에 열면 바로 확인하는 개인용 모바일 웹앱.

> **🔗 바로 사용하기 →** https://hoisuk.github.io/myparking/

---

## 주요 기능

- **원탭 저장** — B1 / B2 / B3 버튼을 탭하면 펄스 애니메이션 후 층·시각이 자동 저장
- **현재 위치 카드** — 저장된 층(대형 숫자)과 "오늘 오후 3:24 저장" 형태의 시각 표시
- **위치 지우기** — "차 찾음 · 위치 지우기"로 다음 주차를 위해 초기화
- **층별 색상 코드** — B1 골드 / B2 청록 / B3 코랄
- **텔레그램 알림** — 주차 저장 시 내 텔레그램으로 자동 메시지 전송 (앱 설정창에서 봇 토큰·Chat ID 입력, 기기에만 저장)
- **호랑이 홈 화면 아이콘** — 검정 배경 + 오렌지 호랑이
- **오프라인 유지** — `localStorage`에 저장되어 앱을 껐다 켜도 위치 유지

## 사용 방법 (아이폰)

1. Safari로 https://hoisuk.github.io/myparking/ 접속
2. 공유 버튼 → **"홈 화면에 추가"** → 앱처럼 실행
3. 주차 후 층 버튼을 탭 → 자동 저장

### 텔레그램 알림 설정 (선택)

1. 텔레그램에서 `@BotFather` → `/newbot`으로 봇 생성 후 토큰 복사
2. 만든 봇에게 아무 메시지나 한 번 전송
3. 앱 하단 **"🔔 텔레그램 알림 설정"** 펼치고 토큰 붙여넣기 → **[Chat ID 찾기]**
4. 알림 토글 ON → **[테스트 전송]** 확인 → **[알림 설정 저장]**

> 봇 토큰은 이 기기(localStorage)에만 저장되며 저장소·서버에 올라가지 않습니다.

## 기술 스택

- 단일 HTML 파일, Vanilla JavaScript (프레임워크·백엔드 없음)
- 저장: 브라우저 `localStorage`
- 알림: Telegram Bot API (클라이언트에서 직접 호출)
- 배포: GitHub Pages
- 폰트: Oswald · Noto Sans KR · JetBrains Mono

## 파일 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 앱 본체 (GitHub Pages 진입점) |
| `parking-finder.html` | `index.html`과 동일 사본 (PRD 참조 파일명) |
| `parking-finder-PRD.md` | 제품 요구사항 문서 |
| `apple-touch-icon.png` / `icon-512.png` / `favicon-32.png` | 호랑이 아이콘 |

## 로컬에서 수정 후 배포

```bash
git add -A && git commit -m "수정 내용" && git push
```

푸시하면 GitHub Pages가 자동 재빌드되어 몇 분 내 같은 주소에 반영됩니다.

---

made by **Tiger Soft** 🐯

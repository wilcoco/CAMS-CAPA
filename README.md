# 도장 라인 CAPA · 품질수율 분석 대시보드

자동차 도장 라인의 생산능력(CAPA)과 품질수율(직행률 · 리페어 · 재도장 · 폐각)을
슬라이더로 조정하며 분석하는 웹 대시보드입니다.

## 주요 기능
- 9개 주요 변수 슬라이더 조정 (직행률 / 리페어대상률 / 리페어소화율 / 재도장률 / 폐각률 / UPH / 가동율 / 가용시간 / 투입배율)
- 실시간 산출: 양품율, 최종 양품률, 라인 부하율(재도장 가중), 시간당 물량 균형(리페어 병목 진단)
- 품질 흐름 시각화 및 품목별 도장 부하표

## 로컬 실행
```bash
npm start          # http://localhost:3000
```
의존성 없음(Node 18+ 내장 모듈만 사용).

## Railway 배포
1. Railway에서 **New Project → Deploy from GitHub repo** 선택
2. 이 저장소 / 브랜치 선택
3. Nixpacks가 `package.json`을 감지 → `npm start` 자동 실행
4. 서버는 Railway가 주입하는 `$PORT`에 바인딩됨 (`server.js`)
5. **Settings → Networking → Generate Domain**으로 공개 URL 생성

설정은 `railway.json`에 정의되어 있습니다.

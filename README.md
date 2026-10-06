# stewardcopilot.com

Steward Copilot LLC 회사 홈페이지. 빌드 과정 없는 정적 단일 페이지 —
`index.html` + `assets/`(실제 제품 스크린샷)가 전부다.

목적: GolfNow Affiliate 심사자가 신청서의 bk.jeon@stewardcopilot.com 도메인을
방문했을 때 "실제 운영자"로 보이는 것. 내용은 전부 사실만 담는다 — 라이브 제품
4종 링크, TeeSniper 파일럿 실스크린샷, 각 제품 레포에서 가져온 설명, 코드로
존재하는 통합 원칙. 가짜 고객사·지표·팀 금지.

## 배포 (GitHub Pages — 최초 1회 설정)

1. 이 레포 **Settings → Pages** → Source: *Deploy from a branch* →
   Branch `main` / `/ (root)` → Save.
2. 같은 화면 Custom domain에 `stewardcopilot.com` 입력 → Save
   (`CNAME` 파일이 이미 있으므로 유지됨). "Enforce HTTPS" 체크.
3. 도메인 등록기관 DNS에서:
   - A 레코드 4개: `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - `www` → CNAME `byungkwonjeon.github.io`
4. 전파 후(수 분~수 시간) https://stewardcopilot.com 확인:
   라이트/다크 모드, 폰 화면 폭, `mailto:` 링크, 제품 링크 5개.

이후 수정은 main에 push하면 자동 배포된다.

## 수정 시 주의

- **신청서와 문구 일관성** — 심사자는 TeeSniper 레포의
  `docs/AFFILIATE_API_APPLICATION.md` 제출본과 이 사이트를 교차 확인한다.
  특히 "official channels" 포지셔닝, 런칭 지역(LA/OC), 연락처, "Steward
  Copilot LLC" 표기.
- **제품 상태 태그는 정직하게** — Live는 클릭해서 멀쩡한 것만. 깨진 링크보다
  "In development" 라벨이 낫다.
- 스크린샷 교체: TeeSniper UI가 바뀌면 390x844 뷰포트(deviceScaleFactor 2)로
  재캡처해 `assets/`를 교체.
- 과장 금지: 지표·고객·파트너 로고는 실제로 생기기 전까지 싣지 않는다.

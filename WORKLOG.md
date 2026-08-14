# 작업 기록 — 2026-08-14

## 현재 상태
- 실제 서비스 주소: mzcd-code-manager.vercel.app/code-manager.html
- 배포는 Vercel이 담당하며, GitHub 저장소 aiden-220/mzcd-code-manager 의 main 브랜치와 연결되어 있음. 거기에 커밋하면 자동 재배포됨.
- 이 저장소(Music-Code-Management-System)에는 같은 code-manager.html 사본을 보관 중.
- 주의: 배포에 연결된 것은 mzcd-code-manager 쪽. 이 사본을 고쳐도 실제 페이지는 바뀌지 않음.
- 데이터 저장 방식: 브라우저 localStorage (키 이름 mzcd_codes_v1). 기기 간 동기화 없음.

## 완료한 것
- Vercel 배포 완료 및 기능 테스트 통과
- 새 코드 발급 / 중복 검사 → 토스트 정상, 브라우저 alert 안 뜸
- 전체 삭제 → 페이지 내 커스텀 모달 정상, 브라우저 confirm 안 뜸
- 콘솔 에러 없음
- 테스트로 발급했던 코드 11건 삭제 완료 (현재 0건)

## 남은 할 일
1. 루트 주소(/)가 404. vercel.json 리라이트 추가 필요.
2. 저장 방식을 localStorage에서 서버(Supabase)로 옮길지 검토 중.
   - 미정: 어느 Supabase 프로젝트를 쓸지
   - 미정: 혼자 쓸지 팀이 같이 쓸지. 팀이면 코드 목록을 공유해야 중복 검사가 제대로 동작함.
3. 자동 백업 보강 (지금은 JSON 내보내기 수동)
4. 저장소 정리: 같은 파일이 두 저장소에 있음. 하나로 합칠지 결정 필요.
5. favicon 없음

## 주의사항
- aiden-220/YouTube-Upload-Check 는 용도가 다른 저장소. 건드리지 말 것.
- 이 저장소는 Public(공개). API 키나 비밀번호를 코드에 절대 넣지 말 것.

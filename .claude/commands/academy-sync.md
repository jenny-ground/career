---
description: 이미 만든 과외 학원(예: 일본어)에 영어 학원의 최신 운영 개선 사항을 반영한다
argument-hint: <학원 폴더, 예: japanese>
---

`$ARGUMENTS` 폴더의 과외 학원을 최신 운영 방식으로 업데이트해줘.

1. 최신 플레이북을 가져온다: `git fetch origin ccr-266527c7-lmdhm7` 후 `git show origin/ccr-266527c7-lmdhm7:academy-playbook.md`를 읽는다. 참고 구현은 같은 브랜치의 `english/claude-teacher.md`, `english/academy/roadmap.md`, `english/academy/pattern-bank.md`.
2. 플레이북 **7. 기존 학원 업데이트 목록**(U1~U6)을 하나씩 확인해서, `$ARGUMENTS/` 학원에 빠진 것만 반영한다. 언어에 맞게 바꾼다(예: 일본어는 부록의 "일본어 대화 패턴 초안"으로 pattern-bank.md를 만들고, 쓰임새는 정중체/반말/비즈니스 경어).
3. 지침 원본을 고치면 노션 "선생님 지침" 사본도 똑같이 고친다(fetch 후 저장 형식에 맞춰 update_content). 노션 "핵심 표현" 표에 `종류`(패턴/문장) 칸이 없으면 추가한다.
4. 이 세션의 주간 점검 예약 프롬프트에 pattern-bank.md 읽기를 넣고, 플레이북 5번 "이틀 점검 예약"으로 새 예약을 만든다(다른 학원과 시간이 겹치지 않게).
5. 이 세션의 브랜치에 커밋·푸시하고, 학생에게 바뀐 점을 3~5줄로 알린다.

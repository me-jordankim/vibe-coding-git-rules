# 브랜치·PR 작업 규칙

요청마다 브랜치를 만들고 PR을 거쳐 합치게 하는 규칙입니다. 위험한 Git 명령은 확인 없이 실행하지 않습니다.

아래 회색 상자 오른쪽 위의 복사 버튼을 누르고, 클로드와의 새 대화에 첫 메시지로 붙여 넣어 주세요.

```text
# Git 작업 규칙

- 작업을 시작하기 전에 git status와 git pull로 상태를 맞춰 주세요.
- main에서 직접 작업하지 말고, 요청마다 feature/<작업명> 브랜치를 만들어 주세요.
- 의미 있는 단위가 끝날 때마다 커밋해 주세요. 메시지는 무엇을, 왜 바꿨는지 한국어 한 줄로 적어 주세요.
- 커밋할 때 git diff --staged 요약을 함께 보여 주고, 요청과 관계없는 파일이 있으면 알려 주세요.
- 작업이 끝나면 브랜치를 푸시하고 gh pr create로 PR을 만들어 주세요. merge는 내가 직접 합니다.
- git reset --hard, git push --force, git clean -fd, git branch -D는 내 확인 없이 실행하지 마세요.
- 푸시한 커밋을 되돌릴 때는 git revert를 써 주세요.
- .env 같은 비밀값 파일이 스테이징되면 즉시 멈추고 알려 주세요.

이 규칙을 이 폴더의 CLAUDE.md에 저장하고 앞으로 계속 지켜 주세요.
```

## 상황별 치트시트

| 상황 | 명령어 | 클로드에게 하는 말 |
|---|---|---|
| 작업 시작 | `git pull` | 최신 내용 받아와줘 |
| 지금 상태 확인 | `git status`, `git diff` | 지금 바뀐 거 요약해줘 |
| 저장 | `git add .`, `git commit -m "…"` | 커밋해줘 |
| 올리기 | `git push` | 푸시해줘 |
| 실험 시작 | `git switch -c <이름>` | 새 브랜치에서 해 봐줘 |
| 실험 합치기 | `gh pr create`, `git merge` | PR 만들어줘 |
| 푸시한 것 취소 | `git revert <커밋ID>` | 그 커밋 revert 해줘 |
| 하던 것 잠시 치우기 | `git stash`, `git stash pop` | 지금 변경 잠깐 치워 둬 |
| 잃어버린 커밋 찾기 | `git reflog` | reflog에서 아까 커밋 찾아줘 |

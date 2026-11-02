# 06. VSCode GitHub 연동 증거

VSCode에서 GitHub 계정(linkcontent7-huisun)으로 로그인했고, AllinONE 저장소를 열어 원격 주소를 확인했다. 캡처는 `E1-1/screenshots/`에 있다.

## 1. 계정 로그인 확인 (캡처: [vscode-github-account-menu.png](../screenshots/vscode-github-account-menu.png))

VSCode 왼쪽 아래 계정 메뉴에 `linkcontent7-huisun (GitHub)`이 로그인된 상태로 표시된다.

## 2. 원격 저장소 확인 (캡처: [vscode-git-remote-terminal.png](../screenshots/vscode-git-remote-terminal.png))

```
$ git remote -v
origin	git@github.com:linkcontent7-huisun/AllinONE.git (fetch)
origin	git@github.com:linkcontent7-huisun/AllinONE.git (push)
```

## 3. 현재 브랜치 확인
```
$ git branch --show-current
main
```

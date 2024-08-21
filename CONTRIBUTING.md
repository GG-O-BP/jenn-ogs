# 개발 환경

운영 체제에 최소 4GB의 물리적 메모리 할당과 4GB의 스왑 공간이 할당되어 있어야 하며, 그렇지 않으면 `npm run dev` 명령어가 시스템을 멈추게 할 수 있습니다.

설정은 간단합니다. [Node.js](https://nodejs.org/)를 설치한 후, 저장소를 클론하고 작업 디렉토리 내에서 다음 명령어를 실행하세요:

```
# 처음 한 번만 실행하면 됩니다
npm install yarn
npm run yarn install
npx husky install

# 개발 서버와 빌드 시스템을 시작하려면 이 명령어를 실행하세요
npm run dev
```
npm install yarn 명령어를 실행할 때 React 종속성 오류가 발생하면, 대신 다음을 시도해 보세요:
```
sudo npm install --global yarn
```
리눅스를 사용 중이라면, `make` 명령어를 입력하면 모든 작업이 자동으로 수행됩니다.

윈도우를 사용 중이고 도구 설치 및 저장소 클론에 대한 구체적인 도움이 필요하다면, 아래의 [상세 설정 단계](#detailed-setup-steps-windows-but-applicable-mostly-to-others)를 참조하세요.

(그리고... 이 상세 단계는 리눅스/맥OS에서 시작하는 방법에 대한 유용한 포인터가 될 수 있습니다: 세부 사항이 약간 다를 수 있지만, 전반적으로 적용 가능합니다.)

실행 중인 경우, [http://dev.beta.online-go.com:1420/](http://dev.beta.online-go.com:1420/)로 이동하여 방금 gulp로 시작한 로컬 서버에서 인터페이스를 로드하고 테스트를 위해 베타 서버에 연결할 수 있습니다.

## 시작하기

-   [GitHub 계정](https://github.com/signup/free)에 가입하세요.
-   [이슈 트래커](https://github.com/online-go/online-go.com/issues)에서 문제가 이미 제출되었는지 또는 개선 요청이 있는지 검색하세요.
-   이슈가 존재하지 않는 경우, 이슈를 제출하세요. 가능한 한 아래 정보를 포함해 주세요:
    -   명확한 요약.
    -   테스트한 운영 체제.
    -   버그가 발생한 브라우저 (또는 여러 브라우저에서 버그를 재현한 경우).
    -   브라우저 버전.
    -   문제를 재현하는 단계.
    -   유용할 수 있는 추가 정보.

## 변경 사항 만들기

1. [저장소 포크](https://help.github.com/articles/fork-a-repo/).
    - 아직 하지 않았다면, [git 설정](https://help.github.com/articles/set-up-git/).
2. 저장소를 컴퓨터에 클론하세요. (포크한 저장소를 최신 상태로 유지하는 방법의 2단계에 설명되어 있습니다.)
    - 최신 업데이트를 추적하려면, git을 구성하여 포크를 원래의 online-go 저장소와 동기화해야 합니다. (동일한 문서의 3단계를 참조하세요.)
    - 클론이 완료되지 않으면 [Git LFS](https://git-lfs.github.com/)를 설치해야 할 수 있습니다.
3. 로컬 머신에서 [브랜치 생성](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/). 업데이트에 적합한 이름을 지정하세요.
    - 이 작업은 [git bash 명령줄](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches)에서도 수행할 수 있습니다.
    - 첫 번째 방법을 사용한 경우, [프로젝트의 원격 브랜치를 가져오기](https://stackify.com/git-checkout-remote-branch/)를 확인해야 합니다.
4. 코드 또는 문서에서 원하는 변경 사항을 만드세요.
5. 변경 사항을 [추가, 커밋 및 푸시](https://help.github.com/articles/adding-a-file-to-a-repository-using-the-command-line/)하세요.

## 변경 사항 제출하기

1. GitHub에서 포크한 저장소의 생성한 브랜치로 이동하세요.
2. [`새 풀 리퀘스트`](https://help.github.com/articles/creating-a-pull-request/)를 선택하세요.
3. 제안된 업데이트에 적합한 제목과 댓글을 작성하세요.
4. 풀 리퀘스트를 생성하세요.

## 사용된 기술

이 프로젝트는 주로 TypeScript와 React로 구축되었습니다. 이들에 익숙하지 않다면, 몇 분 동안 익숙해지세요.

-   [React](https://reactjs.org/)
-   [TypeScript](https://www.typescriptlang.org/)

## 상세 설정 단계 (윈도우, 대부분 다른 운영 체제에도 적용 가능)

0. [online-go.com](http://online-go.com)을 포크하세요.
 - [github.com](http://github.com/)에 계정을 만들고 로그인하세요.
 - [GitHub - online-go/online-go.com: Source code for the Online-Go.com web interface](https://github.com/online-go/online-go.com)로 이동하세요.
 - "포크" 버튼을 누르세요.

1. VSCode 설치

2. 윈도우 설치 프로그램에서 git 설치: [Git - Downloading Package (git-scm.com)](https://git-scm.com/download/win).
       모든 기본값을 선택 _하지만_ "**라인 엔딩 변환 구성**"은 제외하세요.
       설명이 무엇이든 상관없이, `checkout-as-is, commit-as-is`를 선택하세요 (설명은 이 옵션을 원하지 않을 것처럼 들리지만).
3. https://github.com/coreybutler/nvm-windows/releases에서 `nvm-setup.exe`를 다운로드하고 실행하세요.
4. 명령어 창에서 다음을 실행하세요.

`nvm install lts`

`npm install -g yarn`

`npm install -g husky`

5. VSCode 열기
 - "git 저장소 클론" 선택
 - "github에서 클론" 선택
 - GitHub에 로그인하도록 허용
 - online-go.com의 *포크한 저장소*를 클론하도록 선택
    - **반드시 포크한 저장소인지 확인** - VSCode는 목록 상단에 공식 저장소를 제공할 수 있으므로, 그 저장소를 선택하지 마세요.
 - 클론할 적절한 로컬 폴더를 선택 (이전에 남은 것과는 확실히 구분되는 폴더여야 합니다!)
 - 권장 확장 프로그램 설치에 동의
     (이 확장 프로그램들은 OGS에 필수적이며, 코딩 표준을 설정하고 편집 중에 린팅을 제공합니다.)

... 이제 VSCode의 왼쪽 창에 OGS 저장소 파일 구조를 보여주는 코드 탐색기가 표시됩니다 (이 보기를 얻으려면 왼쪽 창의 맨 위 아이콘을 클릭해야 할 수도 있습니다).

... 이제 online-go.com을 체크아웃했으며, 불필요한 CRLF 문제 없이 사용할 수 있습니다!

`src/` 디렉토리를 탐색할 수 있습니다.

6. 명령어 창에서 클론된 저장소가 있는 폴더로 이동하여 다음을 실행하세요.

`yarn`

`npm run dev`

이 명령어는 많은 패키지를 설치한 후 서버를 시작하고 실행 중임을 알려줍니다.

브라우저에서 localhost:1420으로 이동하여 로컬 체크아웃이 베타 서버를 렌더링하는지 확인하세요.

... 그리고 이것이 작동하면, VSCode가 완료되고 무언가를 편집할 준비가 된 것입니다.

즉시 무언가를 편집할 수 있습니다:

 - VSCode의 왼쪽 상단 창에서 검색 돋보기를 클릭하세요.
 - 검색 창에 `no games being played`를 입력하세요.

이 문자열이 [ObserveGamesComponent.tsx](src/components/ObserveGamesComponent/ObserveGamesComponent.tsx)에 있는 위치를 보여줄 것입니다.

 - 해당 위치로 이동하려면 클릭하세요.
 - 문자열을 편집하고 파일을 저장하세요.
 - 브라우저에서 "Watch" 페이지가 열려 있는 상태에서 해당 문자열이 업데이트되는 것을 확인하세요.

:tada: OGS UI를 편집했습니다.

7.  변경 사항 커밋 (로컬)

변경 사항을 로컬에서 정기적으로 커밋하고 싶을 것입니다. 이를 준비하기 위해 브랜치를 만들어야 합니다.

이 작업은 VSCode에서 가장 쉽게 수행할 수 있습니다 - 왼쪽 하단에 현재 사용 중인 브랜치를 나타내는 레이블이 있습니다. "소스 제어" 기호 (브랜치 모양)와 브랜치 이름이 표시됩니다. 브랜치를 만들고 커밋하려면:
 - 브랜치 레이블을 클릭하세요.
 - "브랜치 생성" 선택
 - 이름을 지정하세요.

그런 다음

 - 왼쪽 창에서 "소스 제어" 기호를 클릭하세요 (git 작업 선택).
 - 명확한 커밋 메시지를 입력란에 입력하세요.
 - 커밋을 클릭하세요.

이 세 단계를 자주 수행하세요 :slight_smile:

8. 변경 사항 게시 (GitHub에)

 변경 사항이 OGS에 통합될 준비가 되면:

 - 왼쪽에서 "소스 제어"를 클릭하세요.
 - "변경 사항 게시"를 클릭하세요.

**참고**: "게시" 대신 "동기화"라고 표시될 수 있습니다 - 이는 GitHub이 이전에 수행한 작업으로 인해 브랜치를 이미 알고 있다는 의미입니다. 괜찮습니다.

🎉 이제 코드가 메인 저장소로 풀 리퀘스트를 보낼 준비가 되었습니다.

# GIT 시나리오 체험

실제 서비스를 만들기 위해서는 3가지 브랜치가 필요하다.  
**Master 브랜치**, **dev 브랜치**, **topic 브랜치** 이 3가지 브랜치를 통해서 개발을 해볼 예정이다.  
이번 시나리오에서는 1. 환경설정 2. 회원가입 3. 로그인 4. 글쓰기 4가지 기능을 만들 것이다.

## 1. GitHub에서 Repository 만들기

- GitHub에서 새 레포지토리를 만들기 위해 **New repository** 버튼을 클릭한다.  
  ![New Repository](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/219ad56e-58e4-419a-ab07-89bcd506097f/image.png)

- **README 파일을 추가**하면 브랜치가 하나 만들어진다.  
  ![README 생성](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/0a1bdf06-02a0-4ed3-9311-b3bb6e0f4d5a/image.png)

- **README 파일을 생성하지 않으면 브랜치가 만들어지지 않는다**.  
  Add a README file 체크하지 않으면 `git init`만 되고, 체크하면 파일이 생성된다.  
  ![파일 생성](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/e3c02081-cc5c-49b0-9780-5f0c3258e910/image.png)

- 커밋 로그가 하나 생긴다.  
  ![commit](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/91a45a7b-94ed-434e-b1a9-69c5a05943c9/image.png)

- `initial commit`이라는 커밋 로그가 하나 생긴다.  
  리드미 파일을 생성하고 `add`, `commit`까지 완료된 상태이다.  
  리드미 파일을 생성하지 않으면 `git init`까지만 된다.  
  ![git init 상태](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/d3341e14-94fd-4315-95e1-5b939be6a16a/image.png)

## 2. Git Clone

- GitHub에서 제공하는 저장소의 주소를 복사한 후, **Git Clone**을 실행한다.  
  `git clone` 명령어로 저장소를 로컬 환경에 복제한다.
  ```bash
  git clone https://github.com/MooMoongg/blog-along.git
  ```

## 3. 브랜치 설정 및 작업

- `main` 브랜치에서 개발을 하지 않고 `topic` 브랜치에서 개발을 진행한다.
- `git checkout` 명령어를 사용하여 `dev` 브랜치로 이동한다.

## 4. Fast-Forward Merge

- `git merge` 명령어로 `topic` 브랜치를 `dev` 브랜치에 병합한다.
  - 이때 **fast-forward merge**가 이루어지면, 로그는 남지 않는다.
- `git merge --no-ff` 옵션을 사용하여, **fast-forward merge** 상태에서도 로그를 남기고 병합할 수 있다.

## 5. 커밋 관리 및 rebase

- 글쓰기 기능을 구현하는 도중에 커밋 로그를 수정하고 싶을 때 `git rebase -i HEAD~2` 명령어를 사용한다.
  - `rebase` 명령어를 통해 커밋 로그를 수정하거나 합칠 수 있다.

## 6. 태그 관리

- 개발이 완료되면 `git tag` 명령어를 사용하여 태그를 추가한다.
  - `git tag blog1.0.0` 명령어로 태그를 생성하고 확인할 수 있다.
- 태그가 제대로 푸시되지 않으면, `git push origin --tags` 명령어로 태그를 푸시한다.

## 7. 푸시

- 최종적으로 `main` 브랜치에서 작업을 마친 후, 변경 사항을 원격 저장소에 푸시한다.

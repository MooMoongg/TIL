# Git 기본 명령어와 개념

## 1. Git 시작하기

- `git init`: 프로젝트 폴더에 Git을 초기화하여 `.git` 폴더 생성.
- `git add .`: 변경된 모든 파일을 업로드 대기 상태로 설정.
- `git commit -m "message"`: 파일 변경사항을 저장.
- `git remote add origin <URL>`: 원격 저장소와 연결.
- `git push origin master`: 로컬 저장소의 변경사항을 원격 저장소에 업로드.

![git-init-push](https://prod-files-secure.s3.us-west-2.amazonaws.com/53fe439d-a4fb-4a08-87dc-f8b900f6364e/247730f6-913b-469a-9d52-f33505e45627/image.png)

---

# Git의 발전과 GitHub

- **GitHub의 역할**: 개발자들이 소스 코드를 공유하고 협업하는 플랫폼.
- **GitHub과 Microsoft**: GitHub 인수 후, Microsoft는 AI 분석을 통해 소스 코드 빅데이터를 활용하고, 능력 기반으로 인재를 선발하고 해고하는 방식으로 변화.

---

# 버전 관리 시스템 (VCS) 개념

## 1. 문제점

- 파일을 덮어씌우면 과거 버전을 복구할 수 없다는 문제가 있음.
- **VCS**는 이런 문제를 해결하며, 변경된 부분만 기록하고 과거 버전으로 돌아갈 수 있는 기능 제공.

## 2. VCS, CVCS, DVCS

- **VCS**: 기본적인 버전 관리 시스템.
- **CVCS** (Centralized Version Control System): 중앙 서버에서 파일을 관리하는 방식으로 협업이 가능하지만, 중앙 서버에 문제가 생기면 작업이 불가능함.
- **DVCS** (Distributed Version Control System): Git과 같이 분산형 버전 관리 시스템으로, 각 로컬 저장소에 모든 히스토리를 저장하여 협업이 원활하고 서버 문제에 강함.

---

## 서버 wiki

https://github.com/FitToMe/FTM-server/wiki

<br>

# 업무 수행 과정

> 기본적으로 fork 없이 origin에서만 작업

### 0. GitHub Project에서 해야할 일 Draft로 작성

- 프론트의 경우 이슈 앞에 [FE] 붙이기
- 백엔드의 경우 이슈 앞에 [BE] 붙이기

  > 프론트엔드, 백엔드 작업상황을 한눈에 관리하기 위해서
  
### 1. Project에서 자기가 할 일 `issue`로 전환하기

- 업무 내용에 따라 적절한 `label` 붙이기

  > feat, bug, fix, ...

- `assignees` 본인 지정

### 2. 로컬 환경에서 `prefix/{issue번호}` 형태로 새로운 branch 생성

예시

```bash
$ git checkout -b feat/29
```

### 3. 로컬에서 작업하면서 커밋 (커밋 컨벤션 지키기)

- 작업 내용에 따라 적절한 prefix 붙이기

  > feat, fix, refactor, ...
  
- 제목에 간단하게 해당 커밋 설명하기

예시

```bash
$ git commit -m "feat: 비즈니스 로직 관련 Exception은 CustomException으로 처리하도록 변경"
```

### 4. 작업이 완료되면 origin에 push하고 origin main branch로 Pull Request 생성

- 팀원들 reviewer 등록하기

- PR 이름으로는 기본적으로 issue 명을 사용하되 앞에 붙어있는 `[BE]`나 `[FE]` 대신 작업 내용과 관련된 `prefix`를 붙인다.

  > ex) feat: 예외 처리 방식 수정
  
- PR 본문에 `resolve #{issue 번호}` 형식으로 관련된 issue를 언급하면, PR이 머지될때 해당 issue도 같이 close 되도록 할 수 있다.

  > ex) resolve #24

### 5. 다른 사람들은 review 후, squash merge

    > squash merge를 함으로써 main 브랜치에 이슈별로 커밋이 하나씩 존재함으로써 가독성 개선
    >
    > 만약 커밋을 좀 더 세세하게 확인하고 싶다면 제목에서 이슈나 PR 레퍼런스를 클릭해서 확인할 수 있다.

### 6. 해당 브랜치 삭제

```
골치아픈일이 생길 수 있기 때문에 가급적 main 브랜치에는 PR을 통해서만 merge하기.
```

<br>

#### `prefix` 예시

* feat : 새로운 기능에 대한 커밋
* fix : 버그 수정에 대한 커밋
* build : 빌드 관련 파일 수정에 대한 커밋
* chore : 그 외 자잘한 수정에 대한 커밋
* ci : CI관련 설정 수정에 대한 커밋
* docs : 문서 수정에 대한 커밋
* style : 코드 스타일 혹은 포맷 등에 관한 커밋
* refactor :  코드 리팩토링에 대한 커밋
* test : 테스트 코드 수정에 대한 커밋

[참고자료](https://overcome-the-limits.tistory.com/entry/%ED%98%91%EC%97%85-%ED%98%91%EC%97%85%EC%9D%84-%EC%9C%84%ED%95%9C-%EA%B8%B0%EB%B3%B8%EC%A0%81%EC%9D%B8-git-%EC%BB%A4%EB%B0%8B%EC%BB%A8%EB%B2%A4%EC%85%98-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0), [참고자료2](https://beomseok95.tistory.com/m/328)

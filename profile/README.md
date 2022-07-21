## 서버 wiki

https://github.com/FitToMe/FTM-server/wiki

<br>

## 업무 수행 과정

1. 자기가 할 일 issue로 생성

2. 로컬 환경에서 `#issue번호`이랑 작업내용 포함해서 새로운 branch 생성

   * `feature/#001_login_ui`
   * `fix/#001_change_login_ui`

3. 로컬에서 작업하면서 커밋 (커밋 컨벤션 지키기)

4. 작업이 완료되면 origin에 push하고 upstream main branch로 Pull Request 생성. 팀원들 reviewer 등록하기

    > PR 이름으로는 브랜치명을 사용한다.
    > 
    > 기본적으로 PR 생성시 브랜치명이 이름으로 사용된다.

5. 다른 사람들에게 확인 후 squash merge

    > squash merge를 함으로써 main 브랜치에 이슈별로 커밋이 하나씩 존재함으로써 가독성 개선
    >
    > 만약 커밋을 좀 더 세세하게 확인하고 싶다면 제목에서 이슈나 PR 레퍼런스를 클릭해서 확인할 수 있다.

6. 해당 브랜치 삭제

```
골치아픈일이 생길 수 있기 때문에 가급적 main 브랜치에는 PR을 통해서만 merge하기.
```

<br>

## 커밋 컨벤션

```
<type>: 제목

세부 설명
```

* ex) `feat: add tabling system`

#### `prefix` 종류

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

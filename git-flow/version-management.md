# version management

`package.json`에는 version이 명시되어 있다.

이를 활용하여 운영 배포되는 `master` 브랜치를 매니지먼트 하도록 한다.

version은 다음 처럼 표현된다.

- ex) `1.8.0`

점으로 구분되어 있는 숫자들은 각각 의미를 지닌다.

처음에 적혀있는 `1`은 **major**를 뜻한다.

두번째로 있는 `8`은 **minor**를 뜻한다.

세번째 `0`은 **patch**를 뜻한다.

```
<major>.<minor>.<patch>
```

## Major

major는 대규모 업데이트가 진행될 때 올린다.

major의 버전이 1 올라간다면 minor와 patch 버전을 각각 0으로 되돌린다.

- 베이스 라이브러리 변경 (ex) react.js -> next.js)
- 대규모 시스템 개편 (ex) 홈페이지 전체 리뉴얼)
- .. etc

## Minor

minor는 기능 업데이트때 올린다.

minor의 버전이 1 올라간다면 patch 버전을 0으로 되돌린다.

쉽게 말하면 feature PR은 minor 버전 1을 올리면 된다.

- UI/UX 개선
- 기존에 없던 기능 추가
- 불필요한 기능 제거

## Patch

patch는 수정 사항을 뜻한다.

patch는 hotfix와 같이 이슈 수정이 되었거나 자잘한 수정 사항이 있을 때 올린다.

## Release Note

버전은 각 작업 규모에 맞춰 유동성 있게 올리면 된다.

버전을 올리는 시점은 각 PR을 `develop`으로 병합하기 전이다.

버전이 올라가 `master` 브랜치가 운영 서버로 배포 되면 Release Note를 작성한다.

릴리즈 노트는 `master`에 병합될 때마다 항상 작성한다.

릴리즈 노트의 양식은 다음과 같다.

### 제목과 태그

제목과 태그는 릴리즈되는 버전을 명시한다.

```
v1.8.0
```

### 본문

본문에는 다음처럼된 양식으로 간략 요약해 명시한다.

```
## Updates

<!-- 추가된 기능 명시 -->

## Fixes

<!-- 수정 사항 명시 -->

## Others

<!-- 기타 -->

## Ref

<!-- PR 링크 -->

```

모두 다 적을 필요는 없으며, 필요한 사항만을 적도록 한다.

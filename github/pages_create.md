# GitHub Pages 시작하기

GitHub Pages를 이용해 개인 학습 내용을 Markdown 파일로 정리하고 웹에서 확인하는 방법을 정리한다.

---

## 1. GitHub Pages용 Repository 만들기

GitHub Pages는 일반 Repository로도 만들 수 있지만, 개인 사이트의 대표 주소로 사용하려면 Repository 이름을 아래 형식으로 만드는 것이 좋다.

```text
<GitHub아이디>.github.io
```

예를 들어 GitHub 아이디가 다음과 같다면:

```text
jwleepro
```

Repository 이름은 다음과 같이 만든다.

```text
jwleepro.github.io
```

GitHub에서:

```text
우측 상단 + 버튼
→ New repository
```

를 선택한다.

Repository 생성 화면에서 다음과 같이 설정한다.

```text
Repository name
jwleepro.github.io

Visibility
Public

Add a README file
체크
```

그리고:

```text
Create repository
```

를 클릭한다.

Repository 주소 예시:

```text
https://github.com/jwleepro/jwleepro.github.io
```

---

## 2. index.md 파일 만들기

GitHub Pages의 첫 화면으로 사용할 Markdown 파일을 만든다.

Repository에서:

```text
Add file
→ Create new file
```

을 선택한다.

파일 이름을 다음과 같이 입력한다.

```text
index.md
```

내용은 예를 들어 다음과 같이 작성할 수 있다.

```markdown
# 나만의 이야기, 정리해보자

AI를 이용해서 공부한 내용을 정리하는 개인 학습 공간입니다.

## 학습 내용

- Database
- AI
- Backend
- Architecture
```

작성 후:

```text
Commit changes...
```

버튼을 클릭하고 commit 한다.

Repository는 대략 다음과 같은 구조가 된다.

```text
jwleepro.github.io/
├── README.md
└── index.md
```

---

## 3. GitHub Pages 활성화하기

Repository 상단 메뉴에서:

```text
Settings
```

를 선택한다.

왼쪽 메뉴에서:

```text
Pages
```

를 선택한다.

`Build and deployment` 항목에서 다음과 같이 설정한다.

```text
Source
Deploy from a branch
```

Branch는:

```text
main
```

Folder는:

```text
/ (root)
```

를 선택한다.

그리고:

```text
Save
```

를 클릭한다.

설정 구조는 다음과 같다.

```text
GitHub Pages
      ↓
main branch
      ↓
repository root
      ↓
index.md
```

---

## 4. GitHub Pages 접속 확인하기

Repository 이름을 다음과 같이 만들었다면:

```text
jwleepro.github.io
```

GitHub Pages 주소는 다음과 같다.

```text
https://jwleepro.github.io/
```

브라우저에서 위 주소에 접속한다.

`index.md`에 작성한 내용이 웹 페이지로 표시되면 GitHub Pages 설정이 정상적으로 완료된 것이다.

GitHub Pages 주소는 다음 메뉴에서도 확인할 수 있다.

```text
Repository
→ Settings
→ Pages
```

---

## 5. 하위 디렉토리 만들기

GitHub 웹 화면에서는 빈 디렉토리만 별도로 생성할 수 없다.

Git은 기본적으로 빈 디렉토리를 관리하지 않기 때문이다.

따라서 파일을 만들면서 디렉토리 경로를 함께 지정한다.

예를 들어 다음과 같은 파일을 만들고 싶다면:

```text
database/postgresql.md
```

Repository에서:

```text
Add file
→ Create new file
```

을 선택한다.

파일 이름 입력란에:

```text
database/postgresql.md
```

라고 입력한다.

그러면 GitHub가 자동으로 다음 구조를 만든다.

```text
jwleepro.github.io/
├── index.md
└── database/
    └── postgresql.md
```

---

## 6. 여러 디렉토리와 Markdown 파일 추가하기

예를 들어 학습 내용을 다음과 같이 관리할 수 있다.

```text
jwleepro.github.io/
│
├── index.md
│
├── database/
│   ├── postgresql.md
│   ├── clickhouse.md
│   └── etl-elt.md
│
├── ai/
│   ├── llm.md
│   └── rag.md
│
└── architecture/
    └── data-platform.md
```

GitHub에서 각각 다음과 같은 경로로 파일을 만들면 된다.

```text
database/postgresql.md
database/clickhouse.md
database/etl-elt.md

ai/llm.md
ai/rag.md

architecture/data-platform.md
```

---

## 7. index.md에서 하위 문서 연결하기

`index.md`에서 각 Markdown 파일로 링크를 만들 수 있다.

예를 들어:

```markdown
# 나만의 이야기, 정리해보자

AI와 공부한 내용을 정리하는 개인 Knowledge Base입니다.

## Database

- [PostgreSQL](database/postgresql.md)
- [ClickHouse](database/clickhouse.md)
- [ETL / ELT](database/etl-elt.md)

## AI

- [LLM](ai/llm.md)
- [RAG](ai/rag.md)

## Architecture

- [Data Platform](architecture/data-platform.md)
```

GitHub Pages에서는 이 링크를 클릭해서 각 문서로 이동할 수 있다.

---

## 8. 전체 작업 흐름

GitHub Pages를 처음 만드는 전체 과정은 다음과 같다.

```text
GitHub Repository 생성
        ↓
jwleepro.github.io
        ↓
index.md 생성
        ↓
Settings → Pages
        ↓
Deploy from a branch
        ↓
main / root 설정
        ↓
https://jwleepro.github.io 접속
        ↓
하위 Markdown 문서 추가
        ↓
index.md에서 문서 링크
```

---

## 9. 앞으로의 학습 자료 관리 방법

AI와 공부한 내용을 대화 그대로 저장하기보다는, 학습이 끝난 후 정리된 내용을 Markdown 문서로 만드는 것이 좋다.

예를 들어:

```text
AI와 질문 / 토론
        ↓
내용 이해
        ↓
AI에게 정리 요청
        ↓
Markdown 문서 생성
        ↓
GitHub에 저장
        ↓
GitHub Pages에서 조회
```

각 문서는 다음과 같은 형식으로 관리할 수 있다.

```markdown
# 주제명

## 한 줄 요약

## 핵심 개념

## Best Practice

## 주의할 점

## 실제 적용 방법

## 예제

## 추가로 공부할 내용
```

이렇게 관리하면 GitHub Repository 자체가 장기적으로 개인 학습용 Knowledge Base 역할을 할 수 있다.

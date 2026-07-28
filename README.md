# 🔑 OpenSesame, 열려라참깨

> **Forked from:** [Open-Sesame](https://github.com/Choiyuhyeon/Open-Sesame)
>
> 팀 프로젝트 '열려라참깨' 종료 후, 기술적 성장을 이어가고자 포크해 Vercel에 배포했습니다.<br>
> 배포 후 새로고침 직접 접근 시 404가 발생하는 SPA 라우팅 이슈로, 모든 경로를 `index.html`로 rewrite하는 `vercel.json` 추가해 해결했습니다.

<br>

열려라참깨는 사용자가 질문 피드를 만들고, 다른 사용자들과 질문·답변을 주고받으며 소통하는 커뮤니티 서비스입니다.<br>
익명 혹은 기명으로 마음을 열고 대화하는 공간을 지향합니다.
<br><br>

## 📍 목차

- [프로젝트 기간 & 배포링크](#info)
- [주요 기능](#features)
- [기술 스택](#stack)
- [프로젝트 구조](#structure)
- [라우팅 구조](#routing)
- [팀원 및 역할](#team)

---

<div id="info"></div>

## 📅 프로젝트 기간 & 배포링크

- **진행 기간**: 2026년 3월 4일 ~ 2026년 3월 19일
- [**Vercel 배포**](https://opensesame-imyoonsoo.vercel.app)

<br>

<div id="features"></div>

## 🔌 주요 기능

- **피드 생성** — 이름을 입력해 나만의 질문 피드 생성
- **질문하기** — 다른 사용자에게 익명으로 질문 작성
- **답변 관리** — 받은 질문에 답변 작성 / 수정 / 삭제
- **반응하기** — 답변에 좋아요 반응
- **공유하기** — 카카오톡 · 페이스북 · 링크 복사로 피드 공유
- **반응형 디자인** — 모바일 · 태블릿 · 데스크톱 최적화

<br>

<div id="stack"></div>

## 🔧 기술 스택

| Category         | Tech                       |
| ---------------- | -------------------------- |
| **Library**      | React 19                   |
| **Build Tool**   | Vite 7                     |
| **Routing**      | React Router DOM 7         |
| **HTTP Client**  | Axios                      |
| **Styling**      | CSS Modules, CSS Variables |
| **Code Quality** | ESLint, Prettier           |

<br>

<div id="structure"></div>

## 🗂️ 프로젝트 구조

```
src/
├── api/            # API 통신 (question · answer · subject)
├── assets/         # 아이콘 · 이미지 등 정적 자원
├── components/     # 도메인별 UI 컴포넌트 (common · home · list · post · answer)
├── hooks/          # 커스텀 훅
├── layouts/        # 공통 레이아웃 (Layout)
├── pages/          # 페이지 (HomePage · ListPage · PostPage · AnswerPage)
├── styles/         # 색상 · 타이포그래피 (color.css · typography.css · theme.js)
├── utils/          # axios 인스턴스
├── App.jsx         # 라우팅 정의
├── main.jsx        # 앱 진입점
└── global.css      # 전역 스타일
```

<br>

<div id="routing"></div>

## 🛣️ 라우팅 구조

| 경로               | 페이지         | 설명                                      |
| ------------------ | -------------- | ----------------------------------------- |
| `/`                | **HomePage**   | 이름 입력 및 피드 생성                    |
| `/list`            | **ListPage**   | 질문 피드 목록 조회 (정렬 · 페이지네이션) |
| `/post/:id`        | **PostPage**   | 특정 피드 질문 조회, 좋아요 · 공유        |
| `/post/:id/answer` | **AnswerPage** | 답변 작성 / 수정 / 삭제 (관리자 페이지)   |

`/list` · `/post/:id` · `/post/:id/answer`는 공통 `Layout` 안에서 렌더링됩니다.

<br>

<div id="team"></div>

## 👥 팀원 및 역할

<table>
<tr>
<td align="center" width="150px">
<a href="https://github.com/Choiyuhyeon">
<img src="https://github.com/Choiyuhyeon.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>최유현</b>
<br/>
<sub>팀 리더<br/>답변 페이지 구현</sub>
</td>
<td align="center" width="150px">
<a href="https://github.com/isuzzi">
<img src="https://github.com/isuzzi.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>이수진</b>
<br/>
<sub>디자인 총괄<br/>답변 목록 페이지</sub>
</td>
<td align="center" width="150px">
<a href="https://github.com/douk9909">
<img src="https://github.com/douk9909.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>김도욱</b>
<br/>
<sub>프로젝트 세팅<br/>답변 목록 페이지</sub>
</td>
</tr>
<tr>
<td align="center" width="150px">
<a href="https://github.com/imyoonsoo">
<img src="https://github.com/imyoonsoo.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>서윤수</b>
<br/>
<sub>개별 피드 페이지<br/>공유 기능 구현</sub>
</td>
<td align="center" width="150px">
<a href="https://github.com/chahyunlee">
<img src="https://github.com/chahyunlee.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>이차현</b>
<br/>
<sub>프로젝트 구조 설정<br/>공통 컴포넌트</sub>
</td>
<td align="center" width="150px">
<a href="https://github.com/moonky-1">
<img src="https://github.com/moonky-1.png" width="100px" style="border-radius:50%"/>
</a>
<br/>
<b>최문경</b>
<br/>
<sub>메인 페이지 구현</sub>
</td>
</tr>
</table>

<br>

<div id="license"></div>

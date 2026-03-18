## nb05-moonshot-team1

## 팀원 구성

- 정지원 (https://github.com/XOXOXO13)
- 손훈석 (https://github.com/HS-hand)
- 양다온 (https://github.com/june5815)
- 김주호 (https://github.com/juho-creator)

## 프로젝트 소개
- 프로젝트 일정 관리 서비스
- 프로젝트 기간: 2025.11.10 ~ 2025.12.02
- 협업 문서: https://opaque-cinnamon-a76.notion.site/NB-5-1-2a7b1a5286b181269ee6e44cdc6663c9
 
## 기술 스택

- Backend: Node.js, Express, Prisma
- Database: postgreSQL
- 공통 Tool: Git & Github, Discord, Notion

## 팀원별 구현 기능 상세

- 정지원
  (자신이 개발한 기능에 대한 사진이나 gif 파일 첨부)

- 손훈석

  1. 프로젝트
프로젝트 등록

프로젝트 이름, 설명을 입력하여 프로젝트를 생성합니다.
유저당 최대 5개의 프로젝트만 생성 가능합니다.
프로젝트 목록 조회

로그인 한 유저가 참여한 프로젝트 목록이 표시됩니다.
각 프로젝트 마다 이름, 멤버 수, 상태별 할 일 수가 조회됩니다.
최신순, 이름순으로 정렬 가능합니다.
프로젝트 수정

프로젝트를 생성한 사람만 프로젝트 수정이 가능합니다.
프로젝트 삭제

프로젝트를 생성한 사람만 프로젝트 삭제가 가능합니다.
참여 중인 프로젝트가 삭제되었을 경우, 멤버들에게 이메일로 알림이 전송됩니다.

총 4개의 api

2. 멤버
멤버 초대

프로젝트를 생성한 사람은 가입한 유저에게 이메일로 프로젝트 초대 링크를 보낼 수 있습니다.
초대 링크에 접속하면 초대를 수락하며 프로젝트에 참여가 가능합니다.
멤버 목록 조회 화면에서 초대 중 상태를 확인할 수 있습니다.
프로젝트를 생성한 사람은 초대를 수락하기 전에 초대를 취소할 수 있습니다.
멤버 추가

할 일에 담당자 지정 시 해당 프로젝트에 참여하는 멤버 중에서만 설정 가능합니다.
멤버 제외

프로젝트를 생성한 사람만 멤버 제외가 가능합니다.

총 5개의 api

- 김주호
  (자신이 개발한 기능에 대한 사진이나 gif 파일 첨부)

- 양다온
  (자신이 개발한 기능에 대한 사진이나 gif 파일 첨부)

## 파일 구조

```
.
├── domain
│   ├── entities
│   │   ├── comment
│   │   │   └── comment-entity.ts
│   │   ├── member
│   │   │   ├── invitation-entity.ts
│   │   │   └── member-entity.ts
│   │   ├── project
│   │   │   └── project-entity.ts
│   │   ├── social-account
│   │   │   └── social-account-entity.ts
│   │   ├── subtask
│   │   │   └── subtask-entity.ts
│   │   ├── tag
│   │   │   └── tag-entity.ts
│   │   ├── task
│   │   │   ├── attachment-entity.ts
│   │   │   ├── task-entity.ts
│   │   │   ├── task-tag-entity.ts
│   │   │   ├── task-tag-vo.ts
│   │   │   └── user-vo.ts
│   │   └── user
│   │       └── user-entity.ts
│   ├── ports
│   │   ├── I-unit-of-work.ts
│   │   ├── externals
│   │   │   ├── I-externals.ts
│   │   │   └── I-google-externals.ts
│   │   ├── managers
│   │   │   ├── I-hash-manager.ts
│   │   │   └── I-manager.ts
│   │   ├── repositories
│   │   │   ├── I-comment-repository.ts
│   │   │   ├── I-invitation-repository.ts
│   │   │   ├── I-member-repository.ts
│   │   │   ├── I-project-repository.ts
│   │   │   ├── I-repositories.ts
│   │   │   ├── I-subtask-repository.ts
│   │   │   ├── I-tag-repository.ts
│   │   │   ├── I-task-repository.ts
│   │   │   └── I-user-repository.ts
│   │   └── repositories-interface.ts
│   ├── services
│   │   ├── auth-service.ts
│   │   ├── base-service.ts
│   │   ├── comment-service.ts
│   │   ├── invitation-service.ts
│   │   ├── member-service.ts
│   │   ├── project-service.ts
│   │   ├── subtask-service.ts
│   │   ├── task-service.ts
│   │   └── user-service.ts
│   └── services.ts
├── inbound
│   ├── controllers
│   │   ├── auth-controller.ts
│   │   ├── base-controller.ts
│   │   ├── comment-controller.ts
│   │   ├── file-controller.ts
│   │   ├── invitation-controller.ts
│   │   ├── project-controller.ts
│   │   ├── subtask-controller.ts
│   │   ├── task-controller.ts
│   │   └── user-controller.ts
│   ├── middlewares
│   │   └── auth-middleware.ts
│   ├── ports
│   │   ├── I-services.ts
│   │   └── services
│   │       ├── I-auth-service.ts
│   │       ├── I-invitation-service.ts
│   │       ├── I-member-service.ts
│   │       ├── I-project-service.ts
│   │       ├── I-subtask-service.ts
│   │       ├── I-task-service.ts
│   │       └── I-user-service.ts
│   ├── requests
│   │   ├── invite-req-dto.ts
│   │   ├── project-req-dto.ts
│   │   ├── subtask-req-dto.ts
│   │   ├── task-req-dto.ts
│   │   └── user-req-dto.ts
│   └── responses
│       ├── attachment-dto.ts
│       ├── subtask-res-dto.ts
│       ├── task-res-dto.ts
│       └── user-dto.ts
├── index.ts
├── injector.ts
├── outbound
│   ├── email.ts
│   ├── managers
│   │   └── bcrypt-hash-manager.ts
│   ├── mappers
│   │   ├── attachment-mapper.ts
│   │   ├── invitation-mapper.ts
│   │   ├── member-mapper.ts
│   │   ├── project-mapper.ts
│   │   ├── subtask-mapper.ts
│   │   ├── tag-mapper.ts
│   │   └── task-mapper.ts
│   ├── repos
│   │   ├── base-repository.ts
│   │   ├── comment-repository.ts
│   │   ├── invitation-repository.ts
│   │   ├── member-repository.ts
│   │   ├── project-repository.ts
│   │   ├── subtask-repository.ts
│   │   ├── tag-repository.ts
│   │   ├── task-repository.ts
│   │   └── user-repository.ts
│   ├── repository-factory.ts
│   └── unit-of-work.ts
├── server.ts
├── shared
│   ├── exceptions
│   │   ├── business-exception.ts
│   │   └── technical.exception.ts
│   ├── utils
│   │   ├── config-util.ts
│   │   ├── smtp-util.ts
│   │   └── token-util.ts
│   └── utils-interface.ts
└── types
```

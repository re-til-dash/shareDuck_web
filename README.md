# shareDuck_web

이 프로젝트는 사용자가 게시글을 작성하고, 공유하며, 이모지 반응을 할 수 있는 플랫폼입니다. 개인 활동을 추적할 수 있는 개인 대시보드와 팀 협업을 위한 팀 대시보드를 제공합니다. 또한 태그 기반으로 게시글을 분류하고 챌린지에 참여하여 팀과 함께 목표를 달성할 수 있습니다.

## 주요 기능

- 회원가입 및 로그인: 이메일 또는 구글 계정을 통해 회원가입 및 로그인할 수 있습니다.
- 개인 및 팀 대시보드: 개인 활동 및 팀 활동을 한눈에 확인할 수 있는 대시보드 제공.
- 게시글 작성 및 관리: 마크다운 에디터를 사용한 게시글 작성 및 관리.
- 이모지 반응 시스템: 게시글에 이모지로 반응하고, 이모지 반응을 시각화.
- 태그 기반 분류 및 시각화: 게시글을 태그로 분류하고, 대시보드에서 활동을 시각적으로 확인.
- 챌린지 생성 및 참여: 팀에서 챌린지를 생성하고, 구성원들과 함께 목표를 달성.

## 기술 스택

- Next.js
- Styled-components
- Chart.js
- TanStack Query
- Zustand

## 폴더 구조

```bash
src/
  components/           # 재사용 가능한 UI 컴포넌트 (Atomic Design 구조)
    atoms/
      ExAtoms.tsx       # Atoms placeholder 파일
    molecules/
      ExMoles.tsx       # Molecules placeholder 파일
    organisms/
      ExOrs.tsx         # Organisms placeholder 파일
    template/
      ExTemp.tsx        # Template placeholder 파일

  modules/              # 기능별 모듈
    personal/           # 개인 관련 모듈
      components/
        PersonalDashboard.tsx   # 개인 대시보드 컴포넌트
        PersonalPost.tsx        # 개인 게시글 컴포넌트
      pages/
        PersonalDashboardPage.tsx  # 개인 대시보드 페이지
        PersonalPostListPage.tsx   # 개인 게시글 리스트 페이지
        PersonalPostDetailPage.tsx # 개인 게시글 상세 페이지
      store/
        usePersonalStore.ts      # 개인 관련 상태 관리 (Zustand)

    team/               # 팀 관련 모듈
      components/
        TeamDashboard.tsx   # 팀 대시보드 컴포넌트
        TeamPost.tsx        # 팀 게시글(팀 소개) 컴포넌트
        TeamChallenge.tsx   # 팀 챌린지 컴포넌트
      pages/
        TeamDashboardPage.tsx   # 팀 대시보드 페이지
        TeamPostListPage.tsx    # 팀 게시글 리스트 페이지
        TeamPostDetailPage.tsx  # 팀 게시글 상세 페이지
        TeamChallengeListPage.tsx  # 팀 챌린지 리스트 페이지
        TeamChallengeDetailPage.tsx  # 팀 챌린지 상세 페이지
      store/
        useTeamStore.ts         # 팀 관련 상태 관리 (Zustand)

    emoji/               # 이모지 시스템 모듈 (페이지 없이 관리)
      components/
        EmojiReaction.tsx       # 이모지 반응 컴포넌트
        EmojiList.tsx           # 이모지 목록 컴포넌트
      store/
        useEmojiStore.ts        # 이모지 상태 관리 (Zustand)

  api/                  # API 호출 및 관리
    example.ts          # Axios를 사용한 예시 코드

  pages/                # Next.js 페이지 구성
    home/               # 홈 (서비스 메인) 페이지
      HomePage.tsx

    intro/              # 서비스 소개 페이지
      IntroPage.tsx

    [userId]/           # 사용자별 경로
      home/             # 사용자 개인 대시보드 및 게시글
        PersonalDashboardPage.tsx
        PersonalPostListPage.tsx
        PersonalPostDetailPage.tsx

      tags/             # 사용자 태그 관련 페이지
        [tagId]/        # 특정 태그 페이지
          TagDashboardPage.tsx
          TagPostListPage.tsx

      teams/            # 팀 관련 페이지
        [teamId]/       # 특정 팀 페이지
          TeamDashboardPage.tsx
          TeamPostListPage.tsx
          TeamChallengeListPage.tsx

  stores/                # 전역 상태 관리 (Zustand)
    userStore.ts         # 사용자 전역 상태 관리

```

## 설치 및 실행 방법

### 설치

```bash
yarn install
```

### 개발 서버 실행

```bash
yarn dev
```

## 기여 방법

프로젝트에 기여하고 싶으시면 아래 절차를 따라주세요.

- 레포지토리를 Fork합니다.
- 새로운 브랜치를 생성합니다. (예: feature/새로운기능)
- 변경 사항을 커밋하고, 브랜치에 푸시합니다.
- Pull Request를 생성합니다.

## 라이선스

- 이 프로젝트는 MIT 라이선스 하에 배포됩니다.

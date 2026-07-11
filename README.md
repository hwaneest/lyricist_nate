# lyricist_nate

작사가 작업 히스토리 포트폴리오 페이지 — 왼쪽 곡 인덱스, 오른쪽 가사(Markdown) 뷰어.
디자인은 Apple 웹의 컬러/타이포/컴포넌트 토큰을 기반으로 제작.

## 구조
- `index.html` — 단일 파일 정적 사이트 (HTML/CSS/JS 인라인, 빌드 과정 없음)
- `vercel.json` — Vercel 정적 배포 설정

## 로컬 미리보기
그냥 `index.html`을 브라우저로 열거나:
```bash
npx serve .
```

## 콘텐츠 수정 방법
`index.html` 하단 `<script>` 안의 `SONGS` 배열에 곡을 추가/수정합니다.
각 곡의 `lyricsMd` 필드에 Markdown 형식으로 가사를 작성하면 오른쪽 패널에 렌더링됩니다.

```js
{
  date: "2026.03.20",
  title: "곡 제목",
  subtitle: "앨범/싱글명",
  artist: "아티스트명",
  handle: "@instagram",
  role: "작사",
  genre: "장르",
  label: "레이블명",
  tagline: "한 줄 소개",
  lyricsMd: `## Verse 1
가사...

## Chorus
가사...`
}
```

## 배포 (Vercel)
1. 이 저장소를 GitHub에 push
2. [vercel.com](https://vercel.com) → **Add New → Project** → 이 저장소 Import
3. Framework Preset: **Other** (빌드 명령 없음, Output Directory: 루트)
4. Deploy

## 라이선스 / 저작권
페이지에 게재하는 가사의 저작권은 각 권리자에게 있습니다. 본인이 작사한 곡만 게재하세요.

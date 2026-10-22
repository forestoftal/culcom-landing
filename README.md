# 컬컴 건대점 랜딩페이지

DM으로 보낼 링크용 페이지입니다. 빌드 과정 없는 정적 페이지예요.

## 파일
- `index.html` — 페이지 전체 (CSS 내장)
- `images/logo.png` — 로고 (고양이 + 워드마크)
- `images/wordmark.png` — 워드마크만 (현재 미사용, 필요시 교체용)
- `images/class.jpg` — 스터디 현장 사진

## Vercel 배포 — Add New → Project 방식
Vercel의 **Add New → Project**는 Git 저장소를 가져오는 방식입니다. 로컬에서 Git 명령을 사용할 필요는 없고, GitHub 웹사이트에서 파일을 업로드하면 됩니다.

### 1. GitHub에 파일 올리기
1. <https://github.com/new>에서 새 저장소 생성
2. 저장소 이름을 `culcom-landing`으로 입력하고 **Create repository** 선택
3. 생성된 저장소에서 **Add file → Upload files** 선택
4. 이 폴더 안의 `index.html`, `README.md`, `images` 폴더를 업로드
   - ZIP 파일 자체를 올리지 마세요.
   - `index.html`이 저장소 최상위에 있어야 합니다.
5. **Commit changes** 선택

### 2. Vercel에서 New Project 만들기
1. Vercel Dashboard에서 **Add New → Project** 선택
2. **Import Git Repository**에서 방금 만든 `culcom-landing` 저장소의 **Import** 선택
3. Project Name 확인
4. Framework Preset은 **Other** 선택
5. Root Directory는 `./` 그대로 유지
6. Build Command와 Output Directory는 비워두기
7. **Deploy** 선택
8. 완료 후 `https://...vercel.app` 주소에서 페이지, 이미지, 카카오톡 버튼 확인

### 나중에 수정할 때
GitHub 저장소에서 파일을 수정하거나 교체하고 커밋하면 Vercel이 자동으로 다시 배포합니다.

## 버튼
상단 CTA와 하단 고정 바, 두 군데 모두 아래 주소로 바로 이동합니다.
```
https://pf-link.kakao.com/qr/_xeMISK/pages/_Hxh?query=state=konkuk,carrotss1
```
`<a href>` 직접 이동이라 클릭 = 실제 방문입니다. 리스트 등록이 그대로 일어나요.

링크를 바꾸려면 `index.html`에서 `pf-link.kakao.com` 을 검색해 두 곳을 같이 수정하면 됩니다.

## 수정하기 쉬운 곳
- 브랜드 색: `:root` 의 `--red`
- 문구: `<section>` 안의 텍스트
- 사진 교체: `images/class.jpg` 를 같은 이름으로 덮어쓰기

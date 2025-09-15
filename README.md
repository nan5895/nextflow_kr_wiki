# Nextflow Korea Documentation

Nextflow 워크플로우 관리 시스템 한국어 문서 사이트입니다.

## GitHub Pages 설정

1. GitHub에서 새 public repository 생성
2. 이 폴더의 모든 파일을 repository에 업로드
3. Repository Settings > Pages에서 Source를 "Deploy from a branch" 선택
4. Branch를 "main"으로 설정
5. `_config.yml`에서 `url`을 실제 GitHub Pages URL로 수정

## 파일 구조

```
├── index.html          # 메인 페이지
├── tutorials.html      # 튜토리얼 목록
├── slides.html         # 슬라이드 목록  
├── archive.html        # 아카이브 목록
├── assets/
│   └── css/
│       └── style.css   # 스타일시트
├── tutorials/          # 튜토리얼 파일들 (생성 필요)
├── slides/             # PPT/PDF 슬라이드들 (생성 필요)
├── archive/            # 아카이브 파일들 (생성 필요)
├── _config.yml         # Jekyll 설정
└── README.md           # 이 파일
```

## 콘텐츠 추가 방법

### 튜토리얼 추가
1. `tutorials/` 폴더에 HTML 파일 생성
2. `tutorials.html`에 링크 추가

### 슬라이드 추가  
1. `slides/` 폴더에 PDF/PPT 파일 업로드
2. `slides.html`에 링크 추가

### 아카이브 추가
1. `archive/` 폴더에 파일 생성
2. `archive.html`에 링크 추가

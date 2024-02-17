## SAENA's Dev Log

- Jekyll을 사용하여 마크다운 문법으로 블로그를 작성하고 있습니다.
- 개발 이슈, 프론트엔드 개발 경험, 그리고 다양한 기술적인 주제들을 다루며, 최신 웹 개발 동향과 개인적인 학습 내용을 공유하는 공간입니다.

### Environment

- ruby 3.1.3: 2022-11-24 revision 1a6b16756e / arm64-darwin22
- gem 3.3.26: Ruby package manger

#### Install Jekyll

- [jekyll 공식 문서 참고](https://jekyllrb.com/docs/installation/macos/)
- chruby: ruby 버전 관리자
- ruby-install: ruby 설치 도구
- [troubleshooting] 설치하고 나서 ruby -v 동작하지 않을 때
```
source ~/.zshrc 
```

#### Execute

```
# gem 설치
bundle

# local 환경 실행
bundle exec jekyll serve
```

#### Theme

- based [jekyll-theme-yat](https://github.com/jeffreytse/jekyll-theme-yat)

### 폴더 구조
기본적인 폴더 구조는 아래와 같습니다. 
```
nagneo.github.io/
┣ _data/            # Jekyll에서 데이터를 불러와서 페이지를 동적으로 생성함.
┣ _drafts/          # 아직 게시되지 않은 초안 글을 저장하는 디렉토리. 
┣ _includes/        # 페이지나 레이아웃에서 재사용 가능한 코드 조각들을 저장하는 디렉토리. 
┣ _layouts/ Jekyll  # 레이아웃은 페이지 구조를 정의하고, 페이지의 내용이 어떻게 표시될지를 결정.
┣ _posts/           # 게시된 글들을 저장하는 디렉토리. 파일명의 형식은 YYYY-MM-DD-title.md
┣ _sass/            # Sass(SCSS) 파일로 스타일 시트를 관리.
┣ _site/            # Jekyll 빌드 시 생성되는 정적 파일들이 저장되는 디렉토리
┣ assets/           #이미지, 스타일시트, 자바스크립트 등의 정적 자원들을 저장하는 디렉토리입니다.
┣ .gitignore        # Ruby 프로젝트의 의존성을 관리하는 파일
┣ 404.html
┣ Gemfile
┣ README.md
┣ _config.yml       # Jekyll의 설정 파일로, 사이트 전반에 대한 설정
┣ about.html
┣ about.markdown
┣ index.html
┣ index.markdown
┣ jekyll-theme-yat.gemspec

```
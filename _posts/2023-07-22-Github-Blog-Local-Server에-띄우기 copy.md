---
title: Github Blog Local Server에 띄우기
author: jeongork
date: 2023-07-22 14:27:00 +0800
categories: [Github]
tags: [github]
pin: true
---


## 1. Install Ruby

```bash
$ ruby -v
```



## 2. Install Jekyll: Error
```bash
$ gem install bundler jekyll
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.6.0 directory.
```
> 권한 에러가 뜰 것이다!
{: .prompt-tip }


## 3. rbenv를 사용하여 에러 처리
다운로드 가능한 버전 확인
```bash
$ rbenv install -l
3.0.6
3.1.4
3.2.2
jruby-9.4.3.0
mruby-3.2.0
picoruby-3.0.0
truffleruby-23.0.0
truffleruby+graalvm-23.0.0
```

rbenv 설치 -> 3.0.6 버전 선택
```bash
$ rbenv install 3.0.6
```

다운로드한 rbenv 버전 확인
```bash
$ rbenv versions
```

다운로드한 rbenv 버전으로 바꾸기
```bash
$ rbenv global [다운로드 버전]
```


## 4. rbenv 활성화
```bash
$ vim ~/.zshrc
```
zshrc 파일을 편집기를 통해 켠 후
```bash
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
```
위의 내용을 추가로 삽입 후 저장


바뀐 사항 적용
```bash
$ source ~/.zshrc
```


## 5. bundler 설치
```bash
$ gem install bundler
$ gem install jekyll
```

## 6. 로컬 서버 띄우기
```bash
$ bundle exec jekyll serve
```

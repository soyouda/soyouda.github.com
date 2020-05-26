---
title:  "터미널 명령어(Terminal Command)"
categories:
  - 인터페이스
tags:
  - Unix
  - Mac
  - Terminal
  - 터미널
  - 명령어
  - bash
  - zsh
---
평소 GUI에 익숙해져 가끔 CLI를 사용하게 되면 명령어가 생각이 잘 안난다.

그래서 아주 간단하지만 가물가물할 수도 있는 기본적인 터미널 명령어를 기록해둔다.

## TERMINAL 명령어

``` bash
man [명령어] : [명령어] 도움말을 새 창에서 출력. "q"로 빠져나온다.
(man 도움말 내에서) /[검색어] : 검색어를 찾는다. "n"키로 다음 찾은 단어로 이동.
```

{% asset_img 01-45-34.gif man 명령어 실행 결과 %}

``` bash
pwd : (print working directory) 현재 경로를 확인 한다.
mkdir [디렉토리명] : (make directory) directory를 만든다
touch [파일명] : 새로운 빈 파일 생성.
ls : (list segments) 리스트 표시.
ls -al : 숨김파일까지 자세히 표시.
cd [폴더명] : (change directory) directory 이동. tab키로 자동완성.
rm [파일명] : (remove) 파일 삭제.
rmdir [폴더명] : (remove directory) 폴더 삭제.
rm -r [폴더명] : 폴더 내 파일 포함 삭제.
cat [파일명] : 파일 읽기
vi [파일명] : vi 편집기로 열기
nano [파일명] : nano 편집기로 열기
```

``` bash
[명령어] 1> [파일명] : [파일명]에 [명령어] standard output의 실행 결과 저장.
[명령어] 2> [파일명] : [파일명]에 [명령어] standard error의 실행 결과 저장. 
rm [파일명] 1> test.txt 2> error.log : [명령어] 1> [파일명] 2> [파일명] 과 같이 합쳐서도 가능하다.
rm [파일명] 1>> test.txt 2>> error.log : >> 를 사용하면 overwrite 하지 않고 append 한다.
```

1. `1>`는 standard output을 redirection 하여 저장한다. 
2. `2>`는 standard error을 redirection 하여 저장한다.

{% asset_img 03-19-16.gif I/O redirection %}

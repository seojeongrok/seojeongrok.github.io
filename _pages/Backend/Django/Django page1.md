---
title: "Django from A to Z (part 1)"
tags:
    - Django
    - Backend
date: "2024-05-19"
thumbnail: "https://velog.velcdn.com/images%2Fpoding84%2Fpost%2Fd0ec7911-49af-4b0d-aff3-fda4609ac21d%2Fdjango.png"
bookmark: true
---


# 사용배경 
---
* AI 개발자이다. 하지만, 내가 원하는 직무만 딱 할 수 없는 것이... 개발자의 큰 현실이 아닌가...
* 이왕 하는김에 gunicorn 배포, log 찍기.. 내가 하고 어깨 넘어로 배워온 것 기록하며 다시 상기하려 한다.


# Setting
---

## Virtual environment setting
* AI를 모델을 넣게 되면 AI model을 돌리는 환경 버전을 동일하게 서버에 맞춰야 한다. 가상환경 없이 그냥 라이브러리 다운 받으면 나중에 서버에 꼭 필요한 라이브러리만 설치하게 되는 것이 아니고, 오만 것 다 설치해야 한다.. 왠만하면 anaconda로 가상환경 세팅해서 쓰자. 인터넷에 설명 매우 잘 되어있다.


## Install django
```bash
$ pip install django
```
* 이까지 했으면 거의 70%는 다 왔다. 그만큼 사용하기 매우 쉽다.


## Make directory
```bash
$ mkdir [내가 설정하고 싶은 django 프로젝트 명]
$ cd [내가 설정하고 싶은 django 프로젝트 명]
```
* 이건 만들어도 되고, 안 만들어도 되는데, 폴더를 만들고 안에 하면 그냥 나중에 컴퓨터 폴더 관리할 때 편하더라


## Make django project
```bash
$ django-admin startproject [내가 설정하고 싶은 django 프로젝트 명]
```
* 프로젝트 이름 지을 때 python, django 라이브러리 이름으로 설정하면 충돌이 일어나서 오류가 난다. 피하자
![poster]("https://github.com/seojeongrok/seojeongrok.github.io/blob/main/_pages/Backend/Django/django_page1_1.png")


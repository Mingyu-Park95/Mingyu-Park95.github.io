---
author: park
layout: post
title:  "Git이란, Git 로컬저장소의 구조"
date:   2019-02-01 08:39:50 +0900
categories: jekyll update
---
## 1.Git 이란
프로그램의 버전 관리를 위해 만들어진 S/W입니다. 학교 과제나 개인 프로젝트를 할 때
변경 사항을 기록하거나 백업을 위해 프로젝트 폴더 전체를 복사하는 경우가 있습니다.
이 경우 폴더의 용량이 큰 경우 상당한 시간이 걸리며, 중복되는 코드가 다시 복사 되기도
합니다 Git은 이러한 문제를 해결합니다.


또한 Git은 **협업에** 도움을 줍니다.
학과 프로젝트 도중에 에브리타임을 모방한 앱을 만든적이 있습니다.
우선 메인 화면을 만들고 저는 시간표, 동기들은 메신저, 식단표, 공지사항등을 만들었는데
코드를 공유하기 위해서 카카오톡, Gmail을 이용하다보니 서로의 진행사항을 확인하기
힘들었습니다. Git은 프로젝트를 한 곳에 관리함으로서 이러한 문제를 해결합니다. 또한 서로
다른 개발자 A,B가 동시에 같은 파일을 수정하는 경우 A,B의 작업이 서로 겹치지 않게 도와 줍니다.

## 2.Git 로컬 저장소의 구조  
Git 로컬 저장소의 구조는 아래와 같습니다.

![깃 로컬 저장소](../assets/Git-LocalRepo.png)

실제 작업이 이루어지는 Working directory,= Working tree,  
파일을 저장하는 준비를 하는 Staging area = index,  
Git이 프로젝트의 메타 데이터와 객체 데이터베이스를 저장하는 .git directory(repository)이 3개로 나뉩니다.

Woriking directory에서 파일을 수정하고 이를 staging Area에 보냅니다.  
stage Area에서는 Working directory에서 온 정보를 가지고 commit할 파일에 대한 정보를 저장합니다.  
stage Area에 있는 파일을 commit하면 .git directory에 영구적으로 저장할 수 있습니다.

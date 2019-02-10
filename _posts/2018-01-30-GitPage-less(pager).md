---
layout: post
categories: jekyll update
---

# 문제 발생 

## 1.Github page 에러 발생(unrelated history 문제)  
Github page를 만들 때 원격 저장소를 먼저 만들었습니다.  
jekyll로 블로그 관련 폴더를 만든 후 그 폴더를 git로컬 저장소 지정하고 원격저장소에 push하는 경우 "Updates were rejected because the remote contains work that you do not have locally." 에러가 발생합니다. 이는 로컬 저장소에 없는 작업을 원격 저장소가 가지고 있는 경우에 발생합니다.이는 보통의 경우 원격저장소를 pull하여 해결 할 수 있습니다.

하지만 원격저장소의 master branch와 로컬에서 push하려는 브런치에 공통된 commit이 없는 경우 "refusing to merge unrelated histories"라는 에러가 발생합니다. 즉 완전히 다른 두 프로젝트를 연결하는 경우 이러한 문제가 발생합니다. 저는 강제 병합을 통해서 이 문제를 해결했습니다.

    git push -f origin master

명령어를 이용하여 로컬 저장소를 원격저장소에 push할 수 있습니다.
단 이경우에 기존의 원격저장소는 사라지게 되니 주의가 필요합니다.

## 2.less= terminal pager program에서 나가는 방법 (git bash창이 계속 이어질 때)

    git diff
    
명령어를 사용할 때 맨 밑에 줄에 (END)가 엔터를 눌러도 아무 반응이 없는 것을 볼 수 있습니다. 이를 해결하기 위해서 키보드에서 q를 눌러 주면 됩니다.
- less는 텍스트 파일의 내용을 한줄, 혹은 한화면에 보여주는데 사용되는 프로그램 입니다.
- less는 more와 vi 명령어를 이용합니다.

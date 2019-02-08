---
layout: post
title:  "visual studio code preview에 이미지가 적용되지 않을 때"
date:   2019-02-01 08:39:50 +0900
categories: jekyll update
---
visual studio code를 사용하여 md파일을 작성 할 때, 
작성하는 md파일 보다 이미지가 **상위에 디렉토리에** 있는 경우, vscode preview에서 이미지가 보이지 않는 문제가 발생했습니다.
 예를 들어 

    ![강아지](../assets/dog.jpg)

라고 작성했을 때 vscode의 preview는 강아지 이미지를 불러 오지 못했습니다. GFM preview 확장 프로그램을 다운 받기도 했지만 문제는 해결 되지 않았습니다. 그러던 중 검색을 통해 문제를 해결 했습니다.

## 해결방법은 간단합니다.
그것은 상위 디렉토리를 워크스페이스로 지정하는 것 입니다.
![open-folder](../assets/open-folder.png)

위의 캡처와 같이 폴더 열기를 선택하여 **md파일,이미지 파일을 모두 포함하는 상위 디렉토리를** 여는 경우 preview화면에서 보이지않는 이미지를 보이게 할 수 있습니다. vscode가 작업 영역을 상위 폴더까지 인식하게 되어 위의 문제를 해결 할 수 있습니다. 
  
참고링크를 확인하면 개발자가 보안상의 이유로 현재 워크스페이스가 아닌 부모(상위)디렉토리의 파일은 열 수 없게 했다는 답변을 확인 할 수 있습니다.
### 참고 링크
[Markdown relative image in preview not shown](https://github.com/Microsoft/vscode/issues/62995)
  
    
      
        apple  
        
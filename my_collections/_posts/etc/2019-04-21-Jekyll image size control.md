---
title: jekyll 사용시 md파일 이미지 크기 조정
date:   2019-01-30 16:57:50 +0900
categories: etc
---

지킬을 이용하여 md파일을 작성 할 때 이미지를 첨부해야하는 경우가 있습니다. 저는 html 태그인 <img .../>을 사용하여 크기를 조절하였지만 이보다 편리한 방법을 찾아 이 글을 포스트 합니다.

## 이미지 크기 조절

기존 md파일에 이미지를 추가하는 방법은 아래와 같습니다

    ![이름](www.naver.com/img/29.jpg)
    ![이름](/assets/img/dog.jpg)

아래는 600x600 이미지 입니다.
![dog](/assets/image/dog.JPG)

`{: width="" height=""}`를 이용하여 해당 이미지의 크기를 조절 할 수 있습니다.
""안에는 px값 %값을 사용할 수 있습니다.

    ![이름](/assets/img/dog.jpg){: width="" height=""}

width,height 모두 300으로 설정한 경우 입니다.  
![dog](/assets/image/dog.JPG){: width="300" height="300"}

width,height 모두 50%로 설정한 경우 입니다.  

![dog](/assets/image/dog.JPG){: width="50%" height="50%"}

두 이미지의 크기가 다른 이유는 전자의 경우 300px로 크기가 고정되어 있고
후자의 경우 md파일의 이미지가 jekyll에 의해 `<img../>로 변환 된 후 <img../>를 **감싸고 있는 태그의 크기**에 대해 %가 적용 되기 때문입니다.
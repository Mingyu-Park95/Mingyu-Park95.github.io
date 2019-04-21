---
title: jekyll 테마 적용이 안될 때, cannot load such file --bundler (LoadError), jeykyll serve 에러
date:   2019-01-30 16:57:50 +0900
categories: etc
---
jekyll 테마를 적용하다 보면 가끔 아래와 같은 에러가 발생하는 경우가 있습니다.
![LoadError](/assets/image/ruby-gemlock-version-error.PNG)

제 경우에는 번들러의 버전이 맞지 않아 이런 오류가 발생했습니다.

이를 해결하기 위해서 테마가 들어있는 폴더의 Gemfile.lock 파일을 열고 bundled with라고 적힌 문장을 찾아 버전을 확인합니다.

<img src="/assets/image/bundle-version.PNG" alt="bundle-version" width="400"/>

그리고 

    gem install bundler -v 1.16.1

처럼 해당 버전의 번들러를 설치해주시면 문제가 해결 됩니다.

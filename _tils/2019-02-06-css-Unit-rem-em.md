---

---

em과 rem 모두 폰트 사이즈에 영향을 받는 가변적인 CSS UNIT 입니다. 두 단위의 차이점은 아래와 같습니다.

- em : 근접한 조상 element 혹은 자신의 폰트 사이즈에 영향을 받는다.
- rem : root element의 폰트 사이즈의 영향을 받는다.

해당 이미지는 아래의 코드를 따릅니다.

![em-rem](/assets/image/em-rem.png)

html

    <!DOCTYPE html>
    <html>
        <head>
            <link rel="stylesheet" type="text/css" href="main.css">
        </head>
        <body>
            <div class="main-div">
                <div class="rem-div">rem-div</div>
                <div class="em-div">em-div</div>
            </div>
        </body>
    </html>

css
~~~css
    html{
        font-size:10px;
    }
    .main-div{
        font-size:20px;
    }
    .rem-div{
        width: 10rem;
        background-color: red
    }
    .em-div{
        width: 10em;
        background-color: blue;
    }
~~~

rem-div의 경우 html의 폰트 크기와 관련하여 넓이가 100px,  
em-div의 경우 main-div의 폰트 크기가 20px이기 때문에 넓이가 20x10=200입니다.

또한 em의 경우 조상의 폰트 크기를 계속 이어 받을 수 있기 때문에 **사용시 주의** 해야합니다.

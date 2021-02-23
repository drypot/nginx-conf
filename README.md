# nginx-conf

개인적으로 운영하는 웹서버들의 nginx.conf.

## enabled

conf 를 활성화하려면 sites/enabled 폴더에 심볼릭 링크를 생성한다.\
심볼릭 링크를 생성할 때는 Relative 링크를 쓴다.
  
    $ ln -sr default.conf enabled

## 개발 환경에서 user 설정

mac에서는 brew로 nginx를 설치한다.
사용자 계정으로 동작하니 퍼미션 설정이 별도로 필요없다.

linux에서는 기본 http계정으로 동작한다.\
http로 동작하면 개발중인 디렉터리에 접근하지 못한다.\
nginx.conf 의 user를 세팅해줘야 한다.\

    user drypot wheel;  # arch


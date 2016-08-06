# 컴포저 설치
- 특별한 명령은 없고 항상 아래 링크의 가이드를 따른다.
- https://getcomposer.org/download/

# 컴포저 시스템 설치
- 어디서나 사용 가능하도록 경로 설정
- https://getcomposer.org/doc/00-intro.md#globally

# 컴포저를 통해 설치된 명령을 사용하기
- phpunit 등 유틸리티성 어플리케이션을 글로벌로 설치한 경우 어디서나 사용 가능하도록 PATH 설정을 해준다
```
taelkim:~ tael$ composer global require phpunit/phpunit
```
- BASH 쉘의 경우 아래와 같이 처리해 준다.
```
taelkim:bin tael$ vi ~/.bash_profile
PATH=~/.composer/vendor/bin:$PATH
```

# More Info
- 환경변수 설정: http://unix.stackexchange.com/questions/26047/how-to-correctly-add-a-path-to-path

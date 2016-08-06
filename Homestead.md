# 컴포저와 홈스테드를 통한 개발환경 구축
## 홈스테드
- Vagrant 를 기반으로 PHP 개발자에게 친숙한 환경 설정을 제공함.
- 라라벨을 기준으로 되어있지만 다른 프레임워크나 일반 PHP 환경에서도 충분히 이점을 가지고 있음
- 실제로 심포니를 사용하면서도 홈스테드를 기반으로 하는 가이드 문서가 제공됨
- PROS & CONS
  - 가장 큰 장점은 '쉽다' 덜 알아도 된다.
  - 단점은 가상머신에 필요할 지도 모르는 모든 내용을 담아두어서 '무겁다'
    - 하드웨어에 따라 느리게 동작할 수 있다.

## 프로젝트와의 분리
- 몇몇 환경 설정이 굉장히 중요한 프로젝트의 경우는 논외. PHP 프로젝트라면 대부분의 어플리케이션이 같은 개발환경을 사용해도 무관하다.
- 같은 환경을 쓰므로 별개로 분리된 머신에서 구동될 필요가 없다.
- 가상머신 이지만 여러개를 띄워야 할 이유도 없다.
- 프로젝트와 가상머신 개발 환경이 독립되어 개발환경 자유도가 높다.
- 사실 Vagrant 정보는 어플리케이션 구동과 무관하다. 동일한 저장소에서 관리되어야 할 이유가 없다.
- Vagrant 구동 정보는 개개인의 개발환경에 따라 상이하다.
(예, ip를 10.10.10.10 이라는 동일한 정보를 다른 머신에서 사용하고있다면?)
- 위와 같은 이유로, 프로젝트의 저장소에 가상머신 정보를 넣지 않고 각자의 Vagrant 환경을 사용하는 것이 옳다.

# 컴포저 글로벌
- ...

# 설치 및 설정

## VirtualBox
- 패스

## vagrant
- 설치
  - 패스
- 설정
  ```
taelkim:~ tael$ vagrant box add laravel/homestead
```
(최초 다운로드시 10~60분 정도 걸림)

## Homestead 설치(3.0 기준)
- 설치
```
taelkim:~ tael$ cd ~
taelkim:~ tael$ git clone https://github.com/laravel/homestead.git Homestead
Cloning into 'Homestead'...
remote: Counting objects: 1623, done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 1623 (delta 7), reused 0 (delta 0), pack-reused 1611
Receiving objects: 100% (1623/1623), 254.51 KiB | 180.00 KiB/s, done.
Resolving deltas: 100% (955/955), done.
Checking connectivity... done.
taelkim:~ tael$
```

- 초기화
```
taelkim:~ tael$ cd Homestead/
taelkim:Homestead tael$ bash init.sh
Homestead initialized!
taelkim:~ tael$
```
(`~/.homestead`에 기본 설정파일인 `Homestead.yaml`,`after.sh`,`aliases` 파일이 생성됨)


## 컴포저 설치
- 패스
##
-----------------------------------
# 홈스테드 프로젝트별???
## 컴포저를 통해 Homestead 설치(프로젝트별 일 경우에만?)
```
taelkim:~ tael$ composer global require laravel/homestead
```
## 컴포저 글로벌 패스 설정
```
taelkim:bin tael$ vi ~/.bash_profile
PATH=~/.composer/vendor/bin:$PATH
```
환경변수 참고: http://unix.stackexchange.com/questions/26047/how-to-correctly-add-a-path-to-path
> 이제 homestead 명령을 사용할 수 있다.


---- remove ----
Homestead
- 로컬환경에서 글로벌 하게설정하는 것이 좋겠다.
- 설치:
    - https://laravel.com/docs/master/homestead
- 글로벌 환경 처리:
    - https://laravel.com/docs/5.2/homestead#daily-usage
- after.sh 수정을 통해 커스터마이징
    - 참고 예제: postgresql 등 삭제시키기 (비추천)
        - https://gist.github.com/larryli/bee9e699f995376b56cb
- 최신 홈스테드: 아틀라스
    - https://atlas.hashicorp.com/laravel/boxes/homestead
    -  

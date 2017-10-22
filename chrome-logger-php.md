# 크롬 로거 설치 및 사용법
- PHP 로그를 브라우저에서 볼 수 있도록 한다.
- 브라우저에 익스텐션을 설치하고, 라이브러리에서 브라우저의 익스텐션이 인식 가능한 형태로 데이터를 제공하게 한다.
- 디버그 환경에서만 동작하도록 처리하는 것을 권장한다.

## 브라우저 : 크롬로거 익스텐션 설치 
- https://craig.is/writing/chrome-logger

## chromephp 라이브러리
- https://github.com/ccampbell/chromephp
- 예: 일반)
```
ChromePhp::log('Hello console!');
```
- 예: 심포니)
```
$this->container->get('logger')->info('Hello console!');
```

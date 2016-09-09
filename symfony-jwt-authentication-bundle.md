# 심포니에서 JWT 를 이용한 토큰 인증 방식 적용

## JWT
- JSON Web Token
- https://jwt.io/

### 장점
- 다양한 알고리즘을 적용할 수 있음
- 다양한 언어에서 지원
- 단방향 암호화가 아니라 복호화가 가능하지만 복호화에 대한 검증은 발행자(서버)만 가능, 재가공이 불가능하므로 문제되지 않음

### 단점
- 담겨진 양에 비례해서 생성되는 토큰의 길이가 증가함 (1K ~ 8K 정도까지 차이를 보임)
- 담겨진 내용이 공개될 수 있으므로 담을 정보에 주의가 필요(예,패스워드)

## 심포니 번들
- 인증 번들 : https://github.com/lexik/LexikJWTAuthenticationBundle
- 리프레시 토큰 번들 : https://github.com/gesdinet/JWTRefreshTokenBundle


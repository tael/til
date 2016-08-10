# HTTP 를 HTTPS 요청으로 리다이렉트 시키는 방법
- 최근에는 모든 기본 서비스를 HTTPS 로 사용한다.
- 그럼에도 사용성을 위해 HTTP를 유지 해야 이탈을 방지할 수 있다.
- HTTP 로 들어온 요청을 HTTPS로 변경하여 재요청 하는 방법을 설명한다.

## NGINX
```
server {
  listen 80;
  ....
  location / {
    if ($http_x_forwarded_proto != 'https') {
      rewrite ^ https://$host$request_uri? permanent;
    } 
  ....
  }
}
```
## APACHE
```
<VirtualHost *:80>
...
RewriteEngine On
RewriteCond %{HTTP:X-Forwarded-Proto} !https
RewriteRule ^.*$ https://%{SERVER_NAME}%{REQUEST_URI}
...
</VirtualHost>
```
참고:
http://www.emind.co/how-to/how-to-force-https-behind-aws-elb/

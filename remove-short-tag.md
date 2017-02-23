# short tag 없애기 
## short tag
`<? foreach(...)` 와 같이 html 사이에 `<?` 을 통해 PHP 구문을 open 하는 태그. `<?php` 는 long tag 라고 부름.
deprecated 되어 기본 옵션이 사용 불가로 됨..

## short echo
`<?=$var?>` 처럼 값을 바로 출력(echo)하도록 하는 구문. short tag와 다르게 deprecated 되지 않음.

## 솔루션 
php cs fixer 에서 변환하는 옵션을 가지고 있으므로 이를 이용하면 쉽게 일괄 변환이 가능함. 

## 설치
http://cs.sensiolabs.org/

### Homebrew
```
brew upgrade php-cs-fixer
```
### Composer
```
$composer global update friendsofphp/php-cs-fixer
```
## 사용법 
```
$ php-cs-fixer fix --fixers=short_tag --diff --dry-run <path>
```

## 참고 링크
- http://stackoverflow.com/questions/684587/batch-script-to-replace-php-short-open-tags-with-php
- https://github.com/tael/til/blob/master/composer.md

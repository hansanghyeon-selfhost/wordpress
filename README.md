
## Folder structure

```
.
├── .wp
│   └── main // production wordpress (/var/www/html)
├── .db
│   └── main // production wordpress db
└── themes
    └── main // production wordpress theme
```

## 테마 설치 (option)

**roots/sage 설치**

```sh
cd themes/main
rm .gitkeep
composer create-project roots/sage .
```

roots/sage에서 acorn을 사용하지만 태마 설치시에 설치되지 않기 때문에 추가 설치

```sh
composer require roots/acorn
```

**composer가 설치되지 않았을 때**

```
docker run --rm --interactive --tty \
    --volume $PWD:/app \
    --volume ${COMPOSER_HOME:-$HOME/.composer}:/tmp \
    composer 명령어
```

**node_modules 설치**

```sh
yarn install
```

**테마 개발 실행**

```sh
yarn start
```

## Author

👤 **Hansanghyeon**

* Github: [@Hansanghyeon](https://github.com/Hansanghyeon)
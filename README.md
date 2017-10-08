# Node.js 프로젝트 생성하기
```linux
$ npm init
```

# 의존모듈 설치하기
```linux
$ npm install --save express react react-dom
```

# 개발 의존 모듈 설치하기
```linux
$ npm install --save-dev babel-core babel-loader babel-preset-es2015 babel-preset-react react-hot-loader webpack webpack-dev-server
npm install -g babel-cli
mkdir build server public src server/routes && touch public/index.html server/main.js server/routes/posts.js src/App.js src/index.js webpack.dev.config.js
```

# 디렉토리 이해하기
```
./
├── .babelrc                # babel 설정파일
├── build                   # 서버 빌드 디렉토리
├── package.json		
├── public                  # 클라이언트 디렉토리
│    ├── bundle.js          # 컴파일된 스크립트
│    └── index.html         # 메인 페이지
├── server                  # 서버 디렉토리 (ES6)
│    ├── main.js            # 서버 사이드 메인 스크립트
│    └── routes
│        └── posts.js       # 예제 라우터
├── src
│    ├── App.js             # App 컴포넌트
│    └── index.js           # 클라이언트 사이드 메인 스크립트
├── webpack.config.js       # webpack 설정파일
└── webpack.dev.config.js   # webpack-dev-server 를 위한 설정파일
```

# 서버 사이드 코드 컴파일 하기
```bash
$ babel server --out-dir build
```

# webpack 을 통하여 코드를 컴파일하고 합치기
```bash
# webpack 을 이미 글로벌설치를 한 상태라면 디렉토리를 생략하고 webpack 만 입력해도 됩니다.
$ ./node_modules/.bin/webpack
```

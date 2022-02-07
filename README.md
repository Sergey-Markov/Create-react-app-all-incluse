# Create-react-app-all-incluse
1)git clone - клонируем созданный репо;
2)npx create-react-app . - создаем наше приложение в нужной дериктории;
  2.1) если возникли проблеммы - npm init -> npm i react-create-app -> npx create-react-app .
3)Инициализация lint-staged и husky:
- npm install --save-dev prettier eslint;
- npx mrm@2 lint-staged;
- Добавить в package.json: "lint-staged" - .{jsx, js}
- Для комфортной работы, после установки плагинов, нужно добавить несколько настроек редактора для автосохранения и форматирования файлов.

{
  "files.autoSave": "onFocusChange",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
4)Настройка деплоймент:
-"homepage": "https://myusername.github.io/my-app"
-npm install --save gh-pages
- Add the following scripts in your package.json:

                                                  Copy
                                                  "scripts": {
                                                  +   "predeploy": "npm run build",
                                                  +   "deploy": "gh-pages -b gh-pages -d build",
5)Add .pretierrc.json with optionals:
    {
  "printWidth": 80,
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "arrowParens": "avoid",
  "proseWrap": "always"
}
6) For generated some id use Shortid: 
    - npm i shortid;
    - import shortid from 'shortid';
    - const id = shortid.generate();
7)Add Axios for HTTP-requests: npm install axios
8) Install React-Router-DOM: npm install react-router-dom
9) Установить библиотеку React-Loadable - сильно упрощает разделение компонентно-ориентированого кода: npm i react-loadable
10) Библиотека для всплывающих уведомлений - npm i react-toastify
11) Библиотека иконок - npm i react-icons
12) Библиотека для лоадеров,Спинеров 
      -  npm install react-loader-spinner --save
      - import "react-loader-spinner/dist/loader/css/react-spinner-loader.css";
      - import Loader from "react-loader-spinner";
 
 <p>package.json</p>
 <p>whith: {
  "name": "my-app",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://Sergey-Markov.github.io/my-app",
  "dependencies": {
    "axios": "^0.25.0",
    "cra-template": "1.1.3",
    "gh-pages": "^3.2.3",
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-loadable": "^5.5.0",
    "react-loader-spinner": "^5.1.2",
    "react-router-dom": "^6.2.1",
    "react-scripts": "5.0.0",
    "react-toastify": "^8.1.1",
    "shortid": "^2.2.16"
  },
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -b gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "prepare": "husky install"
  },
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  },
  "devDependencies": {
    "eslint": "^8.8.0",
    "husky": "^7.0.4",
    "lint-staged": "^12.3.3",
    "prettier": "^2.5.1"
  },
  "lint-staged": {
    "*.{jsx, js}": "eslint --cache --fix",
    "*.{js,css,md, jsx}": "prettier --write"
  }
}
</p>


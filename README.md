# Create-react-app-all-incluse
1)git clone - клонируем созданный репо;
2)npx create-react-app . - создаем наше приложение в нужной дериктории;
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


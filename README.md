# webpack-boilerplate

Немного переделал сборку вебпак от @Alexander, которую выше выкладывали.
выброшены лишние и не используемые модули, пофикшены мелкие баги.
обновлен babel на @babel 7
добавлен @babel/polyfill - он обработает ваш код по умолчанию. Да, теперь ваши async await будут работать из коробки.
добавлен postcss-loader с плагинами autoprefixer, css-mqpacker, cssnano.
переделан запуск в разных режимах. Теперь не нужно идти в файл, и менять переменную.
npm run dev  - запускает дев сервер и открывает нужный адрес в дефолтном браузере
npm run build - собирает билд в папке dist
npm run lint - проверяет код Eslint'ом с конфигами airbnb-base и prettier. Сам конфиг преттиер не использую, но в сборке оставил
npm run clear - удаляет папку dist

по поводу Eslint в процессе сборки мнения разошлись, поэтому, если точно не хотите что бы Eslint мог участвовать в процессе сборки,  перед установкой модулей, удалите строку
   "eslint-loader": "^3.0.2",

в файле package.json и закомментированный код 
/* , 'eslint-loader' */

в файле webpack.config.js
если хотите что бы Eslint проверял код в процессе сборки вебпаком (ВНИМАНИЕ! eslint не даст проекту собраться при любых ошибках), то просто раскомментируйте 
/* , 'eslint-loader' */

в файле webpack.config.js
по умолчанию нужный модуль устанавливается, но в процессе сборки не участвует.  Когда хотим что бы участвовал,  раскомментируем, когда не хотим комментируем обратно.
https://github.com/Net-zen/webpack-boilerplate
ВНИМАНИЕ!  на windows < 10 версии могут возникнуть проблемы
спасибо @Alexander  за изначальную сборку 

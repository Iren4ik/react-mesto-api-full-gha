

# Проект: Место (frontend + backend)
Проект представляет из себя веб-приложение с бэкенд частью - [проект express-mesto-gha](https://github.com/iren4ik/express-mesto-gha) и фронтенд частью - [проект react-mesto-auth](https://github.com/iren4ik/react-mesto-auth) выполненный в рамках указанного выше учебного курса.

Адрес репозитория: https://github.com/Iren4ik/react-mesto-api-full-gha

## Функциональность проекта

- Backend:
  - В проекте созданы схемы и модели пользователей и карточек с контентом:
    - `card` — схема карточки с контентом
    - `user` — схема пользователя
  - В проекте созданы эндпоинты:
    - `/cards` — обрабатывает:
      - GET запросы — отдаёт все карточки из БД
      - POST запросы — создаёт новую карточку с контентом
    - `/cards/:cardId` — обрабатывает DELETE запросы, удаляет карточку по `cardId`
    - `/cards/:cardId/likes` — обрабатывает:
      - PUT запросы — добавляет лайк карточке с контентом
      - DELETE запросы — удаляет лайк карточке с контентом
    - `/signin` — обрабатывает POST запросы, производит аутентификацию пользователя
    - `/signup` — обрабатывает POST запросы, производит регистрацию пользователя
    - `/users` — обрабатывает:
      - GET запросы — отдаёт всех пользователей из БД
      - POST запросы — создаёт нового пользователя
    - `/users/:userId` — обрабатывает GET запросы, отдаёт пользователя по `userId`
    - `/users/me` — обрабатывает:
      - GET запросы — отдаёт информацию о текущем пользователе
      - PATCH запросы — обновляет информацию о пользователе
      - DELETE запросы — производит выход пользователя, с удалением JWT-токена из Cookie
    - `/users/me/avatar` — обрабатывает PATCH запросы, обновляет аватар пользователя
  - Созданы мидлвары:
    - Централизованной обработки ошибок
    - Авторизации пользователя
    - Ограничитель количества запросов (защита от DDoS атак)
    - Логирования запросов и ошибок
  - Производится валидация поступающих данных:
    - до передачи информации контроллерам с помощью joi и celebrate
    - на уровне схем с помощью validator и встроенных методов mongoose
- Frontend:
  - Возможность регистрации и аутентификации пользователя
  - Возможность редактировать информацию о пользователе (установить имя пользователя, информацию «о себе», аватар)
  - Возможность создавать карточки мест (добавить\удалить карточку места, поставить\снять лайк карточке)
 
## Директории проекта

- `/backend` — директория с файлами бэкенд части проекта
  - `/controllers` — директория с файлами контроллеров
  - `/errors` — директория с файлами кастомных ошибок
  - `/middlewares` — директория с мидлварами
  - `/models` — директория с файлами описания схем и моделей
  - `/routes` — директория с файлами роутера
  - `/utils` — директория со вспомогательными файлами
- `/frontend` — директория с файлами фронтенд части проекта
  - `src/blocks` — директория с CSS файлами
  - `src/components` — директория с компонентами
  - `src/contexts` — директория с элементами контекста
  - `src/fonts` — директория со шрифтами
  - `src/images` — директория с файлами изображений
  - `src/utils` — директория со вспомогательными файлами
  - `src/vendor` — директория с файлами библиотек
 
## Запуск проекта

- Backend:
  - `npm run start` — запускает сервер
  - `npm run dev` — запускает сервер с hot-reload
- Frontend:
  - `npm run build` — запуск проекта в режиме продакшн, с формированием файлов подготовленных к деплою в директории `/build`
  - `npm start` — запуск проекта в режиме разработки

## Используемые технологии

- [Node.js](https://nodejs.org/ru)
- [nodemon](https://nodemon.io/)
- [Express](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [mongoose](https://mongoosejs.com/)
- [bcryptjs](https://www.npmjs.com/package/bcryptjs)
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
- [celebrate](https://www.npmjs.com/package/celebrate)
- [validator](https://www.npmjs.com/package/validator)
- [express-rate-limit](https://www.npmjs.com/package/express-rate-limit)
- [helmet](https://helmetjs.github.io/)
- [winston](https://www.npmjs.com/package/winston)
- [express-winston](https://www.npmjs.com/package/express-winston)
- [ESLint](https://eslint.org/)

## Чему я научилась в процессе

- Разворачивать сервер на Node.js
- Использовать в работе фреймворк Express
- Работать с БД MongoDB
- Использовать в работе с БД ODM mongoose
- Создавать схемы и модели для работы с БД
- Обрабатывать различные виды запросов
- Обрабатывать ошибки некорректных запросов
- Валидировать приходящую в запросе информацию
- Работать с JWT-токеном
- Базовой защите приложения
- Логированию
- Деплою проекта на реальный хостинг

## Планы по доработке

Перенести на gh-pages

Области хранения данных:

- база данных на json-server
- BFF
- redux store

Сущности приложения:

- пользователь: БД ( список пользователей ), BFF (сессия текущего), redux store(отображение в браузере)
- роль пользователя: БД(спсиок ролей), BFF (сессия пользователя с ролью), redux-store (использование на клиенте)
- статья: БД(список статей), redux-store (отображение в браузере)
- комментарий: БД (список комментариев), redux-store (отображение в браузере)

Таблицы БД:

- пользователи - users: id / login / password / registed_at / role_id /
- роли - roles: id / name
- статьи - posts: id / title / image_url / content / published_at
- комментарии - comments: id / author_id / post_id / content

Схема состояния на BFF:

- сессия текущего пользователя: login / password / role

Схема для redux-store (на клиенте) :

- user: id / login / roleId
- posts: массив post: id / title / imageUrl / publishedAt / commentsCount
- post: id / title / imageUrl / content / publishedAt / comments: массив comment: id / author / publishedAt
- users: массив user: id / login / registeredAt / role

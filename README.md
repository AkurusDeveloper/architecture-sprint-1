# Задание 1
 ## Аргументы за Module Federation:
    1. Весь проект построен на React, нет необходимости интегрировать разные фреймворки
    2. Данный проект небольшой и не требует полной изоляции между микрофронтендами
    3. Интеграция с Webpack - проще настроить для React-приложения
# Задание 2
### Структура каталогов
```
mesto-microfrontend/
├── packages/
│   ├── core/               # (хост-приложение)
│   │   ├── src/
│   │   │   ├── App.js      
│   │   │   ├── Header.js
│   │   │   ├── Footer.js
│   │   │   ├── contexts/   # Общие контексты
│   │   │   └── styles/     # Общие стили
│   │   └── package.json
│   │
│   ├── auth/               # Авторизация
│   │   ├── src/
│   │   │   ├── Login.js
│   │   │   ├── Register.js
│   │   │   ├── InfoTooltip.js
│   │   │   ├── ProtectedRoute.js
│   │   │   └── utils/auth.js
│   │   └── package.json
│   │
│   ├── profile/            # Профиль
│   │   ├── src/
│   │   │   ├── ProfileSection.js
│   │   │   ├── EditProfilePopup.js
│   │   │   └── EditAvatarPopup.js
│   │   └── package.json
│   │
│   ├── cards/              # Фото
│   │   ├── src/
│   │   │   ├── CardsSection.js
│   │   │   ├── Card.js
│   │   │   ├── AddPlacePopup.js
│   │   │   └── ImagePopup.js
│   │   └── package.json
│   │
│   └── sharedUtils/             # Общие утилиты и компоненты
│       ├── src/
│       │   ├── api.js
│       │   └── components/
│       │       └── PopupWithForm.js
│       └── package.json
│
├── webpack.config.js       
└── package.json            
```
## Описание модулей
### Ядро
    Маршрутизация, контексты, общие стили
#### Компоненты
    Header, Footer, общие компоненты

### Авторизация
    Логика аутентификации и управления токенами
#### Компоненты
    Login, Register, InfoTooltip

### Профиль
    Управление данными пользователя
#### Компоненты
    EditProfilePopup, EditAvatarPopup

### Фото
    Управление карточками (лайки, удаление, добавление)
#### Компоненты
    Card, AddPlacePopup, ImagePopup
## Общие утилиты и компоненты
#### Компоненты
    PopupWithForm

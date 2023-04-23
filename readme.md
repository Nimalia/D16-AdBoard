
Привет, меня зовут **Алина** 👋

Учусь на курсе ![logo_sf](D16/images/logo_sf.png) 
**Fullstack разработчик на Python**
 

Это итоговый проект по блоку **Backend-разработка**
# [Доска объявлений](http://127.0.0.1:8003/ad/)
[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Rubik+Pixel&pause=1000&color=F7441A&background=FFFBE400&center=true&multiline=true&width=435&lines=%D0%94%D0%BE%D1%81%D0%BA%D0%B0+%D0%BE%D0%B1%D1%8A%D1%8F%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B9.%D0%98%D1%82%D0%BE%D0%B3%D0%BE%D0%B2%D1%8B%D0%B9+%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82+D16)](https://git.io/typing-svg)

---
Задание:
![task](D16/images/task.png)


Проект:

![django logo](https://stepik.org/media/cache/images/courses/101042/cover_NchlrlW/b07af8ed221a030aa536971695a2bb6f.jpg)

### Структура сайта:


1. Для незарегистрированных пользователей доступны страница со всеми объявлениями и регистрация
![doc_pic](D16/images/bar_unreg.png)
   
    
2. Для зарегистрированных пользователей доступны просмотр,создание, редактирование обьявлений, а также просмотр/принятие/удаление комментариев от других пользователей на собственные объявления
![doc_pic](D16/images/bar_reg.png)

   
![doc_pic](D16/images/page_comments.png)


3. При помощи ```ckeditor``` при создание своего обьявления есть возможность добавить медиа-файл 
![doc_pic](D16/images/editor.png)

4. На главной странице организован поиск 
![doc_pic](D16/images/search.png)
   
---
## 🔧Технические детали🔩 

Проект вполне стандартный, из особенностей  - применение ```` allauth```` (позволяет проводить регистрацию пользователей на сайте) и ```` ckeditor```` (позволяет форматировать обьявление, вставлять медиафайлы в объявление)


Cоответсвенно в ````settings.py```` указываем:
```` 
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'django.contrib.sites',
    'django.contrib.flatpages',
    'postboard.apps.PostboardConfig',

    'fpages',
    'django_filters',

    'allauth',
    'allauth.account',
    'allauth.socialaccount',
    'allauth.socialaccount.providers.yandex',

    'ckeditor',
    'ckeditor_uploader',
]

...........

CKEDITOR_CONFIGS = {
    'default': {
        'toolbar': 'full',
        'height': 300,
        'width': 900,
        'image2_responsive': True,
        'image2_maxWidth': 500,
    },
}
............

CKEDITOR_BASEPATH = "/static/ckeditor/ckeditor/"

CKEDITOR_UPLOAD_PATH = 'media/'

MEDIA_ROOT = 'media/'

MEDIA_URL = '/media/'

CKEDITOR_FILENAME_GENERATOR = 'utils.get_filename'

..............

ACCOUNT_EMAIL_REQUIRED = True
ACCOUNT_UNIQUE_EMAIL = True
ACCOUNT_USERNAME_REQUIRED = False
ACCOUNT_AUTHENTICATION_METHOD = 'email'
ACCOUNT_EMAIL_VERIFICATION = 'mandatory'


EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
EMAIL_HOST = 'smtp.yandex.ru'
EMAIL_PORT = 465
EMAIL_HOST_USER = "__________"
EMAIL_HOST_PASSWORD = "----------"
EMAIL_USE_TLS = False
EMAIL_USE_SSL = True

DEFAULT_FROM_EMAIL = "_____________"
SERVER_EMAIL = "__________"

 ````
---
## Ознакомиться ➡️  [Документация allauth](https://django-allauth.readthedocs.io/en/latest/)

Ознакомиться ➡️  [Документация ckeditor](https://django-ckeditor.readthedocs.io/en/latest/)
-------


----
```` Спасибо за уделенное время! 🙏 ````

___

![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Nimalia&theme=solarized_dark)


![](https://komarev.com/ghpvc/?username=Nimalia)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=anuraghazra)](https://github.com/anuraghazra/github-readme-stats)
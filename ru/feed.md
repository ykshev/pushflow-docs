# Создание и настройка фида
## Что такое Фид
Фид (от англ. feed) — место хранения push-подписок. После его создания и настройк для вас будет сгенерирован уникальный JS-скрипт, после размещения которого вы сможете собирать push-подписки в этот фид.

## Как создать фид
Перейдите в раздел «Фиды» в главном меню и нажмите на кнопку «Создать» в правом верхнем углу.

## Свойства Фида

#### Название и описание
Произвольное название и описание, которые помогут вам идентифицировать группу подписок внутри этого фида. Идеи для названия: источник трафика, место сбора подписок или метод сбора. 

#### Постбэк URL
После того, как в данный фид будет добавлена новая подписка, наш сервер отошлет обратный запрос по заданному адресу. [Подробнее о доступных макросах](/ru/tracker)

#### Частота показов
Как часто можно будет отсылать уведомления одному пользователю. Указывается в часах.

## Раздел «Настройки скрипта»
![Окно запроса подписки](../img/push-message.png ':class=mw-300')

Раздел «Настройки скрипта» определяет, куда произойдет редирект после взаимодействия пользователя с окном подписки.

* *Редирект при нажатии «Разрешить»*. Укажите ссылку, по которой будет произведен редирект после успешной подписки пользователя. (Нажатие на кнопку «Allow»).
* *Редирект при ошибке*. Укажите ссылку, по которой будет произведен редирект, если произойдет ошибка при выполнении скрипта. (Например, если пользователь совсем запретил спрашивать окно подписки в браузере или если браузер пользователя не поддерживает веб-пуш уведомления, как в мобильном Safari)
* *Редиректы при нажатии на «Запретить»*. Укажите один или несколько hostnames, куда будет произведен редирект после нажатия на кнопку «Block». Если вы хотите указать несколько ссылок, которые будут перебираться последовательно, то каждую ссылку нужно указать с новой строки. Как это работает, читайте ниже.
Указывайте только hostname, т.е. адрес сайта без дополнительных параметров, которые идут после знака _?_. Например, если ваш сайт находится по адресу: https://**yourdomain.org**/sub/4/index.php?search=1, то нужно указать только hostname **yourdomain.org** и далее поддомены с новой строки. В итоге в этом поле у вас получится:

```
yourdomain.org
1.yourdomain.org
2.yourdomain.org
3.yourdomain.org
```



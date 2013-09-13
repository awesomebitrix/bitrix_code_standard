# Создание пустой страницы с доступом к API Битрикс

Довольно часто нужно создать пустую страницу — без вывода шапки и футера, но с возможностью обращаться к классам Битрикс. Например, такое нужно для работы с ajax. Делается это очень просто. Создаем файл и пишем в нем.

```php
define("NO_KEEP_STATISTIC", true);
define("NOT_CHECK_PERMISSIONS", true);
require($_SERVER["DOCUMENT_ROOT"]."/bitrix/modules/main/include/prolog_before.php");
```

Теперь в этом файле можно легко обращаться к любым классам Битрикс. Не забывайте только модули подключить нужные:

```php
CModule::IncludeModule('название_модуля');
```

[Источник](http://olegorestov.ru/this/create_an_empty_page_with_access_to_the_api_bitrix/)
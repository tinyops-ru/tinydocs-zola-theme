+++
title = "Как добавлять страницы"
weight = 1
+++

## Главная страница раздела

Главная страница раздела отображается на первом уровне меню. Например, вот так:

```
Главная страница раздела 1  
  Суб-страница 1
  Суб-страница 2

Главная страница раздела 2
  Суб-страница 1
  Суб-страница 2
```

Например, нам нужно добавить раздел Введение (Intro). Создаем каталог `content/intro`, а в нем `_index.md` с содержимым:

```toml
+++
title = "Главная страница раздела 1"
weight = 1
sort_by = "weight"
+++

Здесь будет содержимое страницы
```

## Как добавить страницы в раздел

Страницы раздела хранятся в виде `.md`-файлов. Например, нам нужно добавить страницу `Версия` (Version). 
Для этого создадим файл `content/intro/version.md` со следующим содержанием:

```toml
+++
title = "Версия"
weight = 1
sort_by = "weight"
+++

Здесь какая-то информация о версии
```
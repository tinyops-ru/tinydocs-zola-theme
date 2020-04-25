+++
title = "С чего начать"
description = "Как собрать документацию на базе TinyDocs"
weight = 1
+++

Чтобы показать наглядно как легко и быстро создать документацию лучше разобрать пример.
Представим что нам необходимо собрать документацию для приложения `Bubbles` (название вымышленное).

### Создаем проект с документацией



**1. Генерируем скелет zola-проекта:**
 
```bash
zola init bubbles-docs
```

**2. Подключаем тему TinyDocs к проекту**

```bash
cd bubbles-docs

mkdir themes

git clone https://github.com/tinyops-ru/tinydocs-zola-theme.git themes/tinydocs
```

В файле конфигурации проекта `config.toml` указываем тему:

```toml
theme="tinydocs"
```

При генерации сайта zola будет искать тему проекта в подкаталоге `themes/tinydocs`.

**3. Добавляем тестовую страницу**

Создаем каталог `content/intro`, а там файл `_index.md` со следующим содержимым:

```
+++
title = "Введение"
description = "Что такое Bubbles"
keywords = "приложение, bubbles"
weight = 1
sort_by = "weight"
+++

Документация для Bubbles
```

**4. Смотрим результат**

```bash
zola serve
```

Открываем в браузере - [http://localhost:1111](http://localhost:1111)


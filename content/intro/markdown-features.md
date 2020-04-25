+++
title = "Возможности разметки Markdown"
description = "Исчерпывающее руководство с примерами по возможностям языка разметки Markdown"
weight = 5
+++

Это небольшой пример поста того что мы можем делать с темой TinyDocs.
В нем мы постарались описать все возможные комбинации markdown и shortcode.
Управление заголовками, списки, вставки кода и видео, таблицы, цитаты, вложенный текст и т.д.  

## Списки

- Вот список
- Без нумерации

или

1. Упорядоченный список
    1. С вложенной
    2. структурой
2. И мы можем вернуться вновь на первый уровень.

# Заголовки (H1)

## H2

### H3

#### H4

##### H5

###### H6

Мы также можем писать *курсивом* или делать текст **жирным**.

# Код

Пример вставки Rust кода:

```rust
// `vst` uses macros, so we'll need to specify that we're using them!
#[macro_use]
extern crate vst;

// We're implementing a trait `Plugin` that does all the VST-y stuff for us.
impl Plugin for Whisper {
    fn get_info(&self) -> Info {
        Info {
            name: "Whisper".to_string()
        }
    }
}
```

Мы также можем добавить имя файла в наши примеры кода имя файла. Это очень удобно
при написании уроков (tutorials) и т.п. Как это делается:

<div class='filename'>
  <div>www/index.html</div>
</div>

```html
<div class='filename'>
  <div>src/lib.rs</div>
</div>
```

Также можно указать `встроенный код`, что удобно для небольших вставок.

## Горизонтальный разделитель страницы

Как выглядит:

---

Как сделать:

```html
---
```

## Цитаты
{% quote(author="Ричард Фенман") %}
Второй психиатр был, очевидно, более образованным, поскольку его каракули оказалось прочесть труднее.
{% end %}

## Вставка видео с Youtube

С вставкой `yt(id="the_id_here")`
{{ yt(id="ogEjvM-v_-s") }}

## Вставка видео с Vimeo
С вставкой `vm(id="id_here")`
{{ vm(id="115189988") }}

## Ссылки

[Пример ссылки](https://github.com/tinyops-ru/tinydocs-zola-theme)

## Таблицы

Пример

Заголовок 1  | Заголовок 2
------------- | -------------
Содержимое ячейки  | Содержимое ячейки
Содержимое ячейки  | Содержимое ячейки

## Складывающийся контент

<details>
    <summary>Заголовок 1</summary>
    <p>Содержание</p>
</details>

<details>
    <summary>Заголовок 2</summary>
    <p>Содержание</p>
</details>

Как это сделать:

```html
<details>
    <summary>Title 1</summary>
    <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
</details>
```

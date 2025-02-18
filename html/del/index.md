---
title: "`<del>`"
description: "Отображаем удалённый контент."
authors:
  - xpleesid
contributors:
  - tatianafokina
keywords:
  - зачеркнуть
  - удалить
related:
  - html/s
  - css/text-decoration
  - a11y/role-deletion
tags:
  - doka
---

## Кратко

Тег `<del>` используется для отображения удалённого контента. Например, выполненного пункта в списке дел или удалённой части кода.

У тега есть встроенная [роль `deletion`](/a11y/role-deletion/). Благодаря ей пользователи [скринридеров](/a11y/screenreaders/) знают, что содержимое было удалено.

## Как пишется

```html
<h4>Список дел</h4>
<ul>
  <li>
    <del>Помыть посуду</del>
  </li>
  <li>
    <del>Полить цветы</del>
  </li>
  <li>Погулять с собакой</li>
  <li>Пропылесосить комнату</li>
</ul>
```

<iframe title="Базовый пример" src="demos/basic/" height="280"></iframe>

## Как понять

По умолчанию браузеры применяют к `<del>` перечёркивание с помощью `text-decoration: line-through`. Такого же эффекта можно добиться, используя тег [`<s>`](/html/s/) или просто применив к тексту [`text-decoration: line-through`](/css/text-decoration/). Однако `<del>` стоит использовать в том случае, когда нужно подчеркнуть, что какой-то контент был удалён и это важно. Хоть визуально отличий не будет, но это поможет, например, пользователям [скринридеров](/a11y/screenreaders/).

## Атрибуты

Помимо [глобальных атрибутов](/html/global-attrs/) у `<del>` есть специфические:

- `cite` позволяет сослаться на информацию о правке;
- `datetime` позволяет указать время правки.

Оба атрибута необязательные и помогают уточнить правку.

```html
<h4>Сдача проекта</h4>
<ul>
  <li>
    <del cite="https://our-cool-customers.com/reports/123">
      Выгрузить отчёт в сервис заказчика
    </del>
  </li>
  <li>
    <del datetime="2021-12-21T15:00Z">
      Созвониться с подрядчиком по поводу актов
    </del>
  </li>
  <li>Согласовать новую форму оплаты с юристами</li>
</ul>
```

По умолчанию значения атрибутов невидимы для пользователя, но можно автоматически выводить их при помощи скриптов. Например, мы можем добавлять для всех удалённых пунктов дату и время удаления, это будет выглядеть примерно так:

<iframe title="Атрибуты" src="demos/attributes/" height="250"></iframe>

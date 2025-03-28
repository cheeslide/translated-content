---
title: display
slug: Web/Progressive_web_apps/Manifest/Reference/display
---

{{QuickLinksWithSubpages('/ru/docs/Web/Manifest')}}

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Type</th>
      <td><code>String</code></td>
    </tr>
    <tr>
      <th scope="row">Mandatory</th>
      <td>No</td>
    </tr>
    <tr>
      <th scope="row">Example</th>
      <td>
        <pre class="brush: json no-line-numbers">"display": "standalone"</pre>
      </td>
    </tr>
  </tbody>
</table>

> [!NOTE]
> Если свойство `display` не указано, по умолчанию используется `"browser"`.

`display` - это строка, которая определяет предпочитаемый разработчиком режим отображения для веб-сайта. Режим отображения изменяет количество отображаемого пользовательского интерфейса браузера и может варьироваться от `"browser"` (когда отображается полное окно браузера) до `"fullscreen"` (когда приложение полноэкранно).

> [!NOTE]
> Можно выборочно применить CSS к приложению на основе режима отображения, используя медиа-функцию {{cssxref("@media/display-mode", "display-mode")}}. Это может быть использовано для обеспечения более гладкого перехода для пользователя от загрузки сайта по URL к запуску по иконке на рабочем столе.

## Значения

Валидные значения следующие:

| Режим отображения | Описание                                                                                                                                                                                                                                                                                                                                             | Резервный режим отображения |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- |
| `fullscreen`      | Используется все доступное пространство экрана и агент пользователя {{Glossary("chrome")}} не отображается.                                                                                                                                                                                                                                          | `standalone`                |
| `standalone`      | Приложение будет выглядеть и ощущаться, как отдельное приложение. Это может включать наличие другого окна у приложения, собственной иконки в меню запуска и т.д. В этом режиме агент пользователя будет исключать элементы пользовательского интерфейса (ПИ) для контроля за навигацией, но может включать другие элементы ПИ, такие как статус-бар. | `minimal-ui`                |
| `minimal-ui`      | Приложение будет выглядеть и ощущаться, как отдельное приложение, но будет иметь минимальный набор элементов ПИ для контроля над навигацией. Элементы будут варьироваться в зависимости от браузера.                                                                                                                                                 | `browser`                   |
| `browser`         | Приложение открывается в обычной вкладке браузера или новом окне, в зависимости от браузера и платформы. По умолчанию.                                                                                                                                                                                                                               | (None)                      |

## Пример

```json
"display": "standalone"
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

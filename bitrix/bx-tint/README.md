# Интеграция верстки в шаблон компонента Bitrix

Переносит HTML-верстку из `*.html` в одноимённые `*.php` файлы шаблона компонента (`template.html` → `template.php`). PHP-код и функциональные элементы (`<form>`, `<input>`, `<select>`, `<button>`) сохраняются, id и классы из `*.js` добавляются в верстку. Файлы `*.html` не меняются. Шаблон ищется в `local/templates/.default/components/<namespace>/<componentName>/<templateName>/`. Сообщает только об ошибках.

```
Загрузи skill bx-tint и интегрируй верстку в шаблон компонента.
namespace: bitrix, componentName: <компонент>, templateName: .default
```

---
description: 'Переформатирование шаблона компонента Bitrix в соответствии с моими соглашениями.'
name: 'bx-trf'
---

Параметры (если не указаны пользователем — спроси): namespace (по умолчанию `bitrix`), componentName, templateName (по умолчанию `.default`).

Корень проекта — рабочая директория. Используй относительные пути от неё.

Найди дефолтный шаблон компонента по пути:
`local/templates/.default/components/<namespace>/<componentName>/<templateName>/`

Переформатируй все *.php файлы, игнорируя при этом языковые (`lang/*.php`) и служебные файлы (`.parameters.php` и `.description.php`), в соответствии с соглашениями проекта:
- Переименуй локально объявляемые и используемые переменные, согласно префиксам ($lst*, $dct*, $ref* и т.д.), не затрагивая входящие в шаблон переменные ($arParams, $arResult, $APPLICATION и т.д.)
- Перенеси открывающую фигурную скобку `{` блоков `if`, `foreach`, `while` и т.п. на ту же строку что и условие: `if ($Condition) {`
- Оформи блоки if/foreach с HTML через альтернативный синтаксис (: / end*)
- Обязательный канонический guard для Bitrix-пролога: `if (!defined('B_PROLOG_INCLUDED') || B_PROLOG_INCLUDED !== true) die();`
- Однострочные guard-clause без фигурных скобок обязательны, если тело содержит только jump-оператор (`die`, `return`, `continue`, `break`, `include`).
- Удали все табличные теги (`<table>`, `<tr>`, `<td>`, `<th>`, `<thead>`, `<tbody>`, `<tfoot>`) и замени их на div-структуру с CSS классами для стилизации
- Добавь в начало всех php файлов строгую типизацию `declare(strict_types=1);` и следующий PHPDoc блок:
```php
/**
 * @var CMain $APPLICATION
 * @var array $arParams
 * @var array $arResult
 * @var CBitrixComponent $component
 * @var CBitrixComponentTemplate $this
 * @var string $templateName
 * @var string $templateFile
 * @var string $templateFolder
 * @var string $componentPath
 */
```

Разрешаю использовать любые инструменты и действия для выполнения задачи, включая поиск по документации, рефакторинг кода, запись, модификацию, создание файлов и директорий и т.д. Важно сохранить функциональность шаблона и не нарушить его работу.

После завершения всех изменений не предоставляй отчёт и не делай выводов. Сообщи только если возникли ошибки.
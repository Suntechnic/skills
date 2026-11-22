# Переформатирование шаблона компонента Bitrix

Приводит `*.php` файлы шаблона к соглашениям проекта: префиксы локальных переменных, `{` на строке условия, альтернативный синтаксис в блоках с HTML, guard-clause, `declare(strict_types=1)` и PHPDoc с входящими переменными. Табличные теги заменяются на `div`. Языковые файлы (`lang/*.php`), `.parameters.php` и `.description.php` не затрагиваются. Шаблон ищется в `local/templates/.default/components/<namespace>/<componentName>/<templateName>/`. Правит файлы на месте, поэтому запускайте в git-репозитории и проверяйте результат через `git diff`. Сообщает только об ошибках.

```
Загрузи skill bx-trf и переформатируй шаблон компонента.
namespace: bitrix, componentName: <компонент>, templateName: .default
```

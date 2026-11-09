# Ревью этапа

Запускается после IMPL_DONE или по USER_DECISION с next=tosir-reviewstage. Проверяет все изменения этапа от base из log.md до рабочего дерева, включая незакоммиченные. Код не меняет. Итог записывается в log.md: REVIEW_ACCEPTED (дальше tosir-plannextstage), REVIEW_REWORK (создан stage-NN-M.md, дальше tosir-implementstage) или REVIEW_BLOCKED (нужно решение пользователя). После приёмки закоммитьте результат этапа.

```
Загрузи skill tosir-reviewstage и проведи ревью последнего выполненного этапа.
Папка задачи: <путь>
```

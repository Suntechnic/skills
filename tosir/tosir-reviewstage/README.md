# Ревью этапа

Запускается после IMPL_DONE или по USER_DECISION с next=tosir-reviewstage. Проверяет все изменения этапа от base из log.md до текущего рабочего дерева, включая незакоммиченные. Код не меняет, итог пишет в log.md: REVIEW_ACCEPTED (этап принят целиком, дальше tosir-plannextstage), REVIEW_REWORK (создан план доработок stage-NN-M.md, дальше tosir-implementstage) или REVIEW_BLOCKED (нужно решение пользователя в виде записи USER_DECISION). После приёмки закоммитьте результат этапа.

```
Загрузи skill tosir-reviewstage и проведи ревью последнего выполненного этапа.
Папка задачи: <путь>
```

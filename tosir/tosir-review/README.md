# Итоговая приёмка задачи

Запускается после ALL_STAGES_ACCEPTED, которую пишет tosir-plannextstage, когда все блоки overview.md приняты. Также запускается по USER_DECISION с next=tosir-review. Проверяет критерии завершения из overview.md по всем изменениям задачи и пишет в log.md TASK_DONE (задача завершена), TASK_GAPS (перечень пробелов, дальше tosir-plannextstage) или REVIEW_BLOCKED. Код и планы не меняет.

```
Загрузи skill tosir-review и проведи итоговую приёмку задачи.
Папка задачи: <путь>
```

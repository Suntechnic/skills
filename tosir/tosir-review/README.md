# Итоговая приёмка задачи

Запускается после ALL_STAGES_ACCEPTED или по USER_DECISION с next=tosir-review. Проверяет критерии завершения из overview.md по всем изменениям задачи и пишет в log.md TASK_DONE, TASK_GAPS (дальше tosir-plannextstage) или REVIEW_BLOCKED. Код и планы не меняет.

```
Загрузи skill tosir-review и проведи итоговую приёмку задачи.
Папка задачи: <путь>
```

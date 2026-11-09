# Планирование следующего этапа

Запускается, когда последняя запись log.md — OVERVIEW_CREATED, REVIEW_ACCEPTED, TASK_GAPS или USER_DECISION с next=tosir-plannextstage. Создаёт stage-NN.md для ближайшего незавершённого блока overview.md и пишет STAGE_PLANNED. Код проекта не меняет. Если все блоки приняты, пишет ALL_STAGES_ACCEPTED и предлагает запустить tosir-review. Если принятый этап не закоммичен, предупреждает об этом.

```
Загрузи skill tosir-plannextstage.
Папка задачи: <путь>

Подготовь следующий этап с учётом принятых результатов предыдущих этапов.
```

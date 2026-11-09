# tosir — поэтапное выполнение задачи

Это общий регламент, остальные скиллы загружают его сами. Задача ведётся в отдельной папке: overview.md (общий план), stage-NN.md и stage-NN-M.md (этапы и доработки), log.md (журнал состояния). Порядок работы: tosir-overview, затем цикл tosir-plannextstage → tosir-implementstage → tosir-reviewstage, в конце tosir-review. Каждый запуск выполняет одну операцию и останавливается. Следующий шаг определяется по последней записи log.md, не считая CORRECTION; таблица переходов приведена в SKILL.md.

Если скилл остановился с REVIEW_BLOCKED, IMPL_STOPPED или IMPL_STARTED без завершения, добавьте в log.md строку USER_DECISION, где в поле next указан следующий скилл. Пример: `2026-11-08 15:00 | user | - | USER_DECISION | stage=stage-02 | plan=stage-02.md | next=tosir-implementstage text=продолжить`. Существующие строки журнала не редактируются. Между этапами результат обязательно коммитится.

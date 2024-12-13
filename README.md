# Оптимизация проекта "Наставники" курорта Роза Хутор

## Суть проекта
Опытные сотрудники курорта (Наставники) и внешние профессиональные аудиторы проводят проверки сервисных служб на предмет соблюдения стандартов гостеприимного сервиса.
Мои задачи:
- Предоставить техническую базу для проведения аудитов;
- Обработать собранные данные;
- Предоставить результаты и выявленные нарушения руководителям подразделений;

**Точка А**
- Проверки между наставниками распределяются стихийно, качество проверок не контролируется;
- Данные выгружаются в Excel раз в 2 месяца, обрабатываются в течении 8-10 рабочих дней;
- Результаты руководителям отправляются в виде 2 Excel таблиц: полная выгрузка, список выявленных нарушений;

**Точка Б**
- Проверки распределяются пропорционально трафику на объектах;
- Настроен ряд триггеров, фильтрующих неэффективные проверки и фрод;
- Данные выгружаются и предобрабатываются ежедневно пайплайном в Airflow, загружаются в ClickHouse;
- Результаты выводятся на дашборд в DataLens;

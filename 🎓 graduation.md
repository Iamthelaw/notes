# 🎓 Graduation FAQ

## Sections
1. [Postgresql](#postgresql)
    - [Транзакции и ACID](#Транзакции-и-acid)
    - [Изоляционные уровни транзакций](#Изоляционные-уровни-транзакций)
    - [Служебные таблицы](#Служебные-таблицы)
2. [SQL](#sql)
    - Синтаксис DATA DEFINITION (объявление таблиц и всего остального)
    - Синтаксис DATA MANIPULATION (Выборка / Удаление / Изменение данных)
    - [Агрегаты](#Агрегаты)
    - [Индексы](#Индексы)
    - [Транзакции и свойства](#Транзакции-и-свойства)
    - [Средства оптимизации запросов в PostgreSQL](#Средства-оптимизации-запросов-в-postgresql)
3. [Python](#python)
    - [Как работает менеджер контекста](#Как-работает-менеджер-контекста)
    - Что такое абстрактный класс, в чем отличие понятия абстрактного класса от интерфейса (и как сделать подобие интерфейса на соглашениях)
    - [Что такое hashable объекты и хэш функция](#Что-такое-hashable-объекты-и-хэш-функция)
    - [Работа дескрипторов на примерах](#Работа-дескрипторов-на-примерах)
    - [Модули и пакеты](#Модули-и-пакеты)
    - [Классы и ООП в Python](#Классы-и-ооп-в-python)
    - [Работа с исключениями](#Работа-с-исключениями)
    - [Метаклассы](#Метаклассы)
    - Встроенные функции
    - Службы Python времени выполнения
    - Структуры данных, алгоритмы
    - Работа с файлами и каталогами
    - Службы операционной системы
    - Сборка пакета для pip (setuptools)
    - Celery и AMQP протокол / Periodic Tasks
4. [Django](#django)
    - [Queryset API](#queryset-api)
        - [Метод `iterator()`](#Метод-iterator)
        - [Кэширование кверисетов](#Кэширование-кверисетов)
        - [Исключение, когда кэширование не происходит](#Исключение-когда-кэширование-не-происходит)
        - [Композиция кверисетов для подзапроса](#Композиция-кверисетов-для-подзапроса)
        - Отличие применения select related / prefetch related через подзапрос
        - [When QuerySets are evaluated](#when-querysets-are-evaluated)
    - [F Expression](#f-expression)
        - [Что можно сделать, чего нельзя сделать](#Что-можно-сделать-чего-нельзя-сделать)
        - [Использование F в фильтрах](#Использование-f-в-фильтрах)
        - [Использование F в аннотациях](#Использование-f-в-аннотациях)
        - [Когда возникают race condition](#Когда-возникают-race-condition)
    - [Q Expression](#q-expression)
        - [Использование выражений](#Использование-выражений)
        - [Примеры OR lookup](#Примеры-or-lookup)
    - [Func Expression](#func-expression)
    - [Aggregate Expressions](#aggregate-expressions)
    - [Raw-SQL Expression](#raw-sql-expression)
    - [.extra()](#extra)
    - [.update()](#update)
    - [.select_for_update()](#select_for_update)
    - [.in_bulk()](#in_bulk)
    - [Models & Migrations](#models--migrations)
        - [Наследование моделей Django](#Наследование-моделей-django)
        - [Model _meta API](#model-_meta-api)
        - [Model Meta Options](#model-meta-options)
        - [Proxy](#proxy)
    - Повторно используемые приложения Django
    - Упаковка приложений (Packaging your app)
    - Обработка HTTP запросов (Handling HTTP requests)
    - Обработка шаблонов (Templates)
    - Class-based Views
    - Миграции (Migrations)
    - Кэширование в джанго (Django Cache Framework)
    - Логирование в Джанго (Logging)
5. [ExtJS и JavaScript](#extjs-и-javascript)
    - [Layout для форм в ExtJS](#layout-для-форм-в-extjs)
    - Этапы исполнения JavaScript
    - Тег script - расположение
    - Порядок парсинга HTML документа
    - [Типы в JavaScript](#Типы-в-javascript)
    - [Сравнение и приведение типов](#Сравнение-и-привидение-типов)
    - [Способы создания функций и виды функций](#Способы-создания-функций-и-виды-функций)
    - [Контекст вызова и call / apply / bind](#Контекст-вызова-и-call-appl)
    - Работа с компонентами формы ExtJS в м3 (как написать обработчик формы на м3)
    - Работа с документацией ExtJS (Где и как искать информацию по компонентам ExtJS)
    - [ExtLayout в ExtJS](#extlayout-в-extjs)
    - [Области видимости JS кода](#Области-видимости-js-кода)
    - [Расположение и компановка исходников UI компонентов ExtJs и M3]
    - [Базовые классы ExtJS](#Базовые-классы-extjs)
    - Взаимодействия компонентов UI в ExtJS с помощью событий. Обработчики событий.
6. [ООП и проектирование](#ООП-и-проектирование)
    - [Подробные примеры на SOLID](#Подробные-примеры-на-solid)
    - [Модификаторы доступа: применение _protected и __private в Python и механизм работы](#Модификаторы-доступа)
7. [Шаблоны проектирования](#Шаблоны-проектирования)
    - [Стратегия](#Стратегия)
    - [Шаблонный метод](#Шаблонный-метод)
    - [Фабрика](#Фабрика)
    - [Одиночка](#Одиночка)
    - [Подписчик](#Подписчик)
    - [Адаптер](#Адаптер)
8. [Алгоритмические основы](#Алгоритмические-основы)
    - [Подсчет сложности алгоритма](#Подсчет-сложности-алгоритма)
    - [Понятие сложности алгоритма (смысловое определение)](#Понятие-сложности-алгоритма-смысловое-определение)
    - [Типовые сложности алгоритмов (привести пример алгоритма на питоне для каждого случая)](#Типовые-сложности-алгоритмов-привести-пример-алгоритма-на-питоне-для-каждого-случая)
    - [Сравнение алгоритмов по сложности](#Сравнение-алгоритмов-по-сложности)
    - [Сложение / Умножение сложности алгоритма](#Сложение-умножение-сложности-алгоритма)
9. [M3](#m3)
    - [Из каких пакетов состоит М3 - состав и назначение пакетов](#Из-каких-пакетов-состоит-М3-состав-и-назначение-пакетов)
    - [Как создать и запустить проект на м3 с нуля](#Как-создать-и-запустить-проект-на-м3-с-нуля)
    - [URL dispatcher - обработка запросов](#url-dispatcher-обработка-запросов)
    - [Работа с контекстом, устройство контроллера](#Работа-с-контекстом-устройство-контроллера)
    - [Обертки UI компонентов ExtJS и их рендер](#Обертки-ui-компонентов-extjs-и-их-рендер)
    - [Распределение кода приложения по модулям](#Распределение-кода-приложения-по-модулям)
    - [Action/ActionPack - назначение, устройство](#action-actionpack-назначение-устройство)
    - [ObjectPack/RecordPack - назначение, устройство](#objectpack-recordpack-назначение-устройство)
    - [Виртуальные модели](#Виртуальные-модели)
    - [Знание состава компонентов общей кодовой базы educommon](#Знание-состава-компонентов-общей-кодовой-базы-educommon)

***
## Postgresql

***
### Нормализация
это процесс реструктуризации реляционной базы данных с тз так называемых нормальных форм для того чтобы:
- уменьшить избыточность (хранить данные в более чем одной таблице)
- увеличить целостность информации
- логически распределить зависимости (хранить только связанные данные в таблице)
Считается что это здравый смысл формализованный в правилах

Аномалии
- __Insertion anomaly__ (при вставке данные дублируются, или их нельзя вставить потому что есть констрейн на столбец с ненулевым значением)
- __Updation anpmaly__ (При изменении одной строки, нужно захватить еще несколько строк и если их забыть то данные потеряют целостность)
- __Deletion anomaly__ (при удалении данных, связанные данные будут удалены (к примеру класс в котором учится студент))

### Первая форма 1NF
- убрать колонки (группы колонок) с дублирующейся информацией из каждой таблицы. (База данных не должна иметь третьего измерения, колонки с названиями Класс 1, Класс 2, Класс 3)
- создать отдельные таблицы для каждой группы связанных данных и идентифицировать их с помомщью Primary Key

### Вторая форма 2NF
- Соблюсти все правила первой формы
- Убрать дублирующиеся данные в нескольких строках для каждой таблицы и расположить их в отдельной таблице
- Создать отношения между этими таблицами с помощью Foreign Key

### Третья форма 3NF
- Соблюсти все правила первой и второй формы
- Убрать столбцы которые не зависят от Primary Key в таблице (Таблица колонки Студент, Староста, Кабинет старосты)

***
### Транзакции и ACID
__Транзакция__ - последовательность операций составляющая логическую единицу работы:

ACID
- __A__ Атомарность, все или ничего. При фиксации выполняются все операции, при откате не выполняется ни одна
- __C__ Согласованность - целостность данных, система переходит из одного состояния в другое
- __I__ Изоляция - от других транзакций. На результат не должны оказывать влияние другие параллельно работающие транзакции
- __D__ Долговечность - даже после сбоя. Зафиксированные изменения никогда не теряются

***
### Изоляционные уровни транзакций
__Полная изоляция__ - результат параллельного выполнения нескольких транзакций совпадает с результатом их последовательного выполнения

Реализация полной изоляции очень сложная и стандартом SQL допускаются некоторые послабления. На каждом уровне изоляции есть допустимые аномалии

Допустимые аномалии
- __Грязное чтение__ Транзакция может "видеть" незафиксированные изменения в других транзакциях
- __Неповторяемое чтение__ Повторный запрос может показывать измененные строки
- __Фантомное чтение__ Повторный запрос может показывать новые строки

4 уровня изоляции по мере возрастания строгости:

- Read Uncommited
- Read Commited
- Repeatable Read
- Serializable (самый строгий)

На всех уровнях не допускается потеря зафиксированных изменений.

Отсутсвие всех трех феноменов не гарантирует полной изоляции.

Уровень изоляции  | "Грязное" чтение | Неповторяемое чтение | Фантомное чтение | Аномалии сериализации |
----------------- | :-------: | :-----------: | :-------: | :----------: |
| Read uncommited | __-__     | да            | да        | __да__       |
| Read commited   | -         | да            | да        | __да__       |
| Repeatable read | -         | -             | __-__     | __да__       |
| Serializable    | -         | -             | -         | __-__        |

Благодаря многоверсионности в пострегесе изначально "грязное" чтение не допускается. Repeatable read здесь это Serializable по стандарту SQL но с оговоркой что отсутствие всех этих аномалий не может гарантировать полную изоляцию.

Видимость данных внутри транзакции определяется тем в какой момент создается снимком данных.

На уровне __READ COMMITED__
- снимок данных создается каждый раз при старте каждой команды
- каждая команда транзакции "видит" изменения
- возможен несогласованный снимок данных (транзакция пытается обновить то что уже обновлено, попадает на блокировку, когда она снимается - видит несогласованный снимок данных)

Для уровня __REPEATABLE READ__ и __SERIALIZABLE__
- снимок создается перед выполнением первой команды транзакции
- все команды транзакции "видят" изменения зафиксированные на момент старта первой команды транзакции

__READ UNCOMMITED__
- "Грязное" чтение не допускается
- READ UNCOMMITED = READ COMMITED

Управление транзакциями:

В постреге есть параметр __default_transaction_isolation__, значение по умолчанию READ COMMITED

Чтобы явно управлять

```sql
=> BEGIN ISOLATION LEVEL READ COMMITED;
=> END
```
Посмотреть уровень текущей транзакции - параметр __transaction_isolation__

```sql
=> BEGIN;
=> SET TRANSACTION ISOLATION LEVEL READ UNCOMMITED;
=> SHOW transaction_isolation;
=> END
```

2-я транзакция видит только те изменения, которые были зафиксированны на момент старта очередного запроса к БД. Если во время выполнения долгой команды другая транзакция успела зафиксировать изменения, то они не будут видны

С одной стороны сторая транзакция не должна видеть все изменения на начало команды. Но если транзакция повисла на строке которую заняла другая транзакция и ждет разблокировки. Когда транзакция выходит после блокирования она вынуждена перечитать эту строку. Такое происходит только при блокировке.

***
### Служебные таблицы
Системный каталог это некая мета-информация которая хранится в самой базе данных и описывает что в ней есть. Находится в схеме `pg_catalog`. Кроме select from pg_catalog мы можем использовать команды psql

команды \d* [pattern]
- списки по типам объектов (\dt, \dv, \df)
- дополнительная информация - модификатор +
- системные объекты - модификатор S

Правила наименования таблиц и представлений системного каталога такие
- Название начинается с `pg_`
- Названия столбцов имеют трехбуквенный префикс, и он соответствует имени таблицы каталога
    - pg_proc - префикс 'pro'
    - pg_attribute - префикс 'att'
    - pg_namespace - префикс 'nsp'
    - pg_tablespace - префикс 'spc'
    - pg_class - префикс 'rel'

У каждой БД кластера свой набор таблиц системного каталога

8 глобальных для кластера БД таблиц
- базы данных `pg_database`
- табличные пространства `pg_tablespace`
- роли `pg_authid`, `pg_auth_members`
- настройки для ролей `pg_db_role_settings`
- шаблоны процедурных языков `pg_pltemplate`
- зависимости и описания для общих объектов `pg_shdepend`, `pg_shdescription`

***
## SQL
- https://community.modeanalytics.com/sql/
- http://www.sql-tutorial.ru/ru/

***
### Синтаксис DATA DEFINITION (объявление таблиц и всего остального)
__DDL__ (Data Definition Language) - работа со структурой базы
   + CREATE Создание базы данных и любых структурных элементов
       - таблиц `create table table_name (col1 varchar, col2 int)`
       - индексов `create index index_idx on table (column);`
       - вью (виртуальная таблица, из которой потом можно делать селекты) `create view view_name as select column from table where cond`. для апдейта `create or replace view view_name as select * from t1 where id=1`
       - хранимых процедур
       - функций `create or replace function emp_stamp() returns trigger as $emp_stamp$`
       - триггеров `create trigger emp_stamp before insert or update on emp for each row execute procedure emp_stamp()`
   + ALTER Изменение структуры базы
        - `alter table t1 add colum varchar`
        - `alter table t1 drop column col`
        - `alter table t1 alter column col int32`
        - `alter table if exist t1 rename column col1 to col2`
        - `alter table t1 rename to t2`
   + DROP Удаление объектов из базы
        - `drop view view_name`
        - `drop table table_name`
        - `drop index index_idx`
   + TRUNCATE удаление всех записей из таблицы
   + COMMENT Добавление комментариев в *data dictionary*
   + RENAME Переименование объекта

***
### Синтаксис DATA MANIPULATION (Выборка / Удаление / Изменение данных)
__DML__ (Data Manipulation Language) - работа с конкретными записями
   + SELECT взять данные из таблицы
   + INSERT добавить записть в таблицу `insert into t1 (col1, col2) values (val1, val2)`
   + UPDATE изменить записи в таблице `update t1 set col1 = val1, col2 = val2 where cond`
   + DELETE удалить запись из таблицы `delete from t1 where cond`
   + MERGE вставить или изменить запись
   + CALL Вызов PL/SQL субпрограммы
   + EXPLAIN PLAN интерпретация действий с записями (подробный вывод)
   + LOCK TABLE контроль паралельных процессов

***
### Using data string functions to clean data

`LEFT(string, number)` позволяет взять часть строки слева до точки и использовать как отдельную строку. То же самое для `RIGHT`
```sql
SELECT incidnt_num,
    date,
    LEFT(date, 10) AS cleaned_date,
    RIGHT(date, LENGTH(date) - 11) AS cleaned_time
FROM tutorial;
```
`TRIM` используется для удаления символов с начала и конца строки
1. leading, trailing, both
2. symbols
3. column
```sql
SELECT location, TRIM(both '()' FROM location) FROM tutorial;
```
`POSITION` вернет цифровое значение символа в строке, позицию
```sql
SELECT
    incidnt_num,
    descript,
    POSITION('A' IN descript) AS a_position
FROM tutorial.sf_crime_incidents_2014_01;
```
`SUBSTR(string, starting char position, № of chars)`
```sql
SELECT incidnt_num,
    date,
    SUBSTR(date, 4, 2) AS day
FROM tutorial
```
`CONCAT` объединение строк (не забыть про `||`)
```sql
SELECT incidnt_num,
       day_of_week,
       LEFT(date, 10) AS cleaned_date,
       CONCAT(day_of_week, ', ', LEFT(date, 10)) AS day_and_date
  FROM tutorial
```
`COALESCE` значениям NULL дат ьнормальное имя
```sql
SELECT incidnt_num,
       descript,
       COALESCE(descript, 'No Description')
FROM tutorial.sf_crime_incidents_cleandate
ORDER BY descript DESC
```

***
### Subqueries
```sql
SELECT sub.*
  FROM (
        SELECT *
          FROM tutorial.sf_crime_incidents_2014_01
         WHERE day_of_week = 'Friday'
       ) sub
 WHERE sub.resolution = 'NONE'
```
Сначала идет обработка внутреннего запроса, затем внешнего. Обычно подзапросы требуют дать имя. Часто используются для аггрегации в несколько этапов

```sql
SELECT LEFT(sub.date, 2) AS cleaned_month,
       sub.day_of_week,
       AVG(sub.incidents) AS average_incidents
  FROM (
        SELECT day_of_week,
               date,
               COUNT(incidnt_num) AS incidents
          FROM tutorial.sf_crime_incidents_2014_01
         GROUP BY 1,2
       ) sub
 GROUP BY 1,2
 ORDER BY 1,2
```
Также используются в фильтрах, но подзапрос должен вернуть только один результат. Исключение - `IN`. В таком случае давать название подзапросу не нужно
```sql
SELECT * FROM tutorial.sf_crime_incidents_2014_01
WHERE Date = (SELECT MIN(date) FROM tutorial.sf_crime_incidents_2014_01);
```

Также подзапросы можно использовать в джойнах
```sql
SELECT *
  FROM tutorial.sf_crime_incidents_2014_01 incidents
  JOIN ( SELECT date
           FROM tutorial.sf_crime_incidents_2014_01
          ORDER BY date
          LIMIT 5
       ) sub
    ON incidents.date = sub.date
```

***
### Window Functions
`OVER` сигнализирует что это оконная функция. Их нельзя использовать с GROUP BY. Окно это отсортированный кусок данных на которых проведен подсчет.

Оконная функция выполняет вычисления для набора строк, некоторым образом связанных с текущей строкой. Можно сравнить её с агрегатной функцией, но, в отличие от обычной агрегатной функции, при использовании оконной функции несколько строк не группируются в одну, а продолжают существовать отдельно. Внутри же, оконная функция, как и агрегатная, может обращаться не только к текущей строке результата запроса.

Вызов оконной функции всегда содержит предложение OVER, следующее за названием и аргументами оконной функции. Это синтаксически отличает её от обычной или агрегатной функции. Предложение OVER определяет, как именно нужно разделить строки запроса для обработки оконной функцией. Предложение PARTITION BY, дополняющее OVER, указывает, что строки нужно разделить по группам или разделам, объединяя одинаковые значения выражений PARTITION BY. Оконная функция вычисляется по строкам, попадающим в один раздел с текущей строкой.

https://postgrespro.ru/docs/postgrespro/9.5/tutorial-window

```sql
SELECT start_terminal,
       duration_seconds,
       SUM(duration_seconds) OVER
         (PARTITION BY start_terminal ORDER BY start_time)
         AS running_total
  FROM tutorial.dc_bikeshare_q1_2012
 WHERE start_time < '2012-01-08'
```

***
### Оптимизации
`LIMIT` не ускорит запрос если происходит аггрегация, потому что она устроена по другому. Если нужно ускорить запрос до того как произойдет аггрегания, нужно сначала отфильровать таблицу например так
```sql
SELECT COUNT(*) FROM (SELECT * FROM benn.sample_event_table LIMIT 100) sub;
```
Гораздо лучше джойнить уже отфильтрованные таблицы. Например здесь будет 26.989 строк для джойна
```sql
SELECT teams.conference AS conference,
       players.school_name,
       COUNT(1) AS players
  FROM benn.college_football_players players
  JOIN benn.college_football_teams teams
    ON teams.school_name = players.school_name
 GROUP BY 1,2
```
А здесь вего 252
```sql
SELECT teams.conference, sub.*
  FROM (SELECT players.school_name, COUNT(*) AS players
        FROM benn.college_football_players players
        GROUP BY 1) sub
  JOIN benn.college_football_teams teams
  ON teams.school_name = sub.school_name
```
- EXPLAIN

***
### HAVING
Фильтр результата который пришел от GROUP BY
```sql
SELECT year,
       month,
       MAX(high) AS month_high
  FROM tutorial.aapl_historical_stock_price
 GROUP BY year, month
HAVING MAX(high) > 400
 ORDER BY year, month
```

***
### Джойны
```sql
SELECT teams.conference AS conference,
       AVG(players.weight) AS average_weight
  FROM benn.college_football_players players
  JOIN benn.college_football_teams teams
    ON teams.school_name = players.school_name
 GROUP BY teams.conference
 ORDER BY AVG(players.weight) DESC
```

- LEFT JOIN returns only unmatched rows from the left table.
- RIGHT JOIN returns only unmatched rows from the right table.
- FULL OUTER JOIN returns unmatched rows from both tables.
http://joins.spathon.com/

Таблицы которые будут сджойнены можно офильтровать перед слиянием
```sql
SELECT companies.permalink AS companies_permalink,
       companies.name AS companies_name,
       acquisitions.company_permalink AS acquisitions_permalink,
       acquisitions.acquired_at AS acquired_date
  FROM tutorial.crunchbase_companies companies
  LEFT JOIN tutorial.crunchbase_acquisitions acquisitions
    ON companies.permalink = acquisitions.company_permalink
   AND acquisitions.company_permalink != '/company/1000memories'
 ORDER BY 1
```
Здесь фильтр пройдет перед слиянием, аниже после слияния двух таблиц
```sql
SELECT companies.permalink AS companies_permalink,
       companies.name AS companies_name,
       acquisitions.company_permalink AS acquisitions_permalink,
       acquisitions.acquired_at AS acquired_date
  FROM tutorial.crunchbase_companies companies
  LEFT JOIN tutorial.crunchbase_acquisitions acquisitions
    ON companies.permalink = acquisitions.company_permalink
 WHERE acquisitions.company_permalink != '/company/1000memories'
    OR acquisitions.company_permalink IS NULL
 ORDER BY 1
```

`UNION` позволяет соединить две таблицы с одинаковыми колонками

```sql
SELECT *
  FROM tutorial.crunchbase_investments_part1
 UNION
 SELECT *
   FROM tutorial.crunchbase_investments_part2
```
`UNION` по дефолту возвращает результаты без дубликатов, в то время как `UNION ALL` вернет все

ON также может принимать другие операции сравнения, удобно при работе с данными
```sql
SELECT companies.permalink,
       companies.name,
       companies.status,
       COUNT(investments.investor_permalink) AS investors
  FROM tutorial.crunchbase_companies companies
  LEFT JOIN tutorial.crunchbase_investments_part1 investments
    ON companies.permalink = investments.company_permalink
   AND investments.funded_year > companies.founded_year + 5
 GROUP BY 1, 2, 3
```

Можно также джойнить на себя

```sql
SELECT DISTINCT
    japan_investments.company_name,
    japan_investments.company_permalink
  FROM tutorial.crunchbase_investments_part1 japan_investments
  JOIN tutorial.crunchbase_investments_part1 gb_investments
    ON japan_investments.company_name = gb_investments.company_name
   AND gb_investments.investor_country_code = 'GBR'
   AND gb_investments.funded_at > japan_investments.funded_at
 WHERE japan_investments.investor_country_code = 'JPN'
 ORDER BY 1
```

***
### Агрегаты
- AVG
- COUNT
- EVERY (eq bool_and)
    - `SELECT EVERY(id < 10) FROM book` is EVERY ID lower than 10 ?
    - `SELECT authoe_id, EVERY(title LIKE '%a') FROM book GROUP BY author id` Does EVERY book for each author end with the letter "a"?
- MAX
- MIN
- SUM
- ANY
- ALL

https://docs.djangoproject.com/en/2.0/ref/contrib/postgres/aggregates/

***
### Индексы
`CREATE INDEX index_name ON table (column1, column2)` нужно смотреть чаще в выражаении WHERE встречается одна колонка или несколько. Постгрес умеет объединять индексы по отдельным колонкам с помощью битовой карты, и иногда такой подход работает быстрее чем индекс на несколько колонок. кроме того имеет значение порядок колонок. В случае индекса на две колонки он будет использоваться для фильтров по обоим колонкам, по первой колонке, __но__ не по последней колонке если фильтр будет только по ней.

`CREATE UNIQUE INDEX index_name ON table_name (col_name)`

`CREATE INDEX articles_flagged_created_at_index ON articles(created_at) WHERE flagged IS TRUE;`

`CREATE INDEX users_lower_email ON users(lower(email));`

`CREATE INDEX articles_published_at_index ON articles(published_at DESC NULLS LAST);` В B-Tree по умолчанию индексы отсортированы ASC, но можно указать и иначе

`CREATE INDEX CONCURRENTLY` есть только в постгресе

`\d company` информация о таблице, в тч о индексах

`DROP INDEX index_name;`


- __B-Tree__ дефольный индекс получаемый командой `CREATE INDEX`. Практически все базы данных имеют такой механизм. B-tree это сбалансированное дерево, а значит колчество уровней примерно одинаковое. Эффективно используются для выражений = и периодов значений. Оперируют со всеми типами данных и могут быть использованы для вытаскивания NULL значений. Созданы для эффиктивной работы с механизмом кеширования.
- __Hash Indexes__ могут быть использованы только для сравнения =, но также они не безопасны в транзакции, должны пересобираться после краша. Очень мало улучшений по сравнению с B-Tree.
- __Generalized Inverted Indexes (GIN)__ полезны когда необходимо найти соответствие многим значениям в одной строке, B-Tree же оптимальны для случаев когда в строке нужно найти одно значение. Также они хороши для индексации списковых значений а также полнотекстового поиска.
- __Generalized Search Tree (GiST)__ Часто используются для полнотекстового поиска и индексирования геометрических структур, потому что позволяют устанавливать сложные условия чем = и периоды значений.

***
### Транзакции и свойства
__TCL__ (Transaction Control Language) - управление транзакциями
   + COMMIT :: коммит транзакции
   + ROLLBACK :: откатить транзакцию
   + SAVEPOINT :: установить точку сохранения
   + SET TRANSACTION :: установить характеристики транзакции

```sql
-- Транзакция начинается
BEGIN;
-- Добавим уровень изоляции если забыли
SET TRANSACTION ISOLATION LEVEL SERIALIZABLE;
UPDATE naccounts SET balance=balance - 100.00 WHERE name = 'Alice';
SAVEPOINT my_savepoint;
UPDATE naccounts SET balance=balance - 100.00 WHERE name = 'Bob';
-- опс, забыли что то
ROLLBACK TO my_savepoint;
UPDATE naccounts SET balance=balance - 100.00 WHERE name = 'Wally';
-- Транзакция заканчивается
COMMIT;
```

***
### Средства оптимизации запросов в PostgreSQL

__DCL__ (Data Control Language) - работа с правами
   + GRANT дать права
   + REVOKE забрать права

***
## Python
***
### Как работает менеджер контекста
http://effbot.org/zone/python-with-statement.htm

Менеджеров контекста можно увидеть во многих местах стандартной библиотеки. Например
- threading.Lock
- zipfile.ZipFiles
- subprocess.Popen
- tarfile.TarFile
- telnetlib.Telnet
- pathlib.Path

Олдскульный менеджер контекста.
```python
class File():
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode
    def __enter__(self):
        self.open_file = open(self.filename, self.mode)
        return self.open_file
    def __exit__(self, *args):
        self.open_file.close()
```

Используя стандартную библиотеку `contextlib`
```python
from contextlib import contextmanager

@contextmanager
def open_file(path, mode):
    the_file = open(path, mode)
    yield the_file
    the_file.close()
```
Можно отнаследоваться от `ContextDecorator` и создать собственную версию декоратора
```python
from contextlib import ContextDecorator

class makeparagraph(ContextDecorator):
    def __enter__(self):
        print('<p>')
        return self

    def __exit__(self, *exc):
        print('</p>')
        return False

@makeparagraph()
def emit_html():
    print('Here is some non-HTML')
```
Источники:
- https://jeffknupp.com/blog/2016/03/07/python-with-context-managers/
- https://github.com/python/cpython/blob/2.7/Lib/contextlib.py

***
### Что такое абстрактный класс, в чем отличие понятия абстрактного класса от интерфейса (и как сделать подобие интерфейса на соглашениях)

Контракт это концептуальная метафора об условиях и ответственности в гражданско-правовых договорах.

Контракт некоторого метода или функции может включать в себя:

- конкретные __обязательства__, которые любой клиентский модуль должен выполнить перед вызовом метода — `предусловия`, которые дают преимущество для поставщика — он может не проверять выполнение предусловий;
- конкретные __свойства__, которые должны присутствовать после выполнения метода — `постусловия`, которые входят в обязательства поставщика;
- обязательства по выполнению конкретных свойств — `инвариантов`, которые должны выполняться при получении поставщиком сообщения, а также при выходе из метода.

__Интерфейс__ - это контракт, пустая оболочка. Он только описывает как называются методы но ничего не делает внутри них.

__Абстракные классы__, в отличие от интерфейсов, как это не удивительно - классы. Абстрактные классы похожи на интерфейсы но могут содержать как пустые методы которые должны заполнить наследники, так и конкретные имплементации которое будут общими между наследниками.

Java использует интерфейсы потому что у нее нет множественного наследования. В питоне же обычно пишется так

```python
class SomeAbstraction(object):
    pass  # lots of stuff - but missing something

class Mixin1(object):
    def something(self):
        pass  # one implementation

class Mixin2(object):
    def something(self):
        pass  # another

class Concrete1(SomeAbstraction, Mixin1):
    pass

class Concrete2(SomeAbstraction, Mixin2):
    pass
```

Попытка сделать интерфейсы в питоне 
https://zopeinterface.readthedocs.io/en/latest/README.html

***
### Что такое hashable объекты и хэш функция

Объект называется `hashable` если его hash не изменяется в течении всей своей жизни (а также у него есть метод `__hash__()`), также этот объект можно сравнить с другими объектами (должны быть реализованы методы `__eq__()` или `__cmp__()`). Hashable объекты которые при сравнении считаются одинаковыми должны иметь одинаковый hash.

Наличие такого свойства позволяет использовать такие объеты в качестве ключей для словарей и участников set, потому что это структуры функционируют на основе hash.

Все неизменяемые встроенные типы в питоны hashable, и все изменяемы типы нет. Объекты которые получаются из пользовательских классов тоже hashable по умолчанию, они не равны друг другу потому что их hash это `id()`.

У неизменяемым объектам относятся цифры, строки и кортежи. Они не могут изменяться, только заменяться на новый объект. Неизменяемый вариант set - это fromzenset, и он hashable. Кортежи это не неизменяемые списки, а анонимные структуры.

Пример хэширования строки
```python
import hashlib
hash_object = hashlib.md5(b'Hello World')
print(hash_object.hexdigest())
```

`hash()` это встроенная функция, объекты которые имплементируют `__hash__` метод обычно импользуют ее внутренне. всегда возвращает число.

- https://docs.python.org/3/reference/datamodel.html#object._\_hash__
- https://mail.python.org/pipermail/python-list/2000-March/048085.html
- https://en.wikipedia.org/wiki/Hash_table
- https://docs.python.org/3/library/collections.abc.html#collections.abc.Hashable

***
### Работа дескрипторов на примерах

Дескрипторы это специальные классы с особыми методами:

```python
class Descriptor:
    def __get__(self, instance, owner): ..  # return attr value
    def __set__(self, instance, value): ..  # return None
    def __delete__(self, instance): ..  # return None
```

Чтобы сделать дескриптор только для чтения нужно обязательно имплементировать метод `__set__` который бы вызывал ошибку.

__@property__ это особый, predefined дескриптор

Пример дескриптора который возвращает значение в кубе:
```python
class DescSquare:
    def __init__(self, start):
        self.value = start
    def __get__(self, instance, owner):
        return self.value ** 2
    def __set__(self, instance, value):
        self.value = value

class Client1:
    X = DescSquare(3)
```

Крутой пример дескриптора и декоратора из джанго

```python
class cached_property:
    """
    Decorator that converts a method with a single self argument into a
    property cached on the instance.
    Optional ``name`` argument allows you to make cached properties of other
    methods. (e.g.  url = cached_property(get_absolute_url, name='url') )
    """
    def __init__(self, func, name=None):
        self.func = func
        self.__doc__ = getattr(func, '__doc__')
        self.name = name or func.__name__

    def __get__(self, instance, cls=None):
        """
        Call the function and put the return value in instance.__dict__ so that
        subsequent attribute access on the instance returns the cached value
        instead of calling cached_property.__get__().
        """
        if instance is None:
            return self
        return instance.__dict__[self.name] = self.func(instance)
```

Другие примеры использования дескрипторов в джанго:

- [Manager Descriptor](https://github.com/django/django/blob/d7b2aa24f75434c2ce50100cfef3586071e0747a/django/db/models/manager.py#L169)
- [File Descriptor](https://github.com/django/django/blob/d7b2aa24f75434c2ce50100cfef3586071e0747a/django/db/models/fields/files.py#L133)
- [Forward ManyToOne Descriptor](https://github.com/django/django/blob/8b21878357364a461bae711c4d0011a8f338b160/django/db/models/fields/related_descriptors.py#L72)
- [Generic Foreign Key](https://github.com/django/django/blob/d13a9e44ded4e93570c6ba42ec84e45ddca2505b/django/contrib/contenttypes/fields.py#L18)
- [Locale Regex DEscriptior](https://github.com/django/django/blob/d7b2aa24f75434c2ce50100cfef3586071e0747a/django/urls/resolvers.py#L79)
- [Deffered Attribute](https://github.com/django/django/blob/9ba3df82402e7e23b353da20aea6894935241ef9/django/db/models/query_utils.py#L116)

***
### Модули и пакеты
Модуль это файл с расширением `.py` и инструкциями, пакет это папка с модулями и особым модулем `__init__.py`

***
### Классы и ООП в Python
ООП в питоне совсем не обязательно. Все зависит от задачи, если времени мало ООП только навредит, если нужно поддерживать продукт в будущем то нужно использовать классы

MRO method resolution order
```python
class A: x = 'a'
class B(A): pass
class C(A): x = 'c'
class D(B, C): pass
```

Порядок поиска значения будет: __D-B-A-C-A__ в то время как если A наследуется по новым правилам от object, порядок будет такой:
__D-B-C-A-object__

***
### Работа с исключениями
1. __try/except/else/finally__ отлов и обработка исключений
2. __raise__ вызвать исключение
3. __assert__ вызвать эксепшн по условию
4. __with/as__ контекст менеджеры

Создание кастомных exception получается созданием класса с наследованием от Exception

```python
class MyCustomException(Exception):
    pass
```

***
### Метаклассы
Классовые декораторы добавляют логику к классу во время создания инстансов класса, в то время как метакласс изменяет класс во время его создания и возвращает уже измененный класс.

Создавая метакласс мы как бы говорим питону что хотим передать создание этого класса другому классу.

Метакласс наследуется от класса type. Обычно классы наследуются от класса type, но создав метакласс, мы заменяем type на пользовательский класс.

Пример создания класса через type

```python
Spam = type('Spam', (Eggs,), {'data': 1, '__module__': '__main__'})
```

Пример создания класса от метакласса:
```python
class Spam(object):  # Желательно наследоваться от нового object
    __metaclass__ = Eggs
```

И получится

```python
Spam = Eggs(classname, superclasses, attributedict)
```

Если у метакласса определены `__new__` или `__init__` они как раз будут вызываны при создании класса

Метакласс это обычный класс, который должен наследоваться от `type`, и единственное отличие от остальных классов в том, что он будет вызван автоматически после создания класса и изменит его.

Здесь `__new__` взят из type и ничего не делает, но можно видеть как создается метакласс

```python
class Eggs(type):
    def __new__(meta, classname, supers, classdict):
        return type.__new__(meta, classname, supers, classdict)
```

Метакласс не обязательно должен быть классом. Можно использовать мета-функцию

```python
def MetaFunc(classname, supers, classdict):
    return type(classname, supers, classdict)

class Spam(Eggs):
    __metaclass__ = MetaFunc
```

Специальные методы которые использует метакласс
- `__new__` будет вызван перед тем как инстанс класса основанного на метаклассе создан
- `__init__` этот метод будет вызван для установки начальных значений созданного объекта
- `__prepare__` определяет неймспейс в маппинге который хранит аттрибуты
- `__call__` этот метод вызывается когда конструктор нового класса собирается быть использованным для создания объекта

```python
# Singleton metaclass primer

# a final metaclass. Subclassing a class that has the Final metaclass should fail
class Final(type):  
    def __new__(cls, name, bases, attr):
        # Final cannot be subclassed
        # check that a Final class has not been passed as a base
        # if so, raise error, else, create the new class with Final attributes
        type_arr = [type(x) for x in bases]
        for i in type_arr:
            if i is Final:
                raise RuntimeError("You cannot subclass a Final class")
        return super(Final, cls).__new__(cls, name, bases, attr)
```
http://stackabuse.com/python-metaclasses-and-metaprogramming/

***
### Декораторы
```python
from functools import wraps

def notifyfunc(fn):
    @wraps(fn)
    def composite(*args, **kwargs):
        print("Executing '%s'" % fn.__name__)
        return fn(*args, **kwargs)
    return composite
```
***
### Встроенные функции
### Службы Python времени выполнения
### Структуры данных, алгоритмы
### Работа с файлами и каталогами
### Службы операционной системы
### Сборка пакета для pip (setuptools)
### Celery и AMQP протокол / Periodic Tasks

***
## Django
### Queryset API
- Аттрибуты
    - `ordered` вернет правду если кверисет отсортирован
    - `db` база данных на которой будет рпоизведен запрос если сделать его сейчас
    - `query` примерное представление о том каким будет запрос, не являются частью публичного АПИ
- Методы которые возвращают новый QuerySet
    - `filter(**kwargs)`
    - `exclude(**kwargs)`
    - `annotate(*args, **kwargs)`
    - `order_by(*fields)`
    - `reverse()` возвращает данные в обратном порядке
    - `distinct(*fields)`
    - `values(*fields, **expressions)`
    - `values_list(*fields, flat=False, named=False)`
    - `dates(field, kind, order='ASC')` Возвращает кверисет который будет списком объектов
    - `datetime.date` всех доступных дат для определенного типа. kind = ('year', 'month', 'day')
    - `datetimes(field_name, kind, order='ASC', tzinfo=None)`
    - `none()` возвращает пустой кверисет который никогда не будет делать запрос к базе
    - `all()` возвращает копию текущего кверисета
    - `union(*other_qs, all=False)` использует SQL `UNION` чтобы соединить два кверисета. UNION возвращает только уникальные значение по умолчаниюЮ для получения всех значений используй `all=True`
    - `intersection(*other_qs)` SQL `INTERSECT`
    - `difference(*other_qs)` SQL `EXCEPT`
    - `select_related(*fields)`
    - `prefetch_related(*lookups)`
    - `extra(select=None, where=None, params=None, tables=None, order_by=None, select_params=None)` хук для инекции дополнительного запроса в кверисет
    - `defer(*fields)` подсказать джанго какие поля не надо тащить из базы
    - `only(*fields)` тащи из базы только эти поля
    - `using(alias)` для какой базы данных сделать запрос
    - `select_for_update(nowait=False, skip_locked=False, of=())` возвращает кверисет который заблокирует строки до конца транзакции.
    - `raw(raw_query, params=None, translations=None)`. Берет sql запрос и возвращает RawQuerySet который можно перебирать как обычный
- Методы которые не возвращают новый кверисет
    - `get(**kwargs)` возвращает совпавший объект
    - `create(**kwargs)`
    - `get_or_create(defaults=None, **kwargs)`
    - `update_or_create(defaults=None, **kwargs)`
    - `bulk_create(objs, batch_size=None)`
    - `count()`
    - `in_bulk(id_list=None)`
    - `iterator(chunk_size=2000)` выполнить кверисет и вернуть итератор как результат выполнения
    - `latest(*fields)`
    - `earliest(*fields)`
    - `first()`
    - `last()`
    - `aggregate(*args, **kwargs)` возвращает словарь агрегированных данных
    - `exists()` возвращает правду если кверисет содержит какие либо результаты. Пытается сделать самый простой и быстрый запрос к базе, но часто может сделать обычный запрос как если выполнить кверисет
    - `update(**kwargs)` возвращает количество совпавших для обновления строк (при этом если в этих строках уже содержалось нужное значение они все равно будут подсчитаны)
    - `delete()` удаляет один или несколько объектов, возвращает два значения - количество удаленных строк и словарь {приложение.модель: количество удаленных}
    - `as_manager()` возвращает менеджера с копией кверисета

https://github.com/django/django/blob/master/django/db/models/query.py#L179

#### Метод iterator()
Выполняет кверисет (используя сгенерированный sql запрос) и возвращает итератор. Обчно кверисет результат выолнения чтобы последующие выполнения запросов не требовали обращения к базе данных. В отличие от него `iterator()` чистает результат напрямую, без кеширования на уровне кверисета. Для кверисета который содержит большое количество значений которые нужно прочитать только один раз это может помоч производительности и уменьшении требуемой памяти (тк нет шага кеширования?)

> Используя `iterator()` на уже закешированный кверисет вынудит его сделать запрос к базе еще раз! Также при использовании `iterator()` предыдущие вызовы `prefetch_related()` будут проигнорированы так как использование обеих этих оптимизаций вместе не имеет смысла.

В зависимости от бэкенда базы, результат запроса будет загружен целиком или будет потоком из базы используя `server-side cursors`. PostgreSQL с server-side cursor выбудет выгружать результаты потоково без загрузки целиком в память. С таким курсоров параметр `chunk_size` определяет количество результатов которые нужно закешировать на уровне драйвера базы. Получение больших кусков данных уменьшает число обращений к базе за счет увеличения хранимого в памяти места. В PostgreSQL такой курсор будет работать только при включенной настройке `DISABLE_SERVER_SIDE_CURSORS = False` (c джанго 1.11)

https://docs.djangoproject.com/en/2.0/ref/models/querysets/#iterator

#### Кэширование кверисетов
Каждый кверисет кешируется после первого запроса к базе. Если не закешировать кверисет в переменной может получиться два запроса к базе вместо одного

```python
# Two queries
print([e.headline for e in Entry.objects.all()])
print([e.headline for e in Entry.objects.all()])
# Only one
qs = Entry.objects.all()
print([p.headline for p in queryset])
print([p.pub_date for p in queryset])
```
https://docs.djangoproject.com/en/1.11/topics/db/queries/#caching-and-querysets

#### Исключение, когда кэширование не происходит
Когда выполняется запрос к базе на только несколько записей из кверисета, кэш проверяется но если там нет резульатов то будет дополнительный запрос

`_result_cache` объект хранит результат

> Ограничивая кверисет используя слайс или индекс не заполнит кэш

```python
qs = Entry.objects.all()
print(queryset[5])  # Queries the database
print(queryset[5])  # Did it again

# However
qs = Entry.objects.all()
[entry for entry in queryset]
print(queryset[5])  # Uses cache
print(queryset[5])  # Uses cache
```
Способы наполнить кэш
```python
[entry for entry in queryset]
bool(queryset)
entry in queryset
list(queryset)
```
> Печть кверисетов не наполнит кэш. Происходит это потому что вызов `__repr__()` возвращает слайс кверисета
https://docs.djangoproject.com/en/1.11/topics/db/queries/#when-querysets-are-not-cached

***
#### Композиция кверисетов для подзапроса
```python
employee_query = Employee.objects.filter(company='Private').only('id').all()
Person.objects.value('name', 'age').filter(id__in=employee_query)

Нужно быть осторожно с кешированием, джанго может не закешировать подзапрос и тогда весь запрос опять пойдет к базе данных.

```
https://mattrobenolt.com/the-django-orm-and-subqueries/

https://docs.djangoproject.com/en/2.0/ref/models/expressions/#subquery-expressions

с джанго 1.11

```python
from django.db.models import OuterRef, Subquery
newest = Comment.objects.filter(post=OuterRef('pk')).order_by('-created_at')
Post.objects.annotate(newest_commenter_email=Subquery(newest.values('email')[:1]))
```
__OuterRef__ это ссылка на поле из вышестоящего запроса. Работает как `F expression` за исклюючением того, что проверка на то существует ли это поле не производится до тех пока внешний запрос не выполнен.

***
#### Отличие применения select related / prefetch related через подзапрос
__select_related(*fields)__ - возвращает кверисет который следует за FK ссылками выбирая дополнительные данные во время выполнения SQL запроса. С тз оптимизации может дать прирост скорости потому что делается не два запроса к базе а один, но более сложный. Этот метод использует SQL джойны, но имеет ограничения, следует только FR отношениям и OneToOne чтобы обезопасить себя от гигантских запросов которые могут повесить систему.

__prefetch_related(*lookups)__ - возвращает кверисет который автоматически выдернет связанные объекты. Но механизм работы у него отличается от select_related, т.к. этот метод делает несколько запросов к базе и склеивает данные уже на стороне питона. Благодя этому он может делать запросы для получения ManyToMany и ManyToOne отношений.

У обоих этих инструментов цель едина - обеспечить лучшую производительность при запросах связанных объектов из БД.

***
#### When QuerySets are evaluated
* __Iteration__. A QuerySet is iterable, and it executes its database query the first time you iterate over it.
* __Slicing__. Slicing an unevaluated QuerySet usually returns another unevaluated QuerySet, but Django will execute the database query if you use the “step” parameter of slice syntax, and will return a list.
* __Pickling/Caching__
* __repr()__
* __len()__
* __list()__
* __bool()__
* entry in queryset

***
### F Expression
`F()` объект представляет собой значение поля модели или аннотированной колонки. Оно позволяет ссылаться на значение поля и осуществлять операции с базой без хранения в памяти, только на уровне базы.

```python
reporter - Reporters.objects.get(name='Tintin')
reporter.stories_field += 1
reporter.save()
# vs
reporter = Reporters.objects.get(name='Tintin')
reporter.stories_field = F('stories_field') + 1
reporter.save()
```
F() помогает оптимизтировать запросы
- передавая работу базе данных а не питону
- уменьшая количество запросов к базе как например при `update`

F() прикрепленный к полю модели будет доступен после сохранения и будет вызываться при каждом сохранении

```python
reporter = Reporters.objects.get(name='Tintin')
reporter.stories_field = F('stories_field') + 1
reporter.save()
reporter.name = 'Tintin Jr.'
reporter.save()
```
Здесь stories_field будет = 3

https://docs.djangoproject.com/en/2.0/ref/models/expressions/#f-expressions

#### Что можно сделать, чего нельзя сделать
Часто используется в выражении обновления для того чтобы обновить каунтер значения поля за один запрос к базе данных.
```python
reporter = Reporters.objects.filter(name='Tintin')
reporter.update(stories_field=F('stories_field') + 1)
```

#### Использование F в фильтрах
F() часто используется в фильтрах, тк позволяет отфильтровать результат в зависимости от того какое значение в базе данных а не в питоне.

К примеру можно отфильтровать значение поля исходя из занчения другого поля. Нужно найти все записи в блоге количество комментариев в которых в два раза больше количества пингбэков

```python
from django.db.models import F
Entry.objects.filter(n_comments__gt=F('n_pingbacks') * 2)
```

Найти записив которых рейтинг записи меньеш чем сумма пингбэка и комметариев

```python
Entry.objects.filter(rating__lt=F('n_comments') + F('n_pingbacks'))
# Можно таже использовать с отношениями
Entry.objects.filter(authors__name=F('blog__name'))
# Можно также с таймдельтой
from datetime import timedelta
Entry.objects.filter(mod_date__gt=F('pub_date') + timedelta(days=3))
```

https://docs.djangoproject.com/en/2.0/topics/db/queries/#using-f-expressions-in-filters

#### Использование F в аннотациях
F() можно использовать для создания динамических полей на модели комбинируя разные поле с помощью арифметических операторов

```python
company = Company.objects.annotate(chairs_needed=F('num_employees') - F('num_chairs'))
```
> В аннотациях при ссылке на внешнее поле FK, F() возвращает айдишник а не инстанс модели

```python
car = Company.objects.annotate(built_by=F('manufacturer'))[0]
car.manufacturer  # <Manufacturer: Toyota>
car.built_by  # 3
```
https://docs.djangoproject.com/en/2.0/ref/models/expressions/#using-f-with-annotations

#### Когда возникают race condition
F() позволяет избежать race condition. Если два потока питона будут выполнять код из примера выше одновременно, то один из тредов кто быстрее успел закоммитить результат будет сохранен, а работа второго потеряна. Если же база ответственная за обновление поля, сам процесс более защищен. Обновление поля будет зависеть от текущего значения а не от значения которое передает код питона.
https://docs.djangoproject.com/en/2.0/ref/models/expressions/#avoiding-race-conditions-using-f

### Q Expression
https://github.com/django/django/blob/master/django/db/models/query_utils.py#L47
#### Использование выражений
Q-объект(django.db.models.Q) используется для инкапсуляции коллекции аргкментов ака `field lookups`. Q-объекты могут быть объединены операторами `|` и `&`. когда оператор используется с двумя объектами возвращается новый Q-объект. Кроме того объекты Q могут быть негативными используя оператор `~`.
Каждый метод который принимает ключевые аргументы (filter, exclude, get) также может принять один или несколько Q-объектов. Можно также использовать их вместе `Poll.objects.get(Q(pub_date=date(2005, 5, 2)) | Q(pub_date=date(2005, 5, 6)), question__startswith='Who')`. Если изменить порядок - сначала ключевой аргумент, затем Q-объект то это будет невалидненько
https://docs.djangoproject.com/en/1.11/topics/db/queries/#complex-lookups-with-q
#### Примеры OR lookup
https://github.com/django/django/blob/master/tests/or_lookups/tests.py
### Func Expression
Func() это базовый класс от которого созданы такие функции как COALESCE (возвращает первое ненулевое значение), LOWER, SUM

Их можно использовать напрямую
```python
from django.db.models import Func, F

queryset.annotate(field_lower=Func(F('field'), function='LOWER'))
```

Так и для создания своих функций

```python
class Lower(Func):
    function = 'LOWER'

queryset.annotate(field_lower=Lower('field'))
```
https://docs.djangoproject.com/en/2.0/ref/models/expressions/#func-expressions
### Aggregate Expression
Аггрегация это специальный кейс `Func()` выражения которое информирует запрос о том что необходимо сделать `GROUP BY`. Все функции агрегации `Sum()`, `Count()` наследуются от класса `Aggregate()`

```python
from django.db.models import Count
Company.objects.annotate(managers_required=(Count('num_employees') / 4) + Count('num_managers'))
```

Пример создания собственной функции
```python
from django.db.models import Aggregate

def Count(Aggregate):
    function('Count')
    template = '%(function)s(%(distinct)s%(expressions)s)'

    def __init__(self, expression, distinct=False, **extra):
        super().__init__(expression, distinct='DISTINCT ' if distinct else '', output_field=IntegerField(), **extra)
```
https://docs.djangoproject.com/en/2.0/ref/models/expressions/#aggregate-expressions
### Raw-SQL Expression
Когда нельзя просто так взять и описать `WHERE` используй RawSQL
```python
from django.db.models.expressions import RawSQL
queryset.annotate(val=RawSQL("select col from sometable where othercol = %s", (someparam, )))
```
https://docs.djangoproject.com/en/2.0/ref/models/expressions/#raw-sql-expressions
### .extra()
.extra(select=None, where=None, params=None, tables=None, order_by=None, select_params=None)

Джанго предлагает хук для инъекции кода в сгенерированный кверисетом запрос

```python
qs.extra(select={'val': 'select col from sometable where othercol = %s'}, select_params=(comeparam, ))
# vs Equal
qs.annotate(val=RawSQL("select col from sometable where othercol = %s", (someparam, )))
```
Основной бенефит для использования RawSQL вместо extra в том что можно передать `output_field`, а downside в том что в этом кверисете зашит алиас к таблице, и в будущем джанго может изменить этот алиас.
- select
    ```python
    Blog.objects.extra(
    select={
        'entry_count': 'SELECT COUNT(*) FROM blog_entry WHERE blog_entry.blog_id = blog_blog.id'
        },
    )
    ```
- where/tables
    ```python
    Entry.objects.extra(where=["foo='a' OR bar = 'a'", "baz = 'a'"])
    ```
### .update()
.update(**kwargs)

Обновить поле и венуть количество строк которые были затронуты фильтром. Можно обновлять сколько угодно полей одновременно. Обновление запускается сразу же, единственное ограничение - нельзя обновлять поля связанных FK моделей. update можно вызвать на слайс кверисета или такой кверисте который более не может быть отфильтрован. update также помогает с race condition, просто передаем команду базе. и последнее, update работает на уровне базы данных, поэтому save() методы не запускаются, а также не вызывает pre_save и post_save сигналов

### .select_for_update()
.select_for_update(nowait=False, skip_locked=False, of=())

Запускает запрос к базе который заблокирует строки до конца транзакции, вызывая для поддерживаемых баз команду `SELECT ... FOR UPDATE`. Обычно если другая транзакция уже заблокировала нужные строки, этот запрос будет ждать пока лок не снимется. `nowait=True` и `skip_locked` взаимозаменяемые. не может работать с нулевыми FK отношениями

### .in_bulk()
in_bulk(id_list=None)
Берет список значений поля (id_list) и возвращает маппинг значения и инстанса объекта с таким значением
```python
Blog.objects.in_bulk([1, 2])  # {1: <Blog: Beatles Blog>, 2: <Blog: Cheddar Talk>}
```
### Models & Migrations
#### Наследование моделей Django
#### Model _meta API
- Field access API
    - get_field(field_name) возвращает инстанс поля. Скрытые поля нельзя получить по имени
    - get_fields(include_parents=True, include_hidden=Flase) возвращает кортеж полей ассоциированных с моделью
#### Model Meta Options
Options
- abstract
- app_label (если модель определена вне INSTALLED_APPS)
- db_table
- db_tablespace
- default_related_name (по дефолту `<model_name>_set`)
- get_latest_by
- managed (True, может ли джанго изменять таблицу, создавать миграции)
- ordering
- permissions
- default_permissions (add, change, delete)
- proxy
- unique_together ((driver, restaurant), )
- index_together
- verbose_name
- verbose_name_plural

Read-only Attributes
- label `polls.Question`
- label_lower
#### Proxy
Разделение модели от связанных методов
```python
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)

class MyPerson(Person):
    class Meta:
        proxy = True

    def do_something(self):
        pass
```
Или изменить порядок сортировки в модели
```python
class OrderedPerson(Person):
    class Meta:
        ordering = ["last_name"]
        proxy = True
```
Кроме того можно определить своего менеджера для прокси модели
```python
from django.db import models

class NewManager(models.Manager):
    pass

class MyPerson(Person):
    objects = NewManager()

    class Meta:
        proxy = True
```
### Повторно используемые приложения Django
### Упаковка приложений (Packaging your app)
### Обработка HTTP запросов (Handling HTTP requests)
### Обработка шаблонов (Templates)
### Class-based Views
### Миграции (Migrations)
### Кэширование в джанго (Django Cache Framework)
### Логирование в Джанго (Logging)

***
## ExtJS и JavaScript
### Layout для форм в ExtJS
### Этапы исполнения JavaScript
### Тег script - расположение
### Порядок парсинга HTML документа
Сверху вниз, когда встречает ресурс, загружает его. пока загружает другие ресурсы ждут очереди.
### Типы в JavaScript
- Number
- String
- Object (Null и Array это объект)
- Boolean
- Undefined
- Function

### Сравнение и приведение типов
- String(null), true + "test"
- Number("123"), +"123"
- Boolean(1), !!1
### Способы создания функций и виды функций
обычная и анонимная, самовыполняющаяся? можно заасайнить анонимную на переменную а можно с помощью ключевого слова `function`
### Контекст вызова и call / apply / bind
https://stackoverflow.com/questions/15455009/javascript-call-apply-vs-bind#15455043
Call/Apply выполняют функцию сразу в то время как bind возвращает функцию которая, позже вызванная будет иметь нужный контекст.

call/apply отличаются только аргументами которые принимают.
- `person.hello.call({name: "Jim Smith"}, "world")  //this, other args`
- `person.hello.apply(person, [1, 2, 3])`

***
### Работа с компонентами формы ExtJS в м3 (как написать обработчик формы на м3)
Компоненты это основная структурная единица ExtJS, компонент может содержать бесконечное число дочерних компонентов.

#### Ext.Component

Есть иерархия компонентов:
```
                              Ext.Viewport
                          /                  \
             Ext.tab.Panel                    Ext.form.Panel
            /      \                                /      \
Ext.panel.Panel  Ext.panel.Panel    Ext.form.field.Text  Ext.button.Button
```

#### Ext.form.Panel
Это компонент формы, можно указать лейаут

Типы полей:
+ CheckBox
+ ComboBox (выпадающий список)
+ Date
+ Display (только для чтения)
+ File
+ Hidden
+ HtmlEditor
+ Number
+ Radio
+ Text (текстовое поле)
+ TextArea (текстовый блок)
+ Time

#### Ext.grid.Panel
Один из основных компонентов для представления данных является grid. для грида данные должны лежать в сторе. есть разные типы сторов. колонки в гриде описываются через список объектов.

```python
columns: [{
    text: 'First Name',
    dataIndex: 'firstName',
    flex: 1
}, {
    text: 'Last Name',
    dataIndex: 'lastName',
    flex: 1
}, {
    text: 'Phone Number',
    dataIndex: 'phoneNumber',
    flex: 1
}]
```
__dataIndex__ подсказывает гриду, какое поле использовать в качестве названия колонки и связанных данных.

В гриде могут быть три основных типа данных:
+ Boolean
+ Number
+ Date

Кроме того, есть тип от которого наследуются эти типы:
+ Text

И, в грид можно добавить любой компонент или виджет.
+ Component
+ Widget

***
### Работа с документацией ExtJS (Где и как искать информацию по компонентам ExtJS)
https://docs.sencha.com/extjs/3.4.0/

***
### ExtLayout в ExtJS
Лейаут отвечает за размер и позиционирование каждого компонента в приложении.

Каждое приложение ExtJS состоит из компонентов, контейнер это специальный тип компонента который содежит другие компоненты.

Каждый контейнер имеет лейаут который отвечает за размер и расположение его дочерних компонентов.

Дефолтный лейаут для компонента это AutoLayout, типа div, не определяет никаких спецальных размеров и позиционирования. Обычно лейаут определяют именно для компонента контейнер а не для обычных компонентов.

#### basic layouts
+ absolute (абсолютно спозиционированный компонент)
+ accordion (компоненты в гармошке)
+ anchor (позиционирование компонентов относительно углов контейнера)
+ border (окно разделено на несколько компонентов жирной границей)
+ card (TabPanel) расположение компонентов в табах
+ card (Wizard) расположение компонентов в виде пошагового переключения
+ column (расположение компонентов в виде колонок)
+ fit (компонент полностью заполняет контейнер)
+ table (расположение компонентов с помощью html-таблицы)
+ vBox (компоненты расположены друг под другом вертикально)
+ hBox (компоненты расположены друг за другов горизонтально)

#### Пример использования в м3
```python
class ListWindow(BaseListWindow):
    def _do_layout(self):
        super(ListWindow, self)._do_layout()

        self.layout = 'hbox'
        self.layout_config = {'align': 'stretch'}

        self.items[:] = (
            self.grid__persons,
            self.grid__employees,
        )

        self.grid__persons.flex = 2
        self.grid__employees.flex = 3
```

+ [Гайд по лэйаутам](https://docs.sencha.com/extjs/6.2.0/guides/core_concepts/layouts.html)
+ [Online построение лейаута](http://docs.sencha.com/extjs/4.2.5/extjs-build/examples/layout-browser/layout-browser.html)

***
### Области видимости JS кода
Глобальные переменные, находятся в window, это самая глобальная из всех глобальных переменных. В strict mode переменные обозначенные вне блоков и функций не прикрепляются к window. Глобальные переменные перестают действовать когда закрывается вкладка или окно, но видны в окнах внутри окна в котором определены. локальные переменные объявленные в функциях. Параметры функции работают как локальные переменные в js. переменные внутри функуии могут называться как глобальные переменные и будут иметь приоритет. Однако если забыть потавить var пере переменной в функции она станет глобальной.

### Расположение и компановка исходников UI компонентов ExtJs и M3
- m3_ext/views.py
    workspace view для отображения рабочего стола на основе указанного шаблона (m3_workspace.html)
- m3_ext/context_processor.py
    DesktopProcessor добавляет в контекст каждого запроса элементы рабочего стола
- m3_ext/gears ?
- m3_ext/ui
    Основной контент пакета
    - containers
    - controls
    - fields
    - menus
    - misc
    - panels
    - windows
 -m3_ext/templates
    - m3_master.html
        - подключение статики
            - css классы ext-js
            - m3 css
            - lightbox css
            - базовый набор extjs js
            - css рабочего стола
            - js рабочего стола
            - m3-debug.js
            - m3-opt.js
    - m3_workspace.html (наследуется от m3_master) добавляет конфигурацию рабочего стола в виде JSON, верхнюю панель, блок виджетов, нижнюю панель и меню пуск
### Базовые классы ExtJS
- Ext.Container
- Ext.Panel
- Ext.Component
- Ext.Window
- Ext.form
- Ext.grid
- Ext.tree
### Взаимодействия компонентов UI в ExtJS с помощью событий. Обработчики событий.
### Обработчик форм в ExtJS
```javascript
// кеширование полей формы в 
var birthDate1 = Ext.getCmp('{{ component.birth_date1.client_id }}'),
	toEnrollDocNumber = Ext.getCmp('{{ component.to_enroll_doc_number.client_id }}');

// функция которая удаляет лишние пробелы
function trim_after_change(cmp, value) {
	cmp.setValue(Ext.util.Format.trim(value));
}

// просто обработчики которые на изменение поля запускаю функцию удаления пробелов
fromDeductDocNumber.on('change', trim_after_change);
toDeductDocNumber.on('change', trim_after_change);

// функция которая запускается пере отправкой формы на сервер
// если вернуть false запрос видимо не отправится
win.on('beforesubmit', function () {
    if (
        statusFld.getValue() != EXCHANGE_ACCEPTING_STATUS ||
        (confirm1Fld.checked && confirm2Fld.checked)
    ) {
        return true;
    }

    // Показ модального окна
    Ext.Msg.show({
        title: 'Внимание',
        msg: 'Перевод в статус "Согласование" невозможен, ' +
             'оба родителя должны согласовать обмен.',
        icon: Ext.Msg.WARNING,
        buttons: Ext.Msg.OK
    });

    return false;
});
```

Подключается шаблон в определении окна
```python
class ConfirmWindow(BaseEditWindow):
    def set_params(self, params):
        self.template_globals = 'ui-js/pupil-exchange-confirms-window.js'
```
***
## ООП и проектирование
Объе́ктно-ориенти́рованное программи́рование (ООП) — методология программирования, основанная на представлении программы в виде совокупности объектов, каждый из которых является экземпляром определенного класса, а классы образуют иерархию наследования.

Идеологически ООП — подход к программированию как к моделированию информационных объектов, решающий на новом уровне основную задачу структурного программирования: структурирование информации с точки зрения управляемости, что существенно улучшает управляемость самим процессом моделирования,
что в свою очередь особенно важно при реализации крупных проектов.

Управляемость для иерархических систем предполагает минимизацию избыточности данных (аналогичную нормализации) и их целостность, поэтому созданное удобно управляемым — будет и удобно пониматься.

Таким образом через тактическую задачу управляемости решается стратегическая задача — транслировать понимание задачи программистом в наиболее удобную для дальнейшего использования форму.

Основные принципы структурирования в случае ООП связаны с различными аспектами базового понимания предметной задачи, которое требуется для оптимального управления соответствующей моделью:
- __абстрагирование__ для выделения в моделируемом предмете важного для решения конкретной задачи по предмету, в конечном счете — контекстное понимание предмета, формализуемое в виде класса;
- __инкапсуляция__ для быстрой и безопасной организации собственно иерархической управляемости: чтобы было достаточно простой команды «что делать», без одновременного уточнения как именно делать, так как это уже другой уровень управления;
- __наследование__ для быстрой и безопасной организации родственных понятий: чтобы было достаточно на каждом иерархическом шаге учитывать только изменения, не дублируя все остальное, учтенное на предыдущих шагах;
- __полиморфизм__ для определения точки, в которой единое управление лучше распараллелить или наоборот — собрать воедино.

***
### Принципы ООП
#### Инкапсуляция
Означает скрытие деталей работы объекта путем ограничения доступа через accessor и mutator. __accessor__ это публичное проперти или метод класса который отдает информацию о самом классе __mutator__ это публичный метод который изменяет свойства объекта

#### Абстракция
Если кратко то общие свойства конкретных объектов выделенные в отдельный класс.

#### Наследование
Форма переиспользования кода с помощью классов. Наследник получает все методы и свойства родительского класса.

#### Полиморфизм
one name, many forms Означает что можно в настледнике перебить метод родителя путем создания метода с таким же названием и немного другой имплементацией.

#### Misc
+ __Open recursion__
Позволяет вызывать методы на самого себя используя специальное слово this или self. Эта переменная ассайнится в самом конце, чтобы один метод класса мог вызвать другой метод класса или сам себя.
+ __Composition__
Просто означает что классы могут быть связанны с другими классами, вызывать другие классы и т.д. Любой код можно разбить на классы с разными ответственностями, но все они составляют программу.

***
### Подробные примеры на SOLID

***
### Модификаторы доступа
Чем отличается `_protected` от `__private` в Python. `_protected` это аттрибут или метод, который создатель класса считает что перебивать в наследниках не стоит. По конвенции в питоне нет приватных сущностей, мы можем только указать другим разработчикам что сущность используется в класса для внутренних механизмов и ее лечше не трогать.

Есть еще такое свойство как коверканье (mangling) приватной сущности. Когда идентификатор который появляется в лассе имеет в имено два нижних подчеркивания с начала и не имеет два нижних подчеркивания в конце, считается что это приватная сущность данного класса. Такие приватные для класса сущности трансформируются перед генерацией кода в более длинные имена. Изменение добавляет к имени приватной сущности имя класса начинающееся с нижнего подчеркивания. К примеру аттрибут `__span` появляющийся в классе `Ham` будет приведен к виду `_Ham__spam`. Таким образом добивается создание неймспейсов для сущностей. У родительского класса любой `__private` идентификатор будет заменен (во время компиляции) на имя `_Parent__private`, а в его наследниках на `_Child__private`

https://stackoverflow.com/questions/20261517/inheritance-of-private-and-protected-methods-in-python

***
## Шаблоны проектирования

***
### Стратегия
> Позволяет выбирать алгоритм выполнения на лету

Обозначить семью алгоритмов, инкапсулировать каждый и сделать их взаимозаменяемыми. Стратегия позволяет алгоритму развиваться независимо от клиента.

```python
import types


class StrategyExample:

    def __init__(self, func=None):
        self.name = 'Strategy Example 0'
        if callable(func):
            # makes function a class metod
            self.execute = types.MethodType(func, self)

    def execute(self):
        print(self.name)


def execute_replacement1(self):
    print(self.name + ' from execute 1')


def execute_replacement2(self):
    print(self.name + ' from execute 2')


strat0 = StrategyExample()

strat1 = StrategyExample(execute_replacement1)
strat1.name = 'Strategy Example 1'

strat2 = StrategyExample(execute_replacement2)
strat2.name = 'Strategy Example 2'

strat0.execute()
strat1.execute()
strat2.execute()
```

***
### Шаблонный метод
> Обозначает структуру алгоритма, оставляя имплементацию шагов наследникам.

Шаблонный метод позволяет наследникам изменять некоторые шаги алгоритма без изменения структуры самого алгоритма.

```python
import abc


class AbstractClass(metaclass=abc.ABCMeta):
    """
    Define abstract primitive operations that concrete subclasses define
    to implement steps of an algorithm.
    Implement a template method defining the skeleton of an algorithm.
    The template method calls primitive operations as well as operations
    defined in AbstractClass or those of other objects.
    """
    def template_method(self):
        self._primitive_operation_1()
        self._primitive_operation_2()

    @abc.abstractmethod
    def _primitive_operation_1(self):
        pass

    @abc.abstractmethod
    def _primitive_operation_2(self):
        pass


class ConcreteClass(AbstractClass):
    """
    Implement the primitive operations to carry out
    subclass-specificsteps of the algorithm.
    """
    def _primitive_operation_1(self):
        pass

    def _primitive_operation_2(self):
        pass


concrete_class = ConcreteClass()
concrete_class.template_method()
```

***
### Фабрика
> Позволяет создавать объекты без обращения к определенным классам.

```python
import random


class PetShop(object):
    def __init__(self, animal_factory=None):
        self.pet_factory = animal_factory

    def show_pet(self):
        pet = self.pet_factory()
        print("We have a lovely {}".format(pet))


class Dog(object):
    def speak(self):
        return "woof"


class Cat(object):
    def speak(self):
        return "meow"


# Additional factories:
def random_animal():
    return random.choice([Dog, Cat])()


cat_shop = PetShop(Cat)
cat_shop.show_pet()

# A shop that sells random animals
shop = PetShop(random_animal)
```

***
### Одиночка
> Этот паттерн используется когда нам нужно гарантировать что только один инстанс класса существует во время работы программы. Может быть заменен dependency injection.

Удостовериться что у класса есть только один инстанс и дать единую точку доступа к нему. Инкапсулировать инициализацию при первом использовании.

Пример с использованием `__new__`
```python
class Logger(object):
    def __new__(cls, *args, **kwargs):
        if not hasattr(cls, '_logger'):
            cls._logger = super(Logger, cls).__new__(cls, *args, **kwargs)
        return cls._logger
```

Пример с использованием метаклассов
```python
class Singleton(type):
    """
    Define an Instance operation that lets clients access its unique
    instance.
    """

    def __init__(cls, name, bases, attrs, **kwargs):
        super().__init__(name, bases, attrs)
        cls._instance = None

    def __call__(cls, *args, **kwargs):
        if cls._instance is None:
            cls._instance = super().__call__(*args, **kwargs)
        return cls._instance


class MyClass(object):
    __metaclass__ = Singleton
```

***
### Подписчик
> Поддерживает список зависимых объектов и уведомляет их о любом изменении состояния.

Определить одну-ко-многим зависмость между объектами, чтобы при изменении состояния одного из объектов все его зависимости были уведомлены автоматически.

```python
import abc


class Subject:
    """
    Know its observers. Any number of Observer objects may observe a subject.
    Send a notification to its observers when its state changes.
    """
    def __init__(self):
        self._observers = set()
        self._subject_state = None

    def attach(self, observer):
        observer._subject = self
        self._observers.add(observer)

    def detach(self, observer):
        observer._subject = None
        self._observers.discard(observer)

    def _notify(self):
        for observer in self._observers:
            observer.update(self._subject_state)

    @property
    def subject_state(self):
        return self._subject_state

    @subject_state.setter
    def subject_state(self, arg):
        self._subject_state = arg
        self._notify()


class Observer(metaclass=abc.ABCMeta):
    """Define an updating interface for objects that should be notified of changes in a subject."""
    def __init__(self):
        self._subject = None
        self._observer_state = None

    @abc.abstractmethod
    def update(self, arg):
        pass


class ConcreteObserver(Observer):
    """
    Implement the Observer updating interface to keep its state consistent with the subject's.
    Store state that should stay consistent with the subject's.
    """
    def update(self, arg):
        self._observer_state = arg
        # ...

subject = Subject()
concrete_observer = ConcreteObserver()
subject.attach(concrete_observer)
subject.subject_state = 123
```

***
### Адаптер
> Позволяет интерфейсу существующего класса быть использованным как другой интерфейс.

Фасад используется для упрощения интерфейса, в то время как Адаптер говорит об изменении интерфейса. Как использовать корову когда система ожидает утку.

```python
import socket

def log(message, destination):
    destination.write('[{}] - {}'.format(datetime.now(), message))


# У сокета нет метода write() поэтому его
# нельзя использовать с функцией log
class SocketWriter(object):

    def __init__(self, ip, port):
        self._socket = socket.socket(socket.AF_INET,
                                     socket.SOCK_DGRAM)
        self._ip = ip
        self._port = port

    def write(self, message):
        self._socket.send(message, (self._ip, self._port))

def log(message, destination):
    destination.write('[{}] - {}'.format(datetime.now(), message))

upd_logger = SocketWriter('1.2.3.4', '9999')
log('Something happened', udp_destination)
```

***
## Алгоритмические основы
Алгоритм — это точное предписание, однозначно определяющее вычислительный процесс, ведущий от варьируемых начальных данных к искомому результату

### Подсчет сложности алгоритма

### Понятие сложности алгоритма (смысловое определение)
Оцениваемым ресурсом чаще всего является процессорное время (вычислительная сложность) и память (сложность алгоритма по памяти). Оценка позволяет предсказать время выполнения и сравнивать эффективность алгоритмов.

### Типовые сложности алгоритмов (привести пример алгоритма на питоне для каждого случая)

#### O(n) — линейная сложность
Такой сложностью обладает, например, алгоритм поиска наибольшего элемента в не отсортированном массиве. Нам придётся пройтись по всем n элементам массива, чтобы понять, какой из них максимальный.

```python
def sequential_search(container, element):
    for el in container:
        if el == element:
            return True
    return False

squential_search([1, 2, 3], 1)
```

```
начало; поиск минимального элемента массива array из N элементов
min := array[1]
для i от 2 до N выполнять:
    если array[i] < min
    min := array[i]
конец; вернуть min
```

#### O(log n) — логарифмическая сложность
Простейший пример — бинарный поиск. Если массив отсортирован, мы можем проверить, есть ли в нём какое-то конкретное значение, методом деления пополам. Проверим средний элемент, если он больше искомого, то отбросим вторую половину массива — там его точно нет. Если же меньше, то наоборот — отбросим начальную половину. И так будем продолжать делить пополам, в итоге проверим log n элементов.

```python
def binary_search(sorted_collection, item):
    low = 0
    hight = len(sorted_collection) - 1

    while low <= hight:
        midpoint = (low + hight) // 2
        current_item = sorted_collection[midpoint]
        if current_item == item:
            return midpoint
        else:
            if item < current_item:
                hight = midpoint - 1
            else:
                low = midpoint + 1
    return None

binary_search([0, 5, 7, 10, 15], 6)
```

```
начало; поиск элемента E в отсортированном по возрастанию массиве array из N элементов
left := 1, right := N; левая и правая граница, в которых находится искомый элемент
выполнять пока left =< right:
    mid := (right + left) div 2; вычисление индекса элемента посередине рассматриваемой части массива
    если array[mid] = E
    конец; вернуть true (элемент найден)
    если array[mid] < E; искомый элемент больше середины, значит все элементы левее mid можно отбросить
    left := mid + 1;
    иначе
    right := mid
конец; вернуть false (элемент не найден)
```

#### O(n<sup>2</sup>) — квадратичная сложность
Такую сложность имеет, например, алгоритм сортировки вставками. В канонической реализации он представляет из себя два вложенных цикла: один, чтобы проходить по всему массиву, а второй, чтобы находить место очередному элементу в уже отсортированной части. Таким образом, количество операций будет зависеть от размера массива как n * n, т. е. n2.

```python
def bubble_sort(collection):
    length = len(collection)
    for _ in range(length):
        for i in range(length - 1):
            if collection[i] > collection[i + 1]:
                collection[i], collection[i + 1] = collection[i + 1], collection[i]
    return collection

bubble_sort([-2, -5, -45])
```

```
начало; пузырьковая сортировка массива array из N элементов
nPairs := N; количество пар элементов
hasSwapped := false; пока что ни одна пара не нарушила порядок
для всех i от 1 до nPairs-1 выполнять:
    если array[i] > array[i+1] то:
    swap(array[i], array[i+1]); обменять элементы местами
    hasSwapped := true; найдена перестановка
    nPairs := nPairs - 1; наибольший элемент гарантированно помещен в конец
    если hasSwapped = true - то перейти на п.3
    конец; массив array отсортирован
```

### Сравнение алгоритмов по сложности

Algorithm      | TC Best     | TC Average     | TC Worst       | Space Complexity Worst |
-------------- | :---------: | :------------: | :------------: | :--------------------: |
Quicksort      | Ω(n log(n)) | Θ(n log(n))    | O(n^2)         | O(log(n))              |
Mergesort      | Ω(n log(n)) | Θ(n log(n))    | O(n log(n))    | O(n)                   |
Timsort        | Ω(n)        | Θ(n log(n))    | O(n log(n))    | O(n)                   |
Heapsort       | Ω(n log(n)) | Θ(n log(n))    | O(n log(n))    | O(1)                   |
Bubble Sort    | Ω(n)        | Θ(n^2)         | O(n^2)         | O(1)                   |
Insertion Sort | Ω(n)        | Θ(n^2)         | O(n^2)         | O(1)                   |
Selection Sort | Ω(n^2)      | Θ(n^2)         | O(n^2)         | O(1)                   |
Tree Sort      | Ω(n log(n)) | Θ(n log(n))    | O(n^2)         | O(n)                   |
Shell Sort     | Ω(n log(n)) | Θ(n(log(n))^2) | O(n(log(n))^2) | O(1)                   |
Bucket Sort    | Ω(n+k)      | Θ(n+k)         | O(n^2)         | O(n)                   |
Radix Sort     | Ω(nk)       | Θ(nk)          | O(nk)          | O(n+k)                 |
Counting Sort  | Ω(n+k)      | Θ(n+k)         | O(n+k)         | O(k)                   |
Cubesort       | Ω(n)        | Θ(n log(n))    | O(n log(n))    | O(n)                   |

http://bigocheatsheet.com/

### Сложение / Умножение сложности алгоритма

***
## M3
http://m3.bars-open.ru/stories/modules.html
***
### Из каких пакетов состоит М3 - состав и назначение пакетов
- __m3-core__ (базовый модуль m3)
    + инструменты для работы с экшенами: Action
    + инструменты для работы с паками: Pack
    + механизм автоматической сборки урлов: ActionController и ActionControllerCache
    + инструмент для декларации контекста для экшенов: ACD
    + cтандартные классы для http-ответов: ActionResult, PreJsonResult, etc.
- __m3-ext__ (серверные и клиентские UI-компоненты)
    + серверные обертки над ExtJS и своими компонентами для работы с ними в python
    + свои js-компоненты: выбор из справочника, livegrid, плагин для заморозки строк в таблице и одновременной группировки
    + базовая view для приложений: desktop_processor
    + актуальную версию библиотекиы ExtJS
- __m3-legacy__ (устаревший (deprecated) функционал)
- __m3-objectpack__ (расширяет возможности m3-core и m3-ext и позволяет экстремально быстро разрабатывать справочники для различных учётных систем.)
- __m3-users__ (инструменты для работы с пользователями, ролями и правами пользователей)
- __simple-report__ (позволяет разработчику составлять отчеты таких форматов как docx, doc, rtf; xlsx, xls.)
- __m3-audit__ (реализует журналирование действий)

***
### Как создать и запустить проект на м3 с нуля
- __m3-blank__ пустой проект с м3
- __m3-objectpack-demo__ лучшие практики

***
### URL dispatcher - обработка запросов
```python
def get_app_urlpatterns():
    '''
    Возвращает конфигурацию урлов, объявленных в app_meta приложений.

    Данная функция не проглатывает ошибки, а выбрасывает все наружу.
    Перехват исключительных ситуаций данной фунции необходимо осуществлять
    вручную в urls.py прикладных приложений
    '''
    url_patterns = []

    for app_name in settings.INSTALLED_APPS:
        try:
            module = import_module('.app_meta', app_name)
        except ImportError, err:
            # по идее, такая ошибка возникает в случае, если у нас для
            # установленного приложения нет модуля app_meta.py
            if err.args[0].find('No module named') == -1:
                raise
            continue
        proc = getattr(module, 'register_urlpatterns', None)
        if callable(proc):
            url_patterns += proc()

    return url_patterns
```
### Работа с контекстом, устройство контроллера
Связующим звеном между деревом экшенов и вьюшкой котроллера, является класс ActionController. Он хранит экшенпаки и отвечает за обработку запросов. Как правило контроллер бывает один на приложение.

Самый первый запрос к вьюшке контроллера вызывает метод populate() в ControllerCache. Этот класс отвечает за хранение глобального списка контроллеров и начальную инициализацию дерева экшенов.

После первичного формирования дерева экшенов и контроллеров, запрос отправляется к конкретному котроллеру приложения. Получив сырой запрос, он разбирает его и проходит по дереву экшенов в поисках нужного. Если не находит, то генерирует исключение 404. Если находит то выполняет все встретившиеся на пути, от корня до экшена, методы pre_run(). Выполнив экшен, в обратном порядке выполняются все методы post_run(). Причем если хоть один из них вернул результат отличный от None, обработка прерывается и результат уходит наружу, во вьюшку контроллера.

#### Класс ActionController и его использование

Определение контроллера состоит из нескольких этапов:

1. Экземпляр контроллера как правило создается в файле app_meta.py внутри приложения.
2. Чтобы передавать в него запросы Django нужно создать вьюшку контроллера dict_view и зарегистрировать url pattern для неё в методе register_urlpatterns. Он вызывается автоматически для всех приложений.
3. Регистрация паков в контроллере производится методом register_actions.

Пример файла app_meta.py внутри приложения dicts:

```python
# Именованный экземпляр контроллера
dict_controller = ActionController(url='/core-dicts', name=u'Справочники')

def register_urlpatterns():
    """ Регистрация вьюшки контроллера """
    return urls.defaults.patterns('',
            (r'^core-dicts/', 'mis.core.dicts.app_meta.dict_view'),
        )

def dict_view(request):
    """ Вьюшка контроллера """
    return dict_controller.process_request(request)

def register_actions():
    """ Регистрация паков в контроллере """
    dict_controller.packs.extend([
        MyFormActionPack,
        MyDictionaryActions
    ])
```

При добавлении пака в контроллер вызывается метод `_build_pack_node`, который создает экземпляр пака и всех вложенных в него экшенов и паков. Заполняются служебные атрибуты, с помощью которых можно обходить дерево:

- parent - ссылка на родительский пак
- controller - ссылка на родительский контроллер

Чаще всего бывает нужно найти экшен или пак в уже сформированной иерархии. Для этого есть несколько методов:

- По известному адресу экшен можно найти методом get_action_by_url
- Пак по имени или классу можно найти методом find_pack
- Рекомендуется искать экшены и паки по короткому имени (псевдониму). Для него есть атрибут `short_name`.

Пример:
```python
from m3.helpers import urls

my_action = urls.get_action('my-action-alias')
my_pack = urls.get_pack('my-pack-alias')
```
#### Контекст запросов в М3 (m3.actions.context)¶

В Django параметры запросов передаются с помощью класса `HttpRequest` в трех словарях POST, GET и REQUEST. Извлекаемые из них значения не проверяются и не конвертируются в сложные типы Python. Ещё один минус, что извлечение, как правило, делают внутри кода вьюшки, таким образом загромождается место под бизнес логику.

В М3 был разработан механизм контекста, который позволяет:

- Автоматически извлекать значения из запроса по заранее заданным правилам.
- Преобразовывать сырое значение в указанный в правилах тип.
- Передавать контекст в ответе к визуальным компонентам.

#### Определение контекста в экшенах

Правила извлечения контекста задаются внутри метода `context_declaration` экшена. Представляют собой список экземпляров класса `ActionContextDeclaration` или его упрощенное написание `ACD`. Так же можно использовать декларативное описание по определенной схеме.

Пример определения правил:

```python
from m3.actions.context import ActionContextDeclaration, ACD

class GetRowsAction(Action):
    def context_declaration(self):
            return [
                ActionContextDeclaration(name='id', type=int, required=True, verbose_name=u'Идентификатор модели'),
                ActionContextDeclaration(name='start', type=int, required=True),
                ActionContextDeclaration(name='limit', type=int, required=True)
            ]
        ...

class GetRowsAction(Action):
    url = 'save'

    def context_declaration(self):
        # декларативное опимание контекста
        return {
            # параметр запроса -> параметры разбора
            'ids': {
                # значение по умолчанию,
                # используется при отсутствии параметра в запросе
                # если не указано - параметр считается обязательным
                'default': '',

                # тип парсера, может быть:
                # - строкой - именем одного из предопределенных парсеров
                # - callable-объектом, выполняющим парсинг. Такой объект
                #   может возбуждать ValueError/TypeError/KeyError/IndexError
                #   в случае неправильного формата данных, что позволяет
                #   использовать в качестве парсера что-то вроде:
                #     'type': ['on', 'yes'].__contains__
                #     'type': {1: 'Male', 2: 'Female'}.get
                #     'type': float
                #     'type': json.loads
                'type': int

                # наименование параметра, понятное пользователю
                # используется в сообщениях об ошибках
                'verbose_name': u'Идентификатор объекта'
            },
            #
            'date': {
                'type': datetime.date,
                'verbose_name': u'Дата начала действия изменений'
            },
            'comment': {
                'type': str
            }
        }

    @transaction.commit_on_success
    def run(self, request, context):
        if not hasattr(context, 'comment'):
            context.comment = u'Без комментариев'

        for id in context.ids:
            SomeModel.objects.create(pid=id, comment=context.comment)

        msg = u'Изменения внесены на дату %s' % context.date
        return OperationResult(message=msg)
```
Разберем правило:
```python
ACD(name='date', required=True, type=datetime.date, verbose_name=u'Дата начала действия изменений')
```
Из словаря REQUEST запроса `HttpRequest` будет извлечено значение с именем “date” и приведено к типу datetime.date. Если его нет в REQUEST, то до run() управление не дойдет и будет сгенерировано исключение `RequiredFailed`.

Разберем правило:
```python
ACD(name='comment', type=str)
```
Из словаря REQUEST запроса `HttpRequest` будет извлечено значение с именем “comment”. Если его нет в REQUEST, то соответствующий атрибут не будет добавлен в context, т.к. `required=False` по умолчанию. Управление будет передано в run().

### Обертки UI компонентов ExtJS и их рендер
### Распределение кода приложения по модулям
Приложения проекта должны придерживаться следующей структуры.
- services - модуль либо пакет; содержит сервисы, реализующие бизнес логику проекта.
- ui - модуль либо пакет; содержит классы графического интерфейса.
- actions - модуль либо пакет; содержит Action-ы и ActionPack-и.
- webservices - модуль либо пакет; содержит SOAP-сервисы.
- settings - модуль либо пакет; содержит настройки данного приложения; опционален.
- tasks - модуль либо пакет; содержит описание фоновых задач.
- reports- модуль либо пакет; содержит отчеты.
- models - модуль; содержит модели отображаемые на БД. Простые операции бизнес-уровня содержатся прямо в методах моделей и не содержат управления транзакциями.
- signals - модуль либо пакет; содердит экземпляры сигналов.
- receivers - модуль либо пакет; содержит обработчики сигналов.
- app_meta - модуль; описывает m3-приложение.
### Action/ActionPack - назначение, устройство
#### Класс Action и его использование

Пример экшена, который читает даннные из POST’а. Проверяет значение C и сохраняет в БД значения A и B. Код:
```python
from m3.ui.actions import Action
from m3.ui.actions.results import OperationResult
...

class MyFirstAction(Action):
    url = 'save'
    verbose_name = u'Сохранение данных'
    short_name = 'my-first-action-alias'

    def pre_run(self, request, context):
        """ pre_run удобно использовать для начальных проверок """
        value = request.POST.get('C')
        if value < 0:
            # Обработка запроса на этом прерывается
            return OperationResult(success=False, message=u'Недопустимое значение')

    def run(self, request, context):
        """ Основная работа экшена производится здесь """
        a = request.POST.get('A')
        b = request.POST.get('B')
        SomeModel.objects.create(a=a, b=b)
        return OperationResult(message=u'Данные сохранены')
```
`OperationResult` это один из возможных результатов работы экшена, который автоматически преобразуется в Django `HttpResponse` внутри контроллера. В нашем случае класс `OperationResult` указывает успешно ли завершилась операция `success` и несет соответствующее сообщение `message`.

#### Класс ActionPack и его использование

Экшены и паки входящие внутрь нашего пака задаются с помощью атрибутов actions и subpacks. Пример:
```python
from m3.ui.actions import ActionPack

class MyFormActionPack(ActionPack):
    def __init__(self):
        super(MyFormActionPack, self).__init__()
        self.actions.extend([
            GetWindowAction, GetDataAction(), SaveAction, DeleteAction()
        ])
        self.subpacks.append( InnerActionPack )

class InnerActionPack(ActionPack):
    url = 'inner'
    def __init__(self):
        super(InnerActionPack, self).__init__()
        self.actions.extend([
            SubAction1, SubAction2, ...
        ])
```
Обратите внимание, что в список `actions` можно добавлять как классы, так и экземпляры экшенов. На самом деле это не имеет значения, т.к. контроллер при инициализации автоматически создает экземпляры экшенов и паков, а также дополняет их специальными атрибутами.

Часто бывает необходимо получить прямой доступ к экшенам внутри пака через атрибуты. Живой пример из М3:
```python
class BaseDictionaryActions(ActionPack):
    def __init__(self):
        super(BaseDictionaryActions, self).__init__()
        self.list_window_action   = DictListWindowAction()
        self.select_window_action = DictSelectWindowAction()
        self.edit_window_action   = DictEditWindowAction()
        ...
        self.actions = [
            self.list_window_action,
            self.select_window_action,
            self.edit_window_action,
            ...
        ]
```
### ObjectPack/RecordPack - назначение, устройство
http://objectpack.readthedocs.io/ru/latest/tutorial.html#objectpack
### Виртуальные модели
### Знание состава компонентов общей кодовой базы educommon
- async реестр асинхронные задачи
- audit_log очередная подсистема логирования
- auth
- contingent
- django
    - models
        - BaseModel Базовый класс для всех моделей системы
    - observer
        - ModelObserver Базовый класс для наблюдателей за моделями
    - routers
        - ServiceDbRouterBase Основа роутера для моделей приложений, использующих сервисную БД
- extjs
    - fields
        - input params Параметры фильтрации ввода для различного типа полей ИНН, СНИЛС
- importer Некий загрузчик чего-то
- m3
    - extension
        - ui
            - BaseEditWinExtender Базовый объект для расширения обон редактирования
        - listeners
            - DeleteCheck Проверяет объекты перед удалением на наличие зависимостей
- objectpack
    - actions
        - BaseGridPack Пак умеющий строить динамический грид с изменяющимся количеством колонок в зависимости от значений полей фильтрации.
        - ViewWindowPackMixin Добавляет кнопку просмотра в ListWindow, запрещает редактирование
    - ui
        - GridPanel Панель имеющая grid_url по которому получает грид и вставляет в себя
        - BaseGridWindow Базовое окно с фильтрующей панелью и панелью с гридом
        - BaseListWindow Окно с гридом с возможностью просмотра в режиме read_only
        - BaseEditWindow
        - ModelEditWindow
- report Шаблон для построения отчетной системы
- secure_media Пакет для проверки авторизации пользователя перед доступом к /media/
- utils
- ws_log очередной журнал изменений
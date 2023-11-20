# Домашнее задание к занятию "`Базы данных, их типы`" - `Воронин Алексей`



------


### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы? 

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это 
реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД 
логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

*Приведите ответ в свободной форме.*

---

### Решение 1

1.1 Реляционная СУБД (PostgreSQL или MySQL)

1.2 Для лендингов - MongoDB, для CRM - можно использовать реляционную СУБД (PostgreSQL)

1.3 Подходит реляционная СУБД (SQLite - малый обьём СУБД, PostgreSQL большой обьём)

1.4 Для эффективной работы с данными логистики подойдет графовая СУБД

1.5.* PostgreSQL так как имеет большой вункионал

---
### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

*Приведите ответ в свободной форме.*

---

### Решение 2

2.1

- Аунтификация (проверка прав на данное действие)

- Проверка счёта (откуда списываются средства){на наличее средст/блокировок}

- Проверка счёта (куда зачисляются средства){на блокировку/существование}

- Заморозка средств на счёте списания

- Списание средст 

- Зачисление средст 


2.1.*

- всё тоже самое

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

*Приведите ответ в свободной форме.*

---

### Решение 3

3.1

- Структурированные данные

- Язык запросов

- Транзакции и целостность


---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* 
здесь справится лучше всего и почему?

*Приведите ответ в свободной форме.*

---

### Решение 4

Критерии выбора СУБД:
 - Масштабируемость, производительность, целосность данных, распределенные возможности.

Модель: 
 - Модель СУБД для работы с большими данными BDMS (Big Data Management System)  - которые может обрабатывать большие объемы данных, маштабируемость и поддержку распределенной обработки.(пример Apache Hadoop, Amazon EMR, Google BigQuery)
  

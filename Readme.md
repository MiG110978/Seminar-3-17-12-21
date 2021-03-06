# Инструкция по работе Git

## Что такое Git

Git - одна из реализаций систем контроля версий, имеющая как локальную версионность, так и версионность на сервере. Git является самой популярной системой контроля версий на сегодняшний день.

## Подготовка репозитория

Для того, чтобы создать репозиторий в указанной папке используется команда *git init*. Для этого достаточно написать команду *git init* в папке с будущим репозиторием. 

В результате в существующей папке появится еще одна папка с именем .git и всеми нужными вам файлами репозитория — это будет основа вашего Git-репозитория.

## Cоздание фиксаций

### Просмотр информации об изменениях

Для того, чтобы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду *git status*. Для этого достаточно использовать *git status* в папке с репозиторием.

### Добавление файла к комиту

Для того, чтобы добавить файл к новому комиту ("сохранению") необходимо использоватькоманду *git add*. Используется она следующим образом: в папке с репозиторием пишем команду *git add <имя файла>*.

### Создание коммитов

Для создания новой фиксации необходимо использовать команду *git commit*. Используется она следующим образом: в папке с репозиторием пишется команда *git commit -m "<сообщение к коммиту>"*. Все файлы коммита должны быть предварительно добавлены с помощью команды *git add*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между коммитами

### Просмотр истории коммитов

После того, как вы создали несколько коммитов вам понадобится возможность посмотреть что было сделано - историю коммитов. Для этого используется команда *git log*.

Git log перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке — последние коммиты находятся вверху. Данная команда перечисляет коммиты с их контрольными суммами, именем и электронной почтой автора, датой создания и сообщением коммита. 

### Переход к интересующему коммиту

Если у нас возникло желание увидеть как выглядел файл в одном из предыдущих состояний (коммитов), то необходимо использовать команду *git checkout <контрольная сумма>*. Контрольную сумму интересующего коммита можно узнать из результата выполнения команды *git log*.

### Версия Преподавателя  
для перемещения между коммитами необходимо использовать команду *git checkout*.

## Ветки в Git 

### Ветка - 
это понятие, означающее запуск отдельной линии разработки в проекте. Ветка позволяет вести одновременную разработку в нескольких направлениях, не затрагивающих друг друга. Часто выполняется 
слияние одних веток с другими для воссоединения несоизмеримых усилий. 
Git позволяет просмтаривать, сливать, удалять ветки.

### Для создания новой ветки
используется команда *git branch <имя ветки>*.  
Чтобы увидеть все существующие ветки введите *git branch*. После исполнения этой команды отобразится список всех существующих веток, при этом текущая ветка (в которую будут записываться изменения) будет отмечена звездочкой(*).

### Для перемещения в требуемую ветку 
используется команда *git checkout <имя ветки>*.

### Слияние веток
После того, как работа в отдельном направлении (ветке) закончена, все изменения можно перенести в основное "русло" - произвести слияние с основной (требуемой) веткой.   
Для этого необходимо сначало перейти в ту ветку, в которую будут "вливаться" изменения - *git checkout <имя ветки>*.  
После этого используется команда *git merge <имя ветки>* - где *имя ветки* указывает на ту ветвь, информацию из которой необходимо добавить к текущей ветке.

### Удаление веток
После слияния необходимость вспомогательных веток может пропасть. В этом случае для упрощения дальнейшей работы ненужные ветки можно удалить - *git branch -d <имя ветки>*. Как вы догадались, *имя ветки* в этой команде указывает на удаляемое ответвление.

## Журнал изменений

Мы уже познакомились с командой отобажения истории коммитов *git log*.  
Если к этой команде добавить параметр *-graph* (*git log -graph*), то к обычному списку коммитов добавиться графическое отображение связей между ними, что особенно удобно при ветвлении.

### Версия преподавателя

Для просмотра журнала изменений необходимо использовать команду *git log*. Для этого необходимо в папке с репозиторием написать *git log*.
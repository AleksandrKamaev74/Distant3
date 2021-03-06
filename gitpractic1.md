# Что такое система контроля версий?

**Cистема контроля версий** – это система, записывающая изменения
в файл или набор файлов в течение времени и позволяющая вернуться позже к определенной версии.

# Зачем нужен контроль версий?

Проект для команды - это бесценные знания, накопленные за все время его существования, и никому бы не хотелось, чтобы с ними что-то случилось. Система контроля версий защищает эти накопления от человеческого фактора, непредвиденных последствий и разных форс-мажоров.
Работая в команде, каждый разработчик трудится над какой-то своей частью проекта: создает новые функции, оптимизирует уже существующие, исправляет ошибки в уже написанном коде. Сам проект обычно организован в виде дерева файлов. Контроль версий помогает сотрудникам одновременно работать над проектом, отслеживать, кто какие изменения внес, и избегать при этом различных конфликтов (например, когда два человека изменят один и тот же файл по-разному).
Помимо этого любое изменение кода может привести к непредвиденным последствиям и сломать весь проект вообще. Система контроля версий защищает и от этого.

# Система контроля версий *Git*

В самом простом виде контроль версий — это сохранение на компьютере серии измененных файлов, например с разными датами в названии, или режим отслеживания исправлений в текстовых документах.
Разработчикам часто бывает нужно вернуться к предыдущей версии кода:
если оказывается, что решаемая задача больше не актуальна;
если требуется внести исправления в более раннюю версию программы;
если ошибка нашлась во время работы над новой задачей.
Если над проектом работает много людей, нужно, чтобы они могли вносить изменения в одни и те же файлы без конфликтов и потерь кода. Все эти задачи удобно решаются с помощью Git.
**К базовым возможностям Git относятся:**

*возврат к любой предыдущей версии кода;*

*просмотр истории изменений;*

*параллельная работа над проектом.*

# Настройка Git

Git — самая популярная распределённая система контроля версиями,которая позволяет отслеживать и фиксировать изменения в коде: вы можете восстановить код в случае сбоя или откатить до более ранних версий.
1. Нужно скачать Git на компьютер.
   Для этого жмем на ссылку [id]:<https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git>,скачиваем exe файл и запустим его.

2. Скачать и установить VSC [id]:<https://code.visualstudio.com/>

3. После установки необходимо  ввести в терминале команды:
   git config --global user.name «Ваше имя англ буквами»
   
   git config --global user.email ваша_почта@example.com.

# Основные понятия

1. **Репозиторий** – папка проекта, отслеживаемого Git,с наличием дерева изменений проекта в хронологическом порядке. Все файлы истории находятся в особой папке .git/ внутри папки проекта.

2. **Индекс или область подготовленных файлов**-файлы ,в которых произошли изменения, подготовленные для добавления в коммит.Вы можете включить и выбрать файлы из индекса.

3.**Коммит**–фиксация изменений, внесенных в индекс. Другими словами,коммит – это единица изменений в предстоящем проекте. Коммит хранит измененные файлы, имя автора коммита и время, в которое был сделан коммит. Кроме того, каждый коммит имеет применение идентификатора, который позволяет в любое время к нему не катиться.

4. **Ветка** – это последовательность коммитов. С технической точки зрения ветка — это указатель или ссылка на последний коммит в этой ветке. По умолчанию, имя основной ветки в Git — master. Каждый раз, когда создается новый коммит, указатель ветки master автоматически передвигается на него.

# Создание репозитория.Команда *git init*

**git** пробел **init**-создает новый репозиторий.Команда **git** пробел **init** создает пустой репозиторий в виде скрытой папки.**git**, где и будет в дальнейшем храниться вся информация об истории коммитов.

# Состояние файлов в Git репозитории.Команда *git status*

**git** пробел **status** – отображает список измененных, добавленных и удаленных файлов

# Делаем файлы отслеживаемыми.Команда *git add*

Чтобы сделать файл отслеживаемым, существует команда **git** пробел **add**
Команда **git** пробел **add** позволяет внести в индекс (временное хранилище)  изменения, которые затем войдут в коммит.
Пример: **git** пробел **add** <название файла.расширение>(например, **git** пробел **add** пробел **markdown.md**,где md-расширение файла)  

# Команда *git commit*.Сохранение изменений

Команда **git** пробел **commit** – фиксирует добавленные в индекс изменения.
Например,**git** пробел **commit** пробел-**m “Текстовое сообщение фиксации”**

# Просмотр изменений.Команды *git log и git diff*

**git** пробел **log**-используется для просмотра истории коммитов, начиная с самого свежего и уходя к истокам проекта. По умолчанию, она показывает лишь историю текущей ветки.
**git** пробел **diff**- по умолчанию выводит все неподтвержденные изменения, внесенные после последнего коммита.

# Ветвление в Git

1.создание,преключение и удаление веток;

2.cлияние изменений в Git.

1. создание,переключение и удаление веток;

Создать ветку можно командой **git** пробел **branch**;
**git** пробел **branch** **<название новой ветки>.**
Если потребуется переключиться с одной ветки на другую, вызовем команду **git** пробел  **checkout <имя ветки>**.
Если ветка  больше не нужна, ее можно удалить следующей командой:**git** пробел **branch** пробел **-d <имя ветки,которую хотим удалить>**.

2. cлияние изменений в Git.

Чтобы слить любую ветку с текущей, вызываем **git** пробел **merge <имя ветки для слияния с текущей>**

# Добавление удаленного репозитория к существующему локальному. 
# Команда git remote add.

**git remote add** <*название удаленного репозитория*> <*ссылка на удаленный репозиторий*>. Эта команда устанавливает подключение к удаленному серверу и git репозиторию на нем.

# Отправка изменений в удаленный репозиторий. Команда git push.

**git push** <*имя удаленного репозитория*> <*имя ветки*>

Позволяет отправить свою версию репозитория во внешний репозиторий.
Командой **git branch -M main** переименовывается ветка **master** на локальном репозитории в **main.** Таким образом, изменения, произошедшие на удаленном репозитории больше не конфликтуют с локальным хранилищем, в котором главная ветка стала также называться **main.**
Например,**git push -u origin main** позволяет *запушить* (отправить) ветку **main** на сервер **origin.**

Необходима авторизация в удаленном репозитории!!!


# Получение изменений из удаленного репозитория. Команда git pull.

**git pull**  <*имя удаленного репозитория*>

Получает изменения из переданного удаленного репозитория и обновляет нашу локальную рабочую копию в соответствии с удаленным репозиторием.

# Как настроить совместную работу.

1.*Создать аккаунт на GitHub.com.*

2. *Создать локальный репозиторий.*

3. *Связать локальный и удалённый репозитории.* GitHub при создании нового репозитория подскажет, как это можно сделать.

4. *Отправить (**push**) ваш локальный репозиторий в удалённый (на GitHub), при этом  нужно будет авторизоваться на удалённом репозитории.*

5. *Провести изменения в удаленном репозитории.*
 6. *Выкачать (**pull**) актуальное состояние из удалённого репозитория.*
 
# Pull request. 

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают команду **pull request.** Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет изменения командой push в свой аккаунт на GitHub и даёт команду **pull request.**

**Как сделать pull request?**

1. *Делаем (ответвление) репозитория fork.*

2.*Делаем **git clone** версии репозитория.*  

3.*Создаем новую ветку и в нее вносим свои изменения.*

4.*Фиксируем изменения (делаем коммиты).*

5.*Отправляем свою версию в свой GitHub.*









# Технологии программирования. БГУ весна 2023

Тут будут появляться презентации, записи пар и условия лабораторных работ.

## Общие правила

1. Для выполнения лабораторных работ вы в праве выбрать любой язык программирования (в рамках разумного, без brainfuck и malbolge).
2. Вы можете получить баллы за исправления багов и неточностей в условиях лабораторных и презентациях. 
Однако оценивание полезности вашего исправления исключительно субъективно и остаётся на моё усмотрение. 

Пока всё : )

## Пары и презентации

1. Введение в семестр и в технологии программирования. Почему програмировать сложно: [link
](https://github.com/dasfex/bsu-programming-technologies/blob/trunk/presentations/1.pdf).
2. Вспоминаем git и чуть-чуть о других инструментах: [link](
https://github.com/bsu-spring-2023/programming-technologies/blob/trunk/presentations/2.pdf)

## Лабораторные работы

### Правила сдачи

Пожалуйста, внимательно прочитайте правила сдачи лабораторных работ. 
Их невыполнение может привести к получению минимальной оценки за лабораторную. 

Для сдачи лабораторных работ необходимо создать пуллреквест в своём репозитории 
с номером лабораторной работы.
Например если вы делаете ```cistring```, вы берёте её номер из списка ниже (это 1) и создаёте ветку с именем lab-01 
(аналогично должен быть назван pull request). 
В ней вы оставляете решение, после чего при проверке приходит преподаватель и оставляет ревью. 
Не предполагается, что вы получите баллы за исправление ревью, но т.к. некоторые лабораторные связаны, лучше исправить, 
чтобы проверяющий не напоролся на ошибку снова (и вы не потеряли баллы повторно). 
Пока лабораторная не будет проверена и за неё не будет выставлена оценка в anytask, не закрывайте и не мержите pull request,
чтобы он не потерялся из открытых. 

Дедлайн строгий, т.е. если не успели хоть на минуту, кол-во баллов понижается (вплоть до нуля, если это был хард дедлайн).

После дедлайна никаких изменений в пулл реквесте быть не должно. 

Коммитим лишь то, что необходимо для решения задания (никаких ```.idea```, ```cmake-build-debug``` и прочих ненужных служебных файлов). 
Чтобы не попасться, можно настроить .gitignore по своему усмотрению. 

### Условия

1. ```cistring```: [link](https://github.com/bsu-spring-2023/programming-technologies/blob/trunk/labs/cistring.md). Дедлайн (один хард): 23:30 22.04.2023. До 8 баллов. 
2. ```search 1```: [link](https://github.com/bsu-spring-2023/programming-technologies/blob/trunk/labs/search1.md). Дедлайны: софт 23:30 25.02.2023, хард 23:30 04.03.2023 (с коэффициентом 0.7). До 13 баллов.
3. ```matrix```: [link](https://github.com/bsu-spring-2023/programming-technologies/blob/trunk/labs/matrix.md). Дедлайн (один хард): 23:30 22.04.2023. До 5 баллов.  

### Настройка репозитория

1. Для сдачи лабораторных работ клонируете публичный репозиторий:
```git
git clone git@github.com:bsu-spring-2023/programming-technologies.git bsu-pt
```
Это склонирует вам репозиторий в новую директорию ```bsu-pt```.
Все изменения делаете локально в этом склонированном репозитории. 

2. Каждый раз для его обновления делаете
```git
git pull --rebase
```

3. Для отправки решения на сервер, необходимо, чтобы у вас были заданы имя и email:
```git
git config --global user.name "Vasya Pupkin"
git config --global user.email "vasya@pupkin.com"
```

4. Добавьте в git свой приватный репозиторий. Для этого запустите из директории репозитория команду:
```git
git remote add student $ADDRESS
```
```$ADDRESS``` нужно скопировать со страницы своего приватного репозитория: Code -> SSH.

Цикл решения задач такой:
1. В локальном репозитории делаете
```git
git pull --rebase
```

2. Создаёте ветку с номером лабораторной:
```git
git checkout -b lab-1
```

3. Делаете все необходимые изменения. Коммитите их с именем таким же, как и название ветки.
Т.е. у вас в итоге может получится 5 коммитов с именем ```lab-1``` (пожалуйста, постарайтесь не делать много коммитов, 
если что лучше используйте ```--amend```).

4. Чтобы запушить изменения в свой приватный репозиторий сделайте
```git
git push student
```
При необходимости с флагом ```--force```.

5. В приватном репозитории сделайте pull request из этой ветки в ```trunk```.
Ссылку на него и сдавайте в anytask.

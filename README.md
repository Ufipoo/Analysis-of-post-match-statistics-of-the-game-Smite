# Analysis-of-post-match-statistics-of-the-game-Smite
# Анализ послематчевой статистики игры Smite
Course work
Курсовая работа за 3 курс - Анализ послематчевой статистки игры Smite. 
Закинула сюда все нужные файлы: парсер, модели, эксперименты, графики и т.д.
test1.py и test17.py рабочие модели. Какая из них последней версии не помню, где-то небольшие правик были для измерения точности и построения "красивых" графиков в visdom.

#### [test1.py](https://github.com/Ufipoo/Analysis-of-post-match-statistics-of-the-game-Smite/blob/master/test1.py)
#### [test17.py](https://github.com/Ufipoo/Analysis-of-post-match-statistics-of-the-game-Smite/blob/master/test17.py)

### Постановка задачи
#### Целью данной работы является создание нейронной сети, способной классифицировать исход матча, учитывая состав команд. 
В состав одной команды входят 5 героев, всего в матче 10 героев.
Исход матча определяется одним победителем: победила либо первая, либо вторая команда.
Всего в игре имеется 101 герой (105 в новом датасете).
#### Для понимания сути работы, рассмотрим задачу на примере футбольного матча.Допустим, в матче команда профессиональных игроков играет против дворовой команды. Шансов победить у первой команды будет больше. 
![1](https://i.imgur.com/XGSQpJ8.jpg)
#### Но если мы перемешаем игроков, то ответ будет уже не таким очевидным. Этим и должна заняться сеть. Предсказать исход матча, учитывая состав команд
![2](https://i.imgur.com/PbZ0BYN.jpg)
#### Достижение цели осуществлялось путем решения следующих основных задач:
1. Сбор датасета.
2. Создание нейронной сети, предсказывающая исход матча:
   * Модель без обучения векторного представления команд;
   * Модель с обучение векторного представления команд.
### Схема реализованной модели
![3](https://i.imgur.com/sTB7ZLU.png)
#### В датасет сохранялись не полные имена героев, а их индексы. Например, вектор данного матча, где первая команда победила, выглядит так –
![4](https://i.imgur.com/suegP5p.jpg)
![5](https://i.imgur.com/5esJTfg.jpg)
# Подготовка данных
![6](https://i.imgur.com/07KIljo.png)
# Модель без обучения векторного представления команд
![7](https://i.imgur.com/GI6GBzS.png)
![8](https://i.imgur.com/5YLniP9.png)
![9](https://i.imgur.com/tjHhkWF.jpg)
## Аугментация
![10](https://i.imgur.com/QTE71ds.png)
![11](https://i.imgur.com/uqejDY3.jpg)
# Модель без обучения векторного представления команд
![12](https://i.imgur.com/YbXMLvP.png)
# Результаты работы
Подбор гиперпараметров
![13](https://i.imgur.com/R0Iobvz.png)



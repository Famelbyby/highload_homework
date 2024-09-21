# Pinterest
## 1. Тема и целевая аудитория
### Тема
Pinterest  — социальный интернет-сервис, фотохостинг, позволяющий пользователям добавлять в режиме онлайн изображения [1].
### Целевая аудитория*
- Количество уникальных пользователей за день: около 34 миллиона [2]
- Среднее количество посещений сайта в месяц: 1.1 миллиарда
- Среднее время пребывания пользователя на сайте: 7 минут [3]
- Среднее количество страниц за посещение: 12

Таблица 1 - Распределение пользователей сайта по странам
| Страна   | Процент пользователей |
|----------|:---------------------:|
| США      | 22.44%                |
| Индия    | 8.17%                 |
| Бразилия | 7.98%                 |
| Россия   | 5.52%                 |
| Мексика  | 4.2%                  |

\* - данные за август 2024

### Ключевой функционал
+ Регистрация/авторизация
+ Просмотр ленты постов
+ Создание поста
+ Добавление постов в сохраненные
+ Подписка на пользователей
+ Просмотр пина
+ Поиск по теме поста [4]

### Ключевые продуктовые решения
- Бесконечная лента постов
- Рекомендации постов по интересам

### Список использованной литературы
[1. Pinterest - Wikipedia ](https://ru.wikipedia.org/wiki/Pinterest)

[2. Pinterest | HypeStat](https://hypestat.com/info/pinterest.com)

[3. Website Perfomance](https://pro.similarweb.com/#/digitalsuite/websiteanalysis/overview/website-performance/*/999/1m?webSource=Total&key=pinterest.com)

[4. Pinterest](https://ru.pinterest.com/)

## 2. Расчет нагрузки
### Продуктовые метрики
Таблица 2 - Количество пользователей за период
| Период                         | Количество уникальных пользователей      |
|:------------------------------:|:----------------------------------------:|
|Месяц                           | 363млн                                   |
|День                            | 34млн                                    |

**Пояснение:** данные взяты из [7].

Таблица 3 - Хранилища
| Тип хранилища | Средний размер |
|:-------------:|:--------------:|
|Пользователь   | 0.068 Гб         |

**Пояснение:** в данный момент в Pinterest насчитывается 240 млрд пинов, то есть по 670 пинов на пользователя. Было выявлено, что на видео приходится 0.3% от количества всех пинов, то есть около 2 на каждого пользователя. Эмпирическим путём (после скачивания около 50 картинок, видео и аватарок) было выявлено, что средний вес картинки-пина - 100 Кб, видео-пина - 2 Мб, а аватарки пользователя - 50 Кб. Таким образом, размер одного пользователя: 668 * 100 Кб + 2 * 2 Мб + 50 Кб = 70 Мб = 0.068 Гб. Данные взяты из [1].

Таблица 4 - Действия пользователя по типам
| Тип действия                                           | Среднее количество в день    |
|:------------------------------------------------------:|:----------------------------:|
|Подписка на пользователя                                | 37 млн                       |
|Просмотр ленты                                          | 38.83 млн                    |
|Поиск пина                                              | 166.7 млн                    |
|Создание пина                                           | 120 млн                      |
|Просмотр страницы конкретного пина                      | 138.7 млн                    |
|Авторизация/регистрация                                 | 38.83 млн                    |
|Добавление пина в сохраненные                           | 214.3 млн                    |

**Пояснение:** 
1) за последний месяц количество пользователей изменилось на 4 млн. Если принимать, что процентное содержание пользователей по количества подписчиков остается константой, то по данным из [5] можно определить, что количество подписок за месяц составляет 1.1 млрд (если считать, что количество подписчиков у пользователя изменятся от середины предыдущего диапазона до середины следующего). Выходит, что за день среднее количество подписок на пользователей составляет 37 млн. Данные взяты из [1].
2) за месяц в Pinterest происходит 5 млрд поисков пинов, то есть в день около 166.7 млн. Данные взяты из [1].
3) за месяц в Pinterest происходит около 1.16 млрд сессий, то есть в день около 38.7 млн. Учитывая, что авторизация происходит неявно (и +0.13 млн/день регистраций), то и авторизаций/регистраций составляет 38.83 млн. Данные взяты их [7].
4) по статистике, в неделю происходит 1.5 млрд добавлений пинов в сохранённые, то есть 214.3 млн в неделю. Данные взяты из [3].
5) по статистике, приведённой в [1], количество пользователей за последний месяц составляет 1.5% от суммы пользователей за все время службы Pinterest (Пример: за 1-ый месяц было 100 млн, за 2-ой - 200 млн, за 3-ий - 210 млн. Тогда за 3-ий месяц количество пользователей составляет 210 / (210 + 200 + 100) = 42%). Значит, считая, что количество создаваемых пинов зависит от количества пользователей за месяц, то можно положить, что количество созданных пинов за последний месяц 240 000 000 000 / 100 * 1.5 = 3 600 000 000. Значит, в день создаётся примерно 120 млн пинов. Данные взяты из [8].
6) за месяц в Pinterest происходит около 1.16 млрд сессий, в среднем за одну сессию пользователей посещает 12 страниц, то есть всего посещается 13.92 млрд страниц. 3.6 млрд из них уходит на создание пинов, 5 млрд - на поиск пинов, и ещё 1.16 млрд - на просмотр ленты (так как после неявной/явной авторизации/регистрации переход происходит на страницу ленты; будем предполагать, что пользователь за сессию посещает страницу ленты 1 раз, так как смысла перезагружать её нет, ведь она бесконечная). Таким образом получается, что на просмотр страницы конкретного пина выходит 13.92 - 5 - 3.6 - 1.16 = 4.16 млрд запросов в месяц, то есть в день 4.16 млрд / 30 = 138.7 млн.
7) так как в пункте 6 было принято, что просмотр ленты происходит 1 раз за сессию, то количество таких запросов столько же, сколько и авторизаций/регистраций, то есть 38.83 млн в день.

### Технические метрики
Таблица 5 - Типы хранилищ и их размеры
| Тип хранения                          |      Размер, Тб      |
|:-------------------------------------:|:--------------------:|
|Пользователи                           | 17.1 Тб              |
|Пины                                   | 35 414 Тб            |

**Пояснение:**
1) пользователей всего 363 млн, у каждого из них аватарка может весить в среднем 50 Кб и есть текстовые данные (такие, как описание, имя и тд, которые составляют всего около 500 байт). Таким образом, суммарный размер пользователей: ~50.5 Кб * 363 млн = 17.1 Тб.
2) пинов всего 240 млрд, средний вес картинок-пинов - 100 Кб, средний вес видео-пинов - 2 Мб. Процентаж видео-пинов = 0.3%, то есть их всего 7.2 млрд, а картинок-пинов соответственно - 232.8 млрд. Итого: 232 800 000 000 * 100 Кб + 7 200 000 000 * 2 Мб = 35 414 Тб.

Таблица 6 - Сетевые метрики
| Тип действия                                           | Пиковое потребление в течение суток, Гбит/с | Суммарный суточный, Гбайт/сутки | RPS (средний) | RPS (пиковый) |
|:------------------------------------------------------:|:-------------------------------------------:|:-------------------------------:|:-------------:|:-------------:|
|Подписка на пользователя                                | 0.003                                       |  91.7                           | 428           | 1 044         |
|Просмотр ленты                                          | 11.73                                       |  405 743                        | 449           | 1 096         |
|Поиск пина                                              | 4.71                                        |  162 793                        | 1 930         | 4 710         |
|Создание пина                                           | 3.44                                        |  118 945                        | 1 389         | 3 389         |
|Просмотр пина                                           | 3.13                                        |  108 359                        | 1 605         | 3 917         |
|Авторизация/регистрация                                 | 1.2                                         |  41 229                         | 449           | 1 096         |
|Добавление пина в сохраненные                           | 0.04                                        |  1 328                          | 2 480         | 6 051         |
|**Итого суммарно**                                      | **24.3**                                    |  **838 489**                    | **8 730**     | **21 303**    |

**Пояснение:** 
- Рассматриваются суммарный суточный трафик и средний RPS
  1. в среднем отписка/подписка на пользователя составляет 2.6 Кб сетевого трафика. Таким образом, за день получается 37 млн * 2.6 КБ = 91.7 Гб. Данные взяты из Chrome DevTools.
  2. за день происходит около 37 млн подписок, то есть в среднем за секунду - 37 млн / 86 400 = 428 запросов.
  3. в среднем авторизация/регистрация занимает 1.1 Мб сетевого трафика. Тогда, суммарный суточный трафик составляет 38.83 млн * 1.1 Мб = 41 229 Гб.
  4. за день происходит 38.83 млн авторизаций/регистраций, то есть 449 запросов в секунду.
  5. в среднем добавление пина в сохраненные занимает 6.5 Кб сетевого трафика, то есть в день около 6.5 Кб * 214.3 млн = 1 328 Гб. Данные взяты из Chrome DevTools.
  6. за день происходит 214.3 млн добавлений пина в сохраненные, то есть около 2 480 запросов в секунду.
  7. в среднем просмотр ленты занимает 10.7 Мб сетевого трафика. Значит, суммарный суточный трафик составляет 10.7 Мб * 38.83 млн = 405 743 Гб. Данные взяты из Chrome DevTools.
  8. за день происходит 38.83 млн запросов на просмотр ленты, то есть средний RPS составляет 38.83 млн / 86 400 = 449.
  9. в среднем поиск пина занимает 1 Мб сетевого трафика. Получается, что суммарный суточный трафик - 1 Мб * 166.7 млн = 162 793 Гб. Данные взяты из Chrome DevTools.
  10. за день происходит 166.7 млн поисков пинов, то есть около 1 930 в секунду.
  11. в среднем просмотр пина составляет 0.8 Мб сетевого трафика. Выходит, что суммарный суточный трафик равен 0.8 Мб * 138.7 млн = 108 359 Гб. Данные взяты из Chrome DevTools.
  12. за день происходит 138.7 млн просмотров конкретного пина, то есть средний RPS составляет 138.7 млн / 86 400 = 1 605.
  13. в среднем создание картинки-пина занимает 1 Мб, а создание видео-пина - 5 Мб (данные основаны на вышеперечисленных выявлениях средних значений пинов и умножении на 2 + 1-2 Мб). Так как видео-пины составляют всего 0.3% от всех пинов, то суммарный трафик за день составляет: 120 млн * 0.003 * 6 Мб + 120 млн * 0.997 * 1 Мб = 118 945 Гб. Данные взяты из Chrome DevTools.
  14. за день происходит 120 млн созданий пинов, то есть в секунду в среднем 120 млн / 86 400 = 1 389.
- Рассматриваются пиковое потребление в течение суток и пиковый RPS
  По данным из [6] было определено, что на распределении по часовым поясам пик пользователей приходит на Америку - 95 млн, а среднее количество пользователей по всему миру - 38.9 млн. Таким образом, отношение пикового количества к среднему 95 / 38.9 = 2.44. Значит, отношение пикого RPS к среднему - 2.44.
  
  *Примечание: далее используются трафики из предыдущего списка.*
  
  Тогда просчитаем соответсвующие пиковые RPS и пиковое потребление в течение суток.
  1. пиковый RPS подписок на пользователя 428 * 2.44 = 1 044.
  2. тогда пиковое потребление в течение суток на подписки пользователей составляет 1 044 * 2.6 Кб = 0.003 Гбит/с.
  3. пиковый RPS просмотра ленты 449 * 2.44 = 1 096.
  4. значит, пиковое потребление в течение суток на просмотр ленты составляет 1 096 * 10.7 Мб = 11.73 Гбит/с.
  5. пиковый RPS поиска пина 1 930 * 2.44 = 4 710.
  6. получается, пиковое потребление в течение суток на поиск пинов равно 4 710 * 1 Мб = 4.71 Гбит/с.
  7. пиковый RPS создания пинов 1 389 * 2.44 = 3 389.
  8. таким образом, пиковое потребление в течение суток на создание пинов занимает 3 389 * 0.997 * 1 Мб + 3 389 * 0.003 * 6 Мб = 3.44 Гбит/с.
  9. пиковый RPS просмотра пинов 1 605 * 2.44 = 3 917.
  10. в таком случае пиковое потребление в течение суток на просмотр пинов составляет 3 917 * 0.8 Мб = 3.13 Гбит/с.
  11. пиковый RPS авторизации/регистрации 449 * 2.44 = 1 096.
  12. пиковое потребление в течение суток на авторизацию/регистрацию равно 1 096 * 1.1 Мб = 1.2 Гбит/с.
  13. пиковый RPS добавления пинов в сохранённые 2 480 * 2.44 = 6 051.
  14. итого, пиковое потребление в течение суток на добавление пинов в сохранённые занимает 6 051 * 6.5 Кб = 0.04 Гбит/с.

### Список использованной литературы
[1. Pinterest Statistics 2024 - TrueList](https://truelist.co/blog/pinterest-statistics/)

[2. 28 Pinterest Statistics That Marketers Must Know](https://www.demandsage.com/pinterest-statistics/)

[3. 44 Pinterest Statistics & Facts For 2024](https://www.searchenginejournal.com/pinterest-facts/370926/)

[4. Top Pinterest Influencers | Pinterest Wiki | Fandom](https://pinyourinterest.fandom.com/wiki/Top_Pinterest_Influencers)

[5. Instagram Followers - Everything You Need To Know](https://mention.com/en/reports/instagram/followers/)

[6. Countries With Most Pinterest Users](https://worldpopulationreview.com/country-rankings/pinterest-users-by-country)

[7. Pinterest | HypeStat](https://hypestat.com/info/pinterest.com)

[8. Pinterest Global MAU 2024 | Statista](https://www.statista.com/statistics/463353/pinterest-global-mau/)

## 3. Глобальная балансировка нагрузки
### Функциональное разбиение по доменам
Проанализировав типы действий пользователей на сайте Pinterest, можно прийти к следующему разбиению по доменам:
- _pins.pinterest.com_ - данный домен отвечает за просмотр конкретных пинов, а также подписку на пользователя и добавление пина в сохранённые;
- _feed.pinterest.com_ - текущий домен используется при просмотре ленты и поиске пинов;
- _auth.pinterest.com_ - данный домен отвечает за регистрацию и авторизацию пользователей в Pinterest;
- _create.pinterest.com_ - этот домен предназначен для создания, редактирования пинов и их удаления.
Данное решение было принято следующий образом:
  1) в первую очередь учитывалось объединение действий по логическим принципам. Так, например, создание пинов не имеет логического местонахождения под доменом feed.pinterest.com. К тому же, авторизация и регистрация стоят отдельным "столпом" среди остальных запросов.
  2) далее учитывались продуктовые и сетевые метрики:
      - отмечено, что созданий пинов в день в среднем 120 млн, однако просмотров ленты - всего лишь 38.83 млн. Однако второе является более тяжелым по трафику, а поиск пина - дешевле создния, то разумнее объединить их в один домен.
      - количество просмотров страницы конкретного пина насчитывает 138.7 млн, а добавление пина в сохранённые - аж 214.3 млн. Принимая во внимание, что добавление пина в сохранённые - почти не затратная операция относительно создания пинов или просмотра ленты, то нормальным решением является объединение данного действия с просмотром конкретного пина в один домен - pins.pinterest.com.
### Расположение ДЦ
Принимая во внимание расположение кабелей под водой [2], точки обмена интернет-трафиком [1], расположение пользователей по земному шару [3] и данные рисунка 1, можно выделить следующие города с ДЦ:
  - Лос-Анджелес
  - Торонто
  - Рио-де-Жанейро
  - Буэнос-Айрес
  - Сантьяго
  - Каракас
  - Веракрус
  - Ванкувер
  - Анкоридж
  - Лиссабон
  - Барселона
  - Кардифф
  - Гётеборг
  - Хельсинки
  - Венеция
  - Прага
  - Токио
  - Брисбен
  - Денвер
![image](https://github.com/user-attachments/assets/ae7891cf-2222-4c4f-b967-79202eccd22f)

**Рисунок 1** - Пользователи Pinterest

**Пояснение:** 
  - так как Австралия и Япония находятся далеко от других стран, в которых пользуются Pinterest, то в них необходимо разместить по ДЦ, иначе latency будет неприлично долгим
  - в остальных случаях ДЦ планируется размещать на расстоянии 2-4 тыс. км: необходимо покрыть Европу, Южную Америку, Северную Америку и Канаду.

### Расчет распределения запросов из секции "Расчет нагрузки" по типам запросов по датацентрам
Предлагаю начать распределение по датацентрам с наименее затратных по трафику доменов:
  - _auth.pinterest.com_ - данных запросов в день относительно немного, к тому же данный запрос не требует слишком быстрого ответа, поэтому датацентров, обслуживающих этот домен, можно расположить мало: в Венеции и Лос-Анджелесе.
  - _pins.pinterest.com_ - эти запросы вторые по величине использования трафика, им требуется немного ДЦ: Анкоридж, Лиссабон, Гётеборг, Торонто.
  - _ create.pinterest.com_ - данные запросы достаточно велики по трафику, поэтому эти должны заимствовать тоже немного ДЦ: Веракрус, Барселона, Хельсинки, Буэнос-Айрес.
  - _feed.pinterest.com_ - данные запросы требуют больше всего трафика (и суточного, и в секунду), поэтому их должно быть больше всего, а именно: в Денвере, Сантьяго, Ванкувер, Каракасе, Праге, Кардиффе, Токио и Брисбене.

### Схема DNS балансировки
Так как область пользования Pinterest охватывает весь земной шар (к тому же на противоположные меридианы приходятся области, поддерживающие примерно одинаковые количества пользователей онлайн), то подходящими решениями являются Geo-based DNS или Latency-based DNS. В данном случае я решил воспользоваться **Latency-based DNS**, так как при загрузке ленты пинов необходима скорость, обспечивающаяся за счёт наименьшего latency.

### Список использованной литературы
[1. Internet Exchange Map](https://www.internetexchangemap.com/#/)

[2. Submarine Cable Map](https://www.submarinecablemap.com/)

[3. Pinterest Users by Country 2024](https://worldpopulationreview.com/country-rankings/pinterest-users-by-country)

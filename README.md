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
  - Бордо
![image](https://github.com/user-attachments/assets/ae7891cf-2222-4c4f-b967-79202eccd22f)

**Рисунок 1** - Пользователи Pinterest

**Пояснение:** 
  - так как Австралия и Япония находятся далеко от других стран, в которых пользуются Pinterest, то в них необходимо разместить по ДЦ, иначе latency будет неприлично долгим
  - в остальных случаях ДЦ планируется размещать на расстоянии 2-4 тыс. км: необходимо покрыть Европу, Южную Америку, Северную Америку и Канаду.

### Расчет распределения запросов из секции "Расчет нагрузки" по типам запросов по датацентрам
Предлагаю начать распределение по датацентрам с наименее затратных по трафику доменов:
  - _auth.pinterest.com_ - данных запросов в день относительно немного, к тому же данный запрос не требует слишком быстрого ответа, поэтому датацентров, обслуживающих этот домен, можно расположить мало: в Венеции и Лос-Анджелесе.
  - _pins.pinterest.com_ - эти запросы вторые по величине использования трафика, им требуется немного ДЦ: Анкоридж, Лиссабон, Гётеборг, Торонто.
  - _create.pinterest.com_ - данные запросы достаточно велики по трафику, поэтому эти должны заимствовать тоже немного ДЦ: Веракрус, Барселона, Хельсинки, Буэнос-Айрес.
  - _feed.pinterest.com_ - данные запросы требуют больше всего трафика (и суточного, и в секунду), поэтому их должно быть больше всего, а именно: в Денвере, Сантьяго, Ванкувер, Каракасе, Праге, Кардиффе, Токио и Брисбене.

Так как на просмотр ленты и поиска пина средний RPS составляет 449, а также учитывая расположение на планете, можем составить таблицу распределения запросов:

Таблица 7 - Распределение запроса "Просмотр ленты" по датацентрам
| Датацентр(ы)             | RPS (средний) |
|:------------------------:|:-------------:|
| Денвер                   | 424           |
| Ванкувер                 | 424           |
| Сантьяго                 | 344           |
| Каракас                  | 344           |
| Прага                    | 265           |
| Кардифф                  | 265           |
| Токио                    | 180           |
| Брисбен                  | 132           |

Авторизация/регистрация в среднем составляет 449 запросов в секунду, из этого можно построить таблицу 8.

Таблица 8 - Распределение запроса "Авторизация/регистрация" по датацентрам
| Датацентр(ы)             | RPS (средний) |
|:------------------------:|:-------------:|
| Венеция                  | 160           |
| Лос-Анджелес             | 289           |

Средний RPS создания пина составляет 1 389, исходя из этих данных можно организовать таблицу 9.

Таблица 9 - Распределение запроса "Создание пина" по датацентрам
| Датацентр(ы)             | RPS (средний) |
|:------------------------:|:-------------:|
| Веракрус                 | 80            |
| Буэнос-Айрес             | 80            |
| Барселона                | 65            |
| Хельсинки                | 65            |

Средний RPS подписки на пользователя, просмотр конкретного пина и добавление пина в сохраённые составляет 4 513. Сделаем таблицу 10.

Таблица 10 - Распределение запросов "Подписка на пользователя", "Просмотр пина" и "Добавление пина в сохранённые" по датацентрам
| Датацентр(ы)             | RPS (средний) |
|:------------------------:|:-------------:|
| Анкоридж                 | 967           |
| Лиссабон                 | 967           |
| Торонто                  | 967           |
| Гётеборг                 | 806           |
| Бордо                    | 805           |

### Схема DNS балансировки
Так как область пользования Pinterest охватывает весь земной шар (к тому же на противоположные меридианы приходятся области, поддерживающие примерно одинаковые количества пользователей онлайн), то подходящими решениями являются Geo-based DNS или Latency-based DNS. В данном случае я решил воспользоваться **Latency-based DNS**, так как при загрузке ленты пинов необходима скорость, обспечивающаяся за счёт наименьшего latency.

### Список использованной литературы
[1. Internet Exchange Map](https://www.internetexchangemap.com/#/)

[2. Submarine Cable Map](https://www.submarinecablemap.com/)

[3. Pinterest Users by Country 2024](https://worldpopulationreview.com/country-rankings/pinterest-users-by-country)

# 4. Локальная балансировка нагрузки
## Внешние запросы
Здесь будут использоваться Kubernetes кластеры, так как они подходят и для балансировки запросов, и для оркестрации [2].

Для балансировки внешних запросов будет использоваться такой L7 load balancer, как Nginx. Он был выбран по следующим причинам:
  - на нем можно проводить SSL терминацию
  - перезапускать конфиги/серверы без простоев [1]
  - экономит количество соединений (например, если запросы к БД блокируют worker'ов)
  - при отправке запросы на backend и последующем падении того сервера может переотправить запрос на другие backend'ы
  - на Nginx можно сделать проверку на авторизацию, тем самым уменьшив нагрузку на Kubernetes кластеры.
*Примечание:* целесообразнее будет выключить gzip у Nginx, так как основной передаваемый контент - видео/фотографии, и их архивирование будет излишне тратить серверные ресурсы

![image](https://github.com/user-attachments/assets/9fd45f06-8b9c-4e9f-9bfa-a9b9fa2e349c)
**Рисунок 2** - Схема балансировки внешних запросов

## Внутренние запросы
На уровне L7 будет использоваться Nginx для распределения равномерной нагрузки по CPU на серверы.
## Схема отказоустойчивости
Отказоустойчивость будет обеспечена засчет нескольких пунктов:
  1. Использование Kubernetes - он позволяет автоматически перезапускать сервисы при их падении
  2. Использование Keepalived - данное программное обеспечение работает следующим образом:
       - К основному устройству-владельцу IP (master) добавляется одно или несколько резервных (backup) с такими же сервисами,
       - Каждое устройство дополнительно имеет уникальный служебный IP-адрес и назначаемый приоритет,
       - Резервные устройства непрерывно опрашивают мастера,
       - Как только мастер перестаёт отвечать, резервное устройство, имеющее максимальный приоритет, поднимает публичный IP на своём сетевом интерфейсе [3].
  3. К тому же, периодически может проводиться проверка работоспособности сервера посредством отсылания на него базовых L7 health checks.
## Нагрузка по терминации SSL
Первый слой Nginx отвечает за SSL терминацию, благодаря этому мы будем уверены, что SSL всех запросов будут кэшироваться на одном Nginx, и не надо будет синхронизировать с другими балансировщиками.

В среднем SSL handshake занимает 3ms [4]. Мы будем использовать session cache. Необходимо рассчитать, какое количество запросов будут кешироваться:
  - просмотр ленты
  - поиск пина
  - просмотр пина

Итого: около (1 605 + 1 930 + 449) / 8 730 = 46% (данные взяты отсюда: https://github.com/Famelbyby/highload_homework?tab=readme-ov-file#технические-метрики) 
Так как суммарный пиковый RPS составляет 21 303, то выходит, что 21 303 * 0.54 = 11 504 не попадает в cache, на обработку SSL каждую секунду потребуется 11 504 * 3ms = 34.5s вычислительного времени.
### Список использованной литературы
[1. Nginx Hot Reload Without Downtime](https://code.luasoftware.com/tutorials/nginx/nginx-hot-reload-without-downtime)

[2. Балансировка нагрузки и масштабирование долгоживущих соединений в Kubernetes](https://habr.com/ru/companies/vk/articles/493820/)

[3. Keepalived for Linux](https://keepalived.org/)

[4. SSL handshake overhead](https://www.ibm.com/docs/en/cics-ts/6.x?topic=performance-ssl-handshake-overhead)

# 5. Логическая схема БД
## Таблица, поля и связи между ними
На рисунке 3 представлена диаграмма отношений между выделеннными мной таблицами для обеспечения полной работы API. 

![image](https://github.com/user-attachments/assets/602d137e-f2b3-469f-bf5e-c32f9892715e)

**Рисунок 3** - Диаграмма отношений выделенных таблиц

Таблица 11 - Описание выделенных таблиц
| Имя таблицы             | Поля таблицы               |           Краткое описание таблицы |
|:-----------------------:|:--------------------------:|:----------------------------------:|
| Session                 | session_id - уникальный хеш сессии<br>user_id - пользователь данной сессии<br>exp - дата (timestamp), когда сессия станет невалидной<br>iat - дата (timestamp), когда сессия была создана | В таблице хранятся сессии и соответствующие им пользователи |
| User                    | id - уникальный ID пользователя<br> username - никнейм пользователя<br>first_name - имя<br>last_name - фамилия<br>description - описание<br>avatar - хеш на аватарку, лежащей в minio<br>web_site_ref - ссылка на бизнес-страницу для рекламы<br>created_at - дата создания<br>updated_at - дата последнего изменения| Данная таблица описывает сущность пользователя |
| Follow                  | follow_id - уникальный ID подписки<br>following_user_id - ID пользователя, на которого подписались<br>followed_user_id - ID пользователя, который подписался<br>created_at - дата подписки | Эта таблица отвечает за подписки пользователей друг на друга |
| Pin                     | id - уникальный ID пина<br>title - название пина<br>description - описание пина<br>image - хеш на картинку/видео в minio<br>user_id - ID пользователя, создавшего пина<br>created_at - дата создания пина<br>updated_at - дата последнего изменения | Данная таблица описывает сущность пина |
| Saved_pins              | id - уникальный ID сохранения<br>user_id - ID пользователя, сохраняющего пин<br>pin_id - ID сохранённого пина<br>created_at - дата сохранения пина | Эта таблица отвечает за добавления пользователями пина в сохранённые |
| Tag                     | id - уникальный ID тэга<br>name (unique) - имя тэга | Данная таблица необходима для описания сущности тэга. Она необходима для поиска пинов: поиск по ID быстрее, нежели поиск по строке - названия тэга |
| Pins_tags               | id - уникальный ID тэга конкретного пина<br>pin_id - ID пина<br>tag_id - ID тэга | Данная таблица предназначена для поиска пинов по тэгам |

## Размеры данных и нагрузки на чтение/запись
В таблице 12 представлены оценочные размеры данных для каждой таблицы.

Таблица 12 - Размеры данных каждой таблицы
| Имя таблицы             | Размер данных таблицы               |
|:-----------------------:|:-----------------------------------:|
| Session                 | Допустим, длина хеша - 40 символов. Будем считать, что сессия длится день. Тогда размер данных: 34 млн (DAU) * (5 + 8 + 8 + 8) байт = 0.92 Гб |
| User                    | В среднем имя и фамилия в сумме составляют 20 символов, никнейм - 10. Хеш на аватар в минио - 30 символов. Примем, что описание занимает 30-40 = 35 символов. По данным из [4] можно увидеть, что 55% от всех пользователей имеют ссылку на бизнес-страницу. Допустим, что её длина составляет в среднем 25 символов. Тогда итого: 363 млн * (8 + 3 + 2 + 4 + 16 + 4) байт + 363 млн * 0.55 * 3 байта = 12.5 Гб|
| Follow                  | Из раздела https://github.com/Famelbyby/highload_homework?tab=readme-ov-file#продуктовые-метрики получено, что за месяц происходит около 1.1 млрд подписок. Так как за последний месяц количество пользователей составляет 1.5% от суммы пользователей за всё время, то итого: 1.1 млрд / 1.5 * 100 * (8 + 8 + 8 + 8) байтов = 2 186 Гб |
| Pin                     | всего пинов - 240 млрд, примерно 1 к 10 имеет название и 1 к 80 - описание, 1 к 200 - ссылку на сайт. Хеш файла - около 40 символов. Длина названия - около 6 символов. Описание - около 25. Ссылка на сайт - около 30 символов. Тогда общий размер выходит: 240 млрд * (8 + 5 + 8 + 8 + 8) байт + 24 млрд * 1 байт + 3 млрд * 3 байта + 1.2 млрд * 4 байта = 8 270 Гб + 22.35 Гб + 8.38 Гб + 4.47 Гб = 8 305 Гб|
| Saved_pins              | Из раздела https://github.com/Famelbyby/highload_homework?tab=readme-ov-file#продуктовые-метрики выяснено, что, во-первых, за месяц происходит около 6 млрд добавлений пинов в сохранённые. Во-вторых, количество посетителей за последний месяц составляет около 1.5% от общей суммы всех посетителей. Получается, что за всё время было произведено около 6 млрд / 1.5 * 100 = 400 млрд добавлений пинов в сохранённые. Итого общий размер таблицы: 400 млрд * (8 + 8 + 8 + 8) байт = 11 921 Гб = 11.64 Тб|
| Tag                     | В среднем длина тэга составляет 7-8 слов. На опыте было изучено, что на 1 тэг приходится 1-2 тысячи пинов, возьмём среднее - 1.5 тысячи Тогда общий размер: 240 млрд (количество пинов) / 1 500 * (8 + 8) байт = 2.38 Гб|
| Pins_tags               | всего пинов - 240 млрд, на каждый пин приходится примерно 4.5 тегов [1]. Получается, что размер таблицы 240 млрд * 4.5 * (8 + 8) байт = 16 093 Гб = 15.72 Тб |
|**Итого**                | 38 521 Гб                           |

Кроме того, оценим ещё размер хранилищ с файлами пинов. Они представлены в таблице 13.

Таблица 13 - Размеры хранилища
| Тип хранения                          |      Размер, Тб      |
|:-------------------------------------:|:--------------------:|
|Пины                                   | 35 414 Тб            |

Расчёты приведены здесь: https://github.com/Famelbyby/highload_homework?tab=readme-ov-file#технические-метрики

В таблице 14 приведены нагрузки на чтение и запись.

*Примечание:* в данной таблице учитывается только размер записей, не просчитывается поиск по индексу и т.д.

Таблица 14 - Нагрузки на чтение и запись
| Имя таблицы             | Нагрузка на чтение                    | Нагрузка на запись           |
|:-----------------------:|:-------------------------------------:|:----------------------------:|
| Session                 | Сессия проверяется при каждом запросе, поэтому RPS - 8 730. Тогда нагрузка на чтение составляет: 8 730 * (5 + 8 + 8 + 8) байт = 0.24 Мб/сек | 64 млн (2 * DAU, т.к. удалить и добавить) в день - то есть 787 RPS * (5 + 8 + 8 + 8) байт = 22.2 Кб/сек |
| User                    | Чтение пользователя необходимо при просмотре конкретного пина, а также при просмотре сохранённых пинов (об этом действии - в строке Saved_pins). RPS просмотра сохранённых пинов - 787. RPS просмотра конкретного пина - 1 605. Тогда нагрузка на чтение: (1 605 + 787) * (8 + 3 + 2 + 4 + 16 + 4 + 0.55 * 3) байт = 0.09 Мб/сек | В месяц создается 4 млн пользователей, то есть около 1.54 RPS. Тогда нагрузка на запись около: 1.54 * (8 + 3 + 2 + 4 + 16 + 4) байт * 0.55 * 3 байта = 0.06 Кб/сек |
| Follow                  | Подписка проверяется при просмотре конкретного пина, то есть: 1 605 * (8 + 8 + 8 + 8) байт = 0.05 Мб/сек | В секунду подписывается около 428 человек. Значит, нагрузка составляет 428 * (8 + 8 + 8 + 8) байт = 13 Кб/сек |
| Pin                     | RPS просмотра ленты - 449, за раз возвращается около 20 пинов. RPS просмотра конкретного пина - 1 605. Из следующей строки ясно, что RPS просмотра сохранённых - 787, возвращается по 20 пинов. Тогда нагрузка на чтение составит (787 * 20 + 1 605 + 449 * 20) * (8 + 5 + 8 + 8 + 8) байт = 0.93 Мб/сек | Средний RPS создания пина составляет 1 389. Тогда нагрузка на запись примерно: 1 389 * (8 + 5 + 8 + 8 + 8) байт = 50 Кб/сек |
| Saved_pins              | Пусть человек в среднем просматривает за день 2 раза сохранённые (в начале и в конце). Так как из таблицы 12 выявлено, что сохранённых пинов - 400 млрд, то на каждого пользователя приходится по 1 101 сохранённому пину. Нагрузка на чтение составляет 2 * 34 млн / 86 400 * 1 101 * (8 + 8 + 8 + 8) байт = 26.4 Мб/сек | RPS добавления пина в сохранённные равен 2 480. Итого: 2 480 * (8 + 8 + 8 + 8) байт = 78 Кб/сек |
| Tag                     | RPS поиска пина = 1 930, тогда нагрузка 1 930 * (8 + 8) байт = 0.03 Мб/сек | Так как в таблице 12 было принято, что один тэг на 1 500 пинов, то RPS создания тэга - 0.926, тогда нагрузка: 0.926 * (8 + 8) байт = 0.014 Кб/сек | 
| Pins_tags               | Нагрузка образуется во время поиска пина по тэгу, то есть 1 930 в секунду. Находится около 1 500 пинов. Значит, нагрузка на чтение составляет 1 930 * (8 + 8) байт * 1 500 = 82.8 Мб/сек | Из таблицы 12 можно определить, что на один пин используется 4.5 тэгов. Значит, RPS изменения этой таблицы составляет 4.5 * 1 389 = 6 251. Итого: 6 251 * (8 + 8) байт = 98 Кб/сек |
| **Итого**               | 110.54 Мб/сек | 244 Кб/сек |

Ниже представлены нагрузки на хранилища.

Таблица 15 - Нагрузки на хранилища
| Тип хранилища             | Нагрузка на чтение                    | Нагрузка на запись           |
|:-------------------------:|:-------------------------------------:|:----------------------------:|
| Аватарки пользователей    | Аватарка пользователя необходима при просмотре конкретного пина, а также при просмотре сохранённых пинов. RPS просмотра сохранённых пинов - 787. RPS просмотра конкретного пина - 1 605. Тогда нагрузка на чтение: (1 605 + 787) * 50 Кб = 116.8 Мб/сек | Создание пользователя составляет примерно 1.54 RPS. Учитывая, что в среднем аватарка весит 50 Кб (взято отсюда https://github.com/Famelbyby/highload_homework#технические-метрики), можно высчитать, что нагрузка на запись равна 1.54 * 50 Кб = 77 Кб/сек |
| Видео-пины                | RPS просмотра ленты - 449, за раз возвращается около 20 пинов. RPS просмотра конкретного пина - 1 605. RPS просмотра сохранённых - 787, возвращается по 20 пинов. Процентность видео-пинов - 0.3%. Средний вес видео-пина - 2 Мб. Тогда нагрузка на чтение составит (787 * 20 + 1 605 + 449 * 20) * 2 Мб * 0.003 = 158 Мб/сек | Средний RPS создания пина составляет 1 389. Видео-пины составляют 0.3% от общего количества всех пинов, их средний вес - 2 Мб. Тогда нагрузка на запись примерно: 1 389 * 2 Мб * 0.003 = 8.3 Мб/сек |
| Фото-пины                 | RPS просмотра ленты - 449, за раз возвращается около 20 пинов. RPS просмотра конкретного пина - 1 605. RPS просмотра сохранённых - 787, возвращается по 20 пинов. Процентность фото-пинов - 99.7%. Средний вес видео-пина - 100 Кб. Тогда нагрузка на чтение составит (787 * 20 + 1 605 + 449 * 20) * 100 Кб * 0.997 = 2 563.1 Мб/сек | Средний RPS создания пина составляет 1 389. Фото-пины составляют 99.7% от общего количества всех пинов, их средний вес - 100 Кб. Тогда нагрузка на запись примерно: 1 389 * 100 Кб * 0.997 = 135.2 Мб/сек |
| **Итого**                 | 2 837.9 Мб/сек | 143.6 Мб/сек |

## Указать требования к консистентности
Рассмотрим условия консистентности внтури таблиц.

Таблица 16 - Условия консистентности внутри таблиц
| Имя таблицы             | Условия консистентности               |
|:-----------------------:|:-------------------------------------:|
| Session                 | Сессия уникальна<br>Пользователь уникален |
| User                    | У каждого пользователя уникальный ID<br>У каждого пользователя уникальный хеш на аватарку<br>Аватарка есть в хранилище<br>У каждого пользователя уникальный никнейм |
| Follow                  | Пользователь не может быть подписан на себя<br>Пара (followed_user_id, following_user_id) должны быть уникальны |
| Pin                     | У каждого пина уникальный ID<br>У каждого файла уникальный хеш<br>Файл есть в хранилище<br>Дата изменения не раньше даты создания |
| Saved_pins              | Пара (user_id, pin_id) должны быть уникальны |
| Tag                     | У тэга уникальное имя<br>У тэга уникальный ID |
| Pins_tags               | Пара (tag_id, pin_id) должны быть уникальны |

Далее рассмотрим условия консистентности между таблицами.

Таблица 17 - Условия консистентности между таблицами
| Имя таблицы             | Размер данных таблицы               |
|:-----------------------:|:-----------------------------------:|
| Session                 | user_id существует                  |
| Follow                  | following_user_id и followed_user_id существуют |
| Saved_pins              | pin_id и user_id существуют |
| Pins_tags               | pin_id и tag_id существуют |

И в заключение необходимо проверить условия консистентности таблицы по времени.

Таблица 18 - Условие консистентности таблицы по времени

| Имя таблицы             | Размер данных таблицы               |
|:-----------------------:|:-----------------------------------:|
| Session                 | Конечно, сессия должна обновляться непременно |
| User                    | Непременное появление созданного пользователя у других не обязательно |
| Follow                  | Пины только что подписанного пользователя должны появляться в ленте сразу после подписки |
| Pin                     | Появление только что созданного пина у других пользователей необязательно |
| Saved_pins              | Только что добавленный в сохранённые пин должен появляться в сохранённом каталоге |
| Tag                     | Поиск только что созданного пина с новым тегом не обязателен |
| Pins_tags               | Не имеет условия консистентности, так как изменяется вместе с созданием пинов |

## Указать особенности распределения нагрузки по ключам
Можно выделить следующие особенности:
  1. Очень большая нагрузка приходится на таблицу Pins, так как она является главной: пины фигурирует в большинстве функционала. Ключ: pin_id.
  2. Достаточно большая нагрузка на чтение и маленькая нагрузка на запись в таблице Pins_tags; эта таблица активно используется при возникновении ленты и поиске пина по тэну. Ключ: tag_id.
  3. Большая нагрузка приходит на таблицу Tag, так как она необходима при подборе пинов в ленту. Ключ: tag_id.

### Список использованной литературы

[1. Куда писать теги в Pinterest](https://telegra.ph/Kuda-pisat-tegi-v-Pintereste--Magiya-tegov-na-Pinterest-kak-prevratit-sluchajnyh-posetitelej-v-postoyannyh-klientov-06-29)

[2. Int - SQL Server](https://learn.microsoft.com/ru-ru/sql/t-sql/data-types/int-bigint-smallint-and-tinyint-transact-sql?view=sql-server-ver16)

[3. PostgreSQL - Time](https://www.postgresql.org/docs/current/datatype-datetime.html)

[4. Pinterest Statistics 2024](https://www.demandsage.com/pinterest-statistics/)

# Тематическое моделирование слушателей

Идея - хотим узнать, чем отличаются пользователи vk, слушающие разные жанры музыки

Для этого хотим найти по топ-10 исполнителей по разным жанрам и выкачать их комментарии, подписчиков, а также стены и топ-5 подписок. Далее можем запилить тематическое моделирование по комментам/стенам, а также оценку тональности по комментам. В результате хотим получить тематические портреты средних слушателей разных жанров и сравнить их. 

Текущий план:
- Найти 2 самых противоположных жанра
- Найти топ-10 исполнителей (по сути - топ-10 самых больших групп вк) по этим жанрам
- Выкачать датку
- Посмотреть, получаются ли разумные модели

Классика:
1. https://vk.com/classic_relax (95к)
2. https://vk.com/classicalmusic.classic (53к, но комменты отключены)
3. https://vk.com/classic_best (30к)
4. https://vk.com/classic_online (24k, тоже отключены комменты)
5. https://vk.com/inclassic (22к)
6. https://vk.com/classicstories (22к)
7. https://vk.com/classical_music_guide (8k)
8. https://vk.com/contemporary_classical (14k, очень мало комментов)
9. https://vk.com/pi_a_no (19k)
10. https://vk.com/petertchaikovsky (22k)
11. https://vk.com/wmozart (93k)
12. https://vk.com/ludvigvonbeethoven (35k



Классика:

```python
target_groups = {
    'classic_relax':'30166068',
    'classic_best':'49945538',
    'inclassic':'26484100',
    'classicstories':'67287907_',
    'classical_music_guide':'153374206',
    'contemporary_classical':'44705245',
    'pi_a_no':'52678432',
    'petertchaikovsky':'21244691',
    'wmozart':'126406',
    'ludvigvonbeethoven':'191869',
}
```

Реп:

```python
target_groups ={
     'gazgolder': '1415705',           # 2 179 327
     'NoizeMC': '77521',               # 1 075 908
     'Miyagi&Эндшпиль': '85512864',    # 612 138
     'Элджей': '148220303',            # 97 904 (на оф странице 1.2 миллиона)
     'Feduk': '18022279',              # 279 565
     'Грибы': '120376084',             # 312 122
     'Oxxxymiron': '3113588',          # 921 242
     'PHARAON': '97439489',            # 204 034
     'Johnyboy': '10697541',           # 167 631
     'Хаски': '59790294',              # 237 918
     'LOne': '38213334',               # 681 506
     'Мот': '847771',                  # 760 959
     'ЛСП': '30314549',                # 815 224
     'Face': '95470601'                # 757 411
}
```

Шансон:
```python
target_groups = {
    "Михаил_Круг": '34532', # 126 940
    "Ирина_Круг": '33860393', # 66 640
    "Бутырка": '25040475', # 88 271
    "Трофимов": '202731', # 21 325
    "Жека": '2952094', # 45 834
    'Дюмин': '75015561', # 45 839
    'Воровайки': '632994', # 21 377
    'Шансон': '47951262', # 251 335
    'Шуфутинский': '1176762', # 13 947
    'РусскийШансон': '25993389', # 61 023
}
```

Эстрада: 

```python
target_groups ={
     'Лепс' : '52228413',       # Лепс : 66007
     'Пугачёва' : '24164800',   # Пугачёва : 29175
     'Михайлов' : '925262',     # Михайлов : 8013
     'Меладзе' : '4336146',     # Меладзе : 28081
     'Ваенга' : '57465816',     # Ваенга : 12413
     'Киркоров' : '24344295',   # Киркоров : 46353
     'Валерия' : '17890994',    # Валерия : 31754
     'Агутин' : '290390',       # Агутин : 12810
     'Газманов' : '5640401',    # Газманов : 7213
     'Басков' : '40705635',     # Басков : 3877
     'Николаев' : '106027463',  # Николаев : 3000
     'Ротару' : '37165678',     # Ротару : 12737
     'Лолита' : '1162252',      # Лолита : 26301
     'Леонтьев' : '9208',       # Леонтьев : 7740
     'Буйнов' : '157276422'     # Буйнов : 547
    }
```

Попса: 

```python
target_groups ={
    "LOBODA" : "1632070",      # 283036
    "Билан" : "5599",          # 73555
    "Крид" : "23482802",
    "2Маши" : "104052522",
    "Барских" : "4579233",
    "Гагарина" : "170578",
    "Темникова" : "72665113",
    "SEREBRO" : "74417",
    "Лазарев" : "26990345",
    "Ёлка" : "13762862",
    "Руки вверх" : "5719309",
    "МакSим" : "27112805",
    "Градусы" : "3315442",
    "ВИА ГРА" : "7669847",
    "A'Studio" : "13182484",
    "IOWA" : "20548570",
    "Бузова" : "4887563",
    "Тимати" : "24581636",
    "Нюша" : "11238722",
    "Караулова" : "93965182",
    "Кока" : "4908135",
    "Майами" : "121652498",
    "Беляев" : "14675331"
    }
```


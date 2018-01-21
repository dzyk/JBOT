//EN
JBOT Automatic trading system for the crypto currency exchange wex.nz

Installation:

To run the code, you need a server with a configured php and with extension of curl_php

If your server is installed on the local machine and has the address:

http://127.0.0.1

then extract the contents to the root folder:

/jbot23/api_wex.php
/jbot23/jbot_wex.html
/jbot23/aex.js
/jbot23/cookies.html
/jbot23/xhr.js

//RU
JBOT Автоматическая торговая система для биржи крипто-валют wex.nz

Установка:

Для работы кода, вам необходим сервер с настроенным php и в частности
обязательным расширением curl_php

Если ваш сервер установлен на локальной машине
и имеет адрес:

http://127.0.0.1

то распакуйте содержимое в корневую папку:

/jbot23/api_wex.php
/jbot23/jbot_wex.html
/jbot23/aex.js
/jbot23/cookies.html
/jbot23/xhr.js


Описание:


USD, BTC, LTC, NVC, NMC и т.д. - количество средств на вашем счету. Если средств
менее 0.0001, то показывать будет 0, для упрощения восприятия информации.

Pair - текущая торгующая пара
Бот позволяет торговать 40 валютными парами:
BTC/USD, BTC/RUR, BTC/EUR, LTC/BTC, LTC/USD, LTC/RUR, LTC/EUR,
NMC/BTC, NMC/USD, NVC/BTC, NVC/USD, USD/RUR, EUR/USD, EUR/RUR,
PPC/BTC, PPC/USD, DSH/BTC, DSH/USD, DSH/RUR, DSH/EUR, DSH/LTC,
DSH/ETH, DSH/ZEC, ETH/BTC, ETH/USD, ETH/EUR, ETH/LTC, ETH/RUR,
ETH/ZEC, BCH/USD, BCH/BTC, BCH/RUR, BCH/EUR, BCH/LTC, BCH/ETH,
BCH/DSH, BCH/ZEC, ZEC/BTC, ZEC/USD, ZEC/LTC.

Strategy - три вида стратегии:
- OUTER - стратегия основанная на курсе. если курс растет , то покупает в
пределах диапазона HIGH-LOW, продает, выше диапазона, при падении наоборот.
- INNER24(12,6,2) - стратегия покупки и продажи внутри диапазона HIGH-LOW.

Step Amount - количество BTC/LTC покупаемое или продаваемое

Step Distance - дистанция ступени в величинах. (пример 0.25 говорит покупать на
0.25 ниже предлагаемой цены, а продавать на 0.25 выше предлагаемой цены -
расширяет диапазон, отрицательное значение сужает диапазон)

Delta - дистанция ступени в процентах от спреда. (пример -10 (минус 10) говорит
совершать сделки ближе к центру диапазона HIGH-LOW: покупать на 10% выше LOW а
продавать на 10% ниже HIGH. И наоборот 10 (плюс 10) говорит совершать сделки
дальше от центра диапазона HIGH-LOW: покупать на 10% ниже LOW а продавать на 10%
выше HIGH)

Step Time - время между обновлениями информации, также как и время между
посылаемыми ордерами (оптимально, я полагаю, это 5-10 минут)

Order Life - время жизни ордера. если ордер висит дольше данного времени, он
будет отменен.

Max Orders - максимальное количество ордеров в одну сторону. Бот не может
выставить больше ордеров на покупки или продажу, чем указано.

Around - округление цены (оптимально, я думаю, до 3-4 знака для LTC и до 1-2 для
BTC, NVC, NMC).

В полях BUY и SELL бот предлагает цену покупки и продажи. Если поля окрашиваются
в красный, то средств недостаточно.

Set1-10 - Сохраненные настройки

Allow и Disallow это разрешение бота проводить самостоятельно операции покупки и
продажи.

Password - Пароль для сохранения настроек в зашифрованном виде и подписанным данным 
паролем. Для загрузки настроек необходимо ввести пароль и нажать Load Bot Settings.


FAQ


В: Как мне стать участником вашей системы?
О: Перейдите по ссылке http://funnymay.com/ и начните пользоваться услугами бота
или скачайте его и установите на своем веб-сервере.

В: Если я хочу сменить настройки, мне нужно останавливать бота?
О: При смене настроек, нажмите кнопку «Save settings» и при следующем обновлении
информация будет подхвачена «на лету».
Остановки бота не требуется.

В: Какие операции происходят во время ошибок со словами …XMLHTTP… ?
О: Повторяющиеся ошибки говорят, что завис javascript, при этом никаких операций
не происходит.

В: У меня показывается одна и та-же ошибка со словами …XMLHTTP… что мне делать?
О: Перезагрузите страницу и заново запустите бота кнопкой «Run Bot».

# Тестовые задания в MyTonWallet

Приглашаем выполнить одно из тестовых заданий для MyTonWallet. Успешное выполнение задания является **необходимым условием** для присоединения к команде. Цель тестового задания — оценить квалификацию и самоорганизованность кандидата.

### Использование результатов

Результаты выполнения тестового задания могут использоваться в реальном проекте **только в случае успешного найма** кандидата и при возможности дальнейшего развития своего решения уже в рамках проекта. В этом случае рабочее время, затраченное на тестовое задание, **оплачивается** в первую неделю работы.

В остальных случаях работы кандидатов никак **использованы не будут**. Однако всем кандидатам, полностью выполнившим задание в соответствии с критериями, будет выплачено **вознаграждение** вне зависимости от результатов найма.

### Критерии

Основные критерии оценивания: **скорость работы приложения**, **точное соответствие макетам**, **плавность анимаций** и **внимание к деталям**. Не рекомендуется использовать сторонние библиотеки и фреймворки.

### Сроки выполнения

Перед началом выполнения необходимо оценить задачу по срокам (с учётом собственной загруженности и количества свободного времени) и сообщить нам.

### Прочее

Предлагается выполнить одно из трёх заданий на выбор. Первое задание относится к разработке прототипа нового мобильного приложения, последующие — к улучшению существующего веб-приложения, код которого доступен в [open-source репозитории](https://github.com/mytonwalletorg/mytonwallet).

## ⭐️ Задание 1. Нативное мобильное приложение

<img width="1512" alt="Screenshot 2023-02-21 at 21 00 34" src="https://user-images.githubusercontent.com/102837730/220446253-d14715d3-e773-4dce-85ea-3c36fca96572.png">

**Оплата** в случае успешного найма: до _$3000_ за каждую платформу.

**Вознаграждение** при правильном выполнении задания, но при отсутствии последующего найма: до _$750_ за каждую платформу.

**Описание.** Предлагается разработать MVP мобильных приложений для iOS и/или Android в соответствии с [дизайн-макетами](https://www.figma.com/file/4zlzG0ShKBrhxT6yUZlqtk/MyTonWallet-Design-Mobile-Public?node-id=0%3A1&t=6sQFwq4lfEtj8XS5-0). В MVP должны быть реализованы все экраны авторизации (_Start_, _Creating Wallet_, _Import_), а также главный экран (_Home_) с возможностью просмотра списка доступных токенов (_Assets_) и лентой транзакций (_Activity_) в режиме infinite scroll. Дополнительные экраны (_Token Activity_, _Send_, _Receive_, _Settings_ и т.д.) не являются обязательными, но их реализация может оказаться дополнительным плюсом при оценивании. Наличие ночной темы также опционально. Интерфейс должен быть полностью анимированным по примеру актуальной веб-версии.

Выбор стека технологий остаётся на усмотрение кандидата. Допустимо использование гибридных технологий (например, React Native). При этом вероятно, что реализации с использованием нативных технологий (Swift, Kotlin) могут быть оценены выше из-за более точного соответствия основным критериям.

Важным условием является **переиспользование существующей JavaScript-абстракции** для работы с криптографическими функциями, обращений к блокчейну и эндпоинтам api.mytonwallet.org (папка [/src/api](https://github.com/mytonwalletorg/mytonwallet/tree/master/src/api) в текущем репозитории). Прослойка должна запускаться в виде отдельного JavaScript-процесса внутри мобильного приложения (вне зависимости от основной выбранной технологии) и общаться с основным процессом с помощью сообщений провайдера (см. примеры в `/src/api/providers`).

В целом привествуется сохранение общей архитектуры и стилистики кода основного проекта.

## ⭐️ Задание 2. Раздел Connected Dapps в Настройках

<img width="460" alt="Screenshot 2023-02-28 at 20 24 58" src="https://user-images.githubusercontent.com/102837730/221957841-528c0ab1-5f5c-45aa-ae2e-713c1b25f23c.png">

**Оплата** в случае успешного найма: до _$1000_.

**Вознаграждение** при правильном выполнении задания, но при отсутствии последующего найма: до _$250_.

**Описание.** В режиме расширения для Chrome поддерживается протокол TON Connect для подключения dapp-сайтов (например, getgems.io, tegro.finance и т.п.) Предлагается добавить в Настройках раздел управления подключёнными dapp-сайтами согласно [макетам](https://www.figma.com/file/4zlzG0ShKBrhxT6yUZlqtk/MyTonWallet-Design-Mobile-Public?node-id=3277%3A33896&t=vcntzMfbHADbRQrk-0).

## ⭐️ Задание 3. Экран Swap

<img width="120" alt="Screenshot 2023-02-28 at 20 27 26" src="https://user-images.githubusercontent.com/102837730/221958398-d71d928c-b8ea-430d-a875-e315643902cc.png">

**Оплата** в случае успешного найма: до _$500_.

**Вознаграждение** при правильном выполнении задания, но при отсутствии последующего найма: до _$100_.

**Описание.** Предлагается добавить на главный экран кнопку Swap (согласно макетам). При её нажатии происходит переход к [экрану Swap](https://www.figma.com/file/4zlzG0ShKBrhxT6yUZlqtk/MyTonWallet-Design-Mobile-Public?node-id=2632%3A48601&t=vcntzMfbHADbRQrk-0) (открытие модального окна/панели). Т.к. добавление токенов пока недоступно, небходимо использовать mock-данные для списка доступных токенов и их балансов. С учётом этих mock-данных нужно обрабатывать ошибки — например, когда вводится количество, превышающее баланс (по аналогии с экраном Send).

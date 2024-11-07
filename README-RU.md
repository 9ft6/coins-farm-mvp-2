# О проекте

Author tg: [@9ft6](https://t.me/dev9ft6)

Developer tg chat: [CoinsFarmDevChat](https://t.me/CoinsFarmDevChat)

## Кратко
Проект представляет собой приватное решение, разработанное за четыре месяца и 
прошедшее текущую стадию завершения. В настоящее время оно тестируется на 5000 
аккаунтах Telegram для четырёх игр: **Blum**, **Cats**, **HamsterKombat** и 
**NotPixel**. Продолжается, и начат этап создания MVP-3, который займёт около 
3-4 месяцев. Планируется завершение этого этапа в январе-феврале 2025 года, 
когда будет выпущена публичная версия для желающих попробовать проект.

## Сущности / Entities
### Аккаунты / Accounts
- Импорт аккаунтов с помощью drag-and-drop в браузере в любом формате: TData, сессия, JSON.
- Валидация поступающих данных с отслеживанием.
- Монопольный доступ к аккаунтам осуществляется через собственный контроллер, который отслеживает все действия на аккаунте и устанавливает безопасные таймауты на каждое действие, предотвращая бан.
- Каждому аккаунту при импорте генерируется случайное мобильное устройство с уникальным, реалистичным синтетическим "фингерпринтом", который будет использоваться повсеместно.
- К каждому аккаунту привязываются прокси из прокси-пула (proxyverse) с нужной геолокацией, и все действия на аккаунте выполняются с этого гео.
- Возможность генерировать TON-кошельки разных версий различными способами для дальнейших манипуляций.
- На каждом аккаунте можно регистрировать различные приложения и запускать задачи.
- Хранит авторизационные данные приложений.
- Хранит статистику использования приложений.

### Приложение / Application
- Приложения представляют собой группу задач, сгруппированных по принадлежности к конкретному приложению, такому как **Blum**, **Cats**, **HamsterKombat** или **NotPixel**.
- У каждого приложения есть собственный раннер задач — отдельный микросервис, который запускает и останавливает задачи для своего приложения.

### Задача / Task
- Задача представляет собой алгоритм действий, выполняемый для конкретного аккаунта и приложения.
- Параметры задачи настраиваются при запуске.
- Задача в реальном времени сообщает о своем состоянии системе.
- Может управляться или изменять свое поведение в процессе выполнения централизованно.
- Имеет систему уведомлений и жизненный цикл.
- Может откладывать выполнение в зависимости от условий.
- Может быть создана другими задачами, что удобно, например, для создания сложных реферальных деревьев.

![Tasks Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic1.png)

![Task List Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic2.png)

![Applications Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic3.png)
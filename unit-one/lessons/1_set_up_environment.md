# Настройка среды разработки

Добро пожаловать на вводный курс по Sui Move. В данном разделе рассматривается процесс настройки среды разработки для взаимодействия с Sui Move. В завершение будет создан базовый проект Hello World, как вводный проект для комфортного старта в экосистеме Sui.

## Локальная установка бинарных файлов Sui

1. Для начала необходимо подготовить [зависимости, соответствующие операционной системе](https://docs.sui.io/build/install#prerequisites)

2. Для установки бинарных файлов Sui применяется следующая команда:
    
    `cargo install --locked --git https://github.com/MystenLabs/sui.git --branch devnet sui`

    При необходимости переключения на другую сеть, целевой branch может быть изменён на `testnet` или `mainnet`.

   *Для пользователей Linux: Во время установки могут создаваться временные сборочные файлы в каталоге /tmp. В случае возникновения проблем, связанных с нехваткой дискового пространства, может потребоваться увеличение размера tmpfs как минимум до 11 ГБ.*
    ```
   Для проверки использования tmpfs на Linux используется команда:
   
   df /tmp
   
   Расширение tmpfs возможно через редактирование файла /etc/fstab с установкой размера в 20 ГБ:
   
   tmpfs          /tmp        tmpfs   noatime,size=20G,mode=1777   0 0
    ```

4. Проверка успешности установки:

    `sui --version`

    При корректной установке в терминале отобразится номер версии.

## Использование Docker-образа с предустановленным Sui

1. [Предполагается наличие установленного Docker](https://docs.docker.com/get-docker/)

2. Загрузка официального образа осуществляется с помощью:

    `docker pull mysten/sui-tools:devnet`

3. Запуск и вход в контейнер Docker осуществляется командами:

    `docker run --name suidevcontainer -itd mysten/sui-tools:devnet`

    `docker exec -it suidevcontainer bash`

*💡Примечание: В случае несовместимости образа с архитектурой процессора, возможно использование базового Docker-образа с [Rust](https://hub.docker.com/_/rust), подходящего под архитектуру системы, с последующей установкой бинарных файлов Sui вручную, как описано ранее.*

## (Дополнительно) Настройка среды разработки в VS Code с использованием плагина Move Analyzer

1. [Плагин Move Analyzer](https://marketplace.visualstudio.com/items?itemName=move.move-analyzer) доступен в Visual Studio Marketplace.

2. Для поддержки адресов кошельков в формате Sui предусмотрена установка:

    `cargo install --git https://github.com/move-language/move move-analyzer --features "address20"`

## Основы работы с интерфейсом командной строки Sui (CLI)

[Справочная страница](https://docs.sui.io/build/cli-client)

### Инициализация

- На вопрос `Do you want to connect to a Sui Full node server?` введите `Y`. Затем нажатием `Enter` будет использоваться Devnet по умолчанию.
- Для выбора схемы генерации ключей [`ed25519`](https://ed25519.cr.yp.to/) используется значение `0` .

### Работа с сетями

- Для переключения между сетями используется команда: `sui client switch --env [network alias]`
- Существуют стандартные псевдонимы сетей: 
    - localnet: http://0.0.0.0:9000
    - devnet: https://fullnode.devnet.sui.io:443
- Просмотр всех текущих псевдонимов сетей: `sui client envs`
- Для добавление нового псевдонима сети: `sui client new-env --alias <ALIAS> --rpc <RPC>`
    - Пример добавления testnet: `sui client new-env --alias testnet --rpc https://fullnode.testnet.sui.io:443`

### Проверка активного адреса и объектов газа

- Список текущих адресов: `sui client addresses`
- Активный адрес: `sui client active-address`
- Все контролируемые объекты газа: `sui client gas`

## Получение токенов Sui для сетей Devnet или Testnet

1. [Нужно присоединиться к Discord Sui.](https://discord.gg/sui)
2. Выполните шаги верификации
3. Для получения токенов devnet канал  [`#devnet-faucet`](https://discord.com/channels/916379725201563759/971488439931392130), а для токенов testnet - канал [`#testnet-faucet`](https://discord.com/channels/916379725201563759/1037811694564560966) 
4. Введите команду: `!faucet <WALLET ADDRESS>`


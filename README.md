# Вводный курс по Move

Вводный курс по языку Move, поддерживаемый [Sui Foundation](https://suifoundation.org/).

## Содержание

- **Раздел первый: Настройка среды и Hello World**
    - [Настройка среды разработки](./unit-one/lessons/1_set_up_environment.md)
    - [Структура проекта Sui](./unit-one/lessons/2_sui_project_structure.md)
    - [Пользовательские типы и способности](./unit-one/lessons/3_custom_types_and_abilities.md)
    - [Функции](./unit-one/lessons/4_functions.md)
    - [Публикация контракта](./unit-one/lessons/5_contract_deployment.md)
- **Unit Two: Working with Sui Objects** (не переведено)
    - [Introduction](./unit-two/lessons/1_working_with_sui_objects.md)
    - [Ownership](./unit-two/lessons/2_ownership.md)
    - [Parameter Passing and Object Deletion](./unit-two/lessons/3_parameter_passing_and_object_deletion.md)
    - [Object Wrapping](./unit-two/lessons/4_object_wrapping.md)
    - [Object Wrapping by Example](./unit-two/lessons/5_object_wrapping_example.md)
    - [Capability Design Pattern](./unit-two/lessons/6_capability_design_pattern.md)
    - [Events](./unit-two/lessons/7_events.md)
- **Unit Three: Fungible Tokens**(не переведено)
    - [Sui Framework](./unit-three/lessons/1_sui_framework.md)
    - [Intro to Generics](./unit-three/lessons/2_intro_to_generics.md)
    - [Witness Design Pattern](./unit-three/lessons/3_witness_design_pattern.md)
    - [The `Coin` Resource and `create_currency` Method](./unit-three/lessons/4_the_coin_resource_and_create_currency.md)
    - [Managed Coin Example](./unit-three/lessons/5_managed_coin.md)
    - [`Clock` and Locked Coin](./unit-three/lessons/6_clock_and_locked_coin.md)
    - [Unit Testing](./unit-three/lessons/7_unit_testing.md)    
- **Unit Four: Marketplace**(не переведено)
    - [Homogeneous Collections](./unit-four/lessons/1_homogeneous_collections.md)
    - [Dynamic Fields](./unit-four/lessons/2_dynamic_fields.md)
    - [Heterogeneous Collections](./unit-four/lessons/3_heterogeneous_collections.md)
    - [Marketplace Contract](./unit-four/lessons/4_marketplace_contract.md)
    - [Deployment and Testing](./unit-four/lessons/5_deployment_and_testing.md)
- **Unit Five: Sui Kiosk**(не переведено)
    - [Programmable Transaction Block](./unit-five/lessons/1_programmable_transaction_block.md)
    - [Hot Potato Design Pattern](./unit-five/lessons/2_hot_potato_pattern.md)
    - [Sui Kiosk Basic Concepts](./unit-five/lessons/3_kiosk_basics.md)
    - [Sui Kiosk Basic Usage](./unit-five/lessons/4_kiosk_basic_usage.md)
    - [Transfer Policy](./unit-five/lessons/5_transfer_policy.md)
- **Advanced Topics**(не переведено)
    - [BCS Encoding](./advanced-topics/BCS_encoding/lessons/BCS_encoding.md)

## TODOs

- [x] Написать урок про BCS в Advanced Topics
- [x] Создать мультиплатформенный Docker-образ
- [ ] Добавить упражнения для каждого раздела
- [ ] Добавить материал про Display.move
- [x] Добавить материал про clock и пример разблокировки токена
- [ ] Написать урок по closed loop token standard
- [ ] Написать урок по обновлению пакетов
- [ ] Написать новый урок по киоскам
- [x] Проверить и обновить раздел первый в соответствии с последней версии Sui
- [ ] Проверить и обновить раздел второй в соответствии с последней версии Sui
- [ ] Проверить и обновить раздел третий в соответствии с последней версии Sui
- [ ] Проверить и обновить раздел четвёртый в соответствии с последней версии Sui
- [ ] Проверить и обновить раздел Advanced Topics в соответствии с последней версии Sui

## Общие ресурсы для разработчиков

- [Sui Developer Documentation](https://docs.sui.io/build)
- [Sui Developer Portal](https://sui.io/developers)
- [Sui GitHub](https://github.com/MystenLabs/sui)
- [Sui Framework Documentation](https://github.com/MystenLabs/sui/tree/main/crates/sui-framework/docs)
- [Sui Typescript SDK (official)](https://github.com/MystenLabs/sui/tree/main/sdk/typescript)
- [Sui Typescript SDK (community)](https://github.com/scallop-io/sui-kit)
- [Sui Rust SDK (official)](https://github.com/MystenLabs/sui/tree/main/crates/sui-sdk)
- [Sui Golang SDK (community)](https://github.com/coming-chat/go-sui-sdk)
- [Sui Python SDK (community)](https://github.com/FrankC01/pysui)
- [Sui Java SDK (community)](https://github.com/GrapeBaBa/sui4j)
- [Sui Kotlin SDK (community)](https://github.com/cosmostation/suikotlin)
- [Sui C# SDK (community)](https://github.com/d-moos/SuiNet)
- [Sui Dart SDK(community)](https://github.com/mofalabs/sui)
- [Sui Explorer](https://suiexplorer.com/)

## Социальные сети и сообщества

Если есть желание присоединиться к онлайн-сообществу Sui, можно воспользоваться следующими ссылками:

- [Sui Network Twitter](https://twitter.com/SuiNetwork) 
- [Sui Official Discord](https://discord.gg/sui)
- [Sui Developer Forums](https://forums.sui.io/)

## Переводы репозитория

- [x] Английский
- [x] [Китайский](https://github.com/RandyPen/sui-move-intro-course-zh)
- [x] [Тайский](https://github.com/Contribution-DAO/sui-move-intro-course-thai)

Если есть желание помочь с переводом на другие языки, [свяжитесь с нами](mailto:henry@sui.io).

## Видео и другие форматы

- [x] Видео-серия от Encode Club (английский) [плейлист на YouTube](https://www.youtube.com/playlist?list=PLfEHHr3qexv_aE7p6oDyVtD3WQsDsJngr) | [уроки и код](https://github.com/sui-foundation/encode-sui-educate)
- [x] Видео от BuidlerDAO (китайский) [ссылка](https://www.bilibili.com/video/BV1RY411v7YU)
- [x] Курс от MoveBit по Move в Sui (английский) [плейлист на YouTube](https://www.youtube.com/playlist?list=PL3id4Z64z2sNED_aH7UYIFFwy6MsvKCN9) | [уроки и код](https://github.com/movebit/sui-course-2023)

## FAQ

1. Могу ли я использовать содержимое этого репозитория для создания других обучающих материалов, связанных с Sui или языком программирования Sui Move?

    Да. Это изначально и было целью репозитория — позволить создателям контента и образовательным платформам использовать и расширять материалы внутри этого репозитория для создания различных форм медиа или технического контента о Sui или языке Sui Move.

    Этот репозиторий лицензирован под лицензией Creative Commons; а именно [лицензия CC-BY-SA-4.0](https://github.com/sui-foundation/sui-move-intro-course/blob/main/LICENSE). Это позволяет любому модифицировать, строить на его основе, распространять и использовать содержимое репозитория для любых целей, при условии, что производное содержимое также лицензировано под той же лицензией и с указанием источника.

2. Как можно внести вклад в этот репозиторий?

    Сделайте форк и откройте Pull Request в основной репозиторий. Мы открыты для вклада сообщества.




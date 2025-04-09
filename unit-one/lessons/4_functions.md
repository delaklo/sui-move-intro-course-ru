# Функции

В этом разделе рассматриваются функции в Sui Move, а также будет создана первая функция в рамках примера Hello World.

## Видимость функций

Функции в Sui Move имеют три типа видимости:

- **private**: видимость по умолчанию; доступ возможен только для функций внутри текущего модуля
- **public**: функция доступна как внутри текущего модуля, так и из других модулей
- **public(package)**: функция доступна для функций модулей внутри того же пакета.

## Возвращаемое значение

Тип возвращаемого значения функции указывается после списка параметров через двоеточие.

Последняя строка функции без точки с запятой считается возвращаемым значением.

Пример:

```move
    public fun addition (a: u8, b: u8): u8 {
        a + b    
    }
```

<!--
## Entry Functions

In Sui Move, entry functions are simply functions that can be called by transactions. They must satisfy the following three requirements:

- Denoted by the keyword `entry`
- have no return value
- (optional) have a mutable reference to an instance of the `TxContext` type in the last parameter

-->

## Контекст транзакции

Функции, вызываемые напрямую через транзакцию, обычно имеют экземпляр `TxContext` в качестве последнего параметра. Этот параметр автоматически передаётся виртуальной машиной Sui Move и его не надо указывать вручную при вызове функции.

Объект `TxContext` содержит [важную информацию](https://github.com/MystenLabs/sui/blob/main/crates/sui-framework/packages/sui-framework/sources/tx_context.move) использованной для вызова входной функции, такую как адрес отправителя,хеш транзакции, эпоху и т.д.

## Создание функции `mint`

Функция чеканки (mint) в примере Hello World выглядит следующим образом:

```move
    public fun mint(ctx: &mut TxContext) {
        let object = HelloWorldObject {
            id: object::new(ctx),
            text: string::utf8(b"Hello World!")
        };
        transfer::public_transfer(object, tx_context::sender(ctx));
    }
```

Эта функция создаёт новый экземпляр пользовательского типа `HelloWorldObject`, после чего вызывает системную функцию [`public_transfer`](https://github.com/MystenLabs/sui/blob/main/crates/sui-framework/docs/sui/transfer.md#function-public_transfer) из фреймворка Sui для передачи созданного объекта отправителю транзакции.



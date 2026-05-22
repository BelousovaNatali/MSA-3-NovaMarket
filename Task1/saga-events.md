# Реестр событий Saga-хореографии оформления заказа

| Этап                               | Тип события   | Название                   |
|------------------------------------|---------------|----------------------------|
| Заказ создан                       | domain        | `OrderCreated`             |
| Товары проверены и зарезервированы | domain        | `ItemsReserved`            |
| Ошибка резервирования товаров      | failure       | `ItemsReservationFailed`   |
| Оплата запрошена                   | domain        | `PaymentRequested`         |
| Оплата успешно проведена           | domain        | `PaymentSucceeded`         |
| Ошибка оплаты                      | failure       | `PaymentFailed`            |
| Возврат платежа                    | compensation  | `PaymentRefunded`          |
| Снятие резерва товаров             | compensation  | `ItemsReservationCanceled` |
| Заказ подтверждён                  | domain        | `OrderConfirmed`           |
| Заказ отменён                      | domain        | `OrderCancelled`           |
| Заявка на доставку создана         | domain        | `DeliveryRequested`        |
| Превышено время ожидания оплаты    | timeout       | `PaymentTimeout`           |
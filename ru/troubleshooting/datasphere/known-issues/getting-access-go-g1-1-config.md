# Получение доступа к конфигурациям GPU g1.1 и выше в DataSphere


## Описание задачи {#issue-description}

При попытке задействовать в DataSphere конфигурацию GPU g1.1 или выше отображается сообщение об ошибке:

* `Access Denied: Spec g1.1 is not available for your cloud. Please contact your administrator or Support`

## Решение {#issue-resolution}

Доступ к конфигурации g1.1 для DataSphere открывается после перехода на платное потребление и пополнения лицевого счёта на сумму от 500 рублей. Об этом мы пишем [в разделе «Лимиты» в документации DataSphere](../../../datasphere/concepts/limits.md).
GPU — достаточно востребованный ресурс. Мы хотим, чтобы все пользователи имели возможность протестировать свои сценарии в Yandex Cloud в полной мере, поэтому мы просим пополнить баланс.

Обратите внимание, что после перехода на платное потребление для оплаты ресурсов в первую очередь будут использоваться активные гранты. Средства с лицевого счёта начнут списываться только после того, как средства гранта будут потрачены, или истечёт срок его действия. Подробнее об этом – [в разделе «Цикл оплаты» в документации на Cloud Billing](../../../billing/payment/billing-cycle-individual.md).

Чтобы воспользоваться платформой g1.1, пополните баланс лицевого счёта на необходимую сумму, а затем сделайте следующее:

1. Остановите вычисления и выйдите из проекта с помощью **File** → **Stop IDE executions**.
2. Войдите в проект повторно из консоли Yandex Cloud.

Правила тарификации ресурсов внутри проектов представлены [в соответствующем разделе документации DataSphere](../../../datasphere/pricing.md)

## Если проблема осталась {#if-issue-still-persists}

Если вышеописанные действия не помогли решить проблему, [создайте запрос в техническую поддержку](https://console.cloud.yandex.ru/support?section=contact).
В запросе укажите следующую информацию:

1. Идентификатор сообщества DataSphere;
2. Желаемый тип GPU-конфигурации, к которой требуется получить доступ;
3. Подробный сценарий использования GPU-конфигурации в вашем проекте DataSphere.

# Устранение ошибок доступа к бакету с назначенной политикой безопасности


## Описание проблемы {#issue-description}

* При попытке получить доступ к бакету с назначенной политикой из интерфейса Консоли управления отображается ошибка «Access Denied»;
* Не удаётся отобразить спискок объектов в бакете назначенной политикой безопасности.

## Диагностика и воспроизведение

Проверьте наличие политик безопасности на бакете.

## Решение {#issue-resolution}

Отредактируйте политику таким образом, чтобы в поле  «Ресурс» находилось название бакета без `/*`.
Это требуется для выполнения действий с бакетом, в то время как указание бакета с `/*` распространяется на действия с объектами внутри бакета.

## Если проблема осталась {#if-issue-still-persists}

Если вышеописанные действия не помогли решить проблему, [создайте запрос в техническую поддержку](https://console.cloud.yandex.ru/support?section=contact).
В запросе укажите следующую информацию:

1. Имя бакета в Object Storage;
2. Описание проблемы.
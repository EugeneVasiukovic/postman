# postman

# Методы запроса
## Get - запрашивает ресурс, данный запрос только получает данные, являетсе идемпотентным методам запроса, является безапасным т.к. не меняет состояние сервера. другими словами безопасный метод проводит операцию "только на чтение". не имеет тело (принято сообществом программистов), а так может иметь тело если ты богахульник. Является кэшируемым, то есть можно сохраненить ответ для дальнейшего восстановления и использования позже. Кэширование используется для снижения числа запросов на сервер.

## head - запрашивает ресурс как и метод ` GET ` не имеет тела ответа. используется для проверки работаспособности сервера, и чтенения метаданных, является идемпотентным методам запроса, является безопастным т.к. не меняет состояния сервера, другими словами безопастный метод проводит операцию "только на чтение". не имеет тела запроса, является кэшируемы, то есть можно сохранить ответ для дальнешего востоновления и использования. Кэширование используется для снижения числа запросов на сервер.

## POST - используется для отправки сущностей на сервер. Вызыввает изменения состояния или какие-то побочные эффекты на сервере. не является идемпотентным, т.к. повтрным запрос может изменить ответ или полученные данные с сервера пример: добавление в карзину товара, повторное отправление может добавить дополнительную еденицу товара, оплата товара если повторно отправить запрос на опалту, скорее всего ты оплатишь товара дважды, не является безапастным, т.к. отправляя запрос на сервер мы запрашиваем изменения состояния, внося новые данные. может быть кешируемый если внести если внесены настройки ` cash-control ` используется для задания инструкций кеширования как для запросов, так и для ответов.
> ` cach-comtrol и  expires ` - являются идикаторами свежасти

## PUT - используется для изменения или обновления ресурса. Имеет тело запроса и тело должно содержать обновленные данные ресурся полностью или только обновляемую часть. Является идемпотентнвм т.к. повторное отправление одного и тогоже не повлекут за собой изменений и ответ будет одним и темже (при условии отправки ожних и тех же данных). не явялется безопасным т.к. влечет за собой изменения состояния сервера, внося новые данные. не является кешируемым

## DELETE -  используется для удаления сущностей. является идемпотентным методам (при повтрный запрос на удаление закончится также), не является идемпонтентым когда происходи декрмент счетчки в данном случае,  не явялется безопасным т.к. влечет за собой изменения состояния сервера, внося новые данные. не является кешируемым

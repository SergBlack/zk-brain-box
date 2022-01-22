202201222027
Tags: #clouds #aws 

--- 
# Lambda Invocation
## Invocation models
- Push model
- Pull model

## Invocation Types
- RequestResponse (sync) - возвращает респонс сервису, который сделал запрос
- Event (async) - лямбда обрабатывает какое-то событие, например из SQS, и далее SQS не нужно знать о том, как обработалось событие, то есть тут ничего не возвращается в SQS обратно
- DryRun - используется например когда через Serverless вызываем лямбду через команду invoke

--- 
### Links
- [[]]
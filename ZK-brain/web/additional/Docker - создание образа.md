202202242316
Tags: #virtualization 

--- 
# Docker - создание образа
При создании своего образа всегда указывается базовый образ и все слои нового создаваемого образа, добавляются к слоям базового образа.

Этапы создания:
- для создания образа нужен `Dockerfile`;
- обычно он помещается в корень проекта;
- `Dockerfile` содержит в себе инструкции по созданию образа;
- при создании образа можно указать `имя` и `тег` для образа;
- на основе готового образа можно создавать контейнеры.

--- 
### Links
- [[Dockerfile]]
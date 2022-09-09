202209090835
Tags: #fundamentals 

--- 
# OOP. Polymorphism
Allows for the uniform treatment of classes in a hierarchy.
Object from child classes share the same interface as their parent (super) class. We can change the behavior of a child class by overriding parent methods. At run-time the appropriate method will be called depending on the type of object.

Polymorphism - наследование методов и полей от родительского (супер) класса. Наследник может переопределить какие-то методы и поля чтобы изменить поведение по умолчанию.

## Example
У нас есть много разных фигур, все они наследуются от некого класса Shape, если мы вызовем у каждой фигуры метод draw(), они отрисуются каждая по своему, так как мы переопределили для каждого наследника этот метод
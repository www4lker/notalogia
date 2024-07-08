---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/metodos-e-fucoes-em-python-explicados/","tags":["python","oop","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# metodos e fuções em python explicados

## criado em: 
-  08-05-2023 - 16:11

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/LATAM 2023 - 3.5 Section 5 – sorting simple lists\|LATAM 2023 - 3.5 Section 5 – sorting simple lists]]
- 
- tags: #python #oop #ANELO 
- Fontes & Links: 

---

## Let's talk about methods and functions

Both methods and functions are types of code that allow you to perform specific tasks. **A function is a piece of code that doesn't belong to any specific data - it can take in data, manipulate it, and produce a result**. In other words, you can think of a function as a stand-alone piece of code that can be called from anywhere in your program.

On the other hand, **a method is a specific type of function that is associated with a particular piece of data**. A method can take in data, manipulate it, produce a result, and also change the state of the data it's associated with. So, you can think of a method as a function that's tied to a specific piece of data.

For example, let's say you have a piece of data called "person". You could have a method called "walk" that's associated with that person. When you call the "walk" method on the "person" data, it will change the state of the person and make them walk.

It's important to note that because methods are associated with specific data, they need to be called with that data in mind. This means that when you call a method, you need to specify which data you want to call the method on.

In summary, a method is a specific type of function that's associated with a particular piece of data. It can manipulate that data, produce a result, and change the data's state. In contrast, a function is a stand-alone piece of code that can take in data, manipulate it, and produce a result.

---

## Let's talk about how the concept of methods and functions applies to object-oriented programming (OOP)

In OOP, a "class" is a blueprint for creating objects, which are instances of the class. Each object created from a class has its own set of data and behaviors.

A "method" in OOP is a special type of function that is associated with an object. It defines the behaviors that the object can perform. For example, let's say you have a class called "Dog". You could define a method called "bark" that's associated with the Dog class. When you create an object from the Dog class, you can call the "bark" method on that object, and the dog will bark.

Here's an example of what the Dog class might look like in Python:



```python
class Dog:
    def __init__(self, name):
        self.name = name
        
    def bark(self):
        print(self.name + " says woof!")

```
Now, let's create an object from the Dog class and call the `bark` method:


```python
my_dog = Dog("Fido") 
my_dog.bark() # prints "Fido says woof!"
```


As you can see, we've created an object called `my_dog` from the Dog class and called the `bark` method on that object. This causes the `bark` method to execute and print out the message "Fido says woof!".

**In summary, in OOP, a method is a special type of function that's associated with an object.** It defines the behaviors that the object can perform. By calling a method on an object, you can cause that object to perform the behavior defined by the method.
---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/python-2-and-python-3-md/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# List the main differences between Python 2 and Python 3

## criado em: 
-  30-04-2023 - 11:30

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/comparando Javascript com Python\|comparando Javascript com Python]]
- tags: #python #ANELO 
- Fontes & Links: 

---

Python 2 and Python 3 are both popular versions of the Python programming language. However, they have some significant differences. Here are the main differences between Python 2 and Python 3:

1.  Print statement: The print statement in Python 2 does not require parentheses, while in Python 3, it does. In Python 2, you can use the statement like this: `print "Hello, World!"`, while in Python 3, you need to use parentheses like this: `print("Hello, World!")`.
    
2.  Division operator: In Python 2, if you divide two integers, the result will be an integer, while in Python 3, the result will be a float. For example, in Python 2, `5/2` will return `2`, while in Python 3, `5/2` will return `2.5`.
    
3.  Unicode: Python 2 uses ASCII by default for string handling, while Python 3 uses Unicode. In Python 3, you can handle a wider range of characters, including emoji and other non-ASCII characters.
    
4.  range() function: In Python 2, the range() function returns a list, while in Python 3, it returns a range object. This change was made to improve performance.
    
5.  Error handling: The syntax for error handling has changed in Python 3. In Python 2, you can use the statement `except Exception, e` to catch an exception and get the error message, while in Python 3, you need to use `except Exception as e`.
    
6.  Function arguments: In Python 2, you can define functions with default argument values like this: `def my_func(arg1, arg2=10)`. In Python 3, you can define them like this: `def my_func(arg1, arg2=10, /)`.
    
7.  Handling libraries: Many libraries that were available for Python 2 have not been updated to work with Python 3. If you need to use a library that is only available for Python 2, you may need to use Python 2 instead of Python 3.
    

These are some of the main differences between Python 2 and Python 3. It's important to note that Python 2 is no longer supported, and Python 3 is the recommended version for new projects.
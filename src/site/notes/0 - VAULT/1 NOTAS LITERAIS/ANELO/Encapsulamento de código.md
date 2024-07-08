---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/encapsulamento-de-codigo/","tags":["python","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Encapsulamento de código

## criado em: 
-  20-05-2023 - 11:11

### Conteúdo Relacionado
- notas: 
- tags: #python #ANELO 
- Fontes & Links: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python__entendendo a orientação a objetos 1 de 6\|Python__entendendo a orientação a objetos 1 de 6]]

---

O encapsulamento de código é um conceito relacionado à organização do código e à ocultação de detalhes de implementação. Em Python, podemos encapsular o código em funções e classes. O encapsulamento ajuda a tornar o código mais modular, legível e reutilizável.

No contexto das classes, o encapsulamento é frequentemente alcançado usando modificadores de acesso, como público, privado e protegido. Em Python, não há modificadores de acesso explícitos como em algumas outras linguagens. No entanto, a convenção é usar um sublinhado simples `_` para indicar que um atributo ou método é "privado" e deve ser tratado como tal.

```python
class Exemplo:
    def __init__(self):
        self._atributo_privado = 42

    def _metodo_privado(self):
        return self._atributo_privado * 2

    def metodo_publico(self):
        resultado = self._metodo_privado()
        return resultado


```

Nesse exemplo, o atributo `_atributo_privado` e o método `_metodo_privado` são considerados "privados" por convenção, embora ainda possam ser acessados externamente. O método `metodo_publico` é considerado "público" e pode ser chamado normalmente.    

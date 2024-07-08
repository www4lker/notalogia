---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/jogo-de-palavras-em-python/","tags":["python","chatgpt","gamedev","ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true}
---

# JOGO DE PALAVRAS EM PYTHON

## criado em: 
-  12-05-2023 - 10:36

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/implementação de hangman para wordle\|implementação de hangman para wordle]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/PYTHON AVANÇANDO NA LINGUAGEM - 7 DE 7\|PYTHON AVANÇANDO NA LINGUAGEM - 7 DE 7]]
- tags: #python #chatgpt #gamedev #ANELO 

---
Depois da aula na alura fomos capazes de desnevolver um jogo da forca. Mas me interessa fazer ele mais como Wordle. E colocar no mundo. 
Eis o arquivo original e depois o que nós (chatgpt e eu) juntos:

``` python
import random  
  
  
def jogar():  
abertura_jogo()  
palavra_secreta = carrega_palavra_secreta()  
letras_acertadas = inicializa_letras_corretas(palavra_secreta)  
  
enforcou = False  
acertou = False  
erros = 0  
  
print(letras_acertadas)  
  
while not enforcou and not acertou:  
chute = pede_palpite()  
  
if chute in palavra_secreta:  
indexa_chute_correto(chute, letras_acertadas, palavra_secreta)  
else:  
erros += 1  
  
enforcou = erros == 6  
acertou = "_" not in letras_acertadas  
print(letras_acertadas)  
  
if acertou:  
imprime_mensagem_vencedor()  
else:  
imprime_mensagem_perdedor()  
  
  
# funções  
def abertura_jogo():  
print("*********************************")  
print("***Bem vindo ao jogo da Forca!***")  
print("*********************************")  
  
  
def carrega_palavra_secreta():  
arquivo = open("palavras.txt", "r")  
palavras = []  
  
for linha in arquivo:  
linha = linha.strip()  
palavras.append(linha)  
  
arquivo.close()  
  
numero = random.randrange(0, len(palavras))  
palavra_secreta = palavras[numero].upper()  
return palavra_secreta  
  
  
def inicializa_letras_corretas(palavra):  
return ["_" for letra in palavra]  
  
  
def pede_palpite():  
chute = input("Qual o seu palpite de letra? ")  
chute = chute.strip().upper()  
return chute  
  
  
def indexa_chute_correto(chute, letras_acertadas, palavra_secreta):  
index = 0  
for letra in palavra_secreta:  
if chute == letra:  
letras_acertadas[index] = letra  
index += 1  
  
  
def imprime_mensagem_vencedor():  
print("Você ganhou!!")  
  
  
def imprime_mensagem_perdedor():  
print("Você perdeu!!")  
  
  
if __name__ == "__main__":  
jogar()
```


![[ implementação de hangman para wordle\| implementação de hangman para wordle]]


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/0-vault/1-notas-literais/anelo/o-que-e-e-como-usar-flask/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# o que é e como usar FLASK

## criado em: 
-  12-05-2023 - 10:43

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/implementação de hangman para wordle\|implementação de hangman para wordle]]
- [[0 - VAULT/1 NOTAS LITERAIS/ANELO/JOGO DE PALAVRAS EM PYTHON\|JOGO DE PALAVRAS EM PYTHON]]
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/implementação de hangman para wordle\|implementação de hangman para wordle]]
- tags: #teoria #python #flask #ANELO 
---

O Flask é um framework leve e flexível para criação de aplicativos web em Python. Ele foi projetado para ser simples e fácil de usar, permitindo que os desenvolvedores construam aplicativos web rapidamente e com menos complexidade em comparação com outros frameworks mais robustos.

Aqui estão algumas maneiras pelas quais um aprendiz de programação Python pode se beneficiar do Flask:

1.  Fácil de aprender: O Flask possui uma curva de aprendizado suave, tornando-o acessível para iniciantes em programação. A documentação oficial do Flask é bem organizada e possui exemplos práticos que podem ajudar os iniciantes a entenderem os conceitos e começarem a desenvolver seus próprios aplicativos web.
    
2.  Leveza e simplicidade: O Flask adota uma abordagem minimalista, fornecendo apenas o básico necessário para criar aplicativos web. Ele não impõe muitas restrições e permite que você escolha as bibliotecas e ferramentas adicionais que deseja utilizar, o que é benéfico para iniciantes que desejam entender os componentes fundamentais de um aplicativo web.
    
3.  Flexibilidade: O Flask permite que você desenvolva aplicativos web de diferentes tamanhos e complexidades. Ele não possui uma estrutura rígida, permitindo que você crie seu próprio fluxo de trabalho e estrutura de diretórios. Isso é útil para iniciantes que desejam experimentar e explorar diferentes abordagens de desenvolvimento.
    
4.  Comunidade ativa: O Flask possui uma comunidade vibrante e ativa, com uma ampla variedade de recursos disponíveis, como tutoriais, cursos, blogs e fóruns. Isso significa que, como aprendiz de programação Python, você pode encontrar facilmente suporte e recursos adicionais para ajudá-lo a resolver problemas e expandir seus conhecimentos.
    
5.  Integração com outras bibliotecas e ferramentas: O Flask pode ser combinado com várias bibliotecas e ferramentas Python, permitindo que você aproveite a vasta gama de recursos disponíveis no ecossistema Python. Por exemplo, você pode usar bibliotecas como SQLAlchemy para interagir com um banco de dados, ou adicionar recursos de autenticação usando Flask-Login.
    
6.  Desenvolvimento rápido de protótipos: Devido à sua simplicidade e flexibilidade, o Flask é uma ótima escolha para o desenvolvimento rápido de protótipos. Isso permite que você experimente ideias rapidamente e valide conceitos antes de investir mais tempo e esforço no desenvolvimento completo de um aplicativo.
    

Em resumo, o Flask é uma ferramenta valiosa para um aprendiz de programação Python que deseja iniciar no desenvolvimento web. Ele oferece uma maneira simples de construir aplicativos web, permitindo que você se concentre nos conceitos fundamentais enquanto explora os princípios de desenvolvimento web.

---


Para implementar um jogo web usando Flask, você pode seguir os seguintes passos:

1. Configurar o ambiente:
   - Certifique-se de ter o Python instalado em seu sistema.
   - Instale o Flask usando o gerenciador de pacotes pip: `pip install flask`.

2. Crie uma estrutura básica do projeto:
   - Crie uma pasta para o seu projeto.
   - Dentro da pasta, crie um arquivo chamado `app.py` (ou qualquer outro nome de sua preferência).
   - Crie uma pasta chamada `templates` para armazenar os arquivos de modelo (templates) do Flask.
   - Crie uma pasta chamada `static` para armazenar os arquivos estáticos do jogo, como imagens, CSS e JavaScript.

3. Importe o Flask e defina uma rota:
   - No arquivo `app.py`, importe o Flask e crie uma instância da aplicação Flask.
   - Defina uma rota inicial para a página inicial do jogo.

   ```python
   from flask import Flask, render_template

   app = Flask(__name__)

   @app.route('/')
   def index():
       return render_template('index.html')
   ```

4. Crie um arquivo de modelo:
   - Dentro da pasta `templates`, crie um arquivo chamado `index.html` (ou qualquer outro nome relevante).
   - Projete o layout da página inicial do jogo nesse arquivo HTML.
   - Você pode usar HTML, CSS e JavaScript para criar a interface do jogo.

5. Adicione os arquivos estáticos:
   - Coloque todos os arquivos estáticos do jogo (imagens, CSS, JavaScript) na pasta `static` que você criou anteriormente.

6. Execute o aplicativo Flask:
   - No arquivo `app.py`, adicione o seguinte código para executar o aplicativo Flask.

   ```python
   if __name__ == '__main__':
       app.run(debug=True)
   ```

7. Inicie o servidor Flask:
   - No terminal, navegue até o diretório do projeto e execute o arquivo `app.py`.
   - Você verá uma mensagem informando que o servidor Flask está sendo executado.
   - Abra um navegador e acesse `http://localhost:5000` (ou qualquer outra porta fornecida na mensagem do servidor Flask).
   - Você deverá ver a página inicial do seu jogo.

A partir deste ponto, você pode expandir a implementação adicionando mais rotas ao seu aplicativo Flask para lidar com diferentes páginas do jogo, implementar lógica de jogo no lado do servidor usando Python e interagir com o front-end usando JavaScript.

Tenha em mente que Flask é um framework minimalista e pode não ser a melhor escolha para jogos complexos, especialmente se você precisar de recursos gráficos avançados. Nesse caso, você pode considerar usar frameworks específicos para jogos, como Pygame ou Unity, para criar seu jogo.

</div></div>


### Programação Orientada a Objetos
#### Erros e Exceções
---

### Motivação

Considere os métodos a seguir:

```python
@nome.setter
def nome(self, n):
    '''Set para o nome de uma pessoa'''
    if type(n) == str:
        self._nome = n
    else:
        print('n precisa ser do tipo string')
```

```python
def registraEntrada(self):
    '''Entra um carro'''
    if self.vagas > 0:
        self.vagas -= 1
        print("Um carro entrou.")
    else:
        print("Estacionamento sem vagas")
```
---

### Motivação

- O programa _apenas imprime_ uma mensagem de erro
- Entretanto, a execução do programa __continua__
- Como fazer para o programa encerrar a sua execução?

---

### Motivação

Mais ainda:

- Como __notificar__ o restante do programa que a
  execução do método não foi bem sucedida?
- Como __tratar/detectar__ (por exemplo, por quem chamou o método)
  que a execução do método não foi bem sucedida?
---

### Motivação

Estamos interessados em fazer o programa "emitir um erro":

- Emitir erro: notificar **e encerrar o programa**
- Fazer o programa "__Levantar uma exceção__"
    - Do inglês "*raise an exception*"
    - Também conhecido em português como "lançar uma exceção" ou
      "subir uma exceção"
---

### Motivação

Você já deve ter se deparado com alguns erros em Python:

- Índice não valido (fora dos limites): 
>`IndexError: list index out of range`

- Divisão por 0:
> `ZeroDivisionError: division by zero`
---

### Motivação

Você já deve ter se deparado com alguns erros em Python:

- Uma variável inexistente é utilizada:
> `NameError: name x is not defined`
---

### Objetivo

Apresentar o mecanismo de tratamento de exceções

- O que é uma exceção
- Como levantar exceções em Python
- Como tratar exceções em Python
- Como implementar classes que representam exceções em Python
---

### Exceções e Tratamento

- Uma _exceção_ é um __erro__ não necessariamente fatal detectável na execução de um programa
    - Diferente de erro de compilação
- Para **levantar uma exceção**,  utilizamos o comando `raise`
    - Similar ao comando `throw` de Java e C++
---

### Exceções e Tratamento

- `Exception` é a _superclasse_ das exceções definidas pelo usuário
- A lista de classes de exceções predefinidas em Python está
  [aqui](https://docs.python.org/3/library/exceptions.html)
---

### Exceções e Tratamento
<img src="python_excecoes.png">

(Imagem de [*Stanford Python Course* (link)](https://drive.google.com/file/d/0B-eHIhYpHrGDWUtObjZ5MDI0dHc/view))
---

### Tratamento de Exceções

- Após levantada, uma exceção pode ser **tratada**
- Tratamento de exceções: trecho de código responsável por fazer o programa se
  __recuperar__ da exceção levantada
- De acordo com a _classe da exceção_, o programa pode tratá-la de forma diferente
---

### Ideia Geral 

- A cláusula `try` contém um bloco de código que _pode_ levantar exceções. 
  Ela __tenta__ executar o bloco de comando nela contido
- Se uma exceção for levantada dentro do `try`,
  o fluxo do programa é _redirecionado_ para a cláusula `except`

```python
try:
    # Tenta executar o bloco
except: 
    #tratamento
```
---

### Exceções

Mais detalhes sobre exceções
no [Notebook](14-excecoes.ipynb)

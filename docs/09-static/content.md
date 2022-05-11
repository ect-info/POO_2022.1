### Programação Orientada a Objetos
#### Atributos e Métodos de Classe
---

### Objetivo

Apresentar atributos e métodos de classe:

- Utilidade
- Sintaxe em Python

---

### Atributos e Métodos de Classe

- Frequentemente, é desejável ter atributos/métodos que são "globais",
  ou seja, que não dizem respeito a uma instância específica de uma classe
- Por exemplo:
  - O endereço IP de um servidor de banco de dados
  - As possíveis `cores` de um `Carro`
  - A quantidade de instâncias criadas de uma classe

---

### Atributos e Métodos de Instância vs. Atributos e Métodos de Classe

Até então, todos os atributos e métodos vistos são **de instância**
- Dizem respeito a uma instância/objeto específico daquela classe
- São comumente chamados de atributos/métodos (a parte *de instância* do nome
  *atributo de instância* é implícita)

---

### Atributos e Métodos de Instância vs. Atributos e Métodos de Classe
- Atributos e métodos de classe dizem respeito à classe, e não
  a um objeto específico daquela classe
  - Também chamados de dados *static* ou *atributos/métodos estáticos*
  - Não precisam de uma instância da classe para serem utilizados
- Úteis para compartilhar informações entre todos os objetos de uma mesma
  classe

---

### UML: Atributos e Métodos de Classe

<img src="./img/classe_pessoa_static.png" width=500 />

Notação UML: texto sublinhado indica métodos e atributos de classe (estáticos)
---

### Atributos e Métodos de Classe

Como é em Python (mais detalhes no notebook):

```python
class A:

    # Atributos de classe são declarados fora do __init__
    atributo_de_classe1 = ...
    atributo_de_classe2 = ...
    
    def __init__(self, ...):
      # Não confundir com os atributos de instância (declarados no __init__)
      self.atributo_de_instancia1 = ...
      self.atributo_de_instancia2 = ...
      self.atributo_de_instancia3 = ...

    # Método de classe não tem parâmetro self
    def metodo_de_classe():
      ...

```
---

### Como Funciona na Prática
[09-static](09-Static.ipynb)
---
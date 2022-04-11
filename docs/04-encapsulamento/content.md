### Programação Orientada a Objetos
#### Encapsulamento
---

### Revisão 

#### Classe
Abstração para agrupar objetos comuns

Descreve de maneira _abstrata_ o comportamento dos

#### Objetos 
*Instâncias* de uma classe

Encapsulam um _estado_
---

### Revisão 

- _Atributos_: características da entidade sendo modelada
- _Métodos_: definem o *comportamento*
- _Inicializaodor_: inicializa os atributos (construtor em outras linguagens)
- `self`: referência que um objeto tem dele mesmo
---

### Objetivos

Nesta aula aprenderemos:
  - _Encapsulamento_: __segundo pilar__ de POO
  - Setters/getters e `@property`: primeiro decorador em Python
---

### Encapsulamento

> Capacidade de esconder informações (dados) nos objetos

- Alguns atributos/métodos são usados apenas como parte
  da lógica da implementação da classe
- Estes atributos/métodos devem ser impedidos de 
  serem utilizados fora da classe
- As classes devem __expôr o mínimo necessário__ para serem utilizadas
    -  Similar a funções: os dados mínimos que elas precisam são os parâmetros
       e as suas variáveis locais não ficam acessíveis por quem as chama
---

### Interface Pública de uma Classe

- Toda classe tem uma **interface pública**: conjunto de métodos
  que devem ser chamados para que objetos de uma classe sejam
  utilizados
- A interface pública da classe informa ao **usuário da classe**
  como ele deve utilizá-la
    - Usuário da classe é quem utiliza a classe e portanto é
      um programador
    - Usuário da classe não é o mesmo que o usuário do programa
      (que é uma pessoa que não necessariamente entende de programação)
---

### Encapsulamento

- Os usuários da classe só podem acessar os atributos e
  métodos **públicos** da classe
- Ao chamar um método, o usuário da classe pode ignorar
  como ele foi implementado
  - Basta que ele saiba o que deve ser passado como parâmetro
    e qual o retorno do método para chamá-lo
- Facilita a manutenção e reaproveitamento do código
---

### Modificadores de Acesso

Os __modificadores de acesso__ valem para atributos e métodos:

- __Público__:  o atributo/método pode ser acessado/chamado de dentro ou
  fora da classe
- __Privado__: o atributo/método só pode ser acessado/chamado de dentro da
  classe; ele não é herdado pelas subclasses
- __Protegido__: o atributo/método só pode ser acessado/chamado de dentro da
  classe; ele é herdado pelas subclasses
---

### Modificadores de Acesso

> A implementação dos modificadores é um mecanismo dependente da linguagem. Em C++ e
Java, por exemplo, as palavras chaves `public` e `private` devem ser usadas
para esta função

---

### Modificadores de Acesso
#### Exemplo em Java

```java
public class Pessoa{
    // Atributos
    private String nome;
    private int idade;
    // Método público
    public String cumprimentar(Pessoa outro)
    {...
    }
}
```

Em Python, não é assim que funciona. Mais sobre isto no
notebook da aula. 
---

### Exemplo: Estacionamento

- Um estacionamento tem capacidade para um número n > 0 de vagas. 
- Devemos controlar quantos carros estão dentro do estacionamento. 
- Os carros podem entrar só se há vagas disponíveis.

---

### Exemplo: Estacionamento

Nesse sistema podemos identificar:
- _Classes_: Carros e o Estacionamento (por enquanto, vamos ignorar os carros)
- _Atributos_: número de vagas, capacidade máxima
- _Métodos_: Os carros podem _entrar_ e _sair_. Além disso, podemos consultar o número de vagas disponíveis.

--- 

### Exemplo: Estacionamento

Pergunta: o usuário da classe `Estacionamento` deveria __modificar diretamente__
o atributo `vagas`?

Para responder, pense na consistência do objeto 
`Estacionamento`. Ela pode ser mantida dessa forma?

---

### Exemplo: Estacionamento

A resposta é *Não!*: o valor do atributo _vagas_ não deve ser modificado diretamente.

> Isto deve ser feito exclusivamente utilizando chamada aos método
> que informam que um carro entrou ou saiu do estacionamento.
> Estes métodos, por sua vez, são quem deve alterar o a quantidade
> de vagas do estacionamento.

---

### Encapsulamento

Utilizado para:
- *Esconder* os atributos de uma classe
- *Esconder* como funcionam os métodos da classe
- *Facilitar o reaproveitamento* de código
- *Garantir a consistência* (do estado) dos objetos

---

### Encapsulamento em Python
[04-Encapsulamento](04-Encapsulamento.ipynb)

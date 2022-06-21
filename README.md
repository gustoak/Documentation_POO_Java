# Documentation POO Java


# Polimorfismo

O polimorfismo é o uso de duas ou mais classes derivadas de uma mesma superclasse e podem invocar métodos que têm a mesma identificação, assinatura, mas podem executar comportamentos distintos para as classes derivadas.

**Polimorfismo : Sobrecarga**
>A implementação de uma interface faz a sobrescrita, ou seja, altera o comportamento dos métodos definidos na interface.


Por exemplo, temos uma interface Animal definida com o método fala.


- Interface Animal com o método fala (sem corpo, apenas a assinatura).

~~~java
  public interface Animal {
        public String fala(String fala);  
  }                     
~~~

- Os métodos da interface são implementados e modificados nas subclasses, ganhando corpo de acordo com as necessidades específicas de cada subclasse.


~~~java
  public class Cachorro implements Animal{
    @Override
    public String fala(String fala){
      return "Auau";
    }
  }                     
~~~

~~~java
  public class Gato implements Animal{
    @Override
    public String fala(String fala){
      return "Miau";
    }
  }                     
~~~

~~~java
  public class Galo implements Animal{
    @Override
    public String fala(String fala){
      return "Cocoricó";
    }
  }                     
~~~

>Podemos dizer que implementamos várias formas (polimorfismo) de Animal. Ou seja, Animal tem várias formas: Cachorro, Gato e Galo.



# Encapsulamento

O Encapsulamento serve para controlar o acesso aos atributos e métodos de uma classe. 
É uma forma eficiente de proteger os dados manipulados dentro da classe, além de determinar onde esta classe poderá ser manipulada. 
Usamos o nível de acesso mais restritivo, private, que faça sentido para um membro particular. Sempre utilizar private, a menos que tenhamos um bom motivo para deixá-lo com outro nível de acesso.

O encapsulamento é dividido em dois níveis:

- Nível de classe: Quando determinamos o acesso de uma classe inteira que pode ser public ou Package-Private (padrão);
- Nível de membro: Quando determinamos o acesso de atributos ou métodos de uma classe que podem ser public, private, protected ou Package-Private (padrão).


>**Exemplo 1**

~~~java
private String atributo1 = new String();
private String atributo2 = new String();
public String getAtributo1(){
  return this.atributo1;
}
public String getAtributo2(){
  return this.atributo2;
}                    
~~~

>**Exemplo 2**

~~~java
public class Pessoa{
  private String nome;
  private String sobrenome;
  private String dataNasc;
  private String rg;
  private String[] telefones;

  public String getNome(){
    return nome;
  }
  public void setNome(String n){
    nome = n;
  }
  public String getSobrenome(){
    return sobrenome;
  }
  public void setSobrenome(String s){
    sobrenome = s;
  }
  public String getDataNasc(){
    return dataNasc;
  }
  public void setDataNasc(String d){
    dataNasc = d;
  }
  public String getRg(){
    return rg;
  }
  public void setRg(String r){
    r = rg;
  }
  public String getTelefones(){
    return telefones;
  }
  public void setTelefones(String[] telefones){
    telefones[] = telefones;
  }
}public class Pessoa{
  private String nome;
  private String sobrenome;
  private String dataNasc;
  private String rg;
  private String[] telefones;

  public String getNome(){
    return nome;
  }
  public void setNome(String n){
    nome = n;
  }
  public String getSobrenome(){
    return sobrenome;
  }
  public void setSobrenome(String s){
    sobrenome = s;
  }
  public String getDataNasc(){
    return dataNasc;
  }
  public void setDataNasc(String d){
    dataNasc = d;
  }
  public String getRg(){
    return rg;
  }
  public void setRg(String r){
    r = rg;
  }
  public String getTelefones(){
    return telefones;
  }
  public void setTelefones(String[] telefones){
    telefones[] = telefones;
  }
}                
~~~



# Herança

A herança permite criar novas classes a partir de classes já existentes, aproveitando-se das características existentes na classe a ser estendida. 
Este mecanismo é muito interessante, pois promove um grande reuso e reaproveitamento de código existente. Com a herança é possível criar classes derivadas, subclasses, a partir de classes bases, superclasses.

Para detalhar compreender o uso da herença, vamos criar uma classe Pessoa, como mostrado no código a seguir:

>Classe Pessoa com atributos

~~~~java
public class Pessoa{
  public String nome;
  public int idade;
}  	
~~~~

>Classe Aluno herda os atributos da classe Pessoa e inclui o número de **matrícula**.

~~~~java
public class Aluno extends Pessoa{
public String matricula;

}
~~~~

>A classe **Aluno** agora possui três atributos: nome, idade e matricula na classe **Estudos**.

~~~~java
public class Estudos{
  public static void main(String args[]){
    Aluno aluno = new Aluno();
    aluno.nome = "Aluno Esforçado";
    aluno.idade = 20;
    aluno.matricula = "XXXX99999";

    System.out.println("Nome: " + aluno.nome + "\n" +
    "Idade: " + aluno.idade + "\n" +
    "Matrícula: " + aluno.matricula);
  }
}
~~~~

# Referências utilizadas

[DEVMEDIA](https://www.devmedia.com.br)
##### Informações
- Polimorfismo
- Encapisolamento
- Herança

[Computer Science Master](https://www.computersciencemaster.com.br/)
##### Informações
- Polimorfismo
- Encapisolamento
- Herança

[Universidade Java](http://www.universidadejava.com.br/)
##### Informações
- Encapisolamento
- Herança

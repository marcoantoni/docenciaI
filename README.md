# Prática de POO
A prática tem por objetivo exercitar a programação orientada a objetos fixando os conteúdo de Abstração e Encapsulamento

## parte I
1. Para começar, baixe o arquivo [Data.java](http://gpu.rocks/playground) que contém uma estrutura minimalista de uma classe para representar uma data qualquer em orientação a objetos.

2. Crie um novo arquivo chamado AppData.java dentro da pasta onde o arquivo anterior foi baixado. Este arquivo deve ter a estrutura padrão de uma aplicação Java e deve conter o método `public static void main(String args[])`.

3. Dentro do método principal, crie um objeto chamado dataNascimento da classe Data passando como parâmetro 3 inteiros que represtam respectivamente o dia, mes e ano de uma determinada data.

4. Compile e execute esse código. Se estiver no terminal é necessário usar os comandos abaixo:

```bash
 javac AppData.java
 java AppData
```

Irá ocorrer um erro de compilação pois o método construtor não está ajustado para receber todos os parâmetros passados na criação do objeto. Acrescente os atributos mes e ano do tipo int seguindo a estrutura existente na classe Data e ajuste o método construtor para receber os parâmetros mes e ano do tipo inteiro e inicializar os atributos da classe.


Agora vamos exibir os atributos da data criada, para isso adicione o seguinte código dentro do método main em AppData.
```java
System.out.println(dataNascimento.dia + "/" + dataNascimento.mes + "/" + dataNascimento.ano);
```

Recompile e execute novamente o arquivo AppData e veja que a saída será os valores que foram passados na criação do objeto. 

5. Modifique os valor dos atributos do objeto com a instrução abaixo e exiba os dados na tela depois de modificar os atributos do objeto.
```java
dataNascimento.dia = 40;
```
6. Isso mudou o valor do atributo permitindo inserir um valor inválido para uma data. Vamos encapsular os atributos para impedir que eles sejam acessados diretamente. Para isso acrecente a palavra reservada `private` antes do tipo do dado no arquivo `Data.java`. Recompile o código e veja os erros de saída `AppData.java:X: error: dia has private access in Data`. Isto indica que não podemos mais acessar diretamento o atributo pois ele foi encapsulado.

7. Agora vamos criar um método chamado `setData` responsável validar e  atribuir os valores a data. Sempre utilizamos o método `set` para alterar o valor de qualquer atributo que esteja encapsulado.
```java
public void setData(int dia, int mes, int ano){
    int diasmes[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

    if (mes > 0 && mes < 13){
       this.mes = mes;
       // validando o dia de acordo com o mes
       if (dia > 0 && dia <= diasmes[mes+1]){
           this.dia = dia;
       } else {
           System.out.println("Dia inválido");
           this.dia = 1;
       } 
    } else {
       System.out.println("Mês inválido");
       this.mes = 1;
    }

    if (ano > 0){
        this.ano = ano;
    } else {
        System.out.println("Ano inválido");
        this.ano = 1900;
    }
}
```

8. Vamos adicionar um método `get` para pegar o valor dos atributos. Sempre utilizamos o método `get` para pegar o conteúdo de qualquer atributo que esteja encapsulado.
```java
public String getData(){
	return dia + "/" + mes + "/" + ano;
}
```

9. Chame os métodos `setData` e `getData` dentro do método principal de AppData
```java
dataNascimento.setData(2, 6, 2019);

System.out.println( dataNascimento.getData() );

```

10. Compile e execute os códigos. Tente passar valores inválidos ao método `setData`


## Parte II - Implementação de uma classe
Implemente uma classe chamada Pessoa contendo os atributos `nome, cpf, sexo e dataNascimento`. O atributo dataNascimento deve ser do tipo `Data` (classe utilizada anteriormente).

Codifique o método construtor para que ele inicialize todos os atributos da classe e também crie os métodos `get` e `set` para cada atributo da classe. 

 

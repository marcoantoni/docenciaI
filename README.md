# Prática de POO
1. Para começar, baixe o arquivo [Data.java](http://gpu.rocks/playground) que contém uma estrutura minimalista de uma classe para representar uma data qualquer em orientação a objetos

## Crie um novo arquivo chamado AppData.java
2. Este arquivo deve ter a estrutura padrão de uma aplicação Java e deve conter o método `public static void main(String args[])`


3. Dentro do método principal, crie um objeto chamado dataNascimento da classe Data passando como parâmetro 3 inteiros que represtam respectivamente o dia, mes e ano de uma determinada data.

4. Compile e execute esse código

```bash
 javac AppData.java
 java AppData
```

Irá ocorrer um erro de compilação pois o método construtor não está ajustado para receber todos os parâmetros passados na criação do objeto. Acrescente os atributos mes e ano do tipo int seguindo a estrutura existente na classe Data e ajuste o método construtor para receber os parâmetros mes e ano do tipo inteiro e inicializar os atributos da classe.


Agora vamos exibir os atributos da data criada, para isso adicione o seguinte código dentro do método main em AppData.java
```java
System.out.println(dataNascimento.dia + "/" + dataNascimento.mes + "/" + dataNascimento.ano);
```

Recompile e execute novamente o arquivo [AppData.java], a saída será os valores que foram passados na criação do objeto. 

5. Modifique os valor dos atributos do objeto com a instrução abaixo e adicione o comando anterior para exibir os atributos do objeto na tela
```java
dataNascimento.dia = 40;
```
6. Isso mudou o valor do atributo permitindo inserir um valor inválido para uma data. Vamos encapsular os atributos para impedir que eles sejam acessados diretamente. Para isso acrecente a palavra reservada `private` antes do tipo do dado no arquivo [Data.java]

7. Agora vamos criar um método chamado `setData` responsável validar e  atribuir os valores a data
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

8. Vamos adicionar um método `get` para extrair o valor dos atributos
```java
public String getData(){
	return dia + "/" + mes + "/" + ano;
}
```

9. Chame os métodos `setData` e `getData`
```java
dataNascimento.setData(2, 6, 2019);

System.out.println( dataNascimento.getData() );

```

10. Compile e execute os códigos. Tente passar valores inválidos ao método `setData`

## Browser
```java
    public static void main(String[] args){
    
        // TO-DO
    }
```


 
# Table of Contents

NOTE: documentation is slightly out of date for the upcoming release of v2.  We will fix it!  In the mean time, if you'd like to assist (PLEASE) let us know.

* [Installation](#installation)
* [`GPU` Settings](#gpu-settings)
* [`gpu.createKernel` Settings](#gpu-createkernel-settings)
* [Creating and Running Functions](#creating-and-running-functions)
* [Debugging](#debugging)
* [Accepting Input](#accepting-input)
* [Graphical Output](#graphical-output)
* [Combining Kernels](#combining-kernels)
* [Create Kernel Map](#create-kernel-map)
* [Adding Custom Functions](#adding-custom-functions)
* [Adding Custom Functions Directly to Kernel](#adding-custom-functions-directly-to-kernel)
* [Types](#types)
* [Loops](#loops)
* [Pipelining](#pipelining)
* [Offscreen Canvas](#offscreen-canvas)
* [Cleanup](#cleanup)
* [Flattened typed array support](#flattened-typed-array-support)
* [Supported Math functions](#supported-math-functions)
* [Typescript Typings](#typescript-typings)
* [Full API reference](#full-api-reference)
* [Automatically-built Documentation](#automatically-built-documentation)
* [Contributors](#contributors)
* [Contributing](#contributing)
* [How possible in node](#how-possible-in-node)
* [Terms Explained](#terms-explained)
* [License](#license)

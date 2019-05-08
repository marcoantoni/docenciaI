# Prática de POO
Para começar, baixe o arquivo [Data.java](http://gpu.rocks/playground) que contém uma estrutura minimalista de uma classe para representar uma data qualquer em orientação a objetos

# Crie um novo arquivo chamado AppData.java
Este arquivo deve ter a estrutura padrão de uma aplicação Java e deve conter o método 
```java
 public static void main(String args[]){
     // código a ser desenvolvido
 }
```

Dentro do método principal, crie um objeto chamado dataAniversario da classe Data passando como parâmetro 3 inteiros que represtam respectivamente o dia, mes e ano de uma determinada data.

Compile e execute esse código

```bash
 javac AppData.java
 java AppData
```

Irá ocorrer um erro de compilação pois o método construtor não está ajustado para receber todos os parâmetros passados na criação do objeto. Acrescente os atributos mes e ano do tipo int seguindo a estrutura existente na classe Data e ajuste o método construtor para receber os parâmetros mes e ano do tipo inteiro e inicialize os atributos da classe.

Recompile e execute novamente o arquivo AppData.java
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

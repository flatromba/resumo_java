# **Resumo sobre informações da plataforma JAVA**
# Resumo JAVA
## Criando um arquivo
1. **Arquivo:** todo arquivo .java deve começar com letra maiscula, se possuir um nome composto as primeiras palavras sempre iniciarão com letra maiscula.
Ex.: Calculadora.java / MinhaCalculadora.java / MinhaCalculadoraCientifica.java

2. **Classe:** a classe deve possuir o mesmo nome do arquivo.
Ex.:
|arquivo|classe|
| :---: | :---: |
|Calculadora.java|`public class Calculadora{}`|

3. **Variável:** toda variável se inicia com letra minuscula, sendo composta as outras palavras se inciam com maiscula(o nome dessa prática se chama camelCase).
Ex.: `ano` / `anoDeNascimento` 

- **Para declarar uma variável devemos seguir algumas regras.**
    - Deve conter apenas letras, underline(_), $ e números
    - Nunca se deve iniciar com número
    - Deve iniciar com letra minúscula
    - Não pode usar espaços
    - Não pode usar palavras-chave da linguagem
    - O nome deve ser **único**

## Declarando variáveis e métodos
1. Variáveis
|dados primitivos|dados não primitivos|
| :---: | :---: |
|`byte`|`String`|
|`short`|`Arrays`|
|`int`|`Classes`|
|`long`|
|`float`|
|`double`|
|`boolean`|
|`char`|

2. Métodos
- Os métodos seguem uma estrutura bem simples(**tipoDeRetorno NomeNoInfinitivo Parametro(s)**)
Ex.: `public static int somar (int numeroUm, int numeroDois)`

 `public static String formatarCep (long cep)`

 ## Identação
 É um termo aplicado ao código fonte de um programa para ressaltar ou definir a estrutura do algoritmo.
 - Sem identação
  ```
    public static void main(String[] args) {
        int mediaFinal=6;
        if (mediaFinal<6)
        System.out.println("Reprovado");
        else if(mediaFinal==6)
        System.out.println("prova minerva");
        else 
        System.out.println("aprovado");
    }
```
- Com identação
```
    public static void main(String[] args) {
        int mediaFinal = 6;
        if (mediaFinal < 6)
            System.out.println("Reprovado");
        else if (mediaFinal == 6)
             System.out.println("prova minerva");
        else 
            System.out.println("aprovado");
    }
```
## Organizando arquivos
A medida que o sistema evolui, surgem novos arquivos na estrutura. Isso exije uma organização em pacotes(packages).
![Screenshot_2](https://github.com/user-attachments/assets/3927eeb9-c5ab-4807-a358-941b810ee975)

## Java Beans
A linguagem JAVA sugere através de convenções, formas de escrita universal para nossas classes, atributos, métodos e pacotes.
1. Variável
- Deve ser clara
- Sempre no singular(exceto em arrays ou coleção)
- Em um idioma único
Ex.: `int salarioMinimo`
2. Método
- Nomeado como verbo
- Primeira letra de cada palavra em maiúsculo, com exceção da primeira
Ex.: `calcularImposto()`

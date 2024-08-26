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
## Tipos e variáveis
Variável é uma identificação de um espaço em memória, toda variável é composta por: tipo de dado+identificação+valor(opcional).
```
<tipo> <nomeDaVariavel> <valor>
```
Ex.:
```
int idade;
int anoFabricacao= 2020;
byte idade= 15;
String cep= "03035070";
double salario= 2500.00;
long cpf= 44212354662L;
float pi= 3.14F;
boolean doadorDeOrgao= true;
char sexo= 'M';
Date dataDeNascimento= new Date();
```
- Constantes
Valores armazenados em memória que não podem ser modificados depois de declarados.São representados pela palavra reservada `final`, por convenção são escritas em caixa alta.
Ex.: 
```
final int NUMERO=10;
```
## Operadores
1. Aritmético
Utilizado para realizar operações matemáticas entre valores numéricos. Os operadores aritméticos são: adição(+), subtração(-), multiplicação(*), divisão(/) e módulo(%);
Ex.:
```
int soma= 1+2;
int subtracao=2-1;
int multiplicacao=2*2;
double divisao= 10/2;
double modulo= 9%3;
double resultado= (2+2)*(3+3);
```
**Obs.:** O operador de adição quando utilizado em variáveis do tipo texto realizará a concatenação.
```
String nomeCompleto= "Flavio"+"Tromba";
```
2. Unário
São usados juntos com os operadores aritméticos. Eles realizam alguns trabalhos como incrementar, decrementar e inverter valores númericos e booleanos.
- Operador unário de valor positivo(+): Os números sem esse operador explicitamente.
- Operador unário de valor negativo(-): Nega um número ou expressão aritmética.
```
int numero= 5;
System.out.println(- numero);
```
- Operador unário de incremento de valor(++): Incrementa o valor em 1.
```
int numero= 0;
numero++;
```
- Operador unário de decremento de valor(--): Decrementa o valor em 1.
```
int numero= 10;
numero--;
```
- Operador unário lógico de negação(!): Nega o valor de uma expressão booleana.
```
boolean variavel= true;
System.out.println(!variavel);
```
3. Ternário
É uma forma resumida para definir uma condição e escolher por um entre dois valores, é representado pelos símbolos ?:. 
```
<expressãoCondicional> ? <casoSejaTrue> : <casoSejaFalse>
```
Ex.: 
```
int a=5;
int b=6;
String resultado= (a==b) ? "verdadeiro" : "falso";
System.out.println(resultado);
```
4. Relacionais
Avaliam a relação entre duas variáveis ou expressões, retornando um valor booleano como resultado.
- `(==)` verifica se uma variável é igual a outra.
- `(!=)` verifica se uma variável é diferente da outra
- `(>)` verifica se uma variável é maior que a outra
- `(>=)` verifica se uma variável é maior ou igual a outra 
- `(<)` verifica se uma variável é menor que a outra
- `(<=)` verifica se uma variável é menor ou igual a outra 

5. Lógicos
Representam o recurso que nos permite criar expressões lógicas maiores a partir da junção de duas ou mais expressões.
- `(&&)` operador lógico E
- `(||)` operador lógico OU
## Métodos
Correspodem a funções ou subrotinas diponíveis dentro de nossas classes.
1. Nomeação de métodos
Não são obrigatórios, mas é recomendável que sejam seguidos. Ao seguir estas convenções tornamos o código mais legível.
- Deve ser nomeado como verbo
- Seguir o padrão camelCase
```
public int somarNumeros (int numero1, int numero2) {}
```
2. Critério de definição de métodos
Somos auxiliados por uma convenção estrutural para todos os métodos.
- Qual a proposta principal do método? 
- Qual tipo de retorno esperado após executar o método? (caso não retorno nenhum valor, o método será representado pela palavra-chave `void`)
- Quais os parâmetros serão necessários para execução do método?
- O método possui o risco de apresentar alguma exceção?
- Qual a visibilidade do método?
Ex.:
```
public int somar (int numero1, int numero2) {
    // FINALIDADE DO MÉTODO
    return soma;
}

public void imprimir (String texto){
    // FINALIDADE DO MÉTODO
}

public double dividir (int dividendo, int divisor) throws Exception {}
//indica que o método ao ser utilizado pode gerar uma exceção

private void metodoPrivado () {}
//esse método não pode ser visto por outras classes
```
## Escopo
Pode ser entendido como o ambiente onde uma variável pode ser acessada, vai de acordo com o bloco onde ela foi declarada. A variável é criada no primeiro acesso à ela, se tornando inacessível após sair do bloco de execução, ou seja, a variável não pode ser lida ou manipulada fora do escopo da variável.
Em uma classe os atributos são declarados no corpo principal, sendo acessíveis por todos os métodos.
Case declare uma variável **dentro de um método**, o escopo dessa variável está limitado apenas ao corpo desse método.
Ex.:
```
public class Conta{
    double saldo=100.0;

    public void sacar(double valor){
        //variável local
        double novoSaldo=saldo-valor;
    }

    public void imprimirSaldo(){
        System.out.println(saldo);
        //somente o método sacar conhece essa variável
        System.out.println(novoSaldo);
    }
}
```
## Palavras reservadas
São identificadores de uma linguagem que já possuem uma finalidade específica. A linguagem JAVA possui 52 palavras reservadas, todas classificadas em grupos e escritas com letra minúscula.
1. Controle de pacotes
- `import` importa pacotes ou ou classes para dentro de um código
- `package` especifica a que pacote todas as classes de um arquivo pertencem
2. Modificadores de acesso
- `public` acesso de qualquer classe
- `privated` acesso apenas dentro da classe
- `protected` acesso por classes no mesmo pacote ou subclasses
3. primitivos
- `boolean`
- `byte`
- `char`
- `double`
- `float`
- `int`
- `long`
- `short`
- `void`
4. Modificadores de classes, variáveis ou métodos
- `abstract` classe que não pode ser instanciada
- `class` especifica uma classe
- `extends`indica a superclasse que a subclasse está estendendo
- `final` impossibilita que uma classe seja estendida, que um método seja sobrescrito ou que uma variável seja reinicializada
- `implements` indica as interfaces que uma classe irá implementar
- `interface` especifica uma interface
- `native` indica que um método está escrito em uma linguagem dependente de plataforma
- `new` instancia um novo objeto
- `static` faz um método ou variável pertencer à classe
- `strictfp` usado em frente a um método ou classe para indicar que os números de ponto flutuante seguirão as regras de ponto flutuante em todas as expressões
- `synchronized` indica que um método só pode ser acessado por uma thread de cada vez
- `transient` impede a serialização de campos 
- `volatile`indica que uma variável pode ser alterada durante o uso de threads
5. Controle de fluxo dentro de um bloco de código
- `break` sai do bloco
- `case` executa um bloco de código dependendo do teste switch
- `continue` pula a execução do código que viria após essa linha e vai para a próxima passagem do loop
- `default` executa esse bloco de codigo caso nenhum dos teste de switch-case seja verdadeiro
- `do` executa um bloco de código uma vez, e então realiza um teste em conjunto com o while para determinar se o bloco deverá ser executado novamente
- `else` executa um bloco de código alternativo caso o teste if seja falso
- `for` usado para realizar um loop condicional de um bloco de código
- `if` usado para realizar um loop condicional de um bloco de código
- `instanceof` usado para realizar um loop condicional de um bloco de código
- `return` retorna de um método sem executar qualquer código que venha depois desta linha (também pode retornar uma variável)
- `switch` indica a variável a ser comparada nas expressões case
- `while` executa um bloco de código repetidamente enquanto a condição for verdadeira
6. Tratamento de erros
- `assert` testa uma expressão condicional para verificar uma suposição do programador
- `catch` declara o bloco de código usado para tratar uma exceção
- `finally` bloco de código, após um try-catch, que é executado independentemente do fluxo de programa seguido ao lidar com uma exceção
- `throw` usado para passar uma exceção para o método que o chamou
- `throws` indica que um método pode passar uma exceção para o método que o chamou
- `try` bloco de código que tentará ser executado, mas que pode causar uma exceção
7. Variáveis de referência
- `super`refere-se a superclasse imediata
- `this` refere-se a instância atual do objeto
8. Retorno de método
- `void`indica que o método não tem retorno
9. Palavras reservadas não utilizadas
- `const` Não utilize para declarar constantes; use public static fina
- `goto` não implementada na linguagem Java por ser considerada prejudicial

## Documentação JAVA
Podemos compreender e explorar todos os recursos organizados por pacotes e classes bem específicas.[Documentação](https://docs.oracle.com/en/java/javase/22/)
1. Tags
Representam dados relevantes para a compreensão da proposta de uma classe e os conjuntos de seus métodos e atributos

|Tag|Descrição|
|--|--|
|`@author`|autor/criador|
|`@version`|versão do recurso disponibilizado|
|`@since`|versão da disponibilização do recurso|
|`@param`|descrição dos parâmetros dos métodos criados|
|`@return`|definição de um tipo de retorno de um método|
|`@throws`|se o método lança alguma exceção|

Ex.: 
```
/**
 * <h1><Calculadora><h1>
 * a calculadora realiza operações matemáticas entre numeros inteiros
 * @author Flávio Tromba
 * @version 1.0
 * @since 26/08/2024
 */
public class Calculadora {

    /**
     * 
     * @param numero1 primeiro parâmetro
     * @param numero2 segundo parâmetro
     * @return int o resultado deste método é a soma 
     */
    public int somar(int numero1, int numero2){
        return numero1+numero2;
    }   
}
```
2. Tipos de comentários
- One Line
```
// comentário em uma linha
```
- Mult Line
```
/*
*comentário mais detalhado
*quando necessários
*/
```
- Documentation
```
/**
*dois asteriscos acima representam 
*um comentário a nível de documentação 
*/
```
3. Javadoc
É um gerador de documentação para documentar a API dos programas em JAVA, a partir do código fonte. O resultado é expresso em HTML. [Javadoc](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/javadoc.html)
Ex.:
```
// execute o comando no terminal
javadoc -encodig UTF-8 -docencoding ISO-8859-1 -d ../docs src/*.java
```
## Terminal e argumentos
Ao criar um projeto na IDE, terá uma pasta chamada **bin** onde ficarão os arquivos **.class**(bytecode).
### Executando o projeto pelo terminal
- Abra o terminal
- Localize o diretório onde estão as classes do projeto: **`cd C:\Users\Pc\Documents\Cursos\CursoBootCamp\meus-projetos\tipos-variaveis\trilha-java-basico\terminal-argumentos`**
- Acesse a pasta bin: **`cd bin`**
- Digite o comando java NomeDaClasse: **`java MinhaClasse`**
### Argumentos
Quando executamos uma classe que contenha o método `main`, o mesmo permite que passemos um array `[]` de argumentos do tipo `String`. Logo podemos após a definição da classe informar estes parâmetros.
Ex.: 
```
java MinhaClasse argumento1 argumento2
```
1. Classe Scanner
Permite que o usuário tenha uma interação mais assertiva com o programa.
```
Scanner scanner = new Scanner(System.in);
```

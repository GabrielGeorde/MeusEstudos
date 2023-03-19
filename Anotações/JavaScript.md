
# Prototype
O protótipo é um conceito importante em JavaScript e é usado para implementar a herança de objetos. Cada objeto em JavaScript tem um protótipo, que é outro objeto de onde ele herda propriedades.
A palavra-chave "prototype" é usada para acessar o protótipo de uma função construtora ou classe. Por exemplo, se você criar uma função construtora chamada "Pessoa", pode usar o prototype para adicionar propriedades ou métodos a todas as instâncias da classe "Pessoa".<br>
Exemplo:

 >Todos os objetos em JavaScript herdam de um objeto protótipo chamado "Object.prototype". Esse objeto protótipo fornece propriedades e métodos básicos para todos os objetos, como o método "toString" que retorna a representação de uma string de um objeto.

 >O protótipo é uma forma de implementar a herança em JavaScript de forma simples e eficiente. Ao adicionar propriedades e métodos ao protótipo de uma função construtora, é possível compartilhar essas propriedades e métodos com todas as instâncias da classe sem precisar duplicar o código.




# Type conversion ( typecasting) vs Type conversion 
**Alteração de um tipo de dado para outro tipo** <br>
exemplo : <br>
>**console.log('9'+ 5)** // isso me retorna 95 , o javascript força o type NUMBER para STRING<br>
**console.log(Number('9')+ 5)** //já aki é uma type conversion , porque eu altero o tipo com o "Number"



# New
A expressão new cria um novo objeto

>let mid =new String ("kat") 
let bot = new Number(2)
console.log(mid , bot) // imprimi String{"kat"} Number{2}


# Manipulação de string e numeros 


### mudando numero para string e vice versa

Para converter uma string para um número, você pode usar os métodos "parseInt" ou "parseFloat".

O método "parseInt" converte uma string para um inteiro e aceita um segundo argumento opcional que especifica a base numérica da string. Por exemplo:
>let str = "123";
let num = parseInt(str);  // num é um número inteiro com o valor 123
str = "1010";
num = parseInt(str, 2);  // num é um número inteiro com o valor 10

O método "parseFloat" converte uma string para um número de ponto flutuante e aceita um segundo argumento opcional que especifica a base numérica da string. Por exemplo:

>let str = "123.45";
let num = parseFloat(str);  // num é um número de ponto flutuante com o valor 123.45
>str = "3.14";
num = parseFloat(str);  // num é um número de ponto flutuante com o valor 3.14

Para converter um número para uma string, você pode usar o método "toString" ou concatenar o número com uma string vazia. **É mais recomendado usar o método "toString" para converter um número para uma string em JavaScript, ao invés da concatenação com uma string vazia.**

O método "toString" converte um número para uma string e aceita um segundo argumento opcional que especifica a base numérica da string. Por exemplo:

>let num = 123;
let str = num.toString();  // str é uma string com o valor "123"
num = 10;
str = num.toString(2);  // str é uma string com o valor "1010"

Para converter um número para uma string usando a concatenação, basta concatenar o número com uma string vazia. Por exemplo:

>let num = 123;
let str = "" + num;  // str é uma string com o valor "123"
num = 3.14;
str = "" + num;  // str é uma string com o valor "3.14"

É importante lembrar que os métodos "parseInt" e "parseFloat" só funcionam se a string for uma representação válida de um número. Se a string não puder ser convertida para um número, esses métodos retornarão "NaN" (Not a Number).

Por exemplo:

>let str = "abc";
let num = parseInt(str);  // num é "NaN"
str = "3.14abc";
num = parseFloat(str);  // num é 3.14


### Transformar um número querbrado com 2 casas decimais e trocar ponto por virgula

 **toFixed** escolhe a quantidade de casas 
 **replace** escolho oq quero trocar dps pelo oq eu troquei 

 > let numero = 431.143153 
  console.log(number.toFixed(2).replace(".",  ",")) imprime 431,14
 
> let x = 123.456;
console.log(x.toFixed());  // imprime "123"
console.log(x.toFixed(1));  // imprime "123.5"
console.log(x.toFixed(2));  // imprime "123.46"
console.log(x.toFixed(3));  // imprime "123.456"

**OBS: O "toFixed" RETORNA UMA STRING COM A REPRESENTAÇAO FORMATADA DO NÚMERO. SE VOÇE DESEJA MODIFICAR O NÚMERO ORIGINAL , PRECISARÁ ATRIBUIR O RESULTADO DO MÉTODO "toFixed" A UMA VARIÁVEL.**
>let numero = 431.143153;
numero = numero.toFixed(2);  // atribui o resultado do método "toFixed" à variável "numero"
console.log(typeof numero);  // imprime "string"

### Contando quantos  caracteres tem uma palavra e digitos um numero
>let letra = "dizzy"
console.log(letra.length) imprimi 5
let numero = 777
console.log= (String(numer).length) imprimi 3

### Transformando letras Maiúsculas em Minúsculas   e vice versa
simples ToLowerCase para minúscula e ToUpperCase para Maiúscula
>let letra = "PROGRAMAR É PIKA "
console.log(letra.ToLowerCase()) imprimi "programar é pika"

### Verificar se  contém uma determinada palavra n o texto

>let frase = "katarina adora programar"
console.log(frase.includes(katarina)) // imprimi false , porquer ele diferencia letra Maiúscula e Minúsculas

# Manipulando Arrays

### Criando Array com construtor

>let myArray = new Array("a","b","c")
console.log(myArray)

### Contar elementos de um Array 


>console.log(["a" "b" "c"].length) // imprimi 3 //qnt de elementos 
console.log(["a" ,  {type: 'Array'} ,"c"].[2]) // imprimi c
console.log(["a" ,  {type: 'Array'} ,"c"].[1]type) // imprimi Array // tipo do elemento

### Transformar uma cadeia de caracteres em elementos de um array

>let letras="katarina"
console.log(Array.from(letras)) imprmi (11) "k","a","t","a","r","i","n","a"

### Algums metodos 

let tech = ´["HTML","CSS","JS"]

// Adicionar um item no fim
> tech.push("node.js")

// Adicionar um item no começo
> tech.unshift("sql")

// Remover do começo
> tech.pop()

// Remover um item no fim
> tech.shift()

//Pegar somente alguns elementos do array
> console.log(tech.slice(1,3)) // imprimi "css" , "js" 

// Remover 1 ou mais items em qualquer posição do array
> tech.splice(1,2)  //imprimi "html"

//Encontrar a posição de um elemento no array
> let index = tech.indeOf("css")  // posição 1
tech.splice(index,1) // Remove o elemento acima

# Expressões e operadores

### Operador unário

* **typeOF**

O operador de typeof é usado para obter o tipo de uma variável. Por exemplo:
>let x = 10;
console.log(typeof x);  // imprime "number"
x = "olá";
console.log(typeof x);  // imprime "string"
x = true;
console.log(typeof x);  // imprime "boolean"

* **delete**

O operador "delete" é usado para remover uma propriedade de um objeto. Ele não funciona em arrays, mas sim em objetos. Ele aceita um único argumento que especifica o nome da propriedade a ser removida.

>let obj = { nome: "João", idade: 30, cidade: "São Paulo" };
delete obj.idade;  // remove a propriedade "idade" do objeto
console.log(obj);  // { nome: "João", cidade: "São Paulo" }


### Operador ternário

O operador ternário é um operador de condição que permite testar uma expressão e retornar um valor específico dependendo do resultado do teste. <br>Ex:
resultado = expressão_booleana ? valor_se_verdadeiro : valor_se_falso


  **ORDEM DE PRECEDENCIA DOS OPERADORES** 
  * Operadores aritmeticos depois os relacionais depois os logicos
* Se resolve da esquerda para a direita , ja os logicos  primeiro negaçao ! dps conjunçao && dps OU || 

  

### Operador binário




# Falsy e Truthy

### Falsy
Quando um valor é considerado false em  contextos onde um booleano é obrigatório (condicionais e loops)

false
0
-0
""
null
undefined
NaN

exemplo :
console.log( NaN ? 'verdadeiro' : 'falso' )


### Truthy
Quando um valor é considerado true  em  contextos onde um booleano é obrigatório (condicionais e loops)

true
{}
[]
1
3.23
"0"
"false"
-1
infinity
-infinity

exemplo :
console.log( Infinity ? 'verdadeiro' : 'falso' ) 

# Precendência de Operadores

* Grouping                         ( )
* Negaçao e incremento             ! ++
* Multiplicação e divisão          * /
* adição e subtração               + -
* relacional                       < <= > >= 
* igualdade                        == != === !==   
* AND                              &&
* OR                               ||
* condicional                      ? :
* assingment (atribuição)          = += -= *= 

console.log(3 > 2 > 1) // imprimi false , pq ele ler 3>2 "true". e true >1 = false


# Controle de fluxo 
### Parametros e Argumentos
Os argumentos são os valores que são passados para uma função quando ela é chamada. Por exemplo, se você tiver uma função chamada "soma", que recebe dois números como argumentos e retorna a soma desses números, a chamada da função poderia ser algo como "soma(5, 10)", onde 5 e 10 são os argumentos passados para a função.

Os parâmetros são os nomes das variáveis ​​que são usadas para receber os argumentos na função. Por exemplo, na função "soma" acima, os parâmetros podem ser "num1" e "num2", que seriam usados ​​dentro da função para representar os argumentos passados (5 e 10, respectivamente).


### If Else
O comando if verifica se a condição é verdadeira e executa o bloco de código especificado. Se a condição for falsa, o bloco de código dentro do if será ignorado e o fluxo do programa irá para o bloco else, se houver.

	if (condição) {
   	// código a ser executado se a condição for verdadeira
	} else {
 	  // código a ser executado se a condição for falsa
	}





### Switch
Vamos usar uma declaração chamada switch, que tem um papel muito similar ao if e ao else if, vistos na aula passada, porém a estrutura é bem diferente, e aqui veremos essa estrutura.

    let expression = ''
    switch (expression) {   // puxa a expressão para o switch
      case 'a':   // confere se o valor da expressão é o correto
    console.log('a')
    break; // para a execução do switch apenas se verdadeiro
     case 'b':
    console.log('b')
    break;
     default: // caso nenhum valor seja o correto, realizará a 
					 //instrução dentro de si.
    console.log('default')
    break;
    }

Exemplo:

     function calculate(number1, operator, number2) {

    let result = 0;
    switch (operator) {
        case '+':
            result = number1 + number2
            break;
        case '-':
            result = number1 - number2 
            break;
        case '*':
            result = number1 * number2
            break;
        case '/':
            result = number1 / number2 
            break;
        default:
            console.log('não implementado')
            break;
    }
    return result
    }
     console.log(calculate(7, '+', 7))  //imprimi 14



### Throw e Try...Catch 

No JavaScript , "try" e "catch" são estruturas usadas para gerenciar erros que podem surgir durante a execução do código. Quando um erro é detectado no bloco "try", a execução do código é interrompida e a execução é transferida para o bloco "catch", onde é possível tratar o erro e realizar ações apropriadas. O bloco "finally", quando presente, é executado independentemente do resultado do bloco "try" e "catch".

Exemplo:

	try {
	  // Código que pode lançar um erro
	  let resultado = x / y;
	} catch (erro) {
	  // Lidando com o erro
	  console.log("Ocorreu um erro: " + erro.message);
	} finally {
	  // Bloco opcional "finally"
	  console.log("Bloco finally sendo executado");
	}

Se ocorrer um erro durante a divisão de "x" por "y", a mensagem de erro será exibida no console. Se não houver erros, o código dentro do bloco "try" será executado normalmente, e o bloco "finally" será executado no final, independentemente do resultado.

# Estruturas de Repetições
### For
A estrutura de repetição for tem a seguinte sintaxe:

for(inicialização de uma variável; condição de continuação para o loop; expressão final)


    for (let i= 0 , i <100 , i++){

    }

podemos usar um controle com o if.

break - para a execução do loop
continue - pula a execução do momento


     for (let i = 0 ; i < 100 ; i++){
        if (i== 50){             // vai contar ate 50
          break ;
        }
    }


### While
While significa enquanto .
quando usar while e quando usar for
while: qundo não sabemos o momento da parada 


let i = 0
    while(i < 10){
      console.log(i)
  
      i++;
    }


  ### for...of
  
For...of é um loop que itera sobre valores de uma iteração, enquanto o for...in itera sobre as chaves de uma iteração.

O loop for...of é usado para iterar sobre valores em uma iteração, como uma string, um array ou um objeto que implementa a interface iterable. Por exemplo:

>const numbers = [1, 2, 3, 4, 5];
for (const number of numbers) {
  console.log(number);
}

Isso irá imprimir cada número no array numbers na tela.


  ### for...in

Já o loop for...in é usado para iterar sobre as chaves de uma iteração, como um objeto ou um array. Por exemplo:

>const person = {
  name: 'John',
  age: 30,
  city: 'New York'
};

>for (const key in person) {
  console.log(key, person[key]);
}

Isso irá imprimir cada par chave-valor do objeto person na tela.

**É importante lembrar que o for...in itera sobre as chaves de um objeto em qualquer ordem, enquanto o for...of itera em ordem. Além disso, o for...in também itera sobre as chaves herdadas de um objeto, enquanto o for...of só itera sobre as chaves de um objeto que estão diretamente nele.**

Resumo do que ele faz : ???

# DOM
* Os eventos do DOM (Document Object Model) são ações que podem ser realizadas em elementos HTML, como cliques, mouseovers, digitação de texto, etc. Esses eventos podem ser tratados com JavaScript para que ocorram ações específicas quando o evento é disparado.

Para tratar um evento do DOM, basta adicionar um listener de evento ao elemento desejado.<br> Por exemplo:


**Adiciona um listener de evento de clique ao elemento com ID "botao"
document.getElementById("botao").addEventListener("click", function() {
   Código a ser executado quando o botão for clicado
});**

**Adiciona um listener de evento de mouseover ao elemento com ID "link"
document.getElementById("link").addEventListener("mouseover", function() {
   Código a ser executado quando o mouse passar por cima do link
});**

**Adiciona um listener de evento de teclado ao elemento com ID "input"
document.getElementById("input").addEventListener("keydown", function() {
  Código a ser executado quando uma tecla for pressionada no input
});**

1. click: ocorre quando um elemento é clicado;
2. mouseover: ocorre quando o mouse passa por cima de um elemento;
3. mouseout: ocorre quando o mouse sai de cima de um elemento;
4. keydown: ocorre quando uma tecla é pressionada;
5. keyup: ocorre quando uma tecla é solta;
6. focus: ocorre quando um elemento recebe o foco;
7.  blur: ocorre quando um elemento perde o foco.


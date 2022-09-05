# <p align="center">Olá!👋</p>
Essa é uma Doc de como funciona a linguagen da apple para desenvolver para IOS usando Swift.

# Linguagem Swift: história do iOS 


A Apple sempre teve uma política muito restrita em relação aos seus produtos e desenvolvimentos. Basicamente, o que é deles, é deles, ou seja, o MAC OS, iOS e outros sistemas operacionais funcionam maravilhosamente somente dentro do seu próprio ecossistema.

Desde 1980, eles possuem sua própria linguagem de programação, na época o Objective-C, que foi usado por muitos anos para a criação dos seus programas.

Com o avanço da tecnologia e da Era Digital, a Apple também quis facilitar o processo de criação dos novos aplicativos para seus dispositivos e computadores e, assim, a linguagem Swift nasceu em 2014, apresentada na WWDC (conferência anual da Apple para desenvolvedores).

Ela foi criada como uma opção mais simples, intuitiva e com um desempenho superior ao, até então, Objective-C, e passou a ser o código oficial usado para todos os produtos da Apple.

No entanto, também havia a preocupação em relação aos programadores experientes, que já eram especialistas em Objective-C e, mesmo que a linguagem Swift fosse simples de aprender pra eles, pensando nessa possível resistência, a Apple permitiu que utilizassem o mesmo compilador e as duas linguagens pudessem conviver juntas em um mesmo aplicativo. Sendo assim, ninguém foi obrigado a aprendê-la, podendo continuar programando do jeito antigo e ir se adaptando às novas tecnologias no seu ritmo.

Em 2015, foi anunciado que a linguagem Swift seria open source, com o objetivo de expandir o seu uso, bem como o desenvolvimento de novos aplicativos seguros e de bom desempenho para OS X e iOS.

### fonte: [Digital House](https://www.digitalhouse.com/br/blog/linguagem-swift/).

# Aprendendo alguns códigos
Para quem já codou em Python, Kotlin ou JavaScript vai ter mais facilidade para escrever códigos em Swift.

Se compararmo um simples hello word entre C e Swift.

C
```c
#include <stdio.h>

int main(){
    //imprime a mensagem que estive entre aspas duplas
    printf("Ola mundo.");

    //valor de retorno para a função principal
    //indicando que o programa acabou
    return 0;
}
```

Swift
```swift
print("Hello Word😎")
```

## Variáveis Swift
Uma variável é um espaço na memória do computador destinado a um dado que é alterado durante a execução do algoritmo.  

No Swift para definir uma variável, usamos `let`. 
```swift
let username = "Tdroid2.0"
```
Se pedimos para imprimir o resultado veremos a seguinte saída.
```swift
print("Olá " + username)  // Output: Olá Tdroid2.0
```
`let` é uma constante. Então após a atribuição do valor, não poderar ser alterada.

Para criarmos uma variável de fato, usamos `var`. com o var é possível atribuir um valor inicial e mudar ele após a declaração.
```swift
var username = "Tdroid"

username = "Tdroid2.0"

print(username) //Output: Tdroid2.0
```
### Tipos de variáveis
Os tipos mais comuns são Int, Double, String, Bool entre outros. Você pode encontrar mais tipos na [documentação oficial do Swift](https://docs.swift.org/swift-book/ReferenceManual/Types.html).

no código podemos perceber o tipo de uma variável ou função da seguinte forma.
```swift
let username: String = "Tdroid"
```
O `: String` é a declaração do tipo da variável. se tentarmo inserir um número na variavél veremos um erro de sintaxe
```error
cannot convert value of type 'Int' to specified type 'String'
let username: String = 10
                       ^~
```
Podemos converter tipos, por exemplo conveter string para inteiro
```swift
let ageS: String = "10"

let ageI = Int(ageS)

print(ageI) // Optional(10)
```
podemos usar template string (unir duas strings) usando `\(valueHere)`. Veja o exemplo abaixo:
```swift
let lang: String = "Swift";

print("Eu amo \(lang)❤") // Output: Eu amo Swift❤
```

# Operadores
os operadores se assemelhão os operadores do JavaScript.

Um operador é um símbolo, usado para dizer ao compilador para executar as operações matemáticas ou lógicas.

Swift fornece os seguintes operadores:

> operadores aritméticos
> comparação
> Operadores lógicos
> Operadores bit a bit
> Operadores de atribuição
> Operadores de intervalo
> outros operadores


# Operadores de Comparação
![Tabela de Comparação](https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/TabelaDeOperadoresDeCompara%C3%A7%C3%A3o.png)

# Operadores Aritméticos
![Tabela de aritméticos](https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/TabelaDeOperadoresAritmeticos.png)

# Operadores lógicos
![Tabela De OP Lógicos](https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/TabelaDeOperadoresLogicos.png)

# Operadores bit a bit

Operadores bit a bit bits usados ​​para operar, ~, &, |, ^ foram negados, eo bit, ou por pouco e, bit a bit operação XOR com os seguintes exemplos de mesa:

![Tabela Bit a Bit](https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/TabelaDeOperadoresBitABit.png)

Se A = 60; e B = 13; duas variáveis ​​correspondente ao binário é:

```
A = 0011 1100

B = 0000 1101
```

# Operadores de atribuição
![Tabela de atribuição](https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/TabelaDeOperadoresDeAtribuicao.png)

### Fonte do material de operadores: [w3big](http://www.w3big.com/pt/swift/swift-operators.html#gsc.tab=0)
para mais informações de operadores em Swift. recomendo assistir o [video](https://youtu.be/VSuan4RXBQA?t=21) do [Rodrigo Guimaraes](https://www.youtube.com/channel/UCNghEgS-PkKMDbZfiwhvYpA).

# Condicionais
No Swift podemos criar condicionais usando os operadores `if`, `else`, `else if` e switch.
```swift
let owner = "Tdroid";
let ownerId = "554687458";

if(owner == "Tdroid" && ownerId == "554687458") {
  print("É o dono")
} else {
  print("Não é o dono")
}
```
Se rodarmos o código acima, veremos a frase `É o dono`. mais se alterarmos qualquer valor ele irá retornar `Não é o dono`.

```swift
if(owner == "Tdroid" && ownerId == "554687458") {
  print("É o dono")
} else if(owner == "Pla") {
  print("É o sub-dono")
} else {
  print("Não é o dono")
}
```
nesse caso, se rodarmos o codigo com a variável owner como `Pla`, teremos como retorno a frase `É o sub-dono`.

o switch já uma forma mais robusta de fazer condicionais.

```swift
var nome = "Tdroid"

switch nome {
  case "Tdroid": 
    print("Ele é o autor desse material");
  case "Kamal": 
    print("Ele não é o author desse material");
  default: 
    print("Ele é apenas um leitor")
}
```
nesse exemplo ele retornará `Ele é o autor desse material`. você pode testar suas proprias condicionais para praticar

# Arrays
Por questão de tempo, irei ser breve pois esse materia está sendo escrito de madrugada.
<p align="center">
<img src="https://github.com/Tdroid20/Aprendendo-Swift/blob/stable/Assets/DateAndHour.png" alt="Horario da escrita do material 00:20">
</p>

Em programação de computadores, um arranjo/array é uma estrutura de dados que armazena uma coleção de elementos de tal forma que cada um dos elementos possa ser identificado por, pelo menos, um índice ou uma chave. Essa estrutura de dados também é conhecida como variável indexada, vetor e matriz. 

Fonte: [Wikipédia](https://pt.wikipedia.org/wiki/Arranjo_(computa%C3%A7%C3%A3o))
```swift
var users: Array<String> = ["Tdroid", "Henry", "Max"];

print("Os nossos usuários são \(users)"); // Output: Os nossos usuários são ["Tdroid", "Henry", "Max"]

users.append("Kamal"); // Output: ["Tdroid", "Henry", "Max", "Kamal"]
// como o push do JavaScript, o append atribui um valor ao array

print(users);

print("Temos \(users.count) usuários no sistema") // Output: Temos 4 usuários no sistema
// o count retorna o numero de elementos no array

print("Não possuímos nenhum usuário cadastrado? \(users.isEmpty)") // Output: Não possuímos nenhum usuário cadastrado? false
// a função isEmpty retorna um Booleano, se o array estiver vazio irá retornar true, caso contrarío será false
```

# Laços de repetição
Como toda linguagem temos laços de repetição, no Swift temos 4 laços de repetição

O laço While (enquanto) a estrutura básica dele é a seguinte:
```swift
while(condition) {
  // Your code
}
```
Ou seja, enquanto minha condição for verdadeira, o bloco de código será executada, porem tome cuidado com as condições que você cria para executar laços por exemplo se você cria uma condição 1 < 2, o código será executado infinitamente afinal 1 sempre será menor que 2.

Vamos a um Exemplo de Laço **While**:
```swift
var i: Int = 0; // I representa Indice
while i < 3 {
  print("Eu fui executado \(i+1) vezes");
  i += 1
}
```
Outro laço que podemos usar com Swift é o laço **Do-While**, (que significa faça enquanto) sua estrutura não diferencia muito do while, porem ele tem uma peculiaridade bem interessante ele executara seu bloco de código pelo menos uma vez:

Vamos explicar melhor com nosso exemplo, vamos criar um array que representara o carros em vagas de um estacionamento, cada vaga será equivalente a uma posição no array, e em cada posição um carro, (ok, ok, nesse exemplo temos que usar MUITO a imaginação mas vamos la).
```swift
var carros = ["Ferrari", "Gol", "Fusca", "Fiat 147"]
var contador: Int = 0
do {
    println("Esse é meu carro?")
    contador++;
    if(carros[contador] == "Fusca"){
        println("Achei meu carro")
    }
} while carros[contador] != "Fusca"
```
Nesse exemplo, nós percorremos um array verificando cada carro, se esse carro que tem nessa vaga é o nosso, e diferente do while nós executamos toda a verificação pelo menos um vez, para então verificar se a condição nos permitiria executar o bloco novamente.

Vamos o laço For agora, esse laço faz exatamente a mesma coisa que um laço while, sua principal diferença é sua estrutura enquanto o laço while você precisa declarar uma condição de incremento em no meio de seu bloco, com o laço for você pode fazer isso tudo em uma única linha, sua estrutura básica funciona assim:

```swift
for indice in de..até {
  // Your code
}
```
O interessante é que podemos por exemplo declarar uma variável no meio do comando for, por exemplo:
```swift
var Friends: Array<String> = ["Kamal", "Hiro", "Mercena"];

for i in 0..<Friends.count { // ..< Quer dizer que ele vai percorrer o array até uma posição a menos do array
  print("Meu indice da operação é \(i)")
}
```

O C-style foi removido na versão **`Swift 3`**. por tanto não é mais possivel usar o metodo mais conhecido de for: 
```swift
for (inicio, condição , incremento){
  // código
}
```
E apor fim nosso ultimo laço o For-in esse que tem propriedades muito interessantes, por exemplo podemos mandar ele percorrer um array de maneira MUITO mais simples que com os outros laços, vamos voltar a nosso array de carros, digo nosso estacionamento.

```swift
var carros = ["Ferrari", "Gol", "Fusca", "Fiat 147"]
for carro: String in carros{
    print(carro)
}
```
Nesse laço nós percorremos o array mostrando todos os valores dele no caso mostrando todos os carros dele.

Espero que esse post tenha ajudado alguém, foi bem curto, porem tem um conteúdo bem interessante para quem está aprendendo a programar, e se você gostou deste post, de uma olhada no ultimo onde eu falei sobre estruturas de condição.

Muito bem, esse é o fim do primeiro material de Swift. Vejo vocês em breve.

# <p align="center">Creditos</p>

## Autor: Tdroid
[instagram](https://www.instagram.com/tdroid2.0/)
[Youtube](https://www.youtube.com/tdroid20)
[GitHub](https://github.com/Tdroid20)
[Linkedin](https://www.linkedin.com/in/tdroid/)

## Fontes de pesquisa
> [video](https://youtu.be/VSuan4RXBQA?t=21) do [Rodrigo Guimaraes](https://www.youtube.com/channel/UCNghEgS-PkKMDbZfiwhvYpA)
> [w3big](http://www.w3big.com/pt/swift/swift-operators.html#gsc.tab=0)
> [Documentação oficial do Swift](https://docs.swift.org/swift-book/ReferenceManual/Types.html)
> [Digital House](https://www.digitalhouse.com/br/blog/linguagem-swift/)

***REPO FEITO PARA ESTUDOS COM GO***

- > RODANDO O PROJETO COM GO
  
GO É ESTA

TICAMENTE TIPADO -> PRECISA DE DECLARAR TIPO DA VARIAVEL

GP Ñ É UMA LINGUAGEM ORIENTADA A OBJETOS, É UMA LINGUAGEM ORIENTADA A METODOS
Não temos a ideia definida de classes, mas temos a ideia de tipos e métodos associados a esses tipos


***O que é um pacote em go?*** 

::Fases do GO -> 

![Captura de tela 2023-05-01 201401.jpg](..%2F..%2F..%2FDesktop%2FimagensEstudos%2FCaptura%20de%20tela%202023-05-01%20201401.jpg)

Build -> Somente compila o programa, não executa
Run -> Compila e executa o programa

:: O que são os packages em go?
 -> package - coleção de arquivos em comum que pertencem a mesma funcionalidade
EXEMPLO - MAIN - Costuma ter o support, main e helper, 

Existem 2 tipos de pacotes com Go
- Pacotes executáveis (dentro do main)- Geram um arquivo binário que pode ser executado
- Pacotes reutilizáveis (outros pacotes) - Código usado como dependência em outros pacotes

**REMINDER** Sempre deverá ter um arquivo main.go dentro do pacote main, é must have 

:: O que são os imports em go?

Arquivoos no mesmo pacote não precisam de import**

-> Import - Forma de importar pacotes externos ou locais para dentro do seu código
Dê acesso ao meu pacote main a funcionalidade fmt do pacote padrão do go, ou a que estiver importada.

:: O que são os tipos de declaração em go?
-> Declaração de variáveis - Forma de declarar variáveis em go -> var nomeDaVariavel tipoDaVariavel := valorDaVariavel

**REMINDER** -> Não se de declarar variáveis FORA do escopo da função DECLARANDO valor, somente sem valor atribuido.

**REMINDER** -> O go é estaticamente tipado, ou seja, precisa declarar o tipo da variável
-> Na primeira declaração, usa-se :=, as outras podem ser somente =, pois o go já sabe o tipo da variável.


-> Declaração de constantes - Forma de declarar constantes em go 

-> Array e Slices - Forma de declarar arrays e slices em go
ARRAY - NUMERO FIXO

var cards [2]string // declaração de um array de string, com 2 elementos.

SLICE - NUMERO VARIAVEL. Declaração de um slice:

cards := []string{"Ace of Diamonds", newCard()} //
criamos um slice de string, com 2 elementos, o primeiro é uma string e o segundo é uma função que retorna uma string
 -> TODA VEZ QUE EU VER [] É SLICE DE ALGO.

No SLICE, OS TIPOS DE DATA TEM QUE SER =, só string, só int etc.

ADICIONAR CAMPO NO SLICE - cards = append(cards, "Six of Spades") // adiciona um elemento no slice

Difeença entre array e slice em termos de desempenho e busca de dados:
 O Array é mais rápido, pois ele já sabe o tamanho do array, já o slice não, ele precisa percorrer todo o slice para saber o tamanho dele.

:: O que são os loops em go?
-> Loops - Forma de criar loops em go
 for i, card := range cards {
        fmt.Println(i, card)
    }

O range é uma função que retorna 2 valores, o index e o value, o index é o index do elemento no slice e o value é o valor do elemento no slice

OO VS GO APPROACH

![oo approach.PNG](..%2F..%2F..%2FDesktop%2FimagensEstudos%2Foo%20approach.PNG)

![go approach.PNG](..%2F..%2F..%2FDesktop%2FimagensEstudos%2Fgo%20approach.PNG)

:: O que são types em go?
-> Types - Forma de criar tipos em go
type deck []string // declaração de um tipo deck, que é um slice de string

Uma função com um "receiver" é como se fosse um método de uma classe, só que não é uma classe, é um tipo

Logo, se criarmos por exemplo, esse type deck citado, os métodos só funcionam COM ELE.

:: O que são receivers em go?
-> Receivers - Forma de criar receivers em go
Explicado o que é receiver: Uma função com um "receiver" é como se fosse um método de uma classe, só que não é uma classe, é um tipo
 

func (d deck) print() { // função print com um receiver do tipo deck
    for i, card := range d {
        fmt.Println(i, card)
    }
}

O que são structs em go?
-> Structs - Forma de criar structs em go
type person struct {
    firstName string
    lastName  string
}

-> Structs embutidos - Forma de criar structs embutidos em go
type contactInfo struct {
    email   string
    zipCode int
}

type person struct {
    firstName string
    lastName  string
    contact   contactInfo
}

-> Structs embutidos com atalho - Forma de criar structs embutidos com atalho em go

type person struct {
    firstName string
    lastName  string
    contactInfo
}

-> ponteiros em go
-> Ponteiros - Forma de criar ponteiros em go
func (pointerToPerson *person) updateName(newFirstName string) {
    (*pointerToPerson).firstName = newFirstName
}

O * aponta para o endereço (001) de memória da variável, o & retorna o valor ([])do endereço de memória da variável

INTERFACES EM GO -> 
 Usamos para simplificar código,como funciona? 
Você cria a type interface, como se fosse um struct e bota os métodos dentro

Todas as funcs que possuirem esse MÉTODO =, vão assinar a interface

Porém, você define através do RECEIVER QUE VAI TA NO MÉTODO.
Exemplo:
 type bot interface {
    getGreeting() string

 func printGreeting(b bot) {
    fmt.Println(b.getGreeting())

func (englishBot) getGreeting() string {
    // VERY custom logic for generating an english greeting
    return "Hi There!"
}

func (spanishBot) getGreeting() string {
    // VERY custom logic for generating an spanish greeting
    return "Hola!"
}





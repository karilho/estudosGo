***REPO FEITO PARA ESTUDOS COM GO***

- > RODANDO O PROJETO COM GO
  
GO É ESTATICAMENTE TIPADO -> PRECISA DE DECLARAR TIPO DA VARIAVEL

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
-> Import - Forma de importar pacotes externos ou locais para dentro do seu código
Dê acesso ao meu pacote main a funcionalidade fmt do pacote padrão do go, ou a que estiver importada.

:: O que são os tipos de declaração em go?
-> Declaração de variáveis - Forma de declarar variáveis em go -> var nomeDaVariavel tipoDaVariavel := valorDaVariavel

**REMINDER** -> Não se de declarar variáveis FORA do escopo da função DECLARANDO valor, somente sem valor atribuido.

**REMINDER** -> O go é estaticamente tipado, ou seja, precisa declarar o tipo da variável
-> Na primeira declaração, usa-se :=, as outras podem ser somente =, pois o go já sabe o tipo da variável.


-> Declaração de constantes - Forma de declarar constantes em go 


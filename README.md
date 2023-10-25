# Teste de PSI Modelo

## Informação do aluno

    Nome: ...

Teste termina às 09:40 (Turno 1) / 13:25 (Turno 2).

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### 1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    char c = '\u00AE';
    Console.WriteLine($@"\n{c}\n");

P1 - Resposta

    É impresso: \n®\n
    No Console.WriteLine, o caracter '$' no indica que a string a ser impressa é
    interpolada, e o caracter '@' indica que é literal. Logo, a sequência '\n' 
    é impressa exatamente como está escrita, e a variável 'c' entre chavetas
    resulta no caracter unicode '®', correspondente ao valor hexadecimal da variável. 

### 2. Considera o seguinte código

    double d = 0.3513;
    float f = 12.645;

    Console.WriteLine($"{d} + {f} = {d + f}");

### Indica a correção necessária para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    float f = 12.645f;
    É necessário especificar o tipo do valor da variável float com um 'f' no fim,
    pois, por omissão, os números reais são double. Sendo que float é um tipo de
    valor mais "pequeno" que double, não é possível converter implicitamente
    o valor double, por omissão, em float. Logo, é preciso ser explícito,
    adicionando um 'f' no fim do número.

### 3. Escreve um programa que solicite uma string ao utilizador, e seguidamente a mostre no ecrã de forma invertida

P3 - Resposta

    // Variável para guardar input do utilizador
    string input;

    // Pedir que o utilizador escreva uma string
    Console.WriteLine("Escreve uma frase");

    // Guardar a string do utilizador na variável
    input = Console.ReadLine();

    // Ciclo FOR que percorre todos os caracteres da string,
    // do fim até ao início
    for (int i = input.Length - 1; i >= 0; i--)
    {
        // Imprimir um caracter por iteração, todos na mesma linha
        Console.Write(input[i]);
    }

### 4. Quais são os comandos Git para configurares, de uma forma global, o teu **nome** e **email** para realização de *commits*? E se essa configuração for apenas para um repositório?

P4 - Resposta

    Global:
        git config --global user.name "nome"
        git config --global user.email "email"
        
    Apenas num repositório:
        git config user.name "nome"
        git config user.email "email"

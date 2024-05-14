# Comandos de Entrada e Saída em Linguagem C ANSI: Um Guia Completo para Iniciantes

## Introdução

Neste guia, vamos explorar os comandos de entrada e saída em linguagem C ANSI, os quais são essenciais para criar programas interativos que podem se comunicar com o usuário.

Imagine que você está construindo um jogo de adivinhação. Para que o jogo funcione, você precisa pedir ao jogador que digite um número e, em seguida, informar se ele adivinhou o número correto. Isso envolve a entrada de dados do jogador (o número digitado) e a saída de informações para o jogador (se ele adivinhou ou não o número correto).

## Comando `scanf()`: Lendo Dados do Usuário

O comando `scanf()` é usado para ler dados digitados pelo usuário e armazená-los em variáveis. Imagine que você deseja criar um programa que pergunta ao usuário seu nome e idade. Para fazer isso, você pode usar o seguinte código:

```c
#include <stdio.h>

int main() {
  char nome[50]; // Variável para armazenar o nome do usuário
  int idade; // Variável para armazenar a idade do usuário

  printf("Digite seu nome: "); // Solicita ao usuário que digite seu nome
  scanf("%s", nome); // Lê o nome digitado e o armazena na variável `nome`

  printf("Digite sua idade: "); // Solicita ao usuário que digite sua idade
  scanf("%d", &idade); // Lê a idade digitada e a armazena na variável `idade`

  printf("Olá, %s! Você tem %d anos de idade.\n", nome, idade); // Exibe uma mensagem personalizada para o usuário

  return 0;
}
``` 
**Neste Código acima**

- A função `scanf()` é usada duas vezes:
  - Na primeira chamada, ela lê o texto digitado pelo usuário e o armazena na variável nome. O formato `%s` indica que a função espera uma *string* de caracteres.
  - Na segunda chamada, ela lê um número inteiro digitado pelo usuário e o armazena na variável idade. O formato `%d` indica que a função espera um número inteiro.
- A função `printf()` é usada para exibir mensagens na tela. No primeiro caso, ela solicita ao usuário que digite seu nome. No segundo caso, ela exibe uma mensagem personalizada para o usuário, utilizando os valores armazenados nas variáveis nome e idade.

**Exemplo acima:**

<img width="443" alt="2024 05 14 3cRJve" src="https://github.com/pbrmarcos/PAC202411/assets/168874730/43ca4c9e-5ba4-4e20-a7c5-ae14cf88dd27">


## Comando `printf()`: Mostrando Informações na Tela

O comando `printf()` é usado para exibir informações na tela. Ele permite formatar a saída de dados de acordo com suas necessidades. Imagine que você deseja criar um programa que calcula a soma de dois números. Você pode usar o seguinte código:

```c
#include <stdio.h>

int main() {
  int num1, num2, soma;

  printf("Digite o primeiro número: ");
  scanf("%d", &num1);

  printf("Digite o segundo número: ");
  scanf("%d", &num2);

  soma = num1 + num2;

  printf("A soma dos números %d e %d é %d.\n", num1, num2, soma);

  return 0;
}
```
**Neste Código**

- A função `printf()` é usada para exibir três mensagens na tela:
  - A primeira mensagem solicita ao usuário que digite o primeiro número.
  - A segunda mensagem solicita ao usuário que digite o segundo número.
  - A terceira mensagem exibe a soma dos dois números digitados, utilizando os valores armazenados nas variáveis `num1`, `num2` e `soma`.

**Exemplo acima:**

<img width="419" alt="2024 05 14 JqtiBo" src="https://github.com/pbrmarcos/PAC202411/assets/168874730/aa0fe308-e7e8-4e27-aa91-9107c8f07553">


## Formatação de Saída com `printf()`

O comando `printf()` oferece diversas opções de formatação para controlar a aparência da saída na tela. Por exemplo, você pode especificar a largura dos campos, o alinhamento do texto, o número de casas decimais para números flutuantes e muito mais.

Para formatar a saída, você utiliza uma string de formato que contém instruções para `printf()`. A string de formato é composta por:

- Texto normal: O texto que será exibido diretamente na tela.
- Formatadores: Indicadores especiais que definem como os valores das variáveis serão exibidos.

**Exemplo de Formatação:**

```c
printf("O valor de pi é: %3.2f.\n", 3.14159265);
```

-  **%3.2f:** Este formatador indica que o valor da variável pi deve ser

**Exemplo acima:**

<img width="432" alt="2024 05 14 4bb67u" src="https://github.com/pbrmarcos/PAC202411/assets/168874730/7e5a330b-fa8a-4a97-aef6-09593f30f45c">


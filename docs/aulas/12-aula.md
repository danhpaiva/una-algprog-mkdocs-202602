# 🧩 Aula 12: Funções e Procedimentos

Quando um programa cresce, ele vira uma bagunça se tudo ficar no bloco principal. A solução é **dividir para conquistar**: quebrar o código em pequenos blocos com nome próprio, que fazem uma tarefa específica. Esses blocos são as **funções** e **procedimentos**.

---

## 🎯 Por que usar funções?

* **Reuso:** escreva uma vez, use quantas vezes quiser.
* **Organização:** cada bloco tem uma responsabilidade clara.
* **Manutenção:** se há um bug no cálculo, você conserta em **um** lugar só.
* **Legibilidade:** `calcularMedia()` diz mais do que 10 linhas de contas.

!!! quote "Princípio DRY"
    *Don't Repeat Yourself* — "Não se repita". Se você copiou e colou um trecho, provavelmente ele deveria ser uma função.

---

## 🔧 Procedimento (não retorna valor)

Um procedimento **executa uma ação**, mas não devolve um resultado.

```
Algoritmo "Saudacao"

Procedimento saudar()
Inicio
    Escreval("=================")
    Escreval(" Bem-vindo(a)!  ")
    Escreval("=================")
FimProcedimento

Inicio
    saudar()   // chamada do procedimento
    saudar()   // pode ser reutilizado
FimAlgoritmo
```

---

## 🧮 Função (retorna um valor)

Uma função **calcula e devolve** um resultado que pode ser usado em outra parte do código.

```
Algoritmo "Calculadora"

Funcao somar(a: real, b: real): real
Inicio
    Retorne a + b
FimFuncao

Var
    resultado: real
Inicio
    resultado <- somar(10, 5)
    Escreva("A soma é: ", resultado)   // 15
FimAlgoritmo
```

---

## 📥 Parâmetros: enviando dados para a função

Os valores entre parênteses são os **parâmetros** — as informações que a função precisa para trabalhar.

```
Funcao calcularArea(base: real, altura: real): real
Inicio
    Retorne (base * altura) / 2
FimFuncao
```

Aqui `base` e `altura` são parâmetros. Ao chamar `calcularArea(6, 4)`, a função recebe esses valores e retorna `12`.

---

## 🌐 Escopo de Variáveis (local vs. global)

* **Local:** existe só **dentro** da função. Nasce quando a função começa e morre quando ela termina.
* **Global:** declarada fora, visível em todo o programa.

!!! info "Boa prática"
    Prefira variáveis **locais** e a comunicação por **parâmetros** e **retorno**. Isso evita que uma função altere algo que outra não esperava — um dos bugs mais difíceis de caçar.

---

## 🛠️ Exemplo Completo: Verificando Par

```
Algoritmo "Verifica_Par"

Funcao ehPar(numero: inteiro): logico
Inicio
    Se (numero % 2 = 0) entao
        Retorne verdadeiro
    Senao
        Retorne falso
    FimSe
FimFuncao

Var
    n: inteiro
Inicio
    Escreva("Digite um número: ")
    Leia(n)

    Se (ehPar(n)) entao
        Escreva(n, " é par")
    Senao
        Escreva(n, " é ímpar")
    FimSe
FimAlgoritmo
```

---

## 📝 Desafios

??? abstract "Exercício 1: Função Dobro"
    Crie uma função `dobro(n)` que recebe um número e retorna o dobro dele. Teste com três valores.

??? abstract "Exercício 2: Maior de Dois"
    Crie uma função `maior(a, b)` que retorna o maior entre dois números.

??? abstract "Exercício 3: Média com Função"
    Crie uma função `media(n1, n2, n3)` que recebe três notas e retorna a média.

??? abstract "Exercício 4: Procedimento Menu"
    Crie um procedimento `exibirMenu()` que imprime as opções de um menu, e chame-o dentro de um laço.

??? abstract "Exercício 5: Conversor Reutilizável"
    Crie uma função `celsiusParaFahrenheit(c)` e use-a para converter três temperaturas diferentes.

---

!!! tip "Próxima Parada"
    Vamos organizar dados mais complexos com **Matrizes e Registros** na aula de **Estrutura de Dados**. Resolva a **[Lista 12](../listas/12-lista.md)**!

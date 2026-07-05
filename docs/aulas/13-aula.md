# 🗂️ Aula 13: Estrutura de Dados (Matrizes e Registros)

Vetores organizam dados em **linha**. Mas o mundo real muitas vezes é uma **tabela** (linhas e colunas) ou uma **ficha** com vários campos diferentes. Nesta aula ampliamos nossas ferramentas de organização com **matrizes** e **registros**.

---

## 🔲 Matrizes (vetores de duas dimensões)

Uma matriz é como uma **tabela**: tem linhas e colunas. Pense num tabuleiro de xadrez, numa planilha ou nas notas de vários alunos em várias provas.

```
        col 1   col 2   col 3
lin 1 [  8.0  |  7.5  |  9.0 ]
lin 2 [  6.0  |  5.5  |  7.0 ]
```

### Declaração e acesso

```
Var
    notas: vetor[1..2, 1..3] de real   // 2 linhas, 3 colunas
Inicio
    notas[1, 1] <- 8.0   // linha 1, coluna 1
    notas[2, 3] <- 7.0   // linha 2, coluna 3
```

### Percorrendo com laços aninhados

```
Algoritmo "Matriz_Notas"
Var
    notas: vetor[1..2, 1..3] de real
    i, j: inteiro
Inicio
    Para i de 1 ate 2 faca
        Para j de 1 ate 3 faca
            Escreva("Nota do aluno ", i, ", prova ", j, ": ")
            Leia(notas[i, j])
        FimPara
    FimPara

    // Exibindo
    Para i de 1 ate 2 faca
        Para j de 1 ate 3 faca
            Escreva(notas[i, j], " ")
        FimPara
        Escreval("")
    FimPara
FimAlgoritmo
```

!!! info "Regra do laço aninhado"
    O laço **externo** controla as linhas; o **interno** controla as colunas. Para cada linha, percorremos todas as colunas.

---

## 🗃️ Registros (agrupando campos diferentes)

Um vetor guarda vários dados **do mesmo tipo**. Um **registro** guarda vários campos de **tipos diferentes** que descrevem uma mesma entidade.

```
Var
    produto: registro
        nome: caractere
        preco: real
        quantidade: inteiro
    FimRegistro
Inicio
    produto.nome <- "Teclado"
    produto.preco <- 120.00
    produto.quantidade <- 15

    Escreval("Produto: ", produto.nome)
    Escreval("Total em estoque: R$ ", produto.preco * produto.quantidade)
```

Cada campo é acessado com um **ponto**: `produto.nome`, `produto.preco`.

---

## 🧩 Vetor de Registros (o melhor dos dois mundos)

E se você tem **100 produtos**? Um vetor de registros!

```
Var
    estoque: vetor[1..100] de registro
        nome: caractere
        preco: real
    FimRegistro
Inicio
    estoque[1].nome <- "Mouse"
    estoque[1].preco <- 80.00
    estoque[2].nome <- "Monitor"
    estoque[2].preco <- 900.00
```

Essa combinação é a base de praticamente todo sistema real (um cadastro de clientes, um catálogo, uma agenda...).

---

## 📝 Desafios

??? abstract "Exercício 1: Soma de Matriz"
    Leia uma matriz 3x3 de inteiros e exiba a soma de todos os seus elementos.

??? abstract "Exercício 2: Diagonal Principal"
    Leia uma matriz 3x3 e exiba apenas os elementos da diagonal principal (onde linha = coluna).

??? abstract "Exercício 3: Ficha de Aluno (Registro)"
    Crie um registro `aluno` com nome, matrícula e média. Leia os dados e exiba um "boletim" formatado.

??? abstract "Exercício 4: Agenda de Contatos"
    Use um vetor de 5 registros (nome e telefone). Preencha e depois liste todos os contatos.

??? abstract "Exercício 5: Maior da Matriz"
    Leia uma matriz 2x2 e informe qual é o maior valor e em qual posição (linha, coluna) ele está.

---

!!! tip "Próxima Parada"
    Chegamos ao paradigma que domina o mercado: a **Programação Orientada a Objetos (POO)**. Resolva a **[Lista 13](../listas/13-lista.md)**!

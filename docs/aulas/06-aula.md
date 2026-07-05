# 🗃️ Aula 06: Tipos de Dados Primitivos e Compostos

Toda informação que um programa manipula tem um **tipo**. Escolher o tipo certo é como escolher o recipiente certo: você não guarda sopa num saco de papel. Hoje vamos organizar essa "despensa de dados".

---

## 🔤 Tipos Primitivos

São os tipos básicos, os "tijolos" da programação. No Portugol temos quatro:

| Tipo          | Guarda                         | Exemplos                | Ocupa (ideia) |
| :------------ | :----------------------------- | :---------------------- | :------------ |
| **inteiro**   | Números sem casas decimais     | `-3`, `0`, `42`         | pouco         |
| **real**      | Números com casas decimais     | `3.14`, `-0.5`, `10.0`  | médio         |
| **caractere** | Texto entre aspas              | `"Ana"`, `"Rua 7"`      | variável      |
| **logico**    | Verdadeiro ou falso            | `verdadeiro`, `falso`   | mínimo        |

!!! info "Por que o tipo importa?"
    Se você declara um número de telefone como `inteiro`, o zero à esquerda some (`031...` vira `31...`). Telefone e CEP são **texto** (`caractere`), não número!

---

## 🎯 Escolhendo o Tipo Certo

=== "Idade"
    `inteiro` — ninguém tem 25.7 anos.

=== "Preço / Altura / Nota"
    `real` — precisam de casas decimais.

=== "Nome / CPF / Placa"
    `caractere` — são identificadores, não contas.

=== "Está pago? / É maior de idade?"
    `logico` — só há duas respostas possíveis.

---

## 🧩 Tipos Compostos

E quando um dado tem **várias partes**? Um aluno tem nome, matrícula, três notas... Guardar tudo em variáveis soltas vira bagunça. Para isso existem os **tipos compostos**, que agrupam vários valores.

### Vetor (coleção do mesmo tipo)

Um vetor guarda **vários valores do mesmo tipo** sob um único nome, acessados por um índice.

```
Algoritmo "Vetor_Notas"
Var
    notas: vetor[1..3] de real
    i: inteiro
Inicio
    Para i de 1 ate 3 faca
        Escreva("Digite a nota ", i, ": ")
        Leia(notas[i])
    FimPara

    Escreva("A primeira nota foi: ", notas[1])
FimAlgoritmo
```

!!! note "Prévia"
    Vamos nos aprofundar em vetores na **Aula 11**. Aqui é só para você conhecer a ideia de "coleção".

### Registro (agrupa tipos diferentes)

Um registro junta campos de **tipos diferentes** que descrevem uma mesma "coisa".

```
Var
    aluno: registro
        nome: caractere
        matricula: inteiro
        media: real
    FimRegistro
Inicio
    aluno.nome <- "Maria"
    aluno.matricula <- 12345
    aluno.media <- 8.5
```

---

## 🔄 Conversão e Cuidados

Misturar tipos pode dar resultados inesperados:

* `7 / 2` com inteiros pode resultar em `3` (perde a parte decimal) em algumas linguagens.
* `"10" + "5"` como texto vira `"105"`, não `15`.

!!! warning "Regra de ouro"
    Antes de calcular, confirme que os dados são numéricos. Antes de concatenar (juntar textos), confirme que são `caractere`.

---

## 📝 Desafios

??? abstract "Exercício 1: Classificando Dados"
    Para cada dado abaixo, diga qual o tipo mais adequado (inteiro, real, caractere ou logico):
    número de filhos, salário, e-mail, "possui carteira de motorista", temperatura, CEP.

??? abstract "Exercício 2: Ficha do Cliente (Registro)"
    Crie um registro `cliente` com os campos: nome (caractere), idade (inteiro), limite de crédito (real) e ativo (logico). Preencha e exiba os dados.

??? abstract "Exercício 3: Média de um Vetor"
    Crie um vetor de 5 posições do tipo real, leia 5 notas e exiba a soma delas.

---

!!! tip "Próxima Parada"
    Com os dados bem organizados, é hora de fazer o programa **decidir caminhos**. Bem-vindo às **Estruturas de Controle: IF-ELSE**. Resolva a **[Lista 06](../listas/06-lista.md)**!

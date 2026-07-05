# 🔀 Aula 08: Estruturas de Controle — SWITCH / CASE

Imagine um menu de restaurante com 10 opções. Escrever 10 `Se ... Senao Se` funciona, mas fica feio e difícil de ler. Para escolher entre **muitos valores fixos**, existe a estrutura de seleção múltipla: o `Escolha ... Caso` (o famoso *switch-case*).

---

## 🎛️ A Estrutura `Escolha ... Caso`

Ela testa **uma única variável** contra vários valores possíveis.

```
Escolha (variavel)
    Caso valor1
        // ações
    Caso valor2
        // ações
    OutroCaso
        // se não bateu com nenhum
FimEscolha
```

---

## 🍔 Exemplo: Menu de Lanchonete

```
Algoritmo "Menu_Lanchonete"
Var
    opcao: inteiro
Inicio
    Escreval("1 - Hambúrguer")
    Escreval("2 - Pizza")
    Escreval("3 - Refrigerante")
    Escreva("Escolha: ")
    Leia(opcao)

    Escolha (opcao)
        Caso 1
            Escreva("Você pediu Hambúrguer - R$ 20,00")
        Caso 2
            Escreva("Você pediu Pizza - R$ 35,00")
        Caso 3
            Escreva("Você pediu Refrigerante - R$ 8,00")
        OutroCaso
            Escreva("Opção inválida!")
    FimEscolha
FimAlgoritmo
```

---

## ⚔️ SWITCH-CASE vs. IF-ELSE: quando usar cada um?

| Use `Escolha` (switch)                      | Use `Se` (if)                                  |
| :------------------------------------------ | :--------------------------------------------- |
| Comparar **uma variável** com valores fixos | Testar **faixas** ou condições complexas       |
| Menus, dias da semana, códigos, opções      | `nota >= 7`, `idade entre 18 e 65`             |
| Valores exatos e discretos                  | Comparações com `>`, `<`, `e`, `ou`            |

!!! info "Regra prática"
    Se você está comparando **a mesma variável** com vários valores exatos → `Escolha`. Se está testando **intervalos** ou combinando condições → `Se`.

---

## 🗓️ Exemplo: Dia da Semana

```
Algoritmo "Dia_Semana"
Var
    dia: inteiro
Inicio
    Escreva("Digite um número de 1 a 7: ")
    Leia(dia)

    Escolha (dia)
        Caso 1
            Escreva("Domingo")
        Caso 2
            Escreva("Segunda-feira")
        Caso 3
            Escreva("Terça-feira")
        Caso 4
            Escreva("Quarta-feira")
        Caso 5
            Escreva("Quinta-feira")
        Caso 6
            Escreva("Sexta-feira")
        Caso 7
            Escreva("Sábado")
        OutroCaso
            Escreva("Dia inválido")
    FimEscolha
FimAlgoritmo
```

!!! tip "Sempre trate o `OutroCaso`"
    Ele é a sua rede de segurança para entradas inesperadas — equivale ao `Senao` final do `Se`.

---

## 📝 Desafios

??? abstract "Exercício 1: Calculadora Simples"
    Leia dois números e um operador (1=soma, 2=subtração, 3=multiplicação, 4=divisão). Use `Escolha` para executar a operação escolhida.

??? abstract "Exercício 2: Menu de Conversão"
    Crie um menu: 1) Real para Dólar, 2) Real para Euro, 3) Real para Libra. Leia o valor e a opção, e faça a conversão correspondente (use cotações fixas).

??? abstract "Exercício 3: Estações do Ano"
    Leia um número de 1 a 4 e exiba a estação do ano correspondente (1=Verão, 2=Outono, 3=Inverno, 4=Primavera). Trate valores inválidos.

??? abstract "Exercício 4: Conceito por Letra"
    Leia uma letra (A, B, C, D, F) e exiba a mensagem correspondente ao conceito escolar.

---

!!! tip "Próxima Parada"
    E se precisarmos **repetir** uma ação muitas vezes? Entram em cena as **estruturas de repetição**, começando por **WHILE e DO-WHILE**. Resolva a **[Lista 08](../listas/08-lista.md)**!

# 🔁 Aula 09: Estruturas de Repetição — WHILE e DO-WHILE

Computadores são incansáveis: eles repetem uma tarefa milhões de vezes sem reclamar. As estruturas de repetição (ou *loops*) são o que permitem, por exemplo, processar uma planilha com 10 mil linhas. Hoje veremos os laços **condicionais**: `Enquanto` e `Repita`.

---

## ♻️ O Laço `Enquanto` (while)

Repete um bloco **enquanto** uma condição for verdadeira. Ele testa **antes** de executar — então pode rodar **zero** vezes.

```
Enquanto (condicao) faca
    // bloco repetido
FimEnquanto
```

Exemplo — contando de 1 a 5:

```
Algoritmo "Contador"
Var
    i: inteiro
Inicio
    i <- 1
    Enquanto (i <= 5) faca
        Escreval("Número: ", i)
        i <- i + 1   // MUITO importante: atualiza a condição!
    FimEnquanto
FimAlgoritmo
```

!!! danger "O terror do Loop Infinito"
    Se você esquecer o `i <- i + 1`, a condição `i <= 5` nunca fica falsa e o programa trava para sempre. **Todo laço precisa caminhar em direção ao seu fim.**

---

## 🔂 O Laço `Repita` (do-while)

Repete o bloco e **só depois** testa a condição. Por isso ele executa **pelo menos uma vez**, mesmo que a condição já comece falsa. Perfeito para menus e validação de entrada.

```
Repita
    // bloco repetido
Ate (condicao)
```

Exemplo — validando entrada:

```
Algoritmo "Valida_Idade"
Var
    idade: inteiro
Inicio
    Repita
        Escreva("Digite uma idade válida (0 a 120): ")
        Leia(idade)
    Ate (idade >= 0) e (idade <= 120)

    Escreva("Idade registrada: ", idade)
FimAlgoritmo
```

---

## ⚖️ Enquanto vs. Repita

| `Enquanto` (while)              | `Repita` (do-while)                     |
| :------------------------------ | :-------------------------------------- |
| Testa **antes** de executar     | Testa **depois** de executar            |
| Pode rodar **0 vezes**          | Roda **no mínimo 1 vez**                |
| "Enquanto houver fila, atenda"  | "Peça a senha, repita até acertar"      |

---

## 🧮 Padrões Clássicos com Laços

=== "Acumulador (soma)"
    ```
    soma <- 0
    i <- 1
    Enquanto (i <= 5) faca
        Leia(valor)
        soma <- soma + valor
        i <- i + 1
    FimEnquanto
    Escreva("Total: ", soma)
    ```

=== "Contador com condição"
    ```
    pares <- 0
    i <- 1
    Enquanto (i <= 20) faca
        Se (i % 2 = 0) entao
            pares <- pares + 1
        FimSe
        i <- i + 1
    FimEnquanto
    Escreva("Quantidade de pares: ", pares)
    ```

=== "Sentinela (parar por valor)"
    ```
    Leia(numero)
    Enquanto (numero <> 0) faca
        Escreva("Você digitou: ", numero)
        Leia(numero)     // 0 encerra o laço
    FimEnquanto
    ```

---

## 📝 Desafios

??? abstract "Exercício 1: Tabuada"
    Leia um número e exiba sua tabuada de 1 a 10 usando `Enquanto`.

??? abstract "Exercício 2: Soma até parar"
    Leia números do usuário e vá somando. Pare quando ele digitar `0`. No final, exiba a soma total (padrão sentinela).

??? abstract "Exercício 3: Menu com Repita"
    Crie um menu que fica repetindo até o usuário escolher a opção "Sair". Use `Repita ... Ate`.

??? abstract "Exercício 4: Validação de Nota"
    Peça uma nota de 0 a 10. Enquanto o valor for inválido, peça novamente.

---

!!! tip "Próxima Parada"
    Quando sabemos **exatamente quantas vezes** repetir, existe um laço mais elegante: o **FOR (Para)**. Resolva a **[Lista 09](../listas/09-lista.md)**!

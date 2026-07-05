# 🔢 Aula 10: Estruturas de Repetição — FOR e FOREACH

O `Enquanto` é ótimo, mas exige três coisas escritas em lugares diferentes: iniciar o contador, testar e incrementar. Quando sabemos **quantas vezes** vamos repetir, o laço `Para` (for) junta tudo isso em uma linha só — mais limpo e menos sujeito a erros.

---

## 🎯 O Laço `Para` (for)

```
Para variavel de inicio ate fim [passo valor] faca
    // bloco repetido
FimPara
```

Exemplo — contar de 1 a 5:

```
Algoritmo "Contagem_For"
Var
    i: inteiro
Inicio
    Para i de 1 ate 5 faca
        Escreval("Número: ", i)
    FimPara
FimAlgoritmo
```

Repare: o contador `i` é **iniciado, testado e incrementado automaticamente**. Você não precisa escrever `i <- i + 1`.

---

## 👣 O `passo` (incremento personalizado)

Por padrão o `Para` anda de 1 em 1, mas você pode mudar isso.

=== "De 2 em 2"
    ```
    Para i de 0 ate 10 passo 2 faca
        Escreval(i)   // 0, 2, 4, 6, 8, 10
    FimPara
    ```

=== "Contagem regressiva"
    ```
    Para i de 5 ate 1 passo -1 faca
        Escreval(i)   // 5, 4, 3, 2, 1
    FimPara
    ```

---

## 🔄 FOR vs. WHILE: quando usar?

| Use `Para` (for)                          | Use `Enquanto` (while)                         |
| :---------------------------------------- | :--------------------------------------------- |
| Você **sabe** o número de repetições      | O número de repetições **depende** de algo     |
| Percorrer um vetor de tamanho conhecido   | Ler dados até o usuário digitar "sair"         |
| "Repita 10 vezes"                         | "Repita enquanto houver saldo"                 |

!!! info "Os dois resolvem tudo"
    Todo `Para` pode ser reescrito como `Enquanto` e vice-versa. Escolha o que deixa o código **mais claro** para o problema.

---

## 📚 O `Para Cada` (foreach)

Quando percorremos uma **coleção** (como um vetor), muitas linguagens oferecem o *foreach*: ele passa por **cada elemento** sem você precisar controlar o índice.

Ideia (pseudocódigo):

```
Para cada item Em lista faca
    Escreva(item)
FimPara
```

No Portugol trabalhamos o percurso com índice; a ideia do *foreach* ficará mais concreta com vetores (próxima aula) e nas linguagens de mercado (Java, Python, C#).

```
// Percorrendo um vetor com Para (equivalente prático ao foreach)
Para i de 1 ate 5 faca
    Escreva(numeros[i])
FimPara
```

---

## 🧮 Padrões Clássicos

=== "Somatório"
    ```
    soma <- 0
    Para i de 1 ate 100 faca
        soma <- soma + i
    FimPara
    Escreva("Soma de 1 a 100: ", soma)   // 5050
    ```

=== "Fatorial"
    ```
    fat <- 1
    Para i de 1 ate n faca
        fat <- fat * i
    FimPara
    Escreva(n, "! = ", fat)
    ```

=== "Laço aninhado (tabela)"
    ```
    Para i de 1 ate 3 faca
        Para j de 1 ate 3 faca
            Escreva(i * j, " ")
        FimPara
        Escreval("")
    FimPara
    ```

---

## 📝 Desafios

??? abstract "Exercício 1: Tabuada com For"
    Reescreva a tabuada da aula anterior usando `Para` em vez de `Enquanto`.

??? abstract "Exercício 2: Soma dos Pares"
    Some todos os números pares de 1 a 100 e exiba o resultado.

??? abstract "Exercício 3: Fatorial"
    Leia um número `n` e calcule seu fatorial (`n! = 1 * 2 * ... * n`).

??? abstract "Exercício 4: Contagem Regressiva"
    Faça uma contagem regressiva de 10 até 0 e no final exiba "Lançar!".

??? abstract "Exercício 5: Tabuada Completa (aninhado)"
    Use laços aninhados para exibir as tabuadas de 1 a 5, todas de uma vez.

---

!!! tip "Próxima Parada"
    Chegou a hora de guardar **muitos dados** de forma organizada. Bem-vindo aos **Vetores**! Resolva a **[Lista 10](../listas/10-lista.md)**!

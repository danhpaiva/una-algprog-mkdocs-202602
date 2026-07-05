# 📊 Aula 11: Vetores (Arrays)

Até agora, cada variável guardava **um valor**. Mas e se você precisar armazenar as notas de 40 alunos? Criar `nota1`, `nota2`, ..., `nota40` é inviável. A solução é o **vetor**: uma única variável que guarda **vários valores** organizados por posição.

---

## 🧱 O que é um Vetor?

Imagine um prédio com vários apartamentos. O prédio tem **um nome** (a variável) e cada apartamento tem **um número** (o índice). Dentro de cada apartamento mora **um valor**.

```
notas:  [ 7.0 | 8.5 | 6.0 | 9.0 | 5.5 ]
índice:    1     2     3     4     5
```

### Declaração

```
Var
    notas: vetor[1..5] de real
```

Isso cria um vetor chamado `notas` com **5 posições** (de 1 a 5), cada uma guardando um número real.

---

## ✍️ Preenchendo e Lendo um Vetor

Usamos o índice entre colchetes para acessar cada posição.

```
Algoritmo "Notas_Turma"
Var
    notas: vetor[1..5] de real
    i: inteiro
Inicio
    // Preenchendo
    Para i de 1 ate 5 faca
        Escreva("Digite a nota ", i, ": ")
        Leia(notas[i])
    FimPara

    // Lendo
    Escreval("--- Notas digitadas ---")
    Para i de 1 ate 5 faca
        Escreval("Aluno ", i, ": ", notas[i])
    FimPara
FimAlgoritmo
```

!!! danger "Estouro de índice"
    Se o vetor vai de 1 a 5, tentar acessar `notas[6]` é um erro grave (estouro de limites). Sempre respeite o tamanho declarado.

---

## 🧮 Operações Comuns com Vetores

=== "Somar todos"
    ```
    soma <- 0
    Para i de 1 ate 5 faca
        soma <- soma + notas[i]
    FimPara
    media <- soma / 5
    ```

=== "Encontrar o maior"
    ```
    maior <- notas[1]
    Para i de 2 ate 5 faca
        Se (notas[i] > maior) entao
            maior <- notas[i]
        FimSe
    FimPara
    Escreva("Maior nota: ", maior)
    ```

=== "Buscar um valor"
    ```
    Leia(procurado)
    achou <- falso
    Para i de 1 ate 5 faca
        Se (notas[i] = procurado) entao
            achou <- verdadeiro
        FimSe
    FimPara
    Escreva("Encontrado? ", achou)
    ```

---

## 🔤 Vetores de Texto

Vetores não são só de números. Você pode guardar nomes, produtos, etc.

```
Var
    alunos: vetor[1..3] de caractere
Inicio
    alunos[1] <- "Ana"
    alunos[2] <- "Bruno"
    alunos[3] <- "Carla"

    Para i de 1 ate 3 faca
        Escreval(alunos[i])
    FimPara
```

---

## 📝 Desafios

??? abstract "Exercício 1: Média da Turma"
    Leia 10 notas em um vetor, calcule e exiba a média da turma.

??? abstract "Exercício 2: Maior e Menor"
    Leia 8 números em um vetor e exiba o maior e o menor deles.

??? abstract "Exercício 3: Vetor Invertido"
    Leia 5 números e exiba-os na ordem inversa da digitação.

??? abstract "Exercício 4: Contagem de Aprovados"
    Leia 10 notas. Exiba quantos alunos foram aprovados (nota >= 7) e quantos reprovados.

??? abstract "Exercício 5: Busca"
    Leia 6 números em um vetor. Depois pergunte um número ao usuário e informe se ele está no vetor (e em qual posição).

---

!!! tip "Próxima Parada"
    Seu código está crescendo. Para organizá-lo em blocos reutilizáveis, vamos aprender **Funções e Procedimentos**. Resolva a **[Lista 11](../listas/11-lista.md)**!

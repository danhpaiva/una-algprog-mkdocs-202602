# 🔢 Aula 03: Variáveis e Operadores Matemáticos

Se na aula passada aprendemos a desenhar o mapa, hoje vamos aprender a identificar o que carregamos na mochila para essa viagem. No mundo do desenvolvimento, **dados são o novo petróleo**, e as variáveis são os barris onde os guardamos.

---

## 📦 O que é uma Variável?

Imagine uma prateleira com várias caixas de sapatos. Cada caixa tem uma **etiqueta** (nome) e guarda um **conteúdo** específico. Uma variável é um espaço na memória do computador reservado para armazenar um valor que pode mudar durante a execução do programa.

### As 3 Regras de Ouro para Nomes:

1. **Sem espaços:** Use `nota_final` ou `notaFinal`, nunca `nota final`.
2. **Sem números no início:** `1nota` é erro, `nota1` é sucesso.
3. **Sem caracteres especiais:** Evite acentos e cedilhas. O computador fala inglês técnico!

---

## 🗃️ Tipos de Dados no Portugol

Para o computador não desperdiçar memória, precisamos dizer o que vamos guardar em cada "caixa":

| Tipo        | O que guarda?                          | Exemplo              |
| ----------- | -------------------------------------- | -------------------- |
| **inteiro** | Números sem casas decimais.            | `idade <- 25`        |
| **real**    | Números com vírgula (ponto flutuante). | `preco <- 49.90`     |
| **caractere** | Textos e frases (entre aspas).       | `nome <- "Ana"`      |
| **logico**  | Valores de Verdadeiro ou Falso.        | `pago <- verdadeiro` |

---

## ➗ Operadores Matemáticos

O computador é, na essência, uma calculadora gigante. Para manipular os números guardados nas variáveis, usamos os operadores:

* `+` : Adição
* `-` : Subtração
* `*` : Multiplicação
* `/` : Divisão
* `%` ou `mod` : Resto da divisão (Ex: `5 % 2` resulta em `1`)

---

## 🛠️ Colocando a Mão na Massa (Exemplo Prático)

Vamos criar um programa que calcula o **IMC (Índice de Massa Corporal)** de um usuário. Veja como as variáveis e operadores trabalham juntos:

```
Algoritmo "Calculadora_IMC"
Var
    // Declaração das "caixas"
    nome: caractere
    peso, altura, imc: real
Inicio
    Escreva("Digite seu nome: ")
    Leia(nome)

    Escreva("Digite seu peso (kg): ")
    Leia(peso)

    Escreva("Digite sua altura (ex: 1.75): ")
    Leia(altura)

    // O Processamento: Cálculo matemático
    // IMC = Peso / (Altura * Altura)
    imc <- peso / (altura * altura)

    Escreval("Olá ", nome, "!")
    Escreval("Seu IMC calculado é: ", imc)
FimAlgoritmo
```

---

## 🔍 O "Pulo do Gato": Precedência Matemática

Lembra da escola? O computador também segue a ordem de importância. Se você fizer `2 + 3 * 10`, o resultado será **32**, e não 50.

1. **Parênteses `()`** sempre vêm primeiro.
2. **Multiplicação e Divisão** vêm depois.
3. **Soma e Subtração** por último.

!!! info "Dica de Sênior"
    Mesmo que não seja obrigatório, use parênteses para deixar seu código legível. `(base * altura) / 2` é muito mais fácil de ler do que `base * altura / 2`. Código limpo evita dor de cabeça no plantão!

---

## 📝 Desafios de Lógica Matemática

??? abstract "Exercício 1: Conversor de Moedas"
    Crie um algoritmo que:

    1. Receba um valor em **Reais**.
    2. Receba a **Cotação do Dólar** do dia.
    3. Calcule e exiba quanto o usuário tem em **Dólares**.

??? abstract "Exercício 2: O Garçom Amigo"
    Desenhe a lógica para uma conta de restaurante:

    * Leia o `valor_consumo`.
    * Calcule a `taxa_servico` (10% sobre o consumo).
    * Exiba o `valor_total` a ser pago.

    *Dica: Multiplicar por 0.10 é o mesmo que calcular 10%.*

??? abstract "Exercício 3: Cálculo de Área"
    Escreva o pseudocódigo para calcular a área de um triângulo:

    * Fórmula: $Area = \frac{base \cdot altura}{2}$
    * O programa deve ler a base, a altura e mostrar o resultado final.

---

!!! tip "Próxima Parada"
    Dominou as contas? Excelente. Na próxima aula vamos aprender a fazer o computador **comparar** e **combinar** condições com os **Operadores Relacionais e Lógicos**. Não esqueça da **[Lista 03](../listas/03-lista.md)**!

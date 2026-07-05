# ✨ Aula 05: Boas Práticas na Construção de Algoritmos

Um código pode estar "funcionando" e mesmo assim ser ruim. Nesta aula, o foco não é *fazer o computador entender* — ele entende quase qualquer coisa — mas *fazer o ser humano entender*. Afinal, você vai ler seu próprio código daqui a seis meses e precisa se reconhecer nele.

!!! quote
    "Qualquer tolo escreve código que um computador entende. Bons programadores escrevem código que humanos entendem." — Martin Fowler

---

## 🏷️ 1. Nomes que Contam uma História

O nome de uma variável deve dizer o que ela guarda, sem precisar de comentário.

=== "❌ Ruim"
    ```
    Var
        x, y, z: real
    Inicio
        z <- x * y
    ```

=== "✅ Bom"
    ```
    Var
        base, altura, area: real
    Inicio
        area <- base * altura
    ```

---

## 📐 2. Indentação (Recuo)

Indentar é deslocar o código para a direita para mostrar o que está "dentro" de quê. Blocos dentro de `Se`, `Enquanto` e `Para` devem ser recuados.

=== "❌ Sem indentação"
    ```
    Se (idade >= 18) entao
    Escreva("Maior de idade")
    Senao
    Escreva("Menor de idade")
    FimSe
    ```

=== "✅ Com indentação"
    ```
    Se (idade >= 18) entao
        Escreva("Maior de idade")
    Senao
        Escreva("Menor de idade")
    FimSe
    ```

---

## 💬 3. Comentários com Moderação

Comentário bom explica o **porquê**, não o **o quê**. O código já diz o que faz.

```
// Aplica 10% de desconto para clientes do plano premium (regra da promoção de aniversário)
preco_final <- preco * 0.9
```

!!! warning "Evite comentário óbvio"
    `soma <- a + b // soma a com b` não ajuda ninguém. Prefira um nome de variável claro a um comentário que apenas repete o código.

---

## 🔎 4. Teste de Mesa (a arma secreta)

Antes de rodar, simule o algoritmo **na mão**, linha por linha, anotando o valor de cada variável. É assim que se caça um bug sem depender de sorte.

Considere:

```
Var
    a, b, soma: inteiro
Inicio
    a <- 3
    b <- 4
    soma <- a + b
    Escreva(soma)
FimAlgoritmo
```

| Passo | a | b | soma | Saída |
| :---- | :-: | :-: | :--: | :---- |
| a <- 3    | 3 | - | -  |     |
| b <- 4    | 3 | 4 | -  |     |
| soma <- a+b | 3 | 4 | 7  |     |
| Escreva   | 3 | 4 | 7  | 7   |

---

## 🧱 5. Constantes para Valores Fixos

Se um número "mágico" se repete, dê um nome a ele. Fica mais legível e fácil de mudar.

```
Algoritmo "Circunferencia"
Var
    raio, perimetro: real
Inicio
    Leia(raio)
    perimetro <- 2 * 3.14159 * raio  // 3.14159 é o PI
    Escreva(perimetro)
FimAlgoritmo
```

---

## ✅ Checklist do Código Limpo

!!! check "Antes de considerar um algoritmo 'pronto'"
    - [ ] Os nomes das variáveis são claros?
    - [ ] O código está indentado corretamente?
    - [ ] Fiz o teste de mesa com pelo menos dois exemplos?
    - [ ] Removi comentários inúteis e mantive só os que explicam o "porquê"?
    - [ ] Todos os caminhos do algoritmo têm um fim?

---

## 📝 Desafios

??? abstract "Exercício 1: Refatore este código"
    Reescreva o algoritmo abaixo com nomes claros e indentação correta:
    ```
    Var
    a,b,c:real
    Inicio
    Leia(a)
    Leia(b)
    c<-(a+b)/2
    Escreva(c)
    ```

??? abstract "Exercício 2: Teste de Mesa"
    Faça o teste de mesa (tabela) do algoritmo abaixo para `n = 5`:
    ```
    dobro <- n * 2
    triplo <- n * 3
    resultado <- dobro + triplo
    Escreva(resultado)
    ```

??? abstract "Exercício 3: Caça ao Bug"
    O algoritmo deveria calcular a média de duas notas, mas está errado. Encontre e corrija o erro:
    ```
    media <- nota1 + nota2 / 2
    ```

---

!!! tip "Próxima Parada"
    Agora que sabemos escrever bem, vamos nos aprofundar nos **Tipos de Dados Primitivos e Compostos**. Resolva a **[Lista 05](../listas/05-lista.md)**!

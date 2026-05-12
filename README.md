
***

# ✅ RESOLUÇÃO COMPLETA DA ATIVIDADE

*(explicação simples, passo a passo)*

***

## 🧠 1. Antes de programar: pensando no problema

### 📌 O que precisamos fazer?

Temos uma **lista de preços de produtos**.  
Alguns preços podem estar errados.

Regras:

*   ❌ Se o preço for **None** → ignorar (pular)
*   ❌ Se o preço for **negativo** → parar tudo (erro grave)
*   ✅ Só usar preços válidos para calcular a **média**

💡 **Pensar antes de escrever código evita erros**, porque o computador só faz exatamente o que mandamos.

***

## 🧱 2. Criando a lista de produtos

```python
produtos = [100, 150, None, 200, -50, 300]
```

### 🧒 Explicando como para uma criança:

*   Aqui criamos uma **caixa (lista)** com vários preços.
*   Cada número é o preço de um produto.
*   `None` significa: *“não tem preço”*.
*   `-50` é errado, porque preço não pode ser negativo.

***

## ➕ 3. Criando variáveis para soma e contagem

```python
soma = 0
contador = 0
```

### 📘 Explicação:

*   `soma` vai guardar a soma dos preços bons.
*   `contador` vai contar **quantos preços bons existem**.

👶 Imagine:

*   `soma` é como um cofrinho.
*   `contador` é como contar quantas moedas entraram.

***

## 🔁 4. Começando o laço de repetição (`for`)

```python
for preco in produtos:
```

### 📘 O que isso significa?

*   O `for` diz:
    > “Vamos olhar **um preço por vez**, até acabar a lista.”

*   A variável `preco` recebe:
    *   Primeiro: 100
    *   Depois: 150
    *   Depois: None
    *   Depois: 200
    *   Depois: -50
    *   Depois: 300 (mas talvez nem chegue aqui 👀)

***

## ⏭️ 5. Tratando valores `None` com `continue`

```python
    if preco is None:
        continue
```

### 🧠 Explicação simples:

*   `if` significa **“se”**
*   `preco is None` = *“se o preço estiver vazio”*

✅ O que o `continue` faz?

*   Ele diz:
    > “Esse valor não presta, **pule e vá para o próximo**”

🧒 Como uma criança entende:

*   É como dizer:
    > “Esse brinquedo está quebrado, deixa pra lá e pega outro.”

***

## ⛔ 6. Tratando valores negativos com `break`

```python
    if preco < 0:
        print("Erro: preço inválido encontrado.")
        break
```

### 📘 Explicação:

*   `preco < 0` = *“se o preço for menor que zero”*
*   Isso é um **erro grave**

✅ O que o `break` faz?

*   Ele diz:
    > “Pare tudo agora!”

🧒 Exemplo fácil:

*   Se o cinto de segurança do carro quebrar:
    *   Você **não continua dirigindo**
    *   Você **para imediatamente**

***

## ➕ 7. Somando apenas valores válidos

```python
    soma += preco
    contador += 1
```

### 📘 O que acontece aqui?

*   Só chega aqui se o preço:
    ✅ não for `None`
    ✅ não for negativo

*   `soma += preco` → adiciona o preço ao total

*   `contador += 1` → conta mais um preço válido

👶 É como:

*   Colocar uma moeda no cofrinho
*   Marcar que entrou mais uma moeda

***

## ➗ 8. Calculando a média

```python
print("Média dos preços válidos:", soma / contador)
```

### 📘 Explicação:

*   Média = soma ÷ quantidade
*   Mostra o resultado na tela

🧠 Importante:

*   Só funciona porque:
    *   Ignoramos valores vazios
    *   Paramos caso aparecesse erro grave

***

## ✅ 9. CÓDIGO FINAL COMPLETO (comentado)

```python
# Lista com preços dos produtos
produtos = [100, 150, None, 200, -50, 300]

# Variáveis para somar os preços válidos e contar quantos são
soma = 0
contador = 0

# Percorre cada preço da lista
for preco in produtos:
    
    # Se o preço estiver vazio, pula para o próximo
    if preco is None:
        continue
    
    # Se o preço for negativo, mostra erro e para o programa
    if preco < 0:
        print("Erro: preço inválido encontrado.")
        break
    
    # Se o preço for válido, soma e conta
    soma += preco
    contador += 1

# Calcula e mostra a média dos preços válidos
print("Média dos preços válidos:", soma / contador)
```

***

## ❓ 10. Resposta da Pergunta Final

### **Por que é importante organizar o raciocínio lógico antes de escrever o código completo?**

✅ **Resposta simples:**

Porque quando pensamos antes de programar:

*   Evitamos erros
*   Sabemos quando parar o programa
*   Ignoramos dados que não servem
*   O resultado fica correto

Como explicar:

> É como montar um quebra‑cabeça:  
> se você não pensar antes, as peças não encaixam.

***

## 🌟 Conclusão

Você aprendeu a:

*   Usar `for` para repetir
*   Usar `if` para decidir
*   Usar `continue` para pular erros leves
*   Usar `break` para parar erros graves
*   Calcular uma média corretamente
*   Pensar antes de programar ✅

Se quiser, no próximo passo eu posso:


# Calculadora - Projeto Acadêmico

Calculadora desenvolvida em Java como projeto acadêmico, com suporte a operações aritméticas básicas, trigonometria, fórmulas geométricas, equação do 2º grau e juros simples.

---

## Autor

**Max Willian**

---

## Tecnologias Utilizadas

- **Linguagem:** Java
- **Paradigma:** Orientação a Objetos
- **Pacote:** `CalculadoraAAA.dominio`

---

## Estrutura do Projeto

```
Calculadora/
├── dominioCalc      # Classe principal Calculadora (lógica de cálculo)
├── dominoLegenda    # Classe Legenda (menus de navegação)
└── appCalc          # Classe de aplicação
```

### Classes

#### `Calculadora` (`dominioCalc` / `appCalc`)

Classe principal que contém toda a lógica de cálculo.

**Atributos públicos:**

| Atributo | Descrição |
|---|---|
| `valor1`, `valor2` | Operandos das operações básicas |
| `resultado` | Resultado das operações |
| `operador` | Caractere que define a operação |
| `a`, `b`, `c` | Coeficientes da equação do 2º grau |
| `Delta`, `X1`, `X2` | Resultado da equação do 2º grau |
| `b`, `h` | Base e altura (fórmulas geométricas) |
| `r`, `pi` | Raio e PI (área do círculo) |
| `A` | Área resultante |
| `C`, `i`, `t`, `J` | Capital, taxa, tempo e juros (juros simples) |
| `catetoOposto`, `catetoAdjacente`, `hipotenusa` | Lados do triângulo (trigonometria) |

#### `Legenda` (`dominoLegenda`)

Classe responsável por exibir os menus de navegação no console.

---

## Funcionalidades

### Operações Aritméticas Básicas

| Operação | Tecla | Método | Fórmula |
|---|---|---|---|
| Adição | `+` | `Soma()` | `resultado = valor1 + valor2` |
| Subtração | `-` | `Subtracao()` | `resultado = valor1 - valor2` |
| Multiplicação | `*` | `Multiplicacao()` | `resultado = valor1 * valor2` |
| Divisão | `/` | `Divisao()` | `resultado = valor1 / valor2` |
| Potenciação | `^` | `Potenciacao()` | `resultado = valor1 ^ valor2` |
| Raiz Quadrada | `v` | `RaizQuadrada()` | `resultado = √valor1` |

### Trigonometria (tecla `t`)

| Função | Tecla | Método | Fórmula |
|---|---|---|---|
| Seno | `S` | `TrigonometriaSeno()` | `sen = catetoOposto / hipotenusa` |
| Cosseno | `C` | `TrigonometriaCosseno()` | `cos = catetoAdjacente / hipotenusa` |
| Tangente | `T` | `TrigonometriaTangente()` | `tan = catetoOposto / catetoAdjacente` |

### Fórmulas Geométricas (tecla `F`)

| Figura | Tecla | Método | Fórmula |
|---|---|---|---|
| Retângulo | `R` | `F_Retangulo()` | `A = b × h` |
| Triângulo | `T` | `F_Triangulo()` | `A = (b × h) / 2` |
| Círculo | `C` | `F_Círculo()` | `A = π × r²` |
| Equação 2º Grau | `º` | `F_Equacao2Grau()` | `Δ = b² - 4ac` → `X1, X2` |

### Juros Simples (tecla `J`)

| Método | Fórmula | Variáveis |
|---|---|---|
| `Juros()` | `J = C × i × t` | C = Capital, i = Taxa, t = Tempo |

---

## Como Navegar

Ao executar o programa, o menu principal exibe as opções disponíveis:

```
|---------------------------------------|
|Adição aperte o caracter     |'+'|     |
|---------------------------------------|
|Substração aperte o caracter    |'-'|  |
|---------------------------------------|
|Multiplicação aperte o caracter  |'*'| |
|---------------------------------------|
|Divisão aperte o caracter    |'/'|     |
|---------------------------------------|
|Potência aperte o caracter    |'^'|    |
|---------------------------------------|
|RaizQuadrada aperte o caracter   |'v'  |
|---------------------------------------|
|Trigonometria aperte o caracter |'t'|  |
|---------------------------------------|
|Formulas aperte o caracter |'F'|       |
|---------------------------------------|
|Juros aperte o caracter |'J'|          |
|---------------------------------------|
```

Ao selecionar **Trigonometria (`t`)** ou **Fórmulas (`F`)**, um submenu adicional é exibido com as opções correspondentes.

---

## Formato de Saída

Todos os resultados são exibidos com **2 casas decimais**:

```
Resultado: 12.50
```

---

## Contexto Acadêmico

Este projeto foi desenvolvido para fins acadêmicos com o objetivo de praticar os conceitos de:

- Orientação a Objetos em Java (classes, métodos, atributos)
- Estruturas de controle (`switch-case`)
- Uso da biblioteca `Math` do Java (`Math.pow`, `Math.sqrt`)
- Formatação de saída com `System.out.printf`
- Organização de código em pacotes (`package`)
- Implementação de fórmulas matemáticas em código

---

## Observações

- O projeto não possui tratamento de exceções para casos como divisão por zero ou delta negativo na equação do 2º grau.
- Os arquivos `dominioCalc` e `appCalc` contêm a mesma classe `Calculadora`, possivelmente por duplicação durante o desenvolvimento.
- Todo o código e os menus estão escritos em **português**.

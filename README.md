# Calculadora

Projeto acadêmico de uma calculadora desenvolvida em Java com operações aritméticas, trigonometria, fórmulas geométricas, equação do 2º grau e juros simples.

---

## Estrutura do Projeto

```
Calculadora/
├── dominioCalc      # Classe Calculadora
├── appCalc          # Classe Calculadora (duplicata)
└── dominoLegenda    # Classe Legenda
```

> `dominioCalc` e `appCalc` contêm o mesmo código da classe `Calculadora`.

**Pacote:** `CalculadoraAAA.dominio`

---

## Classe `Calculadora`

### Atributos

```java
public double catetoOposto, hipotenusa, catetoAdjacente,
              valor1, valor2, resultado,
              Delta, i, t, C, J, c, a, r, pi, h, A, b, X1, X2;
public char operador;
```

### Método `Resposta()`

Dispatcher central que executa a operação conforme o `operador`:

```java
switch (operador) {
    case '+': Soma();          break;
    case '-': Subtracao();     break;
    case '*': Multiplicacao(); break;
    case '/': Divisao();       break;
    case '^': Potenciacao();   break;
    case 'v': RaizQuadrada();  break;
}
```

---

### Operações Aritméticas

#### `Soma()`
```
resultado = valor1 + valor2
```

#### `Subtracao()`
```
resultado = valor1 - valor2
```

#### `Multiplicacao()`
```
resultado = valor1 * valor2
```

#### `Divisao()`
```
resultado = valor1 / valor2
```

#### `Potenciacao()`
```
resultado = Math.pow(valor1, valor2)
```

#### `RaizQuadrada()`
```
resultado = Math.sqrt(valor1)
```

Todos os métodos acima imprimem com `System.out.printf("\nResultado: %.2f%n", resultado)`.

---

### Fórmulas Geométricas

#### `F_Retangulo()`
```
A = b * h
```

#### `F_Triangulo()`
```
A = b * h / 2
```

#### `F_Círculo()`
```
A = pi * Math.pow(r, 2)
```

#### `F_Equacao2Grau()`
```
Delta = Math.pow(b, 2) - 4 * a * c
X1    = (-b + Math.sqrt(Delta)) / 2 * a
X2    = (-b - Math.sqrt(Delta)) / 2 * a
```
Imprime `Delta`, `X1` e `X2`.

---

### Juros Simples

#### `Juros()`
```
J = C * i * t
```
- `C` = Capital
- `i` = Taxa de juros
- `t` = Tempo

---

### Trigonometria

#### `TrigonometriaSeno()`
```
resultado = catetoOposto / hipotenusa
```

#### `TrigonometriaCosseno()`
```
resultado = catetoAdjacente / hipotenusa
```

#### `TrigonometriaTangente()`
```
resultado = catetoOposto / catetoAdjacente
```

---

## Classe `Legenda`

Responsável por imprimir os menus de navegação no console.

### `ImprimeLegenda()`

Menu principal exibido ao usuário:

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

### `ImprimeLegendaTri()`

Submenu de trigonometria:

```
|---------------------------------------|
|Seno aperte o caracter     |'S'|       |
|---------------------------------------|
|Cosseno aperte o caracter    |'C'|     |
|---------------------------------------|
|Tangente aperte o caracter  |'T'|      |
|---------------------------------------|
```

### `ImprimeLegendaForm()`

Submenu de fórmulas geométricas:

```
|---------------------------------------|
|Retangulo aperte o caracter     |'R'|  |
|---------------------------------------|
|Triangulo aperte o caracter    |'T'|   |
|---------------------------------------|
|Circulo aperte o caracter  |'C'|       |
|---------------------------------------|
|Equação 2ºGrau aperte o caracter |'º'| |
|---------------------------------------|
```

---

## Formato de Saída

Todos os resultados são formatados com duas casas decimais:

```java
System.out.printf("\nResultado: %.2f%n", resultado);
```

Documentação do Projeto: Calculadora Acadêmica
Esta documentação descreve o funcionamento e a estrutura do projeto CalculadoraAAA, um sistema desenvolvido em Java para realizar operações matemáticas básicas, cálculos de fórmulas geométricas, equações de segundo grau, trigonometria e juros.

1. Visão Geral
O projeto está dividido no pacote CalculadoraAAA.dominio e foca na separação de responsabilidades entre o processamento lógico (cálculos) e a interface de usuário (legendas e menus).

2. Estrutura de Classes
A. Classe Calculadora
Esta é a classe principal de processamento. Ela armazena as variáveis de entrada e contém os métodos que executam os cálculos.

- Atributos Principais:

- "valor1", "valor2", "resultado": Usados para operações aritméticas simples.
- "a", "b", "c", "Delta", "X1", "X2": Usados para a Equação do 2º Grau.
- "catetoOposto", "hipotenusa", "catetoAdjacente": Usados para Trigonometria.
- "pi", "r", "h", "A": Usados para cálculos de área (Círculo, Retângulo e Triângulo).
- "C", "i", "t", "J": Usados para o cálculo de Juros.

Métodos de Operação:

Resposta(): Um método controlador que utiliza uma estrutura switch para decidir qual operação aritmética executar com base no caractere armazenado na variável operador.
Aritmética: "Soma()", "Subtracao()", "Multiplicacao()", "Divisao()", "Potenciacao()" e "RaizQuadrada()".
Fórmulas Geométricas: Métodos para calcular a área de Retângulos, Triângulos e Círculos.
Trigonometria: Funções para calcular Seno, Cosseno e Tangente.

B. Classe Legenda

Responsável pela interface visual no console, fornecendo ao usuário as instruções de quais teclas pressionar para acessar cada função.

Métodos de Impressão:

ImprimeLegenda(): Exibe o menu principal com opções de aritmética, trigonometria, fórmulas e juros.
ImprimeLegendaTri(): Exibe as opções específicas de trigonometria (Seno, Cosseno e Tangente).
ImprimeLegendaForm(): Exibe as opções de fórmulas geométricas e a Equação de 2º Grau.

3. Mapeamento de Operadores

Abaixo está a tabela de caracteres utilizados para acionar as funções do sistema:

Operação,      Caractere (Tecla)
Adição,            '+' 
Subtração,         '-' 
Multiplicação,     '*' 
Divisão,           '/' 
Potenciação,       '^' 
Raiz Quadrada,     'v' 
Trigonometria,     't' 
Fórmulas,          'F' 
Juros,             'J' 

4. Observações Técnicas
  
Precisão: O sistema utiliza o método System.out.printf("%.2f") para garantir que os resultados sejam exibidos com duas casas decimais.
Lógica de Equação: O cálculo da Equação do 2º Grau calcula primeiro o determinante ($\Delta$) e depois as raízes $X_1$ e $X_2$ usando a classe Math.sqrt.

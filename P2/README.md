# Compiladores - Prova 2

## compL--

`compL--` é uma linguagem de programação sem funções e sem arrays.
Possui apenas variáveis simples 
e dois tipos básicos: `integer` e `boolean`.
Possui comandos de atribuição, `if-else`, `while` e `return`.
Na declaração de variáveis, sempre deve existir inicialização 
com uma constante. 
O comando `return` deve sempre retornar uma expressão.

```
// programa foo em compL sem erros.

i: integer = 5;
j: integer = 10;
b: boolean = false;

i = 10 * j;
j = j + i * i;
b = i < j;

if (b)
   return i;
else
   return j;
```

1. Indique na prova impressa recebida quais os pontos que serão modificados. (2 pontos)

2. Copie os códigos t3.l e t3.y do seu trabalho T3
para p2/prova2.l e prova2/p2.y respectivamente; 
modifique prova2.l e prova2.y para fazer a análise sintática 
para `compL--`.  Use os arquivos para manipulação de ast
do T3 e adapte se necessário. 
Use o novo arquivo `main.c` fornecido para a prova 2.

3. Implemente verificação de tipos para programas `compL--` 
sintaticamente corretos,
considerando que `integer`e `boolean` 
**não são tipos compatíveis**.
Considere as regras semânticas a seguir. Se qualquer regra
semântica não for atendida, um erro semântico deve ser 
contabilizado.

R1. Uma variável deve ser declarada com inicialização 
antes de ser usada. 

R2. O tipo da constante na inicialização deve ser compatível 
com o tipo declarado para a variável.
Os valores da inicialização devem ser constantes do tipo integer ou do tipo boolean.

R3. Não deve haver mais de variável declarada com o mesmo nome.

R4. Em um comando de atribuição, o lado esquerdo deve ser compatível 
com o lado direito.

R5. A expressão condicional em comandos IF-ELSE ou WHILE 
deve ser do tipo `boolean`.

R6. Operadores aritméticos só podem ter operandos do tipo `integer`;
o resultado de uma expressão aritmética deve ser do tipo `integer`.

R7. Operadores relacionais só podem ter operandos do do tipo `integer`; 
o resultado de uma expressão relacional deve ser do tipo `boolean`.

R8. O comando return deve sempre retornar uma expressão do tipo `integer`.

Todos os testes do T3 devem passar, 
mas não contabilizam para a nota final.

4. Coloque um caso de teste para cada Regra Semântica, no formato `.in` 
e `.ora`. (oráculo)

FIM DA ESPECIFICAÇAO DE P2


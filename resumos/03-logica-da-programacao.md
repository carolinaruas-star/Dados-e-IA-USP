# Aula 03: Lógica de Programação

**Curso:** Dados e Inteligência Artificial (Hype Dados / USP)  
**Professora:** Isabela Brendel / Isa (aluna de Sistemas de Informação na USP e atuante em dados e IA na área de finanças da Amazon Brasil)  

---

## 1. Lógica de Programação e Algoritmos
* **Lógica de Programação:** É a forma de organizar uma sequência de passos para resolver um problema antes de escrever o código. Como o computador não interpreta intenções sozinho, as instruções precisam ser claras, organizadas e na ordem correta. Está presente no cotidiano (ex.: rotas em aplicativos de transporte/mapas, transferências via Pix e consulta de saldo bancário).
* **Algoritmo:** É a sequência organizada de passos para resolver um problema ou executar uma tarefa. Enquanto a lógica de programação é o *como* organizar a sequência da melhor forma, o algoritmo é a sequência de passos em si (como uma receita, ex.: preparar um café verificando água, aquecendo, preparando e servindo na ordem certa).
* **Três Pilares de um Programa:**
  1. **Entrada:** Informações recebidas pelo código (ex.: os números `5` e `3`).
  2. **Processamento:** Operações e manipulação dos dados pelo código (ex.: somar `5 + 3`).
  3. **Saída:** Resultado final produzido pelo programa (ex.: `8`).

---

## 2. Variáveis, Constantes e Tipos de Dados
* **Variáveis:** Espaços na memória (como "caixinhas") que armazenam informações que podem mudar durante a execução do programa (ex.: pontuação ou gols de um jogador, ou a idade de alguém).
* **Constantes:** Valores que permanecem fixos durante toda a execução do código (ex.: o valor de $\pi$, por convenção escrito em caixa alta).
* **Atribuição (`=`):** Em programação, o símbolo `=` representa **atribuição** ("recebe"), não igualdade matemática (ex.: `idade = 25` significa que a variável `idade` recebe o valor `25`).
* **Tipos de Dados Primitivos:**
  * **Inteiro (`int`):** Números inteiros, sem casas decimais (ex.: `1, 2, 3, 4, 25`).
  * **Decimal / Ponto Flutuante (`float`):** Números com parte decimal (*floating numbers*, ex.: `1.65`).
  * **Texto (`string` / `str`):** Palavras, frases e caracteres (ex.: `"Ana"`).
  * **Booleano (`bool`):** Valores lógicos de verdadeiro ou falso (`True` ou `False`, seguindo a convenção em inglês).

---

## 3. Operadores Aritméticos e de Comparação
* **Operadores Aritméticos:**
  | Operador | Operação | Exemplo |
  | :--- | :--- | :--- |
  | `+` | Adição | `5 + 3` $\rightarrow$ `8` |
  | `-` | Subtração | `5 - 3` $\rightarrow$ `2` |
  | `*` | Multiplicação | `5 * 3` $\rightarrow$ `15` |
  | `/` | Divisão | `12 / 2` $\rightarrow$ `6` |
  | `%` | Resto da divisão (módulo) | `7 % 2` $\rightarrow$ `1` (pois `7` dividido por `2` dá `3` e sobra `1`) |
* **Operadores de Comparação:** Retornam `True` ou `False`:
  * `==`: Igual a (comparação de igualdade, diferente da atribuição `=`; ex.: `1 == 1` $\rightarrow$ `True`).
  * `!=`: Diferente de (ex.: `1 != 2` $\rightarrow$ `True`).
  * `>` e `<`: Maior que e menor que (ex.: `2 > 1` e `3 < 4` $\rightarrow$ `True`).
  * `>=` e `<=`: Maior ou igual a e menor ou igual a (ex.: `7 >= 6` e `7 >= 7` $\rightarrow$ `True`).

---

## 4. Estruturas Condicionais e Operadores Lógicos
* **Estruturas Condicionais (`if` / `else`):** Permitem executar blocos diferentes de instruções conforme uma condição. O `if` ("se") avalia uma condição; se for verdadeira (`True`), executa seu bloco e ignora o `else`. Se for falsa (`False`), executa o `else` ("caso contrário").
  * *Exemplo da aula:* Verificar se `idade >= 18` para exibir `"maior de idade"` ou `"menor de idade"`.
* **Operadores Lógicos:**
  * `and` (**E**): Retorna `True` apenas se **todas** as condições envolvidas forem verdadeiras (ex.: `idade >= 18 and tem_cupom` para aplicar desconto).
  * `or` (**OU**): Retorna `True` se **pelo menos uma** das condições for verdadeira (ex.: `tem_cupom or esta_cadastrado` para indicar benefício disponível; só é `False` se ambos forem `False`).
  * `not` (**NÃO**): **Inverte** o valor lógico da condição/variável (ex.: `if not esta_cadastrado` transforma `False` em `True` para exibir mensagem de cadastro pendente).

---

## 5. Estruturas de Repetição
* **Laço `for`:** Usado quando se sabe previamente o intervalo ou a quantidade de repetições sobre uma sequência (ex.: percorrer um intervalo `range` de `1` a `4`, imprimindo `1`, `2` e `3`).
* **Laço `while`:** Executa enquanto uma condição permanecer verdadeira (`True`), parando quando a condição se torna falsa (`False`). Exige controle/atualização da variável de condição (ex.: `contador` iniciando em `1` e incrementando `+ 1` a cada passo até ultrapassar `3`).

---

## 6. Representação de Algoritmos e Exemplo Prático
* **Formas de Representar um Algoritmo Antes de Codar:**
  * **Descrição narrativa:** Explicação passo a passo em linguagem natural.
  * **Fluxograma:** Representação visual com símbolos e setas (detalhado na apostila).
  * **Pseudocódigo:** Representação estruturada próxima da linguagem de programação, usando linguagem simples para descrever início, entradas, processamento, saídas e fim.
* **Exemplo Prático — Média de Duas Notas:**
  1. Receber duas notas (ex.: `8` e `6`).
  2. Calcular a média somando as notas entre parênteses para priorizar a adição e dividindo por `2`: `(nota1 + nota2) / 2` $\rightarrow$ `(8 + 6) / 2 = 7`.
  3. Exibir o resultado na tela usando `print(...)` — assim como o clássico comando inicial `print("Olá Mundo")` / `print("Hello World")`.
* **Dica de Estudo:** Dividir problemas complexos em partes menores e organizadas facilita encontrar a melhor solução e evoluir no processo de aprendizado.
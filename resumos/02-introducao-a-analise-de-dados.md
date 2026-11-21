# Aula 02: Introdução à Análise de Dados

**Curso:** Dados e Inteligência Artificial (Hype Dados / USP)  
**Professora:** Isabela Amorim (graduanda em Sistemas de Informação pela USP e integrante de equipe de Ciência de Dados na 99)

---

## 1. Definição e Ciclo da Análise de Dados
* **Definição:** Análise de dados faz parte do cotidiano e pode atuar tanto em áreas de negócio (decisões *data-driven*) quanto em times dedicados e técnicos de dados.
* **Stakeholders (Partes Interessadas):** Pessoas ou áreas que consomem ou dependem das análises (ex.: gerentes que precisam de evidências e orçamento para defender uma estratégia à diretoria). Também é possível conduzir análises para si mesmo/próprio negócio quando se define as perguntas de investigação.
* **Ciclo Iterativo (inspirado em Agile):**
  1. **Formulação de hipóteses:** Definir as perguntas que vão guiar a investigação (lista aberta que pode ganhar novas perguntas ao longo do processo).
  2. **Coleta:** Obter dados de diversas fontes descentralizadas (bancos de dados, logs de sistema, *web scraping*, etc.), extraindo e concatenando dados brutos.
  3. **Limpeza e tratamento:** Tratar inconsistências e valores nulos (investigando a origem antes de descartar, como falhas de extração ou bugs) e manipular estruturas para o formato adequado. Parte desse fluxo compõe o **ETL** (*Extraction, Transform and Load*), mais próximo da Engenharia de Dados.
  4. **Análise e visualização:** Aplicar técnicas estatísticas e computacionais para identificar padrões e tendências.
  5. **Interpretação:** Traduzir métricas e resultados técnicos em *insights* claros e histórias compreensíveis para o negócio, comparando com as hipóteses iniciais, validando com *stakeholders* e abrindo novos ciclos se necessário.

---

## 2. Categorização dos Dados
* **Quanto ao Tipo:**
  * **Qualitativos:** Categorias não numéricas.
    * *Nominais:* Sem ordem hierárquica intrínseca (ex.: países como Brasil, México, Alemanha, Portugal).
    * *Ordinais:* Com ordem/hierarquia intrínseca (ex.: níveis de escolaridade como ensino básico, fundamental, médio, superior), o que influencia gráficos e preparação para modelos.
  * **Quantitativos:** Valores numéricos.
    * *Discretos:* Números inteiros (ex.: contagens `1, 2, 3, 4...`).
    * *Contínuos:* Números reais em um intervalo (ex.: medidas com casas decimais/intervalos contínuos).
* **Quanto à Organização:**
  * **Estruturados:** Organizados em tabelas (dados relacionais), fáceis de indexar, relacionar e consultar com **SQL**.
  * **Semiestruturados:** Possuem alguma estrutura de organização, mas não em formato tabular rígido (ex.: **JSON**, em pares de chave e valor).
  * **Não estruturados:** Sem estrutura tabular fixa, como textos livres, imagens e áudio — exigem mais esforço e muitas vezes algoritmos de IA para extrair relações.

---

## 3. Tipos de Análise de Dados
| Tipo de Análise | Pergunta Central | Foco e Técnicas / Exemplos |
| :--- | :--- | :--- |
| **Descritiva** | *O que aconteceu?* | Resume o passado: média, mediana, desvio padrão, contagem, volume, percentuais e gráficos de distribuição (ex.: histograma). |
| **Diagnóstica** | *Por que aconteceu?* | Investiga relações e associações (correlação vs. causalidade): *drill down* (segmentar/granularizar dados, ex.: separar por grupos), análise de correlação e análise temporal. |
| **Preditiva** | *O que vai acontecer?* | Mais próxima de Ciência de Dados: usa probabilidade, intervalos de confiança, *machine learning* estatístico e previsão de séries temporais (*forecasting*, ex.: estimar vendas do próximo mês). |
| **Prescritiva** | *O que devemos fazer?* | Recomendações e ações para otimizar resultados futuros: otimização matemática/rotas, simulação de cenários e sistemas de recomendação. |

---

## 4. Conceitos Estatísticos Fundamentais
* **Média vs. Mediana:** A **média** soma todos os valores e divide pela quantidade de observações, sendo sensível a valores extremos (ex.: salários muito altos inflando a média salarial). A **mediana** ordena os valores e pega o ponto central, sendo mais robusta em distribuições assimétricas.
* **Quartis e Percentis:** Dividem os dados ordenados em partes (ex.: 25% / 1º quartil, 50% / 2º quartil ou mediana, 75% / 3º quartil), base para gráficos como o **box plot**.
* **Desvio Padrão e Variância:** Medem o quanto os valores se afastam/dispersam em relação à média (variância é o quadrado do desvio padrão).
* **Outliers:** Valores discrepantes/extremos em relação ao restante dos dados. Podem indicar erro de coleta/medição ou fenômenos reais — avaliar com critério de negócio e contexto antes de remover.
* **Distribuições Estatísticas:** Mostram como os valores de uma variável se distribuem (ex.: **distribuição normal**, em formato de sino), o que influencia a escolha de métricas e testes estatísticos.

---

## 5. Visualização de Dados e Vieses
* **Gráficos Comuns:**
  * *Barras:* Muito confiável para comparar proporções e categorias com clareza.
  * *Pizza:* Pode dificultar a comparação precisa de proporções pelo olho humano (ângulos/áreas) em comparação a barras.
  * *Linhas:* Ideal para acompanhar tendências ao longo do tempo em dados contínuos.
  * *Dispersão:* Útil para observar relações entre variáveis numéricas contínuas e identificar agrupamentos (*clusters*).
* **Boas Práticas de Visualização:**
  1. **Clareza e eficiência:** Facilitar o entendimento rápido sem ambiguidade ou excesso de esforço mental.
  2. **Simplicidade:** Eliminar ruídos visuais e exibir o que é relevante (ex.: agrupar categorias muito pequenas em *"Outros"*).
  3. **Integridade e contexto:** Evitar distorções visuais que induzam a conclusões falsas.
* **Vieses Comuns em Dados e Análises:**
  * **Eixo truncado / distorção visual:** Iniciar um eixo em valor diferente de zero (ex.: começando em `2,6`) pode exagerar visualmente uma variação pequena.
  * ***Cherry picking*:** Selecionar apenas dados favoráveis e descartar evidências contrárias ao argumento desejado.
  * **Viés de sobrevivência / seleção:** Analisar apenas o que "sobreviveu" ou respondeu a um filtro/processo (ex.: pesquisa respondida apenas por quem já gosta de formulários).
  * **Falsa causalidade (relação espúria):** Assumir que duas variáveis correlacionadas têm relação de causa e efeito sem evidência real (ex.: desemprego em Portugal e usuários do Facebook crescendo no mesmo período).
  * **Paradoxo de Simpson:** Uma tendência observada no conjunto total de dados pode se inverter ou mudar quando os dados são segmentados em subgrupos.
  * **Negligência da taxa base:** Avaliar um grupo isolado sem comparar com uma referência/proporção populacional (*baseline*, ex.: hospitalizações sem considerar o tamanho total de vacinados e não vacinados).

---

## 6. Ferramentas Mais Populares
* **Power BI e Tableau:** Ferramentas visuais para criação de gráficos, exploração e *dashboards* interativos.
* **Python:** Linguagem versátil e muito requisitada (inclusive para análises), com sintaxe acessível e apoio de IA generativa. Bibliotecas de destaque: **Pandas** (manipulação de dados) e bibliotecas de visualização (como gráficos estáticos e interativos via **Plotly**).
* **R:** Linguagem muito presente no meio acadêmico e em equipes específicas, voltada à análise estatística e visualização.
* **SQL:** Linguagem fundamental e amplamente exigida para consultar e extrair dados de bancos relacionais/tabelas.
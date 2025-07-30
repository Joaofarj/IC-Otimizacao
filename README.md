# Iniciação científica
Aluno: João Pedro Farjoun Silva / N° usp: 13731319


Orientadora: Franklina M. B. Toledo


Período: 6/09/2023 - 31/07/2024

# Seleção de Portfólio com Foco em Investimento Sustentável

Este repositório contém os códigos, dados e resultados do projeto de Iniciação Científica realizado por João Pedro Farjoun Silva, sob orientação da Profa. Franklina M. B. Toledo, no Instituto de Ciências Matemáticas e de Computação (ICMC-USP), com apoio do CNPq via Programa PIBIC.

## Objetivo

Investigar se é possível obter retornos competitivos no mercado financeiro investindo exclusivamente em ações ESG (Environmental, Social and Governance). Para isso, foi adaptado e aplicado um modelo de otimização de portfólios a dados reais do mercado brasileiro.

---

## Metodologia

Utilizou-se como base o modelo proposto por Mansini e Speranza (2005), que seleciona um portfólio ótimo considerando:

- Limites mínimos e máximos de investimento por ação;
- Diversificação mínima (quantidade mínima de ativos distintos);
- Exclusão dos custos de transação;
- Minimização do risco negativo via semi-desvio;
- Restrições sobre capital investido e retorno mínimo esperado.

A formulação completa está apresentada no relatório em PDF. O modelo foi resolvido usando o solver **SCIP**.

---

## Experimentos

### Etapa 1 – Validação do Modelo

- **Ações**: 10 ações ESG
- **Períodos (T)**: 12 meses
- **Capital (C)**: R$10.000
- **Retorno mínimo (μ₀)**: 110% do retorno médio
- **Diversificação mínima (K)**: 5 ações
- **Investimento mínimo/máximo por ação**: 5%/20% do capital

> As previsões de retorno foram comparadas com os retornos reais das carteiras. O modelo apresentou estabilidade, mesmo com a volatilidade do mercado e o número limitado de ações.

### Etapa 2 – Carteiras com 157 Ações ESG

- **Ações**: 157 do índice ETF-ESG (BTG Pactual)
- **Períodos (T)**: 12 a 17 meses (com e sem acúmulo)
- **Diversificação mínima/máxima (K/M)**: 8 a 20 ações
- **Investimento mínimo/máximo por ação**: 4%/15% do capital

> Foram construídas 5 carteiras (fev-jun 2023), avaliando o retorno após um ano. Os dados mostram retornos, em diversos casos, superiores à Taxa Selic e comparáveis ao Ibovespa.

---

## Resultados

| Mês       | Previsão Acumulada (%) | Previsão Fixa (%) | Selic (%) | Ibovespa (%) |
|-----------|-------------------------|-------------------|-----------|--------------|
| Fevereiro | 10,14                   | 10,14             | 11,68     | 14,64        |
| Março     | 0,86                    | 6,18              | 12,05     | 23,75        |
| Abril     | 15,63                   | 22,86             | 12,14     | 25,11        |
| Maio      | 18,59                   | 26,15             | 12,46     | 24,72        |
| Junho     | 10,89                   | 21,85             | 12,55     | 10,37        |

> Observa-se que o portfólio ESG teve retornos promissores, em alguns casos superando o Ibovespa, mesmo com limitações de horizonte de tempo e instabilidade do mercado.

---

## Conclusões

- Investir em ações ESG **não compromete a rentabilidade**.
- Portfólios sustentáveis **podem superar a Selic e o Ibovespa**, dependendo da conjuntura.
- O modelo adaptado se mostrou aplicável e eficiente para seleção de portfólios ESG no Brasil.
- A **volatilidade de curto prazo** impacta as previsões, reforçando a recomendação de investimentos em janelas mais longas (5 anos, por exemplo).

---

## Trabalhos Futuros

- Avaliação de horizontes maiores (3 a 5 anos);
- Inclusão de custos de transação no modelo;
- Análise com outros índices e classificações ESG;
- Exploração de modelos estocásticos ou com machine learning.

---

## Organização do Repositório

```bash
IC-Otimizacao/
├── Etapa1/                 # Dados e códigos da fase com 10 ações
├── Etapa2/                 # Dados e códigos da fase com 157 ações
└── README.md               # Este arquivo

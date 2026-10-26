# Análise de movimentações de reagentes — setembro de 2026

## Escopo

- Período analisado: 01/09/2026 a 30/09/2026
- Registros de movimentação: 145
- Lotes no arquivo de estoque inicial: 24
- Arquivos de entrada:
  - `movimentacoes_reagentes_setembro_2026.csv`
  - `estoque_inicial_reagentes_2026-09-01.csv`


## Metodologia

O notebook executa as seguintes etapas:

1. Carregamento dos CSVs e conversão de datas e quantidades.
2. Validação de duplicidades, valores ausentes, quantidades inválidas, tipos de movimentação, lotes e intervalo de datas.
3. Perfil de frequência por tipo de movimentação.
4. Contagem diária de operações.
5. Frequência e quantidades retiradas por reagente.
6. Contagem de retiradas por projeto, mantendo quantidades separadas por unidade.
7. Análise de descartes por motivo e reagente.
8. Estimativa de saldo final por lote a partir do saldo inicial e das movimentações.
9. Identificação de lotes com validade próxima.
10. Exportação das tabelas derivadas para CSV.

## Resumo descritivo do conjunto

Distribuição dos registros por tipo:

retirada: 94 (64.8%), descarte: 20 (13.8%), entrada: 19 (13.1%), devolução: 12 (8.3%)

Dia com maior quantidade de operações: **08/09/2026**, com **8 registros**.

Projetos com mais retiradas registradas (por contagem de operações):

- Síntese e catálise: 24 retiradas
- Pesquisa aplicada: 20 retiradas
- Análises físico-químicas: 19 retiradas
- Caracterização de materiais: 17 retiradas
- Tratamento de efluentes: 14 retiradas

Reagentes com maior frequência de movimentações:

- Etanol: 19 operações
- Cloreto de sódio: 18 operações
- Metanol: 15 operações
- Ácido clorídrico: 15 operações
- Carbonato de sódio: 14 operações

## Validações observadas

- **movimentações:** 145
- **lotes no estoque inicial:** 24
- **data inicial:** 01/09/2026
- **data final:** 30/09/2026
- **IDs duplicados:** 0
- **células ausentes (movimentações):** 78
- **quantidades não positivas:** 0
- **lotes sem correspondência no estoque inicial:** 0
- **movimentações fora do período:** 0

Lotes com saldo final negativo estimado: **2**.

- R006-L02 (Cloreto de sódio): saldo inicial 1.478 kg; variação -4.469; saldo final estimado -2.991 kg
- R008-L02 (Sulfato de cobre): saldo inicial 1.104 kg; variação -1.349; saldo final estimado -0.245 kg


## Limitações e recomendações

- Retirada registrada não é necessariamente igual a consumo efetivo.
- Quantidades devem ser analisadas por unidade e por reagente.
- Um mês de dados não é suficiente para inferir sazonalidade ou tendência duradoura.

## Como executar

1. Salve os dois arquivos CSV na mesma pasta do notebook.
2. Instale as dependências: `pip install pandas matplotlib`.
3. Abra `analise_movimentacoes_reagentes_setembro_2026.ipynb` no Jupyter Notebook ou JupyterLab.
4. Execute as células em ordem.

O notebook exporta os resultados derivados como arquivos `resultado_*.csv`.

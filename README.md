# Análise de movimentações e estoque de reagentes

## Estrutura do projeto

- `dados/`: arquivos CSV utilizados pela análise.
- `notebooks/`: notebook Jupyter com as etapas de tratamento, validação e análise.
- `documentacao/`: documentação metodológica e descrição das etapas.

## Como executar

1. Extraia todo o conteúdo do ZIP, preservando as pastas.
2. Abra `notebooks/analise_movimentacoes_reagentes_setembro_2026.ipynb` no Jupyter Notebook ou JupyterLab.
3. Execute as células na ordem apresentada.
4. Caso necessário, instale as bibliotecas utilizadas com `pip install pandas matplotlib`.

O notebook procura os arquivos CSV na pasta `dados/` relativa à estrutura do projeto. Os resultados exportados pelo notebook são salvos na pasta de trabalho definida nas células de exportação.

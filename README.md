# 📊 Análise de Desempenho de E-commerce (UK Online Retail)

## 🎯 Objetivo do Projeto
Analisar dados reais de transações de uma loja online no Reino Unido (2010-2011)[https://archive.ics.uci.edu/dataset/352/online+retail] para identificar tendências de vendas, sazonalidade e perfis de clientes, gerando insights acionáveis para o time de negócios.

## 🛠️ Ferramentas e Técnicas
- **Python (Pandas, NumPy, Matplotlib):** limpeza, engenharia de variáveis e visualização.
- **Limpeza com relatório:** cada regra de remoção (cancelamentos, quantidades e preços inválidos) é contada, e o notebook **falha com mensagem clara** em vez de descartar dados em silêncio.
- **Análises:** produtos e países, sazonalidade (mensal e semanal), **retenção por coorte**, **segmentação RFM** (quintis de Recência, Frequência e Valor) e hábitos dos clientes campeões.
- **Cuidados de interpretação** ao final de cada seção do notebook: o que a análise mostra e o que ela não permite concluir.

## 💡 Principais Descobertas
Período analisado                  01/12/2010 a 09/12/2011
Linhas após a limpeza              530,104
Receita total (£)                  10,666,685
Clientes identificados             4,338
Participação do 1º país            United Kingdom = 84.6% da receita
Mês de maior receita (completo)    2011-11
Retenção média no mês 1            21.5%
Clientes com 2+ compras            64.2%
Campeões                           947 clientes (21.8%) = 64.6% da receita

1. **Países:** o Reino Unido concentra 85% da receita. Alemanha, França e Irlanda já compram, mas a análise não mede crescimento, então expansão para esses países é uma **hipótese a testar**.
2. **Produtos:** excluindo frete, taxas e ajustes, os produtos de maior receita são REGENCY CAKESTAND 3 TIER, PAPER CRAFT , LITTLE BIRDIE, WHITE HANGING HEART T-LIGHT HOLDER, PARTY BUNTING e 
JUMBO BAG RED RETROSPOT.
3. **Sazonalidade:** o mês completo de maior receita foi Novembro de 2011. Só há um ano de dados e o padrão coincide com a temporada de fim de ano, então a análise **não separa Black Friday de Natal**.
4. **Retenção:** 21.5% dos clientes voltam a comprar no mês seguinte à primeira compra, e 64.2% compraram 2 vezes ou mais.
5. **Segmentação RFM:** 947 clientes "Campeões" (21.8% dos clientes) geram 64.6% da receita. *Ação sugerida:* testar um programa de fidelidade com grupo de controle.
6. **Hábitos dos campeões:** os produtos que mais geram receita nesse grupo são 
REGENCY CAKAESTAND, WHITE HANGING HEART T LIGHT HOLD,  JUMBO BAG RED RETROSPOT, PARTY BUNTING e ASSORTED COLOUR BIR ORNAMENT. Antes de falar em *preferência*, compare com os demais clientes. Campanhas de recomendação e *bundles* são hipóteses a testar.

## ⚠️ Limitações
- Apenas 13 meses de dados: não dá para afirmar que a sazonalidade se repete.
- A base começa em dez/2010, então a coorte inicial mistura clientes novos e antigos.
- Parte da receita não tem `CustomerID` e fica fora das análises de coorte e RFM.
- Cancelamentos foram removidos: a receita é bruta, sem devoluções.
- Os cortes do RFM (quintis, nota >= 4) são uma convenção.

## 📂 Estrutura do Projeto
```
notebooks/01_eda.ipynb   notebook completo (limpeza, análises e visualizações)
dataset/                 coloque aqui a base original (veja dataset/README.md)
requirements.txt         dependências
```

## 🚀 Como rodar
1. Clone o repositório.
2. Baixe a base e salve em `dataset/` (instruções em [`dataset/README.md`](dataset/README.md)).
3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
4. Abra `notebooks/01_eda.ipynb` no Jupyter ou no VS Code e execute todas as células. Os caminhos são relativos, então funciona em qualquer computador.

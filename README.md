# 📊 Análise de Desempenho de E-commerce (UK Online Retail)

## 🎯 Objetivo do Projeto
Analisar dados reais de transações de uma loja online no Reino Unido (2010-2011)[https://archive.ics.uci.edu/dataset/352/online+retail] para identificar tendências de vendas, sazonalidade e perfis de clientes, gerando insights acionáveis para o time de negócios.

## 🛠️ Ferramentas Utilizadas
- **Python (Pandas, Matplotlib):** Para limpeza de dados, engenharia de features e visualização.
- **Técnicas de Análise:** Tratamento de dados nulos/sujos, Análise RFM (Recência, Frequência, Monetário) e Análise de Sazonalidade.

## 💡 Principais Descobertas (Insights de Negócio)
1. **Produtos e Países Estrela:** O Reino Unido domina massivamente as vendas. Os produtos mais lucrativos foram itens de decoração e presentes (ex: *White Hanging Heart T-Light Holder*).
2. **Sazonalidade e Black Friday:** A receita atinge seu pico absoluto em **Novembro**, impulsionado pela Black Friday. *Ação sugerida:* Garantir estoque e campanhas de marketing focadas nos "produtos estrela" já em outubro.
3. **Segmentação de Clientes (RFM):** Identificamos um grupo de "Campeões" (clientes com alta frequência e alto gasto). *Ação sugerida:* Criar um programa de fidelidade ou descontos progressivos para múltiplos itens para reter esse público de alto valor.

4. **Análise Mundial de Grownth:** Países como Alemanha, França e Irlanda apresentam grande número de vendas, uma oportunidade para expandir o mercado para essas áreas!

5. **Análise de Hábitos de Clientes VIP:** Ao analisar os produtos mais comprados pelos nossos clientes "Campeões" (e aplicando um filtro para remover ruídos operacionais como o "POSTAGE"), identificamos forte preferência por itens como *CARRIAGE*, *CINDERELLA CHANDELIER* e *VICTORIAN SEWING BOX*. **Ação sugerida:** Criar campanhas de recomendação cruzada ("quem comprou isso, também comprou aquilo") ou bundles exclusivos com esses itens para atrair novos clientes com perfil semelhante ao dos nossos VIPs.

## 📂 Estrutura do Projeto
- `online_retail.csv`: Dataset original.
- `online_retail_cleaned.csv`: Dataset após tratamento (remoção de cancelamentos e valores negativos).
- `analise_completa.ipynb`: Notebook com todo o código, limpeza e visualizações.

## 🚀 Como rodar
1. Clone o repositório.
2. Instale as dependências: `pip install pandas | matplotlib | numpy`
3. Abra o arquivo `analise_completa.ipynb` no Jupyter/VS Code e execute as células.

# Dados

A base **não é versionada** neste repositório (tamanho e licença). Para rodar a análise:

1. Abra a página da base: https://archive.ics.uci.edu/dataset/352/online+retail e confira a licença de uso.
2. Baixe o arquivo `.zip` e extraia o `Online Retail.xlsx`.
3. Salve o arquivo nesta pasta (`dataset/`) com o nome `Online Retail.xlsx`.

O notebook também aceita uma versão em CSV chamada `online_retail.csv` (aceita vírgula ou ponto como separador decimal).

Colunas esperadas: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`.
O período esperado é de 01/12/2010 a 09/12/2011. O notebook para com uma mensagem clara se o período ou os tipos de dado estiverem fora disso.

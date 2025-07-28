# Projeto_1_Programa_Desenvolve_GB


<img width="988" height="799" alt="Image" src="https://github.com/user-attachments/assets/33b05318-28d4-428d-a9fb-77b84462f37d" />


## Projeto: Data-Driven Insights

Este repositório contém um projeto prático de **exploração e visualização de dados com Python**, utilizando uma base de **dados simulados de vendas** disponível no Kaggle.

---

### Objetivo

Explorar, transformar e visualizar dados com base em estruturas do Python e bibliotecas como **pandas**, **numpy** e **matplotlib**, gerando **insights descritivos** sobre vendas, clientes e produtos.

---

### Base de Dados

**🛍️ Sample Sales Data**
Fonte: [Kaggle – Sample Sales Data](https://www.kaggle.com/datasets/kyanyoga/sample-sales-data)
Formato: `.csv`

A base contém informações como:

* Número do pedido (`ORDERNUMBER`)
* Quantidade de produtos pedidos (`QUANTITYORDERED`)
* Preço unitário (`PRICEEACH`)
* Valor total da venda (`SALES`)
* Data do pedido (`ORDERDATE`)
* Status do pedido (`STATUS`)
* Categoria do produto (`PRODUCTLINE`)
* País e cidade do cliente (`COUNTRY`, `CITY`)
* Nome do cliente e contato

---

### 🧰 Tecnologias e Bibliotecas Utilizadas

* Python 3
* Google Colab
* `pandas`
* `numpy`
* `matplotlib`

---

### Funcionalidades do Projeto

* ✔️ Uso de **listas, tuplas e dicionários**
✔️ Aplicação de **condicionais** (`if/else`) e **loops** (`for`, `while`)
✔️ **Manipulação de dados com pandas** (criação, exclusão, modificação de colunas)
✔️ Operações vetoriais com **NumPy**
✔️ **Filtragens, agrupamentos e resumos estatísticos**
✔️ Visualizações com gráficos de:

* **Linha** (Quantidade de produtos Vendidos por mês)
* **Barras** (Vendas em $ por Pais)
* **Dispersão** (Relação entre preço e total vendido)

✔️ Comentários explicativos e **insights** em Markdown
✔️ **Relatório final** com principais descobertas

---

### Principais Aprendizados e Descobertas


## Relatório Final – *Data Driven Insights*

Neste projeto, explorei a base **Sample Sales Data**, com um total de **N linhas e Y colunas** (substituir após análise final). A base traz informações sobre pedidos, produtos, clientes e valores de vendas.

Ao longo da análise, utilizei **listas, tuplas, dicionários, estruturas condicionais, laços, arrays NumPy e visualizações com matplotlib**, extraindo padrões e curiosidades sobre comportamento de compra, sazonalidade e produtos mais relevantes.

---

### **Etapa 2 – Leitura e Exploração Inicial da Base**

* **Insight 1:** A leitura inicial falhou devido à codificação do arquivo `.csv`, que não era UTF-8. Corrigi adicionando `encoding='latin1'` no `read_csv`.
* **Insight 2:** Através do `df.head()`, percebi que a base inclui dados de pedidos, produtos, preços e clientes — permitindo analisar itens mais vendidos, sazonalidade, destinos e tamanhos das encomendas.
* **Insight 3:** O `df.columns` revelou 25 colunas relacionadas ao processo de vendas.
* **Insight 4:** O `df.dtypes` mostrou que a maioria das colunas são do tipo `object`, seguidas por `int` e `float`.

---

###  **Etapa 3 – Listas, Dicionários e Tuplas**

* **Insight 5:** Analisando a coluna `DEALSIZE`, percebi que a maioria das encomendas é de tamanho **médio** — indicando um padrão de compra consolidado.
* **Insight 6:** Cruzando `CUSTOMERNAME` com `DEALSIZE`, confirmei que clientes estão comprando em quantidades médias ou maiores.
* **Insight 7:** Identifiquei que a loja **Land of Toys Inc.**, localizada em **New York City**, encomendou 30 produtos — primeiro registro da base.

---

### **Etapa 4 – Condicionais e Laços**

* **Insight 8:** A soma das 5 primeiras vendas (`SALES`) resultou em **18.473,21**, mostrando alto valor logo no início da base.
* **Insight 9:** O primeiro valor de venda acima de 5000 ocorreu na **linha 4**, facilitando a identificação de grandes transações.

---

### **Etapa 5 – Operações Aritméticas com Pandas**

* **Insight 10:** Realizei uma divisão entre o total da venda e o preço do produto, identificando que a maior quantidade vendida ocorreu na **linha 4**.
* **Insight 11:** Ao simular descontos, observei que o total das vendas sofreu **reduções significativas**, evidenciando o impacto de promoções.

---

### **Etapa 6 – NumPy e Arrays**

* **Insight 12:** Analisando a coluna `QTR_ID`, notei repetição dos trimestres 1, 2 e 3, sugerindo picos de vendas nesses períodos.
* **Insight 13:** Concentrei a análise na coluna `PRICEEACH`, por ser mais adequada a operações numéricas diretas.
* **Insight 14:** Realizei as operações `+10`, `*2`, `**2`, além de média, valor máximo e mínimo:

  * **Média**: 83.66 → maioria dos produtos custa acima de 60.
  * **Máximo**: 100.0 → valor de topo coerente com a média.
  * **Mínimo**: 26.88 → valor muito abaixo da média, com z-score de -2.81, indicando dispersão significativa.

---

### **Etapa 7 – Manipulação com Pandas**

* **Insight 15:** Simulei um aumento de preço unitário de R\$10 (como imposto ou reajuste).
* **Insight 16:** Simulei também o dobro do preço unitário, como se fossem compradas 2 unidades por item, como isso pode-se simular o valor de um combo de produtos.
* **Insight 17:** Obti os valores agregados:

  * Soma dos preços unitários: **236.168,07**
  * Média: **83,66**

---

### **Etapa 8 – Visualização de Dados com Matplotlib**

* **Insight 18:** Gráfico por mês (`MONTH_ID`) mostrou menor volume de vendas nos meses 6 a 9 e **pico em novembro (mês 11)**, sugerindo sazonalidade natalina.
* **Insight 19:** Gráfico por país (`COUNTRY`) revelou que os países com **maior volume de vendas** foram:

  1. USA
  2. Spain
  3. France
     E os com **menor volume**:
  4. Ireland
  5. Philippines
  6. Belgium
* **Insight 20:** Gráfico de dispersão (`PRICEEACH` x `SALES`) mostrou maior concentração de vendas entre preços **90 e 100**, com baixa recorrência entre **25 e 40**, mas com **dispersões significativas** em torno de 35, 75 e 90.

---

### 📌 **Reflexões Finais**

Este projeto possibilitou entender a base de vendas simuladas em múltiplas dimensões, aplicando conceitos fundamentais de Python, Pandas e NumPy com foco analítico.
Com essas análises, novas perguntas podem ser investigadas:

* Quais clientes compram com maior frequência?
* Existe relação entre tipo de produto e país de envio?
* O preço médio varia por trimestre?



### Como Executar

1. Abra o notebook `data_driven_insights.ipynb` no [Google Colab](https://colab.research.google.com/drive/1-DsItyT-BvNIqPNnQDT2xHAgA9f3S8Dc#scrollTo=ZXAFTc-I8F6T)
2. Execute as células em ordem
3. Siga as anotações em Markdown para entender cada etapa da análise

---

### 👩🏾‍💻 Feito com propósito e curiosidade por

**Carol Ribeiro** – [LinkedIn]((https://www.linkedin.com/in/carolisribeiro/)


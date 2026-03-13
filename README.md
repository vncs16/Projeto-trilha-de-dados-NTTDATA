# 🚦 Análise de Impacto e Letalidade no Trânsito (Belo Horizonte - 2021)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)

## 📖 Visão Geral do Projeto
Este projeto de Engenharia e Análise de Dados tem como objetivo quantificar o risco viário e o impacto do trânsito na saúde pública da cidade de Belo Horizonte. 

Indo além da simples contagem de acidentes, este estudo cruza dados de ocorrências de trânsito com bases demográficas e de mortalidade geral, estabelecendo métricas padronizadas (como a taxa de letalidade por 100 mil habitantes) e contextualizando os números dentro do cenário atípico da pandemia de COVID-19 no ano de 2021.

## 🎯 Objetivos e Problemas de Negócio Resolvidos
- **Qualidade de Dados:** Limpeza e tratamento de bases governamentais brutas (Data Parsing).
- **Modelagem Relacional:** Criação de um banco de dados local para cruzamento de múltiplas fontes.
- **Identificação de Padrões:** Descoberta de sazonalidades (dias da semana mais críticos) e tipologias de acidentes mais letais.
- **Apoio à Decisão:** Fornecimento de *insights* baseados em dados para alocação inteligente de recursos de fiscalização e campanhas de educação no trânsito.

## 🗄️ Fontes de Dados
Para garantir a precisão da análise, foram integradas três bases de dados distintas:
1. **Ocorrências Viárias:** Base de acidentes de trânsito. (Fonte: dados.gov)
2. **Mortalidade Geral:** Dados oficiais de óbitos do município (Fonte: **DataSUS**).
3. **Demografia:** População residente oficial e estimada (Fonte: **IBGE**).

## 🛠️ Ferramentas e Tecnologias Utilizadas
- **Python:** Linguagem principal para orquestração e análise.
- **Pandas:** Manipulação, limpeza e enriquecimento dos dados (ETL).
- **Great Expectations:** Validação e garantia de qualidade dos dados limpos.
- **SQLite:** Motor de banco de dados relacional para consultas SQL complexas (`JOINs`, `GROUP BY`, Funções de Agregação e Janela).
- **Matplotlib:** Criação de visualizações de dados e *Storytelling*.

## 📂 Estrutura do Repositório
Para facilitar a reprodutibilidade, o projeto está organizado em *Jupyter Notebooks* focados em cada etapa do pipeline de dados, separando claramente os dados brutos (Raw) dos dados processados (Clean):

📦 analise-transito-bh
 ┣ 📂 dados
 ┃  ┣ 📜 acidentes_transito_original.csv
 ┃  ┣ 📜 obitos_datasus_original.csv
 ┃  ┣ 📜 populacao_ibge_original.xls
 ┃  ┣ 📜 acidentes_transito_limpo.csv
 ┃  ┣ 📜 obitos_gerais_bh_2021.csv
 ┃  ┗ 📜 populacao_bh_utf8.csv
 ┣ 📓 01_limpeza_e_validacao.ipynb    # Tratamento de nulos, tipagem e Great Expectations
 ┣ 📓 02_visualizacao.ipynb           # Geração de gráficos e painéis analíticos
 ┗ 📓 03_banco_de_dados_sql.ipynb     # Criação do BD e Consultas Relacionais

## 📊 Principais Insights
* **A Métrica de Risco Real:** A padronização da taxa de acidentes por 100 mil habitantes permitiu dimensionar o perigo viário de forma comparável a padrões internacionais, fugindo da distorção de números absolutos.
* **O Efeito Pandêmico:** A integração com os dados do DataSUS revelou que, embora o trânsito seja uma causa constante de letalidade, sua proporção frente à mortalidade geral em 2021 foi atipicamente espremida pelo altíssimo volume de óbitos gerados pela COVID-19.
* **Sazonalidade Crítica:** A extração temporal (*Date Parsing* em SQL) comprovou que fins de semana concentram os acidentes de maior gravidade, sugerindo uma correlação entre dias de descanso e direção perigosa.

## 🚀 Como Executar este Projeto Localmente

1. Clone este repositório:
```bash
git clone [https://github.com/vncs16/Projeto-trilha-de-dados-NTTDATA.git](https://github.com/vncs16/Projeto-trilha-de-dados-NTTDATA.git)

Instale as dependências necessárias:
pip install pandas matplotlib sqlite3 great_expectations

Autor
Vinícius | Analista de Dados / Desenvolvedor

### 👨‍💻 Autor
**Vinícius Aguiar** | Analista de Dados / Desenvolvedor  
🔗 [LinkedIn](https://www.linkedin.com/in/vin%C3%ADcius-aguiar/) | 🐙 [GitHub](https://github.com/vncs16)

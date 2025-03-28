# Modelo de Regressão Linear para Avaliação Imobiliária em Vitória-ES

## Descrição do Projeto

Este projeto implementa um modelo de regressão linear múltipla para prever o preço unitário de apartamentos no bairro Praia do Canto, em Vitória-ES. O modelo foi desenvolvido utilizando técnicas de ciência de dados e aprendizado de máquina, com o objetivo de fornecer uma ferramenta quantitativa para auxiliar na tomada de decisões de profissionais do setor imobiliário, investidores e compradores potenciais.

## Funcionalidades

-   **Web Scraping:** Coleta automatizada de dados de anúncios de apartamentos do portal Viva Real.
-   **Carregamento e Preparação de Dados:** Carrega os dados de um arquivo CSV e realiza a limpeza inicial.
-   **Transformação de Variáveis:** Cria a variável `log_Area` a partir da variável `Área`.
-   **Divisão de Dados:** Divide os dados em conjuntos de treinamento e teste.
-   **Treinamento do Modelo:** Implementa um modelo de regressão linear múltipla com variáveis como `log_Area`, `Vagas`, `Padrao` e `Lancamento`.
-   **Avaliação do Modelo:** Avalia o desempenho do modelo utilizando métricas como R² e MSE.
-   **Análise de Resíduos:** Plota o gráfico de resíduos para verificar a adequação do modelo.
-   **Cálculo do VIF:** Calcula o Variance Inflation Factor (VIF) para verificar a multicolinearidade entre as variáveis independentes.

## Tecnologias Utilizadas

-   Python 3.8+
-   Pandas para manipulação e análise de dados
-   NumPy para operações numéricas
-   Selenium e Undetected ChromeDriver para web scraping
-   Statsmodels para construção do modelo de regressão linear
-   Scikit-learn para divisão dos dados em treino e teste e para métricas de avaliação
-   Matplotlib e Seaborn para visualização de dados

## Estrutura do Projeto

modelo-regressao-linear-avaliacao-imobiliaria/ │ ├── dados/ │ └── dados_atualizados_com_lancamentos.csv (Dados com a variável de lançamento) │ └── apt_02.csv (Dados coletados do Viva Real) │ ├── notebooks/ │ └── modelo_regressao.ipynb (Notebook com a construção e avaliação do modelo) │ ├── src/ │ └── web_scraping.py (Script para coleta de dados do Viva Real) │ └── modelo.py (Script com a implementação do modelo de regressão) │ ├── README.md └── requirements.txt

## Como Usar

1.  Clone o repositório:

    ```
    git clone https://github.com/seu-usuario/modelo-regressao-linear-avaliacao-imobiliaria.git
    ```

2.  Instale as dependências:

    ```
    pip install -r requirements.txt
    ```

3.  **Coleta de Dados (Web Scraping):**
    -   Execute o script Python para coletar os dados do Viva Real:

        ```
        python src/web_scraping.py
        ```

    -   O script irá salvar os dados coletados em um arquivo CSV chamado `apt_02.csv` na pasta `dados/`.

4.  **Modelo de Regressão:**
    -   Execute o script Python para carregar os dados, treinar o modelo e avaliar o desempenho:

        ```
        python src/modelo.py
        ```

    -   O script irá carregar os dados do arquivo `dados_atualizados_com_lancamentos.csv`, treinar o modelo de regressão linear e exibir os resultados.

## Resultados

O modelo de regressão linear múltipla é avaliado utilizando métricas como R² e MSE. O gráfico de resíduos é plotado para verificar a adequação do modelo. O Variance Inflation Factor (VIF) é calculado para verificar a multicolinearidade entre as variáveis independentes.

As variáveis utilizadas no modelo são:

-   `log_Area`: Logaritmo da área do apartamento.
-   `Vagas`: Número de vagas de garagem.
-   `Padrao`: Padrão do imóvel (1=baixo, 2=médio, 3=alto, 4=luxo).
-   `Lancamento`: Indica se o imóvel é um lançamento (1 para sim, 0 para não).

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e enviar pull requests.

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Contato

Patrícia Carolina Costa Dias - [pccd23@gmail.com]

Orientador: Prof. César Augusto F. de Rose

Link do projeto: [https://github.com/PatriciaDiasDS/modelo-regressao-linear-avaliacao-imobiliaria](https://github.com/PatriciaDiasDS/modelo-regressao-linear-avaliacao-imobiliaria)



# Análise de Dados: Emendas Parlamentares

Este projeto consiste na análise, limpeza e transformação de um conjunto de dados sobre emendas parlamentares brasileiras utilizando a biblioteca **Pandas** em Python.

## Etapas do Projeto

O desenvolvimento foi dividido em etapas de tratamento de dados para garantir a integridade das análises financeiras.

### 1. Limpeza e Tratamento de Nulos
*   Identificação de valores ausentes em colunas críticas.
*   Preenchimento de valores nulos nas colunas de identificação:
    *   `Código do Autor da Emenda` preenchido com `-1`.
    *   `Nome do Autor da Emenda` preenchido com `'desconhecido'`.

### 2. Transformação de Tipos de Dados
*   Conversão da coluna `Ano da Emenda` de inteiro para **String**, facilitando a plotagem de gráficos e filtros categóricos.
*   Garantia de que a coluna `Valor Empenhado` esteja no formato **Float** para cálculos matemáticos precisos.

### 3. Engenharia de Dados (Criação de Colunas)
*   Criação da coluna **`Saldo a Pagar`**: Calculada através da subtração entre o `Valor Empenhado` e o `Valor Pago`.

### 4. Análise Exploratória
*   **Agrupamento por Região:** Identificação das regiões que mais receberam recursos.
*   **Frequência de Funções:** Levantamento das 5 áreas (funções) com maior volume de emendas registradas.

### 5. Exportação
*   O DataFrame final, após todas as correções e novas colunas, foi exportado para o formato **JSON** (`emendas_transformadas.json`) com orientação por registros.

## Tecnologias Utilizadas
*   **Python 3.14**
*   **Pandas**: Manipulação e análise de dados.
*   **JSON**: Formato para exportação de dados.

## Como executar o projeto
1. Certifique-se de ter o Python e o Pandas instalados.
2. Clone este repositório.
3. Execute o arquivo `.ipynb` ou `.py` para processar os dados.

---

### Aprendizados Técnicos
Durante o projeto, foram solucionados problemas comuns em Ciência de Dados, como:
*   Tratamento de erros de indexação (`KeyError`).
*   Manipulação de memória e eixos do DataFrame (`axis=1`).
*   Persistência de dados após transformações.


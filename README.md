# Análise de Correspondência (ACS / CA) -- Perfil x Tipo de Aplicação

## Descrição do Projeto

Este projeto aplica a **Análise de Correspondência Simples (ACS/CA)**
para investigar a relação entre duas variáveis categóricas: o **Perfil
de Investidor** (Conservador, Moderado, Agressivo) e o **Tipo de
Aplicação Financeira** (Ações, CDB, Poupança).\
A técnica permite identificar **associações**, **oposições** e **padrões
de comportamento** entre categorias, além de representar visualmente
essas relações em um **mapa fatorial**.

------------------------------------------------------------------------

## Etapas do Projeto

### 1. Importação e Análise Inicial dos Dados

-   Carregamento do dataset original (Perfil Aplicação.xlsx), conforme
    referência de Fávero & Belfiore (2017).
-   Visualização e inspeção das variáveis categóricas:
    -   Estudante
    -   Perfil
    -   Tipo de Aplicação
-   Resumo exploratório:
    -   100 observações
    -   3 variáveis categóricas
    -   Perfis distribuídos entre agressivo, moderado e conservador
    -   Aplicações distribuídas entre ações, CDB e poupança

------------------------------------------------------------------------

### 2. Construção da Tabela de Contingência

-   A partir das variáveis Perfil e Tipo de Aplicação, foi construída
    uma **tabela de contingência** contendo as frequências observadas:
    -   Agressivo → 36 ações, 20 CDB, 2 poupança
    -   Moderado → 4 ações, 16 CDB, 5 poupança
    -   Conservador → 5 ações, 4 CDB, 8 poupança

------------------------------------------------------------------------

### 3. Teste de Dependência -- Qui-Quadrado

Aplicação do teste **Qui² de independência** para verificar se existe
relação estatística entre as duas variáveis categóricas.

-   Estatística Qui²: 31.764\
-   Valor-p: 2.13 × 10⁻⁶\
-   Graus de liberdade: 4

Conclusão: Como p \< 0.05, há **associação estatisticamente
significativa** entre Perfil e Tipo de Aplicação.

------------------------------------------------------------------------

### 4. Aplicação da Análise de Correspondência (CA)

-   Ajuste do modelo via biblioteca `prince`.
-   Cálculo das coordenadas das linhas (Perfis) e colunas (Aplicações).
-   Cálculo das medidas fatoriais:
    -   Autovalores
    -   Inércia total
    -   Inércia explicada por dimensão

Resultados: - Autovalores: 0.2332 e 0.0844 - Inércia total: 0.3176 -
Inércia explicada: - Dimensão 1: 73.4% - Dimensão 2: 26.6%

------------------------------------------------------------------------

### 5. Cálculo das Coordenadas Fatoriais

As coordenadas indicaram padrões claros:

-   Agressivo alinhado com Ações\
-   Moderado próximo a CDB\
-   Conservador associado à Poupança

------------------------------------------------------------------------

### 6. Visualização -- Mapa Fatorial

-   Construção manual do gráfico fatorial utilizando `matplotlib`.
-   Plotagem dos perfis e investimentos no plano formado pelas Dimensões
    1 e 2.
-   Interpretação visual:
    -   Dimensão 1 separa investimentos de baixa e alta exposição ao
        risco.
    -   Dimensão 2 diferencia nuances de moderação e preferência.

------------------------------------------------------------------------

## Principais Bibliotecas Utilizadas

pandas\
numpy\
scipy\
matplotlib\
seaborn\
prince\
openpyxl

------------------------------------------------------------------------

## Contato

**E-mail:** thiago.a.v.souza@gmail.com\
**LinkedIn:** https://www.linkedin.com/in/thiagoavsouza/

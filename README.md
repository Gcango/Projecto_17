# Projecto_17
 
Classificação de Crédito de Clientes com Machine Learning
Este projeto visa prever a probabilidade de clientes cumprirem seus pagamentos de empréstimo, utilizando técnicas de Machine Learning. A análise compara três algoritmos de classificação populares — Naive Bayes, Árvore de Decisão e Random Forest — para determinar qual deles oferece o melhor desempenho na detecção de inadimplência.

1. Objetivo do Projeto
O objetivo principal deste projeto é prever se um cliente irá pagar ou não um empréstimo com base em características financeiras e demográficas (ex.: idade, renda, valor do empréstimo). Esta é uma tarefa de classificação binária, onde as classes são:
0: Pagamento do empréstimo em dia.
1: Inadimplência no pagamento do empréstimo.

Para problemas de crédito, é importante otimizar a identificação de clientes inadimplentes, minimizando falsos negativos para reduzir o risco financeiro. As principais métricas de avaliação incluem acurácia, recall e f1-score para a classe 1.
A base de dados original foi adaptada para este projeto e está disponível no Kaggle.

2. Estrutura do Projeto
Este projeto é dividido em diversas etapas descritas no notebook, garantindo uma abordagem estruturada para análise e modelagem:
Análise Inicial dos Dados: Exploração e resumo estatístico das variáveis.
Visualização dos Dados: Gráficos e distribuições para compreensão das variáveis e relações entre elas.
Tratamento de Valores Inconsistentes: Remoção ou ajuste de valores que possam distorcer o modelo.
Pré-processamento: Seleção de variáveis (previsores) que serão usadas nos algoritmos.
Escalonamento e Padronização: Ajuste das variáveis numéricas para melhorar o desempenho dos algoritmos.
Divisão dos Dados: Separação entre dados de treinamento e teste para avaliação imparcial dos modelos.
Salvamento dos Dados Processados: Conversão dos dados para o formato Pickle para armazenamento e reutilização.
Carregamento e Treinamento dos Modelos: Utilização dos dados processados para treinar, testar e avaliar os algoritmos.
Relatório de Classificação: Análise detalhada dos resultados de cada modelo, com métricas de desempenho.

4. Modelos Utilizados e Resultados
3.1 Naive Bayes
Acurácia: 0.938 (93,8%)
Análise das métricas:
Classe 0 (Pagadores): precisão de 0.95, recall de 0.98, f1-score de 0.97.
Classe 1 (Inadimplentes): precisão de 0.84, recall de 0.64, f1-score de 0.73.
Interpretação:
Embora o Naive Bayes tenha uma boa acurácia geral, apresenta dificuldades em identificar a classe 1 (clientes inadimplentes), com um recall de apenas 0.64. Esse baixo recall indica que o modelo tende a classificar inadimplentes incorretamente como pagadores, o que pode ser problemático para o gerenciamento de risco.

3.2 Árvore de Decisão
Acurácia: 0.982 (98,2%)
Análise das métricas:
Classe 0: precisão de 0.99, recall de 0.99.
Classe 1: precisão de 0.91, recall de 0.95, f1-score de 0.93.
Interpretação:
A árvore de decisão demonstrou bom desempenho para ambas as classes, com alta precisão e recall para a classe 1. Isso indica que o modelo é capaz de identificar inadimplentes com maior precisão, o que reduz os riscos financeiros.

3.3 Random Forest
Acurácia: 0.984 (98,4%)
Análise das métricas:
Classe 0: precisão de 0.99, recall de 0.99.
Classe 1: precisão de 0.95, recall de 0.92, f1-score de 0.94.
Interpretação:
O Random Forest oferece desempenho ligeiramente superior ao da árvore de decisão e mantém um bom equilíbrio entre precisão e recall para ambas as classes. A estabilidade deste modelo sugere que ele é bem ajustado para prever tanto clientes pagadores quanto inadimplentes, minimizando erros em ambas as direções.

6. Comparação e Considerações Finais
Naive Bayes: Embora seja eficiente, ele apresenta limitações, especialmente na identificação da classe 1 devido a suposições simplificadas sobre a independência das variáveis. Isso o torna menos adequado para problemas de crédito, onde as variáveis como idade e renda podem ter correlações importantes.
Árvore de Decisão: Este modelo mostrou-se eficaz, oferecendo um bom equilíbrio entre precisão e recall para a classe 1, o que é crucial para reduzir riscos financeiros.
Random Forest: Com a melhor acurácia e métricas estáveis, o Random Forest é o modelo mais adequado para este problema. A combinação de múltiplas árvores permite um desempenho robusto e minimiza a variância, sendo ideal para problemas de classificação complexos como a análise de crédito.

7. Conclusão e Recomendação
Com base nas análises, Random Forest é o modelo recomendado para este problema. Ele apresenta um excelente equilíbrio entre precisão e recall, com uma acurácia muito alta, e é capaz de lidar com a complexidade e variabilidade dos dados de crédito. Este modelo pode ser implementado para fornecer uma previsão confiável, auxiliando na gestão de risco para concessão de crédito.

9. Repositório
O notebook deste projeto contém a implementação detalhada e a análise dos modelos. Para cada modelo, foram incluídos os passos de pré-processamento, treinamento, avaliação e interpretação dos resultados. Os dados processados também foram armazenados em formato Pickle para facilitar a reprodução e o uso em outras análises.

Nota: Este projeto utiliza uma base de dados adaptada, originalmente encontrada no Kaggle.



Organização do Repositório
notebooks/: Contém o notebook principal com toda a análise, processamento de dados, implementação dos modelos e relatórios de desempenho.
data/: Arquivo de dados em formato CSV.
models/: Modelos salvos e arquivos Pickle com dados processados.


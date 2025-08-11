Análise Preditiva de Evasão de Clientes (Churn) - Telecom X

🚀 Visão Geral do Projeto

Este projeto utiliza técnicas de Machine Learning para construir um modelo preditivo capaz de identificar clientes em risco de evasão (Churn) para a empresa de telecomunicações Telecom X. O objetivo é fornecer insights estratégicos e acionáveis, permitindo à empresa atuar de forma proativa na retenção de sua base de clientes.

🎯 Objetivo de Negócio

    Prever quais clientes têm maior probabilidade de cancelar seus serviços (Churn).

    Identificar os principais fatores que influenciam a evasão.

    Oferecer recomendações estratégicas para mitigar o Churn e aumentar a fidelidade do cliente.

📈 Metodologia (Pipeline de Machine Learning)

O projeto seguiu um pipeline robusto e validado, documentado em um Jupyter Notebook (.ipynb). As principais etapas foram:

    Pré-processamento de Dados:

        Carregamento e análise exploratória do dataset df_limpo.csv.

        Remoção de colunas irrelevantes (customerID).

        Tratamento de valores nulos e inconsistências.

    Engenharia de Features:

        Aplicação de One-Hot Encoding para variáveis categóricas.

        Cálculo do VIF (Fator de Inflação da Variância) para verificar a multicolinearidade das features.

        Análise da matriz de correlação para identificar as variáveis mais relevantes.

    Modelagem e Treinamento:

        Aplicação da técnica de Oversampling SMOTE no conjunto de treino para balanceamento de classes.

        Padronização dos dados numéricos com StandardScaler.

        Divisão dos dados em treino e teste, e treinamento de dois modelos de classificação: Regressão Logística e Random Forest.

    Avaliação e Interpretação:

        Avaliação do desempenho dos modelos com accuracy_score e classification_report.

        Análise da importância das variáveis do modelo Random Forest para extrair insights estratégicos.

✨ Principais Resultados

O modelo de Random Forest foi o melhor performer, destacando-se na identificação de clientes de risco.

    Acurácia: 77.43% 

F1-Score (Churn): 0.64  - Um bom equilíbrio entre a capacidade do modelo de identificar clientes que evadem (recall) e a precisão de suas previsões.

Conclusão Estratégica e Recomendações

A análise de importância das variáveis nos permitiu identificar os fatores mais críticos para o Churn, que formam a base das seguintes recomendações:

    Foco na Retenção de Clientes em Contratos Mensais: A variável account.Contract_Month-to-month é o fator mais importante para prever a evasão. A empresa deve criar programas de fidelidade para incentivar a migração para contratos mais longos.

    Engajamento de Novos Clientes: O customer.tenure (tempo de cliente) é o segundo fator mais relevante. Recomenda-se um esforço de engajamento e suporte nos primeiros meses de serviço.

    Análise de Custo-Benefício do Serviço de Fibra Óptica: A alta importância de internet.InternetService_Fiber optic sugere uma investigação na qualidade ou nos custos percebidos por clientes deste serviço.

    Otimização de Pagamentos e Segurança: Incentivar a migração de pagamentos via cheque eletrônico e reforçar a oferta de segurança online são ações que podem mitigar a evasão.

🛠️ Instruções de Uso

Para replicar este projeto, clone o repositório e utilize um ambiente com as seguintes bibliotecas instaladas:
Bash

pandas
numpy
scikit-learn
seaborn
matplotlib
imblearn
statsmodels

O arquivo Telecom_X_Analise_Preditiva.ipynb contém o código completo e os comentários passo a passo.

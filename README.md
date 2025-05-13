# Projeto Churn - Previsão de Cancelamento de Clientes em Telecom

🧠 Sobre o Projeto

Este projeto tem como objetivo prever quais clientes de uma empresa de telecomunicações estão propensos a cancelar o serviço (churn), permitindo ações proativas por parte da empresa para reduzir a perda de clientes.

O projeto simula um cenário real de negócios e foi desenvolvido seguindo todas as etapas de um pipeline de ciência de dados: EDA, pré-processamento, modelagem preditiva e deploy com Streamlit.

🎯 Objetivo de Negócio

Empresas do setor de telecom enfrentam grandes desafios com altas taxas de cancelamento. Saber quais clientes têm maior risco de churn é crucial para direcionar campanhas de retenção, personalizar o atendimento e evitar prejuízos.

Com base em dados históricos, desenvolvi um modelo de Machine Learning para:

Prever se um cliente irá cancelar.
Oferecer uma interface simples para uso interno (via API Streamlit).

1. Exploração dos Dados (EDA)
Verifiquei padrões de cancelamento por tipo de contrato, serviços contratados e comportamento de pagamento.
Destaques:
Contratos mensais apresentaram mais churn.
Clientes com suporte técnico e cobrança eletrônica tendem a cancelar mais.
2. Pré-processamento
Tratamento de dados nulos.
Codificação de variáveis categóricas (OneHotEncoder).
Normalização com StandardScaler.
Balanceamento com SMOTE para lidar com o desbalanceamento (apenas 26% dos clientes cancelam).
3. Modelagem Preditiva
Modelos testados: Regressão Logística e Random Forest.
Melhor resultado com Random Forest + SMOTE:
Acurácia: 77%
AUC: 0.70
Recall otimizado para a classe "cancelou".
4. Deploy com Streamlit
Criação de uma API simples e interativa com Streamlit.
Usuário preenche as informações do cliente e o modelo retorna a previsão:
“Cliente vai cancelar” ou “Cliente vai permanecer”.

⚙️ Tecnologias Utilizadas

Python 3.12
Pandas & NumPy
Matplotlib & Seaborn
Scikit-learn
Imbalanced-learn (SMOTE)
Streamlit
Pickle

✅ Resultados

Interface de fácil uso para previsão individual.
Modelo robusto com bom desempenho e equilíbrio entre precisão e recall.
Solução pronta para ser integrada a fluxos de negócios reais.

📌 Próximos Passos

Implementar logging de uso da API.
Subir a aplicação em nuvem (Ex: Streamlit Cloud ou AWS).
Melhorar a explicabilidade com SHAP ou LIME.



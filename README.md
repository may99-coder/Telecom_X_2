# Telecom_X_2
# 📊 Relatório Detalhado sobre Evasão de Clientes

Este relatório sumariza as descobertas da análise exploratória de dados e dos modelos de machine learning treinados para prever a evasão de clientes. O objetivo é identificar os principais fatores de risco e propor estratégias eficazes de retenção.

---

## 1. 🔍 Análise de Correlação e Importância das Variáveis

A análise de correlação e a importância das variáveis (obtida dos modelos) revelaram insights importantes sobre quais fatores estão mais associados à evasão:

- **Tempo de Contrato (`customer.tenure`)**: Foi consistentemente uma das variáveis mais importantes em todos os modelos. Clientes com menor tempo de contrato tendem a ter maior probabilidade de evasão.
- **Total Gasto (`account.Charges.Total`)**: Embora menos correlacionado que o tempo de contrato, o total gasto apareceu como fator relevante, especialmente no modelo Random Forest.
- **Cobranças Mensais (`account.Charges.Monthly`)**: Clientes que evadiram apresentaram, em geral, cobranças mensais mais altas.
- **Serviço de Internet (Fibra Óptica vs. DSL)**: Clientes com Fibra Óptica mostraram maior chance de evasão.
- **Suporte Técnico (`internet.TechSupport`)**: A ausência de suporte técnico online foi identificada como um fator de risco.
- **Contrato (`account.Contract`)**: Clientes com contratos de mês a mês têm maior probabilidade de evasão do que contratos anuais.
- **Pagamento Online (`account.PaperlessBilling`)**: Clientes com contas online demonstraram maior propensão à evasão.
- **Método de Pagamento (Cheque Eletrônico)**: Também associado à evasão.
- **Serviços de Streaming (`internet.StreamingTV`, `internet.StreamingMovies`)**: Influenciaram a evasão em alguns modelos.

---

## 2. 🤖 Desempenho dos Modelos

Avaliou-se o desempenho de quatro modelos de classificação na previsão de evasão: **Regressão Logística**, **Random Forest**, **KNN** e **SVM Linear**. As métricas principais comparadas foram:

| Modelo              | Acurácia | F1-score (macro) | Precisão (macro) | Recall (macro) |
|---------------------|----------|------------------|------------------|----------------|
| Regressão Logística | 0.7974   | 0.7267           | 0.7415           | 0.7164         |
| SVM Linear          | 0.7913   | 0.7200           | 0.7324           | 0.7111         |
| Random Forest       | 0.7847   | 0.7030           | 0.7240           | 0.6907         |
| KNN                 | 0.7444   | 0.6697           | 0.6712           | 0.6684         |

> 💡 A **Regressão Logística** teve o melhor desempenho geral.

---

## 3. ⚠️ Principais Fatores de Risco de Evasão

Com base nas análises:

- **Clientes Novos**: Pouco tempo de contrato aumenta risco de evasão.
- **Clientes com Fibra Óptica**: Maior risco, possível insatisfação com o serviço.
- **Sem Suporte Técnico**: Mais propensos a evadir.
- **Contrato Mês a Mês**: Flexibilidade facilita evasão.
- **Contas Online**: Podem indicar menor engajamento.
- **Cheque Eletrônico**: Método associado a maior evasão.

---

## 4. 🛡️ Estratégias de Retenção Propostas

Com base nos fatores de risco, propõem-se:

1. **Foco em Novos Clientes**: Onboarding efetivo e ofertas nos primeiros meses.
2. **Análise da Evasão com Fibra Óptica**: Pesquisas de satisfação e auditoria técnica.
3. **Promoção de Suporte Técnico Online**: Incentivos e melhorias no canal.
4. **Incentivos para Contratos Longos**: Benefícios e descontos para fidelização.
5. **Engajamento com Contas Online**: Comunicação personalizada e programas de fidelidade.
6. **Revisão do Cheque Eletrônico**: Investigar causas de insatisfação.
7. **Monitoramento de Clientes de Alto Risco**: Uso dos modelos para ações proativas.
8. **Melhoria Contínua dos Serviços**: Foco na qualidade e suporte ao cliente.

---

## 📌 Conclusão

Este relatório fornece uma base sólida para o desenvolvimento de estratégias de retenção orientadas por dados. A combinação de análise exploratória e machine learning permite não apenas prever a evasão, mas também **atuar preventivamente** para reduzi-la e melhorar a experiência do cliente.


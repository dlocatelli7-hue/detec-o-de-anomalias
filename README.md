 Detecção de Anomalias em Transações Financeiras

# O Problema do Desbalanceamento
Em sistemas de detecção de fraudes, a grande maioria das transações é legítima (~99.8%) e apenas uma pequena fração é fraudulenta (~0.17%). A acurácia tradicional engana nestes cenários, por isso o foco deste projeto é avaliar o desempenho através de **Recall**, **Precision**, **F1-Score** e a curva **PR-AUC**.

# Pré-processamento dos Dados
- **Escalamento:** Aplicação de `StandardScaler` nos campos de tempo e valor.
- **Divisão Estratificada:** Separação em treino e teste mantendo a proporção real das classes de fraude.

# Modelos Comparados
1. **Regressão Logística** Com ajuste `class_weight='balanced'`.
2. **Random Forest:** Modelo ensemble com pesos ajustados para equilibrar o aprendizado.
3. **XGBoost Classifier:** Otimizado com `scale_pos_weight`.

## 📐 Métricas e Explicabilidade
- **Ajuste de Limiar (Thresholding):** Otimização da fronteira de decisão para priorizar a captura de fraudes (Recall) reduzindo falsos alarmes.


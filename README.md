# Previsão de Estouro de Peso na Coleta de Resíduos

Este projeto utiliza Regressão Linear Múltipla para prever a quantidade de **estouros de peso** nos caminhões de coleta de resíduos da empresa **Ponta Grossa Ambiental**, com o objetivo de tornar a operação mais eficiente e segura.

---

## 🏭 Contexto

A frota da empresa conta com **22 caminhões**, operando em **67 setores de coleta**, divididos entre **dois turnos (Diurno e Noturno)** e **duas frequências (SEG/QUA/SEX e TER/QUI/SÁB)**.

Cada caminhão, visando agilidade, frequentemente ultrapassa o limite de peso especificado pelo fabricante — situação chamada de **estouro de peso**, que acarreta:

- Desgaste excessivo de molas, pneus e motor
- Risco estrutural ao caminhão
- Aumento da chance de acidentes

---

## 🎯 Objetivo

Criar um modelo preditivo capaz de **estimar a quantidade de estouros de peso** de acordo com:

- Quilometragem total da coleta (Km)
- Peso estimado a ser coletado (Kg)
- Dia da semana (DDS)

---

## 🔍 Dados Utilizados

Cada entrada no conjunto de dados contém:

- Data da coleta
- Peso total coletado no dia
- Quilometragem total percorrida
- Dia da semana
- Quantidade de estouros de peso (variável-alvo)

---

## 🧠 Modelo

Utilizamos um modelo de **Regressão Linear Múltipla**, treinado para prever a variável `ACIMA`, que representa a quantidade de estouros de peso.

### ⚙️ Métricas de Desempenho

| Métrica | Resultado | Interpretação |
|--------|-----------|---------------|
| MSE    | 6.85      | Erro médio quadrático. Penaliza mais os erros grandes |
| RMSE   | 2.62      | Erro médio quadrático na mesma unidade da variável alvo |
| MAE    | 2.07      | Erro médio absoluto (±2 ocorrências) |
| R²     | 0.89      | 89% da variabilidade explicada pelo modelo |

---

## 📈 Como esse modelo impacta a operação?

- **Planejamento inteligente**: permite alterar trajeto, frequência e turno visando reduzir estouros
- **Redução de custos**: menos manutenções com molas, pneus, motor e compactador
- **Segurança**: menos risco de acidentes causados por excesso de carga
- **Monitoramento de desempenho**: comparação entre o previsto e o real
- **Apoio à reestruturação da setorização da cidade**

---

## ▶️ Como usar

Dada uma entrada com:

- `Km` total a ser percorrido
- `Kg` estimado a ser coletado
- `Dia da semana`

O modelo retorna o número previsto de **estouros de peso** para aquele dia.

---

## 📁 Estrutura do Projeto

```
projeto-estouro-peso/
├── data/               # Dados brutos ou pré-processados
├── notebooks/          # Análises exploratórias e modelagem (Jupyter/Colab)
├── src/                # Scripts Python
├── models/             # Modelos treinados (se aplicável)
├── results/            # Gráficos e tabelas de avaliação
├── README.md           # Este arquivo
└── requirements.txt    # Dependências (opcional)
```

---

## 🚧 Próximos Passos

- Incluir variáveis climáticas (chuva, temperatura) na previsão
- Testar outros algoritmos (Random Forest, XGBoost)
- Criar uma dashboard interativa com Streamlit


## 📌 Conclusão

Com esse modelo, a empresa passa a tomar decisões **baseadas em dados**, reduzindo custos, otimizando a coleta e aumentando a segurança da operação. A previsão de estouros de peso, antes impossível, agora é uma ferramenta prática e acessível para o dia a dia da gestão.

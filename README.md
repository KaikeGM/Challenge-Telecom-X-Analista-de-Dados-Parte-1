# Análise de Evasão de Clientes - Telecom X

## Descrição do Projeto
Este projeto visa analisar os fatores que contribuem para a evasão de clientes (churn) na Telecom X. Através de análise exploratória de dados (EDA), identificamos padrões e características comuns entre os clientes que cancelam o serviço. Os insights gerados servirão de base para ações estratégicas de retenção de clientes.

## Contexto de Negócio
A Telecom X enfrenta um alto índice de cancelamentos (churn) e precisa entender os motivos que levam os clientes a deixarem a empresa. A análise visa responder:
- Quais características dos clientes estão mais associadas à evasão?
- Quais serviços ou planos têm maior impacto na retenção?
- Como fatores financeiros (mensalidade, gastos totais) se relacionam com o churn?

## Principais Análises e Insights

### 1. Distribuição de Churn
- **25.4%** dos clientes cancelaram o serviço
- Clientes ativos representam **74.6%** da base
- Taxa de evasão dentro do esperado para o setor (15-30%)

![Distribuição de Churn](baixados5.png)

### 2. Fatores Críticos de Evasão

#### a) Tipo de Contrato
- **Contrato mensal**: 41.0% evasão
- **Contrato anual**: 10.9% evasão
- **Contrato bianual**: 2.8% evasão

**Insight**: Contratos de longo prazo reduzem drasticamente a evasão.

![Evasão por Contrato](Captura%20de%20tela%202025-06-10%20191839.png)

#### b) Método de Pagamento
- **Cheque eletrônico**: 43.2% evasão
- **Cartão de crédito (automático)**: 14.8% evasão

**Insight**: Pagamentos automáticos reduzem a evasão em mais de 60%.

#### c) Serviços Adicionais
- **Sem segurança online**: 40.0% evasão
- **Com segurança online**: 14.2% evasão
- **Sem suporte técnico**: 39.8% evasão
- **Com suporte técnico**: 14.7% evasão

**Insight**: Serviços adicionais são fortes fatores de proteção contra evasão.

![Evasão por Suporte Técnico](Captura%20de%20tela%202025-06-10%20191720.png)

### 3. Análise Financeira

#### a) Gastos Mensais
- Clientes que evadem: **R$74.93** (média)
- Clientes ativos: **R$61.57** (média)
- Diferença: **21.7% mais alto** para quem cancela

**Insight**: Mensalidades mais altas estão associadas a maior risco de evasão.

![Distribuição de Gastos Mensais](baixados3.png)

#### b) Gastos Totais
- Clientes que evadem: **R$1,569.06** (média)
- Clientes ativos: **R$2,554.50** (média)
- Diferença: **38.6% menor** para quem cancela

**Insight**: Clientes fiéis geram mais receita e têm menor propensão a cancelar.

![Distribuição de Gastos Totais](baixados2.png)

### 4. Correlações Principais
As variáveis mais correlacionadas com churn são:
- **Positivo** (aumentam evasão):
  - Pagamento por cheque eletrônico: 0.29
  - Gastos mensais elevados: 0.19
- **Negativo** (reduzem evasão):
  - Contrato bianual: -0.29
  - Serviços de segurança/suporte: -0.16

![Correlações com Evasão](baixados1.png)

## Conclusões e Recomendações

### Principais Conclusões
1. **Contratos mensais** são o maior fator de risco para evasão
2. **Pagamentos não automáticos** (cheque eletrônico) dobram o risco de churn
3. **Serviços adicionais** (segurança e suporte) são fortes fatores de proteção
4. Clientes com **mensalidades altas** e **pouco tempo de contrato** são os mais propensos a cancelar

### Recomendações Estratégicas
1. **Converter contratos mensais em anuais:**
   - Oferecer desconto de 10-15% no primeiro ano
   - Benefícios adicionais (ex: 3 meses grátis de streaming)

2. **Incentivar pagamentos automáticos:**
   - Desconto de 5% para pagamentos automáticos
   - Campanha de migração com suporte prioritário

3. **Promover pacotes de serviços adicionais:**
   - Pacote "Segurança Total" (OnlineSecurity + TechSupport) por R$15/mês
   - Teste gratuito por 30 dias

4. **Programa de fidelidade para clientes de alto valor:**
   - Benefícios progressivos para clientes com mensalidade > R$80
   - Atendimento prioritário e descontos em serviços adicionais

**Meta**: Reduzir a taxa de evasão em 30% nos próximos 12 meses

## Como Reproduzir a Análise

### Pré-requisitos
- Python 3.11+
- Bibliotecas: pandas, numpy, matplotlib, seaborn

### Instalação
```bash
pip install pandas numpy matplotlib seaborn
```

### Execução
1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/telecom-churn-analysis.git
```

2. Execute o notebook Jupyter:
```bash
jupyter notebook telecom_churn_analysis.ipynb
```

### Estrutura de Arquivos
```
telecom-churn-analysis/
├── data/
│   └── telecom_dataset.csv
├── notebooks/
│   └── telecom_churn_analysis.ipynb
├── reports/
│   └── churn_analysis_report.pdf
├── README.md
└── requirements.txt
```

## Referências
- Dataset: Base interna da Telecom X (2025)
- Bibliotecas Python: pandas, seaborn, matplotlib
- Referências metodológicas: CRISP-DM, Análise Exploratória de Dados (EDA)

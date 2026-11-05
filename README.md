# 🧮 Calculadoras Trabalhistas — SENAI 2026

Projeto acadêmico desenvolvido em Python para simular cálculos de folha de pagamento e rescisão trabalhista. O repositório reúne dois notebooks independentes, organizados para fins de estudo.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-orange?logo=jupyter&logoColor=white)
![SENAI](https://img.shields.io/badge/Projeto-SENAI-red)

## 🧭 Neste projeto

- [Calculadora de Folha de Pagamento (FOPAG)](#-calculadora-de-folha-de-pagamento-fopag)
- [Calculadora de Rescisão](#-calculadora-de-rescisão)
- [Destaques técnicos](#️-destaques-técnicos)
- [Como executar](#-como-executar)
- [Aviso de uso](#️-aviso-de-uso)

## 💼 Calculadora de Folha de Pagamento (FOPAG)

Notebook para simular a folha de pagamento e gerar um demonstrativo com proventos e descontos.

[![Abrir FOPAG no Colab 💼](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thbieltraining/Calculadora-SENAI/blob/main/CALCULADORA_SENAI_ADME2026.ipynb)

### Funcionalidades

- **Salário e adicionais de risco**
  - Insalubridade nos graus mínimo (10%), médio (20%) e máximo (40%), conforme os parâmetros definidos no projeto.
  - Periculosidade de 30% sobre o salário-base.
- **Horas extras**
  - Adicionais parametrizados de 50%, 70% e 100%.
  - Arredondamento em duas etapas: valor da hora e valor total.
- **Faltas e DSR**
  - Leitura de períodos no formato `m-s-d` (mês, semana e dias), com suporte a múltiplos registros, como `4-3-1, 5-1-1`.
  - Cálculo do desconto de faltas e tratamento da perda do DSR por semana com falta injustificada.
- **Férias**
  - Cálculo dos dias de férias e do adicional constitucional de 1/3.
  - Simulação de abono pecuniário.
- **13º salário**
  - Projeção por avos trabalhados.
  - Simulação da primeira e da segunda parcela.
- **Descontos**
  - Cálculo de INSS e IRRF com os parâmetros configurados no projeto.
  - Vale-transporte limitado a 6% do salário-base.

### Executar a FOPAG no Google Colab

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1eaNgiV_8z6LJMG_x95SbOYrQdiR_PoSw?usp=sharing)

## 🧾 Calculadora de Rescisão

Notebook independente, com foco na simulação das verbas e dos descontos relacionados ao encerramento do contrato de trabalho.

[![Abrir calculadora de rescisão no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thbieltraining/Calculadora-SENAI/blob/main/CALCULADORA_RESCISAO_SENAI_2026.ipynb)

### Funcionalidades

- Cálculo de saldo de salário e descontos por faltas.
- Cálculo de aviso-prévio e projeção, quando aplicável.
- Apuração de 13º salário e férias proporcionais.
- Consideração de médias de remuneração variável.
- Simulações relacionadas a contratos de experiência.
- Cálculo de INSS, IRRF, FGTS e multa rescisória.
- Verificação do prazo de pagamento e da possível multa prevista no art. 477 da CLT.
- Emissão de demonstrativo com proventos, descontos, valor líquido e memória de FGTS.

### Executar a calculadora de rescisão no Colab

Depois de enviar o notebook ao repositório, ele poderá ser aberto pelo Colab:

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thbieltraining/Calculadora-SENAI/blob/main/notebooks/RECIS%C3%83O_CALC_SENAI_2026.ipynb)

## 🛠️ Destaques técnicos

- **Precisão monetária:** uso de `decimal.Decimal` e arredondamento `ROUND_HALF_UP`.
- **Organização por responsabilidade:** funções separadas para cálculos, validação de entradas e geração dos demonstrativos.
- **Entradas validadas:** leitura de valores, datas, meses e opções informadas pelo usuário.
- **Notebooks independentes:** FOPAG e rescisão podem ser estudadas e executadas separadamente.

## 🚀 Como executar

### Google Colab

Use o botão de Colab disponível na seção da calculadora desejada.

### Localmente

**Pré-requisitos:** Python 3.8 ou superior e Jupyter Notebook.

1. Clone o repositório:

   ```bash
   git clone https://github.com/thbieltraining/Calculadora-SENAI.git
   cd Calculadora-SENAI

# 🧮 Calculadora de Folha de Pagamento (FOPAG) - SENAI 2026

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Projeto desenvolvido em Python para automação e simulação de cálculos trabalhistas e elaboração de Holerites/Demonstrativos de Pagamento, estruturado com base nas diretrizes acadêmicas do **SENAI** e atualizado com os parâmetros fiscais de **2026**.

---

## 📌 Funcionalidades

- **Salário Base & Adicionais de Risco:**
  - Insalubridade (Graus Mínimo 10%, Médio 20% e Máximo 40% sobre o Salário Mínimo).
  - Periculosidade (30% sobre o Salário Base).
- **Horas Extras (HE):**
  - Cálculo parametrizado para adicionais de **50%**, **70%** e **100%**.
  - Arredondamento em duas etapas (Valor Unitário e Valor Total).
- **Gestão de Faltas & DSR (Descanso Semanal Remunerado):**
  - Leitura avançada via Regex no formato `m-s-d` (Mês-Semana-Dias), com suporte a múltiplos períodos (ex: `4-3-1, 5-1-1`).
  - Tratamento de perda do DSR por semana com falta injustificada.
  - Limite automatizado de retenção (até 14 dias por mês).
- **Férias:**
  - Cálculo de dias gozados + 1/3 constitucional (Tributável).
  - Simulação de Abono Pecuniário (Venda de 10 dias + 1/3 - Isento).
- **13º Salário:**
  - Projeção por avos trabalhados.
  - Simulação de 1ª Parcela (Sem Descontos) e 2ª Parcela (com dedução de INSS e IRRF).
- **Deduções e Impostos Fiscais:**
  - **INSS:** Tabela progressiva atualizada.
  - **IRRF:** Faixas de tributação com verificação de regra de isenção até R$ 5.000,00.
  - **Vale-Transporte (VT):** Desconto limitado ao teto legal de 6% do Salário Base.

---

## 🛠️ Destaques Técnicos

1. **Precisão Monetária (`decimal.Decimal`):** 
   Utiliza `ROUND_HALF_UP` com precisão de duas casas decimais para conformidade com arredondamentos contábeis.
2. **Parsing com Regex:** 
   Expressões regulares para interpretação flexível de entradas complexas do usuário na gestão de faltas.
3. **Modularidade:** 
   Funções isoladas por responsabilidade (cálculo de tributos, adição de adicionais, apuração de HE e geração de demonstrativo).

---

## 🚀 Como Executar

### Pré-requisitos
- Python 3.8 ou superior instalado (não requer instalação de bibliotecas externas, utiliza apenas a biblioteca padrão).

### Passos

1. Clone este repositório:
   ```bash
   git clone [)

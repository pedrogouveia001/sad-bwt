# SAD BWT — Best Worst Tradeoff

Este repositório é o módulo independente do ecossistema **SAD MCDM**, configurado para operar exclusivamente com o método **BWT (Best Worst Tradeoff)**.

---

## 🎨 Identidade Visual e Branding
- **Nome Oficial:** SAD BWT
- **Cores Oficiais:** Carmim (`#DC2626`) e Areia/Dourado (`#D97706`)
- **Conceito Visual:** Curva de bisseção interceptando um plano bidimensional de taxas de tradeoffs locais.
- **Copyright:** Direitos Reservados © 2026 SAD-MCDM. Todos os direitos reservados.

---

## 🧠 Formulação Matemática e Funcionamento

O **Best Worst Tradeoff (BWT)** une os conceitos de simplificação e redução de comparações do método BWM (Best Worst) com a fundamentação científica axiomática da teoria da utilidade multiatributo baseada em taxas reais de tradeoffs.

### 1. Elicitação por Bisseção (Intra-critério)
Para definir as funções de valor de cada critério de forma individual e não-linear, o decisor realiza o processo de bisseção:
* Identifica os limites físicos extremos do critério $j$: pior valor ($x_j^{\min}$) e melhor valor ($x_j^{\max}$).
* Define $v_j(x_j^{\min}) = 0$ e $v_j(x_j^{\max}) = 1$.
* O decisor identifica o ponto intermediário $x_{0.5}$ onde sente que a melhoria de $x_j^{\min}$ para $x_{0.5}$ possui o mesmo ganho de utilidade psicológica que a melhoria de $x_{0.5}$ para $x_j^{\max}$. Portanto, $v_j(x_{0.5}) = 0.5$.
* Repete-se a bisseção para os pontos $x_{0.25}$ e $x_{0.75}$ se for necessário maior fidelidade na curva.

### 2. Taxas de Tradeoff Inter-critério
Para definir as relações reais de pesos cardinais entre os critérios:
* O decisor determina o critério de referência **Best** ($c_B$).
* Para cada outro critério $j$, ele define qual melhoria de consequência no critério $j$ equivale a uma perda específica no critério Best de forma física e real.
* As razões de tradeoff induzem o sistema de desigualdades físicas:
  $$w_B \cdot \Delta v_B \approx w_j \cdot \Delta v_j$$

O solucionador do SAD BWT executa uma Programação Linear que reconcilia os desvios de tradeoff, resolvendo para o conjunto de pesos cardinais ótimos $w^*$ e garantindo a consistência global da elicitação.

---

## 🚀 Instalação e Execução
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```
Acesse: `http://127.0.0.1:5000`

# Nexus BWT — Best Worst Tradeoff

Este repositório é o módulo independente do ecossistema **NEXUS MCDM**, configurado para operar exclusivamente com o método **BWT (Best Worst Tradeoff)**.

---

## 🎨 Identidade Visual e Branding
- **Nome Oficial:** Nexus BWT
- **Cores Oficiais:** Carmim (`#DC2626`) e Areia/Dourado (`#D97706`)
- **Conceito Visual:** Curva de bisseção interceptando um plano bidimensional de taxas de tradeoffs locais.
- **Copyright:** Direitos Reservados © 2026 NEXUS-MCDM.

---

## 🌟 Recursos e Matemática

- **Elicitação Intra-critério por Bisseção:** O decisor ajusta o controle físico para determinar o ponto $x_{0.5}$ onde a utilidade parcial é exatamente 50% ($v(x_{0.5}) = 0.5$).
- **Taxas Reais de Tradeoff:** Comparações par a par estruturadas entre o melhor e pior critério baseadas em taxas físicas reais de substituição.
- **Programação Linear:** Otimização matemática para consistência global e extração de pesos cardinais reais.

---

## 🚀 Instalação e Execução
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
```

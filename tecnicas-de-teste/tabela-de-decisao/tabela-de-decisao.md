# Tabela de Decisão

A **Tabela de Decisão** é uma técnica de projeto de testes amplamente utilizada em testes de software, especialmente em abordagens de **caixa-preta**, quando o sistema possui **múltiplas regras de negócio combinadas**.

De acordo com o *International Software Testing Qualifications Board (ISTQB)*, a tabela de decisão é uma técnica usada para representar combinações de condições e suas respectivas ações, garantindo que todas as combinações relevantes sejam avaliadas.

Segundo Glenford J. Myers:

> **"Quando o resultado do processamento depende de combinações de condições, a tabela de decisão fornece um método sistemático e completo para derivar casos de teste."**

Já Boris Beizer destaca que sistemas com regras de negócio complexas tendem a apresentar defeitos justamente nas **interações entre condições**, e não nas condições isoladas.

---

## Conceito Fundamental

A técnica parte do princípio de que:

> **Quando múltiplas condições influenciam o comportamento do sistema, é necessário testar suas combinações de forma estruturada.**

Uma **Tabela de Decisão** é composta por:

- **Condições** (entradas ou regras)
- **Ações** (saídas ou comportamentos do sistema)
- **Regras** (combinações específicas de condições)

---

## Estrutura de uma Tabela de Decisão

| Elemento | Descrição |
|----------|------------|
| Condições | Fatores que influenciam a decisão |
| Ações | Resultados esperados |
| Regras | Combinações possíveis de condições |
| Colunas | Cada coluna representa um caso de teste |

---

## Quando Utilizar

A técnica é especialmente indicada quando:

- Existem **múltiplas regras de negócio combinadas**;
- Há dependência entre condições;
- O comportamento do sistema varia conforme diferentes cenários;
- É necessário garantir cobertura sistemática das combinações.

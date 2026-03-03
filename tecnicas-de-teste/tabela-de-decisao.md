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

---

## Exemplo Prático – Exercício de Aplicação

### Contexto do Sistema

Um sistema de concessão de desconto possui as seguintes regras:

1. Cliente é cadastrado?
2. Compra acima de R$ 500?
3. Pagamento à vista?

### Regras de Negócio

- Se for cliente cadastrado **e** compra > R$ 500 → 10% de desconto.
- Se não for cadastrado, mas compra > R$ 500 **e** pagamento à vista → 5% de desconto.
- Caso contrário → sem desconto.

---

## Tabela de Decisão

| Condições / Regras        | R1 | R2 | R3 | R4 | R5 | R6 | R7 | R8 |
|---------------------------|----|----|----|----|----|----|----|----|
| Cliente cadastrado?       | S  | S  | S  | S  | N  | N  | N  | N  |
| Compra > R$ 500?          | S  | S  | N  | N  | S  | S  | N  | N  |
| Pagamento à vista?        | S  | N  | S  | N  | S  | N  | S  | N  |
| **Ação: 10% desconto**    | X  | X  |    |    |    |    |    |    |
| **Ação: 5% desconto**     |    |    |    |    | X  |    |    |    |
| **Ação: Sem desconto**    |    |    | X  | X  |    | X  | X  | X  |

Legenda:  
"S" = Sim  
"N" = Não  
"-" = Irrelevante  
"X" = Ação executada  

## Interpretação das Regras

- R1: Cadastrado + Compra > 500 + À vista → 10%
- R2: Cadastrado + Compra > 500 + Não à vista → 10%
- R3: Cadastrado + Compra ≤ 500 + À vista → Sem desconto
- R4: Cadastrado + Compra ≤ 500 + Não à vista → Sem desconto
- R5: Não cadastrado + Compra > 500 + À vista → 5%
- R6: Não cadastrado + Compra > 500 + Não à vista → Sem desconto
- R7: Não cadastrado + Compra ≤ 500 + À vista → Sem desconto
- R8: Não cadastrado + Compra ≤ 500 + Não à vista → Sem desconto

---

## Casos de Teste Derivados

| Caso de Teste | Cliente | Valor Compra | À Vista | Resultado Esperado |
|--------------|----------|--------------|----------|--------------------|
| CT-01 | Sim | 600 | Não | 10% desconto |
| CT-02 | Não | 600 | Sim | 5% desconto |
| CT-03 | Sim | 300 | Não | Sem desconto |
| CT-04 | Não | 300 | Não | Sem desconto |

---

## Relação com Outras Técnicas

A Tabela de Decisão é frequentemente combinada com:

- **Particionamento de Equivalência**, para validar entradas;
- **Análise de Valor Limite**, quando há regras envolvendo limites numéricos;
- Modelagem por estados, quando o comportamento depende de transições.

Segundo Rex Black, a utilização de tabelas de decisão reduz significativamente o risco de omissão de cenários em sistemas orientados a regras de negócio.

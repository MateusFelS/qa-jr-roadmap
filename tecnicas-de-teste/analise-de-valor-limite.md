# Análise de Valor Limite

A **Análise de Valor Limite** é uma técnica de projeto de testes de caixa-preta que complementa o Particionamento de Equivalência, focando especificamente no **comportamento do sistema nas fronteiras entre as partições**.

De acordo com o ISTQB, a experiência mostra que sistemas frequentemente falham nos limites de seus domínios de entrada. Por isso, testar os valores exatos das bordas aumenta significativamente a probabilidade de encontrar defeitos.

Segundo **Ron Patton** (em *Software Testing*):

> **"Mais erros de software ocorrem nos limites dos domínios de entrada do que no meio deles. A análise de valor limite concentra-se exatamente nessas áreas críticas."**

**Louise Tamres** (em *Introducing Software Testing*) complementa que a técnica explora tanto os valores mínimos e máximos aceitos quanto aqueles imediatamente abaixo e acima desses limites, revelando falhas de validação.

---

## Conceito Fundamental

A técnica parte do princípio de que:

> Os erros tendem a se concentrar nas bordas das partições. Portanto, devem ser testados:
> - O valor mínimo da partição
> - O valor máximo da partição
> - O valor imediatamente abaixo do mínimo (inválido)
> - O valor imediatamente acima do máximo (inválido)

---

## Diferença entre Particionamento de Equivalência e Análise de Valor Limite

| Particionamento de Equivalência | Análise de Valor Limite |
|----------------------------------|-------------------------|
| Testa um valor representativo de cada partição | Testa os valores exatos das bordas |
| Foca no comportamento geral do domínio | Foca no comportamento nas fronteiras |
| Ignora extremos (desde que dentro da partição) | Explora limites superior e inferior |
| Reduz quantidade de testes | Aumenta precisão na detecção de falhas |

---

## Regra Geral para Identificação de Valores Limite

Para um domínio com limite inferior **L** e superior **U**:

| Valor | Descrição | Classificação |
|-------|-----------|---------------|
| L - 1 | Abaixo do mínimo | Inválido |
| L     | Mínimo aceito | Válido |
| L + 1 | Acima do mínimo | Válido |
| U - 1 | Abaixo do máximo | Válido |
| U     | Máximo aceito | Válido |
| U + 1 | Acima do máximo | Inválido |

---

## Combinação com Particionamento de Equivalência

Para cobertura completa, as duas técnicas devem ser usadas em conjunto:

1. **Particionamento de Equivalência** → identifica classes válidas e inválidas
2. **Análise de Valor Limite** → testa as fronteiras exatas dessas classes

**Exemplo integrado para campo Idade:**

| Técnica | Valores testados |
|---------|------------------|
| Particionamento | 30 (válido), 17 (inválido), 61 (inválido), "abc" (inválido) |
| Valor Limite | 17, 18, 19, 59, 60, 61 |

Segundo **Cem Kaner** (em *Testing Computer Software*):

> **"As duas técnicas se reforçam mutuamente. O particionamento garante cobertura ampla; a análise de valor limite garante profundidade nas áreas mais propensas a falhas."**

---

## Exercício – Aplicação de Análise de Valor Limite

### Contexto

Sistema de **cadastro de produtos** com as regras:
- Nome do produto: mínimo 3, máximo 100 caracteres
- Preço: mínimo R$ 0,01, máximo R$ 10.000,00
- Quantidade em estoque: mínimo 0, máximo 1.000 unidades
- Categoria: obrigatória (lista fixa com 5 opções)

👉 **Identifique os valores limite para cada campo**

---

### Valores Limite – Campo Nome

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-01 | 2 caracteres | Inválido | Abaixo do mínimo |
| VL-02 | 3 caracteres | Válido | Mínimo |
| VL-03 | 4 caracteres | Válido | Acima do mínimo|
| VL-04 | 99 caracteres | Válido | Abaixo do máximo |
| VL-05 | 100 caracteres | Válido | Máximo |
| VL-06 | 101 caracteres | Inválido | Acima do máximo |

### Valores Limite – Preço

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-07 | R$ 0,00 | Inválido | Abaixo do mínimo |
| VL-08 | R$ 0,01 | Válido | Mínimo |
| VL-09 | R$ 0,02 | Válido | Acima do mínimo |
| VL-10 | R$ 9.999,99 | Válido | Abaixo do máximo |
| VL-11 | R$ 10.000,00 | Válido | Máximo |
| VL-12 | R$ 10.000,01 | Inválido | Acima do máximo |

### Valores Limite – Quantidade em Estoque

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-13 | -1 | Inválido | Abaixo do mínimo |
| VL-14 | 0 | Válido | Mínimo |
| VL-15 | 1 | Válido | Acima do mínimo |
| VL-16 | 999 | Válido | Abaixo do máximo |
| VL-17 | 1.000 | Válido | Máximo |
| VL-18 | 1.001 | Inválido | Acima do máximo |

### Valores Limite – Categoria

Para campos com domínio discreto (lista fixa), a análise de valor limite se aplica de forma adaptada:

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-19 | Nenhuma selecionada | Inválido | Abaixo do mínimo (obrigatório) |
| VL-20 | Primeira opção da lista | Válido | Valor mínimo do domínio |
| VL-21 | Segunda opção | Válido | Representativo |
| VL-22 | Última opção da lista | Válido | Valor máximo do domínio |
| VL-23 | Opção inexistente | Inválido | Acima do máximo |

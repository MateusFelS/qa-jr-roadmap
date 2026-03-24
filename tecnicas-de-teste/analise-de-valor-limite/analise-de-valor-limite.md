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

# Análise de Valor Limite

A **Análise de Valor Limite (AVL)** é uma técnica de projeto de testes utilizada principalmente em testes de **caixa-preta**. Seu objetivo é identificar defeitos que ocorrem nos extremos das faixas de entrada, onde há maior probabilidade de erro.

Segundo Glenford J. Myers:

> **"Erros tendem a ocorrer com maior frequência nos limites do domínio de entrada do que no centro."**

A técnica complementa o **Particionamento de Equivalência**, focando especificamente nos valores de fronteira das partições.

---

## Conceito Fundamental

A técnica parte do princípio de que:

> Se o sistema falhar, há grande probabilidade de a falha ocorrer nos valores mínimos, máximos ou próximos a eles.

Assim, testam-se:

- o valor mínimo permitido;
- o valor máximo permitido;
- valores imediatamente abaixo e acima desses limites.

---

## Tipos de Valores Testados

Para cada limite identificado, normalmente são testados:

| Tipo de Valor | Descrição |
|---------------|------------|
| Logo abaixo do limite inferior | Valor inválido imediatamente menor que o mínimo |
| Limite inferior | Valor mínimo permitido |
| Logo acima do limite inferior | Primeiro valor válido após o mínimo |
| Logo abaixo do limite superior | Último valor válido antes do máximo |
| Limite superior | Valor máximo permitido |
| Logo acima do limite superior | Primeiro valor inválido após o máximo |

---

## Exemplo Prático – Campo "Idade"

### Regras do Sistema

- O valor deve ser numérico.
- Deve estar entre **18 e 60 anos**.
- O campo é obrigatório.

---

## Casos de Teste – Análise de Valor Limite

| ID | Valor Testado | Justificativa | Resultado Esperado |
|----|---------------|---------------|--------------------|
| AVL-01 | 17 | Abaixo do limite inferior | Rejeitar |
| AVL-02 | 18 | Limite inferior | Aceitar |
| AVL-03 | 19 | Acima do limite inferior | Aceitar |
| AVL-04 | 59 | Abaixo do limite superior | Aceitar |
| AVL-05 | 60 | Limite superior | Aceitar |
| AVL-06 | 61 | Acima do limite superior | Rejeitar |

---

## Quando Utilizar

A Análise de Valor Limite é indicada para:

- Faixas numéricas (idade, salário, quantidade)
- Datas (períodos válidos)
- Tamanho mínimo/máximo de caracteres
- Limites de capacidade (memória, registros, armazenamento)
- Índices de listas (primeiro e último elemento)

---

## Relação com Outras Técnicas

A técnica é frequentemente combinada com:

- **Particionamento de Equivalência**, para definir as faixas válidas e inválidas;
- Tabelas de decisão;
- Casos de uso e cenários de teste.

A combinação dessas técnicas aumenta significativamente a probabilidade de identificação de defeitos em validações de entrada.

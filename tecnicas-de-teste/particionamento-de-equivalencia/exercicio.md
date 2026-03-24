# Exemplo Prático – Exercício de Aplicação

## Contexto do Sistema

Considere um campo "Idade" com as seguintes regras:

- O valor deve ser numérico.
- Deve estar entre **18 e 60 anos**.
- O campo é obrigatório.

## Minha Tarefa

Identificar as **partições de equivalência** e seus respectivos valores representativos.

---

## Partições de Equivalência – Campo Idade

| ID | Partição | Tipo | Valor Representativo |
|----|-----------|------|----------------------|
| PE-01 | Idade entre 18 e 60 anos | Válido | 30 |
| PE-02 | Idade menor que 18 anos | Inválido | 17 |
| PE-03 | Idade maior que 60 anos | Inválido | 61 |
| PE-04 | Valor não numérico | Inválido | "abc" |
| PE-05 | Campo vazio | Inválido | "" |
 
---

## Relação com Outras Técnicas

O particionamento de equivalência é frequentemente combinado com:

- **Análise de Valor Limite**, para testar extremos das partições;
- Tabelas de decisão, quando há múltiplas regras combinadas;
- Casos de uso e cenários de teste, para garantir cobertura funcional completa.

Segundo Rex Black, a combinação dessas técnicas aumenta significativamente a probabilidade de identificação de defeitos relacionados a validações de entrada.

# Particionamento de Equivalência

O **Particionamento de Equivalência** é uma técnica de projeto de testes amplamente utilizada em testes de software, especialmente em abordagens de **caixa-preta**. Seu objetivo é **reduzir a quantidade de casos de teste sem comprometer a cobertura funcional**, agrupando entradas que possuem comportamento semelhante.

De acordo com o <entity type="organization">International Software Testing Qualifications Board (ISTQB)</entity>, o particionamento de equivalência consiste em dividir os dados de entrada em grupos (partições) que devem ser tratados da mesma forma pelo sistema.

Segundo Glenford J. Myers:

> **"Os casos de teste devem ser derivados de forma a cobrir classes de equivalência válidas e inválidas, reduzindo o número total de testes necessários sem perder efetividade."**

Já Boris Beizer destaca que as partições devem ser:

- mutuamente exclusivas;
- coletivamente exaustivas;
- representativas do comportamento esperado do sistema.

Nesse contexto, o particionamento de equivalência:

- divide o domínio de entrada em classes válidas e inválidas;
- seleciona valores representativos de cada classe;
- reduz redundância nos testes;
- melhora a eficiência da modelagem de testes;
- contribui para cobertura sistemática dos requisitos.

---

## Conceito Fundamental

A técnica parte do princípio de que:

> Se um valor de uma partição apresenta determinado comportamento, os demais valores daquela mesma partição tendem a apresentar o mesmo resultado.

Assim, testa-se **um valor representativo por partição**, em vez de todos os valores possíveis.

---

## Tipos de Partições

| Tipo de Partição | Descrição |
|------------------|------------|
| Válida | Conjunto de entradas que devem ser aceitas pelo sistema |
| Inválida | Conjunto de entradas que devem ser rejeitadas |
| De formato | Relacionadas ao tipo ou estrutura dos dados |
| De intervalo | Relacionadas a faixas numéricas ou limites |

---

## Exemplo Prático – Exercício de Aplicação

### Contexto do Sistema

Considere um campo "Idade" com as seguintes regras:

- O valor deve ser numérico.
- Deve estar entre **18 e 60 anos**.
- O campo é obrigatório.

### Minha Tarefa

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

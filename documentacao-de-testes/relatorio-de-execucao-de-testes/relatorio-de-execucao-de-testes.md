# Relatório de Execução de Testes

Um **relatório de execução de testes** é o documento que registra os resultados da execução dos testes, permitindo avaliar a qualidade do sistema e apoiar a tomada de decisão sobre sua liberação.

Segundo o ISTQB (International Software Testing Qualifications Board):

> **"Um relatório de teste é um documento que resume as atividades e resultados dos testes, fornecendo uma avaliação da qualidade do produto."**

Já Rex Black, em *Managing the Testing Process*, destaca:

> **"Relatórios de teste eficazes não apenas mostram resultados, mas comunicam riscos e ajudam stakeholders a tomar decisões."**

---

## Objetivo do Relatório de Execução de Testes

Um relatório de execução de testes tem como principal objetivo:

- Mostrar o que foi testado  
- Indicar quais testes **passaram e falharam**  
- Evidenciar **problemas e riscos**  
- Apoiar decisões sobre a liberação do sistema  

---

## Tipos de Relatórios

### Relatório Detalhado
- Foco técnico  
- Contém resultados dos testes e evidências  

### Relatório Resumido
- Foco gerencial  
- Mostra status geral, métricas e riscos  

---

## Estrutura de um Relatório

| Campo | Descrição |
|------|----------|
| ID do relatório | Identificação |
| Data | Quando foi executado |
| Ambiente | Onde foi testado |
| Versão | Build testada |
| Responsável | Quem executou |
| Casos executados | Total |
| Casos aprovados | Passaram |
| Casos reprovados | Falharam |
| Taxa de sucesso | % de aprovação |
| Defeitos | Problemas encontrados |
| Evidências | Prints, logs |
| Observações | Comentários |

---

## Métricas

- Taxa de Sucesso:  
  $$
  \frac{Aprovados}{Executados} \times 100
  $$

- Taxa de Falha:  
  $$
  \frac{Reprovados}{Executados} \times 100
  $$

- Densidade de Defeitos:  
  $$
  \frac{Defeitos}{Tamanho\ do\ Sistema}
  $$
  
---

## Características de um Bom Relatório

- **Claro** → fácil de entender  
- **Objetivo** → sem informação desnecessária  
- **Transparente** → mostra problemas reais  
- **Rastreável** → liga teste → resultado → defeito  
- **Com evidências** → comprova falhas  

---

## Erros Comuns

- Falta de evidências  
- Métricas erradas  
- Falta de contexto  
- Excesso de tecnicidade  
- Omissão de falhas  

---

## Relação com Casos de Teste

- Caso de teste → define o que testar  
- Execução → gera resultados  
- Relatório → consolida e comunica  

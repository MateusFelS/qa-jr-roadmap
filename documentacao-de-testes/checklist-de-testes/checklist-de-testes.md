# Checklist de Testes

Um **checklist de testes** é uma lista estruturada de verificações que devem ser realizadas durante a validação de um sistema, garantindo consistência e cobertura mínima sem necessariamente detalhar cada passo como em um caso de teste.

Segundo o ISTQB (International Software Testing Qualifications Board):

> **"Checklist-based testing é uma técnica baseada na experiência, onde o testador utiliza uma lista de itens a serem verificados."**

Já Glenford Myers, em *The Art of Software Testing*, destaca:

> **"A experiência do testador pode ser estruturada em listas que ajudam a evitar esquecimentos sistemáticos."**

---

## Objetivo do Checklist de Testes

Um checklist bem definido deve:

- Garantir **cobertura básica e rápida**
- Reduzir o risco de **esquecimento de cenários comuns**
- Padronizar verificações entre testadores
- Servir como apoio para **testes exploratórios**
- Aumentar a eficiência em **regressões**

---

## Diferença entre Checklist e Caso de Teste

| Aspecto | Caso de Teste | Checklist |
|--------|--------------|----------|
| Nível de detalhe | Alto | Baixo |
| Estrutura | Formal e completa | Lista simples |
| Execução | Passo a passo | Verificação direta |
| Objetivo | Validar comportamento específico | Garantir cobertura geral |

---

## Estrutura

| Campo | Descrição |
|------|----------|
| ID | Identificador |
| Item | O que verificar |
| Status | OK / NOK |
| Observações | Notas ou problemas |

---

## Tipos de Checklist

- **Funcional** → funcionalidades funcionando  
- **UI** → layout e usabilidade  
- **Validação** → regras de entrada  
- **Regressão** → nada quebrou após mudanças  

---

## Boas Práticas

- Ser **simples e direto**
- Baseado em **experiência**
- Ser **enxuto** (sem excesso)
- **Reutilizável**
- **Atualizado com bugs encontrados**

---

## Quando Usar

- Testes exploratórios  
- Smoke tests  
- Regressão  
- Pouco tempo disponível  

---

## Erros Comuns

- Muito genérico  
- Muito detalhado (vira caso de teste)  
- Ambíguo  
- Não atualizar  

---

## Relação com Outras Técnicas

- Teste exploratório  
- Error guessing  
- Teste baseado em risco  

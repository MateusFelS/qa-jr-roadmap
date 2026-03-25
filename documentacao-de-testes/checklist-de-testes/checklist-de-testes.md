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

👉 Resumindo:  
- **Caso de teste = profundo**  
- **Checklist = rápido e abrangente**

---

## Estrutura de um Checklist de Testes

Um checklist geralmente contém:

| Campo | Descrição |
|------|----------|
| ID | Identificador do item |
| Item | O que deve ser verificado |
| Status | OK / NOK (ou Passou/Falhou) |
| Observações | Problemas encontrados ou notas |

---

## Tipos de Checklist

### 1. Checklist Funcional

Verifica se funcionalidades funcionam corretamente.

Exemplo:
- Login funciona com credenciais válidas
- Mensagem de erro aparece corretamente

---

### 2. Checklist de Interface (UI)

Focado em layout e usabilidade.

- Botões visíveis
- Campos alinhados
- Responsividade

---

### 3. Checklist de Validação

Verifica regras de entrada.

- Campos obrigatórios
- Formatos válidos
- Limites de caracteres

---

### 4. Checklist de Regressão

Usado após mudanças no sistema.

- Funcionalidades principais continuam funcionando
- Bugs corrigidos não retornaram

---

## Características de um Bom Checklist

### 1. Simples e Direto

Segundo Lisa Crispin:

> **"Checklists devem ser rápidos de usar — caso contrário, não serão usados."**

✔ Bom:
> "Verificar se botão de login está habilitado"

✘ Ruim:
> "Testar comportamento completo do login com múltiplos cenários"

---

### 2. Baseado em Experiência

Checklist evolui com o tempo:

- Bugs anteriores viram itens
- Padrões recorrentes são adicionados

---

### 3. Abrangente, mas Enxuto

Evite:

- Itens duplicados
- Detalhamento excessivo

---

### 4. Reutilizável

Um bom checklist pode ser usado:

- Em diferentes versões
- Em diferentes projetos similares

---

### 5. Atualizável

Checklist **não é estático**:

- Deve evoluir conforme o sistema cresce
- Deve incorporar novos riscos

---

## Exemplo de Checklist – Tela de Login

| ID | Item | Status | Observações |
|----|------|--------|------------|
| CL-01 | Campo de e-mail aceita formato válido | — | — |
| CL-02 | Campo de senha oculta caracteres | — | — |
| CL-03 | Botão "Entrar" está habilitado | — | — |
| CL-04 | Login com dados válidos funciona | — | — |
| CL-05 | Mensagem exibida para credenciais inválidas | — | — |
| CL-06 | Sistema bloqueia após múltiplas tentativas | — | — |
| CL-07 | Layout responsivo em mobile | — | — |

---

## Quando Usar Checklist

Checklist é ideal para:

- Testes exploratórios
- Testes rápidos (smoke test)
- Regressões
- Quando não há tempo para casos detalhados

---

## Erros Comuns

- Checklist muito genérico
- Checklist detalhado demais (vira caso de teste)
- Itens ambíguos
- Não atualizar após bugs encontrados

Segundo Cem Kaner:

> **"Se você não aprende com os defeitos encontrados, seu processo de teste está incompleto."**

---

## Relação com Outras Técnicas

Checklist está ligado a técnicas baseadas em experiência, como:

- Teste exploratório  
- Error guessing  
- Sessões de teste baseadas em risco  

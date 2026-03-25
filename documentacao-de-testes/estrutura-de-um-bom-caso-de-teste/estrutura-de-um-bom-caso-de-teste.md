# Estrutura de um Bom Caso de Teste

Um **caso de teste** é um conjunto estruturado de condições, entradas, ações e resultados esperados utilizado para verificar se um sistema atende aos requisitos especificados.

Segundo o ISTQB (International Software Testing Qualifications Board):

> **"um conjunto de pré-condições, entradas, ações (quando aplicável) e resultados esperados, desenvolvidos com base em condições de teste."**

Já Cem Kaner, em *Testing Computer Software*, enfatiza:

> **"Um bom caso de teste não é apenas sobre encontrar defeitos, mas sobre comunicar claramente o que está sendo testado e por quê."**

---

## Objetivo de um Caso de Teste

Um caso de teste bem estruturado deve:

- Validar um comportamento específico do sistema
- Ser **reprodutível**
- Ser **claro e compreensível**
- Ser **independente de quem executa**
- Facilitar a **detecção de defeitos**

---

## Estrutura Básica de um Caso de Teste

Embora existam variações, a maioria dos padrões converge para os seguintes elementos:

| Campo | Descrição |
|------|----------|
| ID | Identificador único do teste |
| Título | Descrição curta do objetivo |
| Pré-condições | Estado necessário antes da execução |
| Dados de entrada | Valores utilizados no teste |
| Passos | Sequência de ações a executar |
| Resultado esperado | Comportamento esperado do sistema |
| Resultado obtido | (Executado) comportamento real |
| Status | Passou / Falhou |
| Observações | Informações adicionais |

---

## Características de um Bom Caso de Teste

### 1. Clareza e Objetividade

O caso deve ser entendido por qualquer pessoa da equipe.

✔ Bom:
> "Inserir e-mail válido no campo e submeter o formulário"

✘ Ruim:
> "Testar login"

---

### 2. Independência

Segundo Ron Patton:

> **"Cada teste deve ser capaz de ser executado isoladamente."**

Isso evita dependência de execução sequencial e facilita automação.

---

### 3. Reprodutibilidade

Qualquer pessoa deve conseguir executar e obter o mesmo resultado.

- Passos bem definidos
- Dados explícitos
- Ambiente conhecido

---

### 4. Cobertura Clara

Cada caso de teste deve validar **apenas um objetivo principal**.

Isso facilita:
- Identificação de falhas
- Manutenção dos testes

---

### 5. Resultado Esperado Específico

Evite resultados vagos.

✔ Bom:
> "Mensagem 'Usuário inválido' é exibida"

✘ Ruim:
> "Erro aparece"

---

## Exemplo de Caso de Teste Bem Estruturado

### Caso de Teste – Login com credenciais válidas

| Campo | Valor |
|------|-------|
| ID | CT-001 |
| Título | Login com usuário válido |
| Pré-condições | Usuário cadastrado no sistema |
| Dados de entrada | usuário: "user@test.com", senha: "123456" |
| Passos | 1. Acessar página de login<br>2. Inserir usuário<br>3. Inserir senha<br>4. Clicar em "Entrar" |
| Resultado esperado | Usuário é redirecionado para a página inicial |
| Resultado obtido | — |
| Status | — |
| Observações | — |

---

## Erros Comuns na Criação de Casos de Teste

- Casos vagos ou genéricos
- Falta de resultado esperado
- Dependência entre testes
- Muitos objetivos em um único teste
- Dados implícitos (não documentados)

Segundo Lisa Crispin:

> **"Se o teste não pode ser entendido sem explicação adicional, ele não está bem escrito."**

---

## Relação com Outras Técnicas de Teste

A estrutura do caso de teste é o **“container”**, enquanto técnicas como:

- Particionamento de equivalência  
- Análise de valor limite  
- Tabela de decisão  

definem **o que testar dentro dele**.

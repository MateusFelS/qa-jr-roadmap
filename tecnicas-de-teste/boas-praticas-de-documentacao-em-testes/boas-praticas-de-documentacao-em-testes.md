# Boas Práticas de Documentação em Testes

A documentação de testes tem como objetivo registrar informações relevantes sobre planejamento, execução, resultados e defeitos de forma clara, organizada e rastreável.

Segundo o ISTQB, a quantidade e o nível de detalhamento da documentação devem ser proporcionais ao contexto, aos riscos e às necessidades do projeto.

Conforme **Rex Black**:

> "Uma documentação eficaz comunica informações essenciais sem gerar burocracia desnecessária."

---

## Conceito Fundamental

Documentar não significa produzir o máximo possível de documentos.

O objetivo é garantir que as informações necessárias estejam disponíveis para:

- Planejamento.
- Execução.
- Auditoria.
- Manutenção.
- Transferência de conhecimento.

---

## Principais Boas Práticas

### 1. Utilizar linguagem clara e objetiva

Evite descrições ambíguas.

**Ruim:**

> Verificar se o sistema funciona corretamente.

**Bom:**

> Verificar se o sistema permite cadastrar clientes com CPF válido.

---

### 2. Garantir rastreabilidade

Cada artefato deve estar relacionado a requisitos e casos de teste.

| Elemento | Relacionamento |
|-----------|---------------|
| Requisito | Caso de teste |
| Caso de teste | Evidência |
| Evidência | Defeito |
| Defeito | Correção |

---

### 3. Padronizar documentos

Utilizar modelos definidos para:

- Casos de teste.
- Relatórios.
- Evidências.
- Registro de defeitos.

A padronização reduz erros e facilita manutenção.

---

### 4. Manter informações atualizadas

Documentos desatualizados geram interpretações incorretas e perda de confiança nas informações.

---

### 5. Registrar apenas informações relevantes

Documentação excessiva aumenta esforço e dificulta manutenção.

Deve existir equilíbrio entre detalhamento e valor gerado.

---

## Exemplo de Estrutura de Caso de Teste

| Campo | Conteúdo |
|---------|----------|
| ID | CT-001 |
| Objetivo | Validar login |
| Pré-condição | Usuário cadastrado |
| Passos | Informar usuário e senha |
| Resultado esperado | Acesso concedido |

---

## Benefícios

- Melhora a comunicação da equipe.
- Facilita auditorias.
- Aumenta a rastreabilidade.
- Reduz dependência de conhecimento individual.
- Apoia a manutenção futura.

Segundo **Louise Tamres**:

> "Documentação eficaz é aquela que continua útil após sua criação."

---

## Relação com Qualidade de Software

| Documentação Deficiente | Documentação Adequada |
|-------------------------|----------------------|
| Informações inconsistentes | Informações confiáveis |
| Baixa rastreabilidade | Histórico completo |
| Dificuldade de auditoria | Evidências organizadas |
| Retrabalho frequente | Maior eficiência |

A documentação deve apoiar o processo de testes, e não se tornar um obstáculo para sua execução.

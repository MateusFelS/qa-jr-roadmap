# Exercício – Boas Práticas de Documentação

## Contexto

Considere o seguinte caso de teste documentado:

**Objetivo:**
Verificar se o cadastro funciona.

**Passos:**
1. Fazer cadastro
2. Salvar

**Resultado esperado:**
Sistema funciona corretamente.

👉 Identifique problemas de documentação e proponha melhorias.

---

## Resolução

### Problemas Encontrados

| Problema | Justificativa |
|-----------|--------------|
| Objetivo genérico | Não informa o que será validado |
| Passos incompletos | Não descrevem a execução |
| Resultado esperado vago | Não permite validação objetiva |
| Falta de pré-condições | Não informa cenário necessário |
| Falta de dados de teste | Execução pode variar |

---

### Versão Melhorada

| Campo | Conteúdo |
|---------|----------|
| ID | CT-CAD-001 |
| Objetivo | Validar cadastro de cliente com CPF válido |
| Pré-condição | Usuário autenticado |
| Passo 1 | Acessar tela de cadastro |
| Passo 2 | Informar nome e CPF válidos |
| Passo 3 | Clicar em Salvar |
| Resultado esperado | Cliente cadastrado com sucesso e mensagem exibida |

---

### Conclusão

A documentação revisada apresenta:

- Clareza
- Rastreabilidade
- Reprodutibilidade
- Objetividade

Características consideradas boas práticas em documentação de testes.

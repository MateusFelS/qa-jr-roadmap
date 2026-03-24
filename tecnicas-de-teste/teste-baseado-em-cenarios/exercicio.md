##Exemplo Prático – Exercício de Aplicação

## Contexto do Sistema

Considere um sistema de **cadastro de usuários** com as seguintes funcionalidades:

- cadastro de novo usuário;
- validação de campos obrigatórios;
- verificação de e-mail já existente;
- confirmação de cadastro.

## Minha Tarefa

Criar **cenários de teste** que representem situações reais de uso do sistema.

---

## Cenários de Teste – Cadastro de Usuário

| ID | Cenário | Descrição |
|----|--------|-----------|
| CT-01 | Cadastro realizado com sucesso | Usuário preenche todos os campos obrigatórios com dados válidos e finaliza o cadastro |
| CT-02 | Tentativa de cadastro com e-mail já existente | Usuário informa um e-mail que já está cadastrado no sistema |
| CT-03 | Cadastro com campo obrigatório vazio | Usuário tenta cadastrar sem preencher um campo obrigatório |
| CT-04 | Cadastro com formato de e-mail inválido | Usuário informa um e-mail em formato incorreto |
| CT-05 | Cancelamento do cadastro | Usuário inicia o cadastro, mas decide cancelar antes da confirmação |

---

## Exemplo de Cenário Detalhado

**Cenário:** Cadastro de usuário com sucesso  

**Pré-condição:** Usuário não possui cadastro no sistema.

**Passos:**

1. Acessar a página de cadastro.
2. Informar nome válido.
3. Informar e-mail válido e não cadastrado.
4. Informar senha válida.
5. Confirmar cadastro.

**Resultado Esperado:**

- O sistema registra o novo usuário.
- Uma mensagem de confirmação é exibida.
- O usuário é redirecionado para a página inicial ou de login.

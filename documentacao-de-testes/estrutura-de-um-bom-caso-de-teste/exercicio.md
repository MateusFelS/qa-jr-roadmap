# Exercício – Estruturação de Casos de Teste

## Contexto

Sistema de **login** com as seguintes regras:

- E-mail deve estar em formato válido
- Senha deve ter no mínimo 6 caracteres
- Usuário deve estar cadastrado
- Após 3 tentativas inválidas, a conta é bloqueada
- Mensagens de erro devem ser exibidas corretamente

---

## Tarefa

👉 Crie casos de teste completos utilizando a estrutura:

- ID  
- Título  
- Pré-condições  
- Dados de entrada  
- Passos  
- Resultado esperado  

---

## Cenários a Cobrir

| ID | Cenário | Descrição |
|----|--------|----------|
| CEN-01 | Login com sucesso | Credenciais válidas e usuário ativo |
| CEN-02 | E-mail inválido | Formato incorreto (ex: "user@") ou campo vazio |
| CEN-03 | Senha inválida | Menos de 6 caracteres ou senha incorreta |
| CEN-04 | Usuário inexistente | E-mail não cadastrado no sistema |
| CEN-05 | Bloqueio de conta | 3 tentativas inválidas consecutivas |
| CEN-06 | Mensagens do sistema | Validação das mensagens exibidas para cada erro |

---

| ID | Título | Pré-condições | Dados de entrada | Passos | Resultado esperado | Resultado obtido | Status |
|----|--------|---------------|------------------|--------|--------------------|------------------|--------|
| CT-001 | Login com sucesso | Usuário cadastrado no sistema | 1. E-mail: email_valido@gmail.com<br>2. Senha: 123456 | 1. Preencha os campos E-mail e senha com credenciais válidas.<br>2. Clique no botão "Entrar". | Usuário recebe uma mensagem de sucesso e é redirecionado para página inicial. | - | - |

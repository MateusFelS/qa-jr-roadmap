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

| ID | Título | Pré-condições | Dados de entrada | Passos | Resultado esperado |
|----|--------|---------------|------------------|--------|--------------------|
| CT-01 | Login com sucesso | Conta cadastrada, ativa e não bloqueada | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com valor válido.<br>3. Preencher o campo "Senha" com valor válido.<br>4. Clicar no botão "Entrar". | Sistema autentica o usuário com sucesso e redireciona para a página inicial. |
| CT-02 | E-mail em formato inválido | Sistema disponível | 1. E-mail: `email_invalido@`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com formato inválido.<br>3. Preencher o campo "Senha" com valor válido.<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem de erro informando que o e-mail é inválido e permanece na tela de login. |
| CT-03A | Senha com menos de 6 caracteres | Conta cadastrada, ativa e não bloqueada | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `123` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com valor válido.<br>3. Preencher o campo "Senha" com menos de 6 caracteres.<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem de erro informando que a senha não atende ao tamanho mínimo e permanece na tela de login. |
| CT-03B | Senha incorreta | Conta cadastrada, ativa e não bloqueada | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `senha_errada` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com valor válido.<br>3. Preencher o campo "Senha" com valor incorreto.<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem de erro informando que as credenciais são inválidas e permanece na tela de login. |
| CT-04 | Usuário inexistente | Sistema disponível | 1. E-mail: `naoexiste@gmail.com`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com usuário não cadastrado.<br>3. Preencher o campo "Senha".<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem informando que o usuário não está cadastrado e permanece na tela de login. |
| CT-05 | Bloqueio de conta após tentativas inválidas | Conta cadastrada, ativa e não bloqueada inicialmente | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `senha_errada` | 1. Acessar a tela de login.<br>2. Preencher credenciais inválidas.<br>3. Clicar no botão "Entrar".<br>4. Repetir o processo até completar 3 tentativas inválidas consecutivas. | Sistema bloqueia a conta após 3 tentativas inválidas e exibe mensagem informando o bloqueio. |
| CT-06A | Mensagem para e-mail inválido | Sistema disponível | 1. E-mail: `email@`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com valor inválido.<br>3. Preencher o campo "Senha" com valor válido.<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem de erro informando que o e-mail é inválido e permanece na tela de login. |
| CT-06B | Mensagem para senha inválida | Conta cadastrada, ativa e não bloqueada | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `123` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com valor válido.<br>3. Preencher o campo "Senha" inválida.<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem de erro informando que a senha é inválida e permanece na tela de login. |
| CT-06C | Mensagem para usuário inexistente | Sistema disponível | 1. E-mail: `naoexiste@gmail.com`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher o campo "E-mail" com usuário não cadastrado.<br>3. Preencher o campo "Senha".<br>4. Clicar no botão "Entrar". | Sistema exibe mensagem informando que o usuário não está cadastrado e permanece na tela de login. |
| CT-06D | Mensagem para conta bloqueada | Conta cadastrada e bloqueada | 1. E-mail: `email_valido@gmail.com`<br>2. Senha: `123456` | 1. Acessar a tela de login.<br>2. Preencher credenciais de conta bloqueada.<br>3. Clicar no botão "Entrar". | Sistema exibe mensagem informando que a conta está bloqueada e impede o login. |

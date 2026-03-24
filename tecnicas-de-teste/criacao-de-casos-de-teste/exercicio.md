# Exemplo Prático – Exercício de Criação de Casos de Teste

## Contexto do Sistema
Considere um **sistema de login** com as seguintes regras:

- O usuário deve informar **e-mail** e **senha**.
- Ambos os campos são obrigatórios.
- O e-mail deve estar em formato válido.
- A senha deve conter no mínimo **6 caracteres**.
- Caso as credenciais estejam corretas, o sistema deve permitir o acesso.
- Caso estejam incorretas, uma mensagem de erro deve ser exibida.

## Minha Tarefa
Com base nesse cenário, criar **casos de teste funcionais** contemplando:

- cenários positivos;
- cenários negativos;
- validação de campos obrigatórios.

## Casos de Teste – Sistema de Login

| ID | Título | Pré-condição | Passos | Dados de Teste | Resultado Esperado |
|----|--------|--------------|--------|----------------|--------------------|
| CT-001 | Login com credenciais válidas | Usuário cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar um e-mail válido<br>3. Informar uma senha válida<br>4. Clicar no botão “Entrar” | E-mail: `email@test.com`<br>Senha: `123456` | Usuário autenticado com sucesso e redirecionado para a página inicial |
| CT-002 | Login com senha inválida | Usuário cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar um e-mail válido<br>3. Informar uma senha inválida<br>4. Clicar no botão “Entrar” | E-mail: `email@test.com`<br>Senha: `senha_invalida` | Sistema exibe a mensagem “E-mail ou senha inválidos” e mantém o usuário na tela de login |
| CT-003 | Login com campos obrigatórios vazios | Nenhuma | 1. Acessar a tela de login<br>2. Deixar os campos e-mail e senha vazios<br>3. Clicar no botão “Entrar” | E-mail: vazio<br>Senha: vazio | Sistema exibe a mensagem “Preencha os campos obrigatórios” |
| CT-004 | Login com senha com menos de 6 caracteres | Usuário cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar um e-mail válido<br>3. Informar uma senha com menos de 6 caracteres<br>4. Clicar no botão “Entrar” | E-mail: `email@test.com`<br>Senha: `12345` | Sistema exibe a mensagem “A senha deve conter no mínimo 6 caracteres” |
| CT-005 | Login com e-mail em formato inválido | Nenhuma | 1. Acessar a tela de login<br>2. Informar um e-mail em formato inválido<br>3. Informar uma senha válida<br>4. Clicar no botão “Entrar” | E-mail: `emailtest.com`<br>Senha: `123456` | Sistema exibe a mensagem “E-mail em formato inválido” |
| CT-006 | Login com e-mail não cadastrado | Usuário não cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar um e-mail não cadastrado<br>3. Informar uma senha válida<br>4. Clicar no botão “Entrar” | E-mail: `naoexiste@test.com`<br>Senha: `123456` | Sistema exibe a mensagem “E-mail ou senha inválidos” |
| CT-007 | Login com campo e-mail vazio | Nenhuma | 1. Acessar a tela de login<br>2. Deixar o campo e-mail vazio<br>3. Informar uma senha válida<br>4. Clicar no botão “Entrar” | E-mail: vazio<br>Senha: `123456` | Sistema exibe a mensagem “Preencha o campo e-mail” |
| CT-008 | Login com campo senha vazio | Nenhuma | 1. Acessar a tela de login<br>2. Informar um e-mail válido<br>3. Deixar o campo senha vazio<br>4. Clicar no botão “Entrar” | E-mail: `email@test.com`<br>Senha: vazio | Sistema exibe a mensagem “Preencha o campo senha” |
| CT-009 | Login com espaços em branco nos campos | Nenhuma | 1. Acessar a tela de login<br>2. Informar apenas espaços no e-mail<br>3. Informar apenas espaços na senha<br>4. Clicar no botão “Entrar” | E-mail: `"   "`<br>Senha: `"   "` | Sistema trata os campos como vazios e exibe mensagem de campos obrigatórios |
| CT-010 | Login válido após tentativa inválida | Usuário realizou uma tentativa inválida anteriormente | 1. Acessar a tela de login<br>2. Informar credenciais válidas<br>3. Clicar no botão “Entrar” | E-mail: `email@test.com`<br>Senha: `123456` | Usuário autenticado com sucesso, sem impacto da tentativa anterior |

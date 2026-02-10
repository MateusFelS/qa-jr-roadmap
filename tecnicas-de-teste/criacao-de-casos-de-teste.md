# Criação de Casos de Teste

A **criação de casos de teste** é uma atividade central no processo de garantia da qualidade de software, pois define de forma estruturada como o sistema será verificado em relação aos seus requisitos e comportamentos esperados.

De acordo com o **ISTQB (International Software Testing Qualifications Board)**, um caso de teste pode ser definido como:

> **“Um conjunto de pré-condições, entradas, ações de execução e resultados esperados, desenvolvido para verificar se um requisito específico foi atendido.”**

Ian Sommerville também destaca que testes bem definidos contribuem para a redução de falhas em produção, pois permitem a validação sistemática do software antes de sua entrega ao usuário final.

Nesse contexto, os casos de teste atuam como um **artefato de comunicação** entre os membros do time, garantindo que desenvolvedores, QAs e stakeholders compartilhem o mesmo entendimento sobre o comportamento esperado do sistema.

Assim, a criação de casos de teste bem estruturados:
- assegura a cobertura dos requisitos funcionais;
- facilita a identificação de defeitos;
- contribui para a rastreabilidade entre requisitos e testes;
- apoia a execução de testes de regressão ao longo do ciclo de vida do software.

---

## Exemplo Prático – Exercício de Criação de Casos de Teste

### Contexto do Sistema
Considere um **sistema de login** com as seguintes regras:

- O usuário deve informar **e-mail** e **senha**.
- Ambos os campos são obrigatórios.
- O e-mail deve estar em formato válido.
- A senha deve conter no mínimo **6 caracteres**.
- Caso as credenciais estejam corretas, o sistema deve permitir o acesso.
- Caso estejam incorretas, uma mensagem de erro deve ser exibida.

### Minha Tarefa
Com base nesse cenário, criar **casos de teste funcionais** contemplando:

- cenários positivos;
- cenários negativos;
- validação de campos obrigatórios.

| ID | Título | Pré-condição | Passos | Dados de Teste | Resultado Esperado |
|----|--------|--------------|--------|----------------|--------------------|
| CT-001 | Login com credenciais válidas | Usuário cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar e-mail válido<br>3. Informar senha válida<br>4. Clicar no botão “Entrar” | e-mail: `email@test.com`<br>senha: `123456` | Usuário autenticado e redirecionado para a página inicial |
| CT-002 | Login com senha inválidas | Usuário cadastrado no sistema | 1. Acessar a tela de login<br>2. Informar um e-mail válido<br>3. Informar uma senha inválida<br>4. Clicar no botão "Entrar" | e-mail: `email@test.com`<br>senha: `senha_inválida` | Usuário recebe uma mensagem de erro "E-mail ou senha inválidos" e permanece na tela de login | 
| CT-003 | Login com campos vazios | - | 1. Acessar a tela de login<br>2. Deixar os campos e-mail e senha vazios<br>3. Clicar no botão "Entrar" | e-mail: ` `<br>senha: ` ` | Usuário recebe mensagem de erro "Preencha os campos obrigatórios" e permanece na tela de login |
| CT-004 | Senha com menos de 6 caracteres |

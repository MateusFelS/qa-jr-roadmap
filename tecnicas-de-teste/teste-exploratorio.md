# Teste Exploratório

O **Teste Exploratório** é uma abordagem de testes de software em que **o aprendizado, o projeto de testes e a execução ocorrem simultaneamente**. Diferente de abordagens altamente documentadas, o testador explora o sistema de forma investigativa, utilizando sua experiência, intuição e conhecimento do domínio para descobrir falhas.

De acordo com o ISTQB (International Software Testing Qualifications Board), o teste exploratório é uma abordagem em que **os testes são projetados e executados dinamicamente**, à medida que o testador aprende mais sobre o sistema.

Segundo James A. Whittaker:

> **"Teste exploratório é sobre aprender o sistema enquanto se testa e usar esse aprendizado para guiar os próximos testes."**

Já Cem Kaner define o teste exploratório como:

> **"Uma abordagem de teste em que o testador controla ativamente o design dos testes enquanto os executa e utiliza as informações obtidas para projetar novos testes melhores."**

Nesse contexto, o teste exploratório:

- incentiva a **investigação ativa do sistema**;
- permite **descobrir defeitos inesperados**;
- valoriza a **experiência e criatividade do testador**;
- adapta os testes conforme o aprendizado sobre o sistema;
- complementa testes estruturados e automatizados.

---

## Conceito Fundamental

O princípio central do teste exploratório é:

> **Aprender sobre o sistema enquanto se testa e usar esse conhecimento para direcionar novas explorações.**

Assim, o testador não segue apenas um roteiro fixo, mas **investiga o comportamento do sistema**, criando novas ideias de teste durante a execução.

---

## Características do Teste Exploratório

| Característica | Descrição |
|----------------|-----------|
| Dinâmico | Os testes são adaptados durante a execução |
| Investigativo | O testador explora o sistema em busca de comportamentos inesperados |
| Baseado em experiência | Depende do conhecimento técnico e do domínio do testador |
| Flexível | Não depende exclusivamente de casos de teste pré-definidos |

---

## Exemplo Prático – Exercício de Aplicação

### Contexto do Sistema

Considere um sistema de **login de usuários** com as seguintes funcionalidades:

- autenticação com e-mail e senha;
- validação de credenciais;
- recuperação de senha;
- bloqueio após múltiplas tentativas inválidas.

### Minha Tarefa

Realizar uma **sessão de teste exploratório** para identificar possíveis falhas no processo de login.

---

## Ideias de Exploração – Sistema de Login

| ID | Área de Exploração | Ação Investigativa |
|----|--------------------|--------------------|
| TE-01 | Validação de campos | Tentar realizar login com campos vazios |
| TE-02 | Formato de e-mail | Inserir e-mails com formatos inválidos |
| TE-03 | Tentativas consecutivas | Realizar várias tentativas de login com senha incorreta |
| TE-04 | Recuperação de senha | Solicitar redefinição de senha repetidas vezes |
| TE-05 | Comportamento do sistema | Testar login em múltiplos navegadores ou abas |

---

## Exemplo de Sessão de Teste Exploratório

**Objetivo:** Explorar o comportamento do sistema durante o processo de login.

**Tempo da sessão:** 30 minutos

**Área explorada:** Tela de autenticação.

**Ações realizadas:**

1. Inserir e-mail válido e senha incorreta.
2. Repetir tentativas de login consecutivas.
3. Tentar login com campos vazios.
4. Inserir caracteres especiais no campo de e-mail.
5. Testar recuperação de senha.

**Possíveis observações:**

- O sistema pode não bloquear o usuário após várias tentativas.
- Mensagens de erro podem não ser claras para o usuário.
- O campo de e-mail pode aceitar formatos inválidos.

**Resultado esperado:**

- O sistema deve validar corretamente as credenciais.
- O sistema deve bloquear o acesso após múltiplas tentativas inválidas.
- As mensagens de erro devem orientar corretamente o usuário.

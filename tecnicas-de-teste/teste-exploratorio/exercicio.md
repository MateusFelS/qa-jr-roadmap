# Exemplo Prático – Exercício de Aplicação

## Contexto do Sistema

Considere um sistema de **login de usuários** com as seguintes funcionalidades:

- autenticação com e-mail e senha;
- validação de credenciais;
- recuperação de senha;
- bloqueio após múltiplas tentativas inválidas.

## Minha Tarefa

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

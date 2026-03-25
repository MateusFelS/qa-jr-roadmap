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

<table>
  <tr>
    <th style="width:5%">ID</th>
    <th style="width:10%">Título</th>
    <th style="width:15%">Pré-condições</th>
    <th style="width:20%">Dados de entrada</th>
    <th style="width:25%">Passos</th>
    <th style="width:25%">Resultado esperado</th>
  </tr>
  <tr>
    <td>CT-01</td>
    <td>Login com sucesso</td>
    <td>Usuário cadastrado no sistema</td>
    <td>
      1. E-mail: <code>email_valido@gmail.com</code><br>
      2. Senha: <code>123456</code>
    </td>
    <td>
      1. Preencha os campos "E-mail" e "Senha"...<br>
      2. Clique no botão "Entrar".
    </td>
    <td>
      Usuário recebe uma mensagem de sucesso e é redirecionado...
    </td>
  </tr>
</table>

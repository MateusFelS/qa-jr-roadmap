# Teste Baseado em Cenários

O **Teste Baseado em Cenários** é uma técnica de projeto de testes que consiste em **validar o comportamento do sistema a partir de situações reais de uso**, simulando como usuários interagem com a aplicação em diferentes contextos.

De acordo com o ISTQB (International Software Testing Qualifications Board), cenários de teste representam **fluxos de interação do usuário com o sistema**, permitindo verificar se os requisitos funcionais são atendidos de forma integrada.

Segundo Rex Black:

> **"Os cenários de teste descrevem como o sistema será utilizado na prática, permitindo validar fluxos completos e comportamentos esperados."**

Já Cem Kaner destaca que cenários são importantes porque:

> **"Eles aproximam os testes da realidade do usuário, permitindo descobrir falhas que testes isolados dificilmente revelariam."**

Nesse contexto, o teste baseado em cenários:

- simula **situações reais de uso do sistema**;
- valida **fluxos completos de interação**;
- permite identificar problemas de **integração entre funcionalidades**;
- aumenta a **qualidade da experiência do usuário**;
- complementa outras técnicas de teste (como particionamento de equivalência e valor limite).

---

## Conceito Fundamental

A técnica parte do princípio de que:

> **Testar funcionalidades isoladas não garante que o sistema funcione corretamente quando utilizado em um fluxo real.**

Assim, o teste baseado em cenários busca **reproduzir jornadas completas do usuário**, verificando se o sistema responde corretamente em cada etapa.

---

## Características dos Cenários de Teste

| Característica | Descrição |
|----------------|-----------|
| Baseado em fluxo | Representa uma sequência de ações do usuário |
| Orientado ao negócio | Reflete situações reais de uso |
| Integrado | Pode envolver múltiplas funcionalidades |
| Narrativo | Descreve o contexto da ação e o resultado esperado |

---

## Exemplo Prático – Exercício de Aplicação

### Contexto do Sistema

Considere um sistema de **cadastro de usuários** com as seguintes funcionalidades:

- cadastro de novo usuário;
- validação de campos obrigatórios;
- verificação de e-mail já existente;
- confirmação de cadastro.

### Minha Tarefa

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

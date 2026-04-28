## Caso 01: Fluxo Principal Completo

| Campo                | Detalhe                                                                 |
|---------------------|-------------------------------------------------------------------------|
| ID                  | CAD_PAC_MAIN_001                                                        |
| Nome                | Fluxo principal completo de cadastro                                   |
| Técnica             | Particionamento de Equivalência + Tabela de Decisão                    |
| Risco               | Alto                                                                    |
| Automatizável       | Sim                                                                     |
| Descrição           | Valida o fluxo completo de cadastro com múltiplos métodos de login     |
| Pré-condições       | Ambiente configurado + contas válidas (Google e Email)                 |
| Cenários Cobertos   | Login Google/Email, idade (18–110), CEP válido, 4 etapas, autenticação |
| Passos              | 1. Acessar sistema<br>2. Escolher login<br>3. Autenticar<br>4. Selecionar perfil<br>5. Preencher etapas 1–4<br>6. Finalizar |
| Resultado Esperado  | Cadastro concluído + login automático + redirecionamento               |
| Critérios de Aceite | Login funcional, validações em tempo real, persistência, progresso salvo |

## Caso 02: Tabela de Validações de Campos

| Campo          | Detalhe                                              |
|----------------|------------------------------------------------------|
| ID             | CAD_PAC_VALID_002                                    |
| Nome           | Validação de campos                                  |
| Técnica        | Valor Limite + Tabela de Decisão                     |
| Risco          | Alto                                                 |
| Automatizável  | Sim                                                  |
| Objetivo       | Validar regras de entrada e comportamento dos campos |

## Matriz de Validações

| Campo | Valor       | Tipo     | Resultado Esperado              |
|-------|------------|----------|--------------------------------|
| Nome  | "Jo"       | Inválido | Erro (mín. 3 caracteres)       |
| Nome  | "Ana"      | Válido   | Campo aceito                   |
| Idade | 17         | Inválido | Erro (mín. 18)                 |
| Idade | 18         | Válido   | Campo aceito                   |
| Idade | 110        | Válido   | Campo aceito                   |
| Idade | 111        | Inválido | Erro (máx. 110)                |
| CEP   | "12345"    | Inválido | Erro de formato                |
| CEP   | "01001-000"| Válido   | Autocompletar endereço         |

## Caso 03: Exceções de Autenticação

| Campo           | Detalhe                                      |
|----------------|----------------------------------------------|
| ID             | CAD_PAC_EXC_003                              |
| Nome           | Exceções de autenticação                     |
| Técnica        | Particionamento de Equivalência              |
| Risco          | Médio                                        |
| Automatizável  | Sim                                          |
| Cenários       | Google sem permissão, OTP inválido, bloqueio |
| Resultado      | Tratamento de erros + mensagens claras       |

## Caso 04: Workflow e Persistência

| Estado Atual | Próximo Estado | Condição           | Resultado        |
|--------------|---------------|--------------------|------------------|
| Etapa 1      | Etapa 2       | Dados válidos      | Avança           |
| Etapa 1      | Etapa 2       | Dados inválidos    | Bloqueia         |
| Etapa 2      | Etapa 3       | Pular opcional     | Avança           |
| Qualquer     | Retorno       | Recarregar página  | Recupera dados   |
| Etapa 4      | Home          | Finalizar cadastro | Autentica usuário|

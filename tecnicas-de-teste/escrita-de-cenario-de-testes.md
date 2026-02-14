# Escrita de Cenários de Teste

A **escrita de cenários de teste** é uma atividade estratégica dentro do planejamento de testes, pois define **o que deve ser testado** em alto nível, antes da elaboração detalhada dos casos de teste.
De acordo com o International Software Testing Qualifications Board (ISTQB), cenários de teste representam situações ou funcionalidades do sistema que precisam ser validadas, servindo como base para a derivação dos casos de teste.
Enquanto os **casos de teste** detalham passo a passo como executar a verificação, os **cenários de teste** descrevem **fluxos ou comportamentos gerais do sistema**, garantindo cobertura funcional ampla.

Segundo Ian Sommerville:

> **"A identificação adequada de cenários de teste contribui para a validação sistemática dos requisitos, reduzindo riscos associados à ausência de cobertura funcional."**

Nesse contexto, os cenários de teste:

- representam funcionalidades ou fluxos de negócio;
- são descritos em alto nível;
- servem como base para criação de múltiplos casos de teste;
- ajudam na validação da cobertura dos requisitos;
- facilitam o planejamento e a priorização dos testes.

---

## Diferença entre Cenário de Teste e Caso de Teste

| Cenário de Teste | Caso de Teste |
|------------------|--------------|
| Descrição em alto nível | Descrição detalhada |
| Define **o que testar** | Define **como testar** |
| Pode gerar vários casos de teste | É executável |
| Foco na funcionalidade | Foco na validação específica |

---

## Exemplo Prático – Exercício de Criação de Cenários de Teste

### Contexto do Sistema

Considere um **sistema de login** com as seguintes regras:

- O usuário deve informar **e-mail** e **senha**.
- Ambos os campos são obrigatórios.
- O e-mail deve estar em formato válido.
- A senha deve conter no mínimo **6 caracteres**.
- Caso as credenciais estejam corretas, o sistema deve permitir o acesso.
- Caso estejam incorretas, uma mensagem de erro deve ser exibida.

### Minha Tarefa

Com base nesse cenário, identificar os **cenários de teste funcionais**, contemplando os principais fluxos e validações.

---

## Cenários de Teste – Sistema de Login

| ID | Cenário de Teste | Descrição |
|----|-------------------|------------|
| CT-01 | Autenticação com credenciais válidas | Validar que o usuário consegue acessar o sistema ao informar e-mail e senha corretos |
| CT-02 | Autenticação com credenciais inválidas | Validar que o sistema impede o acesso quando e-mail ou senha estão incorretos |
| CT-03 | Validação de campos obrigatórios | Verificar se o sistema exige preenchimento dos campos e-mail e senha |
| CT-04 | Validação de formato de e-mail | Garantir que o sistema valida corretamente o formato do e-mail informado |
| CT-05 | Validação de tamanho mínimo da senha | Verificar se o sistema impede senhas com menos de 6 caracteres |
| CT-06 | Tratamento de usuário não cadastrado | Validar comportamento quando o e-mail informado não existe na base |
| CT-07 | Tratamento de espaços em branco | Verificar se o sistema trata campos com apenas espaços como inválidos |
| CT-08 | Persistência após tentativa inválida | Garantir que uma tentativa inválida não comprometa tentativas futuras válidas |

---

## Relação entre Cenários e Casos de Teste

Por exemplo:

O **Cenário CT-03 – Validação de campos obrigatórios** pode gerar:

- caso de teste com ambos os campos vazios;
- caso com apenas e-mail vazio;
- caso com apenas senha vazia;
- caso com espaços em branco.

Assim, percebe-se que **um único cenário pode originar múltiplos casos de teste**, garantindo maior cobertura e detalhamento da verificação.

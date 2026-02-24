# Escrita de Critérios de Aceite

A **escrita de critérios de aceite** é uma atividade essencial na engenharia de requisitos e na validação de software, pois define **quando uma funcionalidade pode ser considerada pronta e correta**.

De acordo com o International Software Testing Qualifications Board (ISTQB), critérios de aceite são condições que um produto deve satisfazer para ser aceito por usuários, clientes ou partes interessadas. Eles conectam requisitos e testes, estabelecendo parâmetros claros e verificáveis.

Enquanto os **requisitos** descrevem *o que o sistema deve fazer*, os **critérios de aceite** definem **as condições mensuráveis que comprovam seu atendimento**.

Conforme Ian Sommerville:

> **"Requisitos bem definidos devem possuir critérios claros de validação, permitindo verificar objetivamente se o sistema atende às necessidades estabelecidas."**

Nesse contexto, os critérios de aceite:

- estabelecem condições objetivas e verificáveis;
- reduzem ambiguidades;
- orientam a criação de casos de teste;
- alinham expectativas entre negócio e equipe técnica;
- fundamentam validação e homologação.

---

## Diferença entre Requisito, Critério de Aceite e Caso de Teste

| Requisito | Critério de Aceite | Caso de Teste |
|------------|-------------------|---------------|
| Define o que o sistema deve fazer | Define quando está correto | Define como validar |
| Pode ser mais abstrato | É objetivo e mensurável | É detalhado e executável |
| Foco na necessidade | Foco na condição de aprovação | Foco na verificação prática |

---

## Importância

Critérios de aceite bem definidos:

- evitam retrabalho;
- reduzem interpretações subjetivas;
- facilitam testes (inclusive automatizados);
- melhoram a comunicação entre Product Owner, desenvolvedores e testers;
- tornam a entrega mais previsível.

Em contextos ágeis, normalmente estão associados às **User Stories**, representando a definição prática de “pronto”.

---

## Características

Bons critérios de aceite devem ser:

- claros;
- objetivos e mensuráveis;
- testáveis;
- específicos;
- independentes de interpretação subjetiva.

Uma prática recomendada é o uso do formato:

**Dado / Quando / Então (Given / When / Then)**

---

## Exercício – Criação de Critérios de Aceite

### Contexto

Sistema de cadastro de produtos com as seguintes regras:

- Campos obrigatórios: nome, categoria, preço e quantidade em estoque;
- Preço > 0;
- Quantidade ≥ 0;
- Nome com mínimo de 3 caracteres;
- Exibição de mensagem de sucesso para cadastro válido;
- Exibição de mensagens de erro específicas para dados inválidos;
- Proibição de cadastro com nome duplicado.

### Tarefa

Elaborar critérios de aceite utilizando o formato **Dado / Quando / Então**, contemplando:

- fluxo principal (cadastro válido);
- validações de campos obrigatórios;
- regras de negócio;
- tratamento de erros.

Não elaborar casos de teste detalhados.

### Critérios de Aceite

**1- Cadastro com dados válidos**
  
**Dado** que o usuário está na página de cadastro de produtos  
**Quando** ele informar um nome com no mínimo 3 caracteres, uma categoria, um preço maior que zero e uma quantidade em estoque igual ou maior que zero  
**E** o nome do produto não estiver previamente cadastrado  
**Então** o sistema deve cadastrar o produto com sucesso  
**E** exibir uma mensagem de confirmação de cadastro realizado  

**2- Campos obrigatórios não preenchidos**
  
**Dado** que o usuário está na página de cadastro  
**Quando** ele tentar cadastrar o produto deixando qualquer campo obrigatório em branco  
**Então** o sistema deve impedir o cadastro  
**E** exibir mensagem de erro informando que o campo é obrigatório  

**3- Nome de produto com menos caracteres que o permitido**
  
**Dado** que o usuário está na página de cadastro de produtos  
**Quando** ele informar um nome com 2 caracteres ou menos  
**Então** o sistema deve impedir o produto de ser cadastrado  
**E** exibir uma mensagem informando que o nome deve conter no mínimo 3 caracteres  

**4- Valores negativos**
  
**Dado** que o usuário está na página de cadastro de produtos  
**Quando** ele informar um preço e/ou quantidade em estoque negativos  
**Então** o sistema deve impedir o produto de ser cadastrado  
**E** exibir uma mensagem informando que o preço e/ou quantidade em estoque devem ser igual ou maior que zero  

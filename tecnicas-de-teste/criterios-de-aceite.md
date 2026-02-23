# Escrita de Critérios de Aceite

A **escrita de critérios de aceite** é uma atividade essencial na engenharia de requisitos e na validação de software, pois define **quando uma funcionalidade pode ser considerada pronta e correta**.

De acordo com o International Software Testing Qualifications Board (ISTQB), critérios de aceite são condições que um produto deve satisfazer para ser aceito por um usuário, cliente ou outra parte interessada. Eles funcionam como uma ponte entre requisitos e testes, estabelecendo parâmetros claros e verificáveis.

Enquanto os **requisitos** descrevem *o que o sistema deve fazer*, os **critérios de aceite** especificam **as condições mensuráveis que comprovam que o requisito foi atendido**.

Segundo Ian Sommerville:

> **"Requisitos bem definidos devem possuir critérios claros de validação, permitindo verificar objetivamente se o sistema atende às necessidades estabelecidas."**

Nesse contexto, os critérios de aceite:

- definem condições objetivas e verificáveis;
- reduzem ambiguidades nos requisitos;
- orientam a criação de casos de teste;
- alinham expectativas entre cliente, negócio e equipe técnica;
- servem como base para validação e homologação.

---

## Diferença entre Requisito, Critério de Aceite e Caso de Teste

| Requisito | Critério de Aceite | Caso de Teste |
|------------|-------------------|---------------|
| Define **o que o sistema deve fazer** | Define **quando está correto** | Define **como validar** |
| Pode ser mais abstrato | É objetivo e mensurável | É detalhado e executável |
| Foco na necessidade | Foco na condição de aprovação | Foco na verificação prática |
| Base do desenvolvimento | Base da validação | Base da execução do teste |

---

## Importância dos Critérios de Aceite

Critérios de aceite bem escritos:

- evitam retrabalho;
- reduzem interpretações subjetivas;
- facilitam testes automatizados;
- melhoram a comunicação entre Product Owner, desenvolvedores e testers;
- tornam a entrega mais previsível.

Em contextos ágeis, os critérios de aceite costumam estar associados às **User Stories**, funcionando como a definição prática do que significa “pronto” para aquela funcionalidade.

---

## Características de Bons Critérios de Aceite

Bons critérios de aceite devem ser:

- **Claros** – sem ambiguidade;
- **Objetivos** – mensuráveis e verificáveis;
- **Testáveis** – possibilitar validação prática;
- **Específicos** – diretamente relacionados ao requisito;
- **Independentes** – não depender de interpretação subjetiva.

Uma prática comum é estruturá-los no formato:

**Dado / Quando / Então (Given / When / Then)**

Pois isso facilita entendimento, rastreabilidade e futura automação de testes.

---

## Exercício – Criação de Critérios de Aceite

### Contexto do Sistema

Considere um **sistema de cadastro de produtos** com as seguintes regras de negócio:

- O usuário deve informar:
  - Nome do produto
  - Categoria
  - Preço
  - Quantidade em estoque
- Todos os campos são obrigatórios.
- O preço deve ser maior que zero.
- A quantidade em estoque não pode ser negativa.
- O nome do produto deve conter no mínimo 3 caracteres.
- O sistema deve exibir mensagem de sucesso após cadastro válido.
- O sistema deve exibir mensagens de erro específicas quando houver dados inválidos.
- Não deve ser permitido cadastrar dois produtos com o mesmo nome.

### Sua Tarefa

Com base nas regras acima:

👉 **Elabore os critérios de aceite para a funcionalidade de cadastro de produtos.**

- Orientações:

  - Utilize o formato **Dado / Quando / Então**.
  - Considere:
    - Fluxo principal (cadastro válido)
    - Validações de campos obrigatórios
    - Regras de negócio
    - Tratamento de erros
  - Crie critérios objetivos, claros e testáveis.
  - Não escreva casos de teste detalhados — apenas critérios de aceite.

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

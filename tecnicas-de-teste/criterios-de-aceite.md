# Escrita de Critérios de Aceite

A **escrita de critérios de aceite** define **quando uma funcionalidade pode ser considerada pronta e correta**.

Segundo o ISTQB, critérios de aceite são condições que um produto deve satisfazer para ser aceito pelas partes interessadas. Eles estabelecem parâmetros claros e verificáveis entre requisitos e testes.

Enquanto **requisitos** descrevem *o que o sistema deve fazer*, os **critérios de aceite** especificam **as condições mensuráveis que comprovam que o requisito foi atendido**.

**Segundo Ian Sommerville:** *"Requisitos bem definidos devem possuir critérios claros de validação, permitindo verificar objetivamente se o sistema atende às necessidades estabelecidas."*

Os critérios de aceite:
- definem condições objetivas e verificáveis;
- reduzem ambiguidades;
- orientam a criação de testes;
- alinham expectativas;
- servem como base para validação.

---

## Diferença entre Requisito, Critério de Aceite e Caso de Teste

| Requisito | Critério de Aceite | Caso de Teste |
|------------|-------------------|---------------|
| **O que** o sistema deve fazer | **Quando** está correto | **Como** validar |
| Pode ser abstrato | Objetivo e mensurável | Detalhado e executável |
| Base do desenvolvimento | Base da validação | Base da execução |

---

## Importância

Critérios de aceite bem escritos:
- evitam retrabalho;
- reduzem subjetividade;
- facilitam testes automatizados;
- melhoram a comunicação;
- tornam a entrega mais previsível.

---

## Características

Bons critérios devem ser:
- **Claros** – sem ambiguidade;
- **Objetivos** – mensuráveis;
- **Testáveis** – validáveis na prática;
- **Específicos** – ligados ao requisito;
- **Independentes** – sem interpretação subjetiva.

Formato recomendado: **Dado / Quando / Então**

---

## Exercício – Critérios de Aceite

### Contexto

**Sistema de cadastro de produtos** com as regras:
- Campos obrigatórios: nome, categoria, preço, quantidade em estoque
- Preço > zero
- Quantidade ≥ zero
- Nome ≥ 3 caracteres
- Mensagem de sucesso após cadastro válido
- Mensagens de erro específicas para dados inválidos
- Nome do produto deve ser único

👉 **Elabore os critérios de aceite da funcionalidade de cadastro.**

### Critérios de Aceite

**1. Cadastro válido**
  
**Dado** que o usuário está na página de cadastro  
**Quando** informar nome (≥3 caracteres), categoria, preço (>0) e quantidade (≥0)  
**E** o nome não estiver cadastrado  
**Então** o sistema cadastra o produto e exibe mensagem de sucesso  

**2. Campos obrigatórios vazios**
  
**Dado** que o usuário está na página de cadastro  
**Quando** tentar cadastrar com algum campo obrigatório em branco  
**Então** o sistema impede o cadastro e informa que o campo é obrigatório  

**3. Nome com menos de 3 caracteres**
  
**Dado** que o usuário está na página de cadastro  
**Quando** informar nome com ≤2 caracteres  
**Então** o sistema impede o cadastro e informa que o nome deve ter no mínimo 3 caracteres  

**4. Valores negativos**
  
**Dado** que o usuário está na página de cadastro  
**Quando** informar preço ou quantidade negativos  
**Então** o sistema impede o cadastro e informa que os valores devem ser ≥ zero

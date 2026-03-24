# Exercício – Critérios de Aceite

## Contexto

**Sistema de cadastro de produtos** com as regras:
- Campos obrigatórios: nome, categoria, preço, quantidade em estoque
- Preço > zero
- Quantidade ≥ zero
- Nome ≥ 3 caracteres
- Mensagem de sucesso após cadastro válido
- Mensagens de erro específicas para dados inválidos
- Nome do produto deve ser único

👉 **Elabore os critérios de aceite da funcionalidade de cadastro.**

## Critérios de Aceite

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

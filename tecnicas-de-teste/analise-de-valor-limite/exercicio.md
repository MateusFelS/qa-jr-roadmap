# Exercício – Aplicação de Análise de Valor Limite

### Contexto

Sistema de **cadastro de produtos** com as regras:
- Nome do produto: mínimo 3, máximo 100 caracteres
- Preço: mínimo R$ 0,01, máximo R$ 10.000,00
- Quantidade em estoque: mínimo 0, máximo 1.000 unidades
- Categoria: obrigatória (lista fixa com 5 opções)

👉 **Identifique os valores limite para cada campo**

---

### Valores Limite – Campo Nome

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-01 | 2 caracteres | Inválido | Abaixo do mínimo |
| VL-02 | 3 caracteres | Válido | Mínimo |
| VL-03 | 4 caracteres | Válido | Acima do mínimo|
| VL-04 | 99 caracteres | Válido | Abaixo do máximo |
| VL-05 | 100 caracteres | Válido | Máximo |
| VL-06 | 101 caracteres | Inválido | Acima do máximo |

### Valores Limite – Preço

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-07 | R$ 0,00 | Inválido | Abaixo do mínimo |
| VL-08 | R$ 0,01 | Válido | Mínimo |
| VL-09 | R$ 0,02 | Válido | Acima do mínimo |
| VL-10 | R$ 9.999,99 | Válido | Abaixo do máximo |
| VL-11 | R$ 10.000,00 | Válido | Máximo |
| VL-12 | R$ 10.000,01 | Inválido | Acima do máximo |

### Valores Limite – Quantidade em Estoque

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-13 | -1 | Inválido | Abaixo do mínimo |
| VL-14 | 0 | Válido | Mínimo |
| VL-15 | 1 | Válido | Acima do mínimo |
| VL-16 | 999 | Válido | Abaixo do máximo |
| VL-17 | 1.000 | Válido | Máximo |
| VL-18 | 1.001 | Inválido | Acima do máximo |

### Valores Limite – Categoria

Para campos com domínio discreto (lista fixa), a análise de valor limite se aplica de forma adaptada:

| ID | Valor | Classificação | Descrição |
|----|-------|---------------|-----------|
| VL-19 | Nenhuma selecionada | Inválido | Abaixo do mínimo (obrigatório) |
| VL-20 | Primeira opção da lista | Válido | Valor mínimo do domínio |
| VL-21 | Segunda opção | Válido | Representativo |
| VL-22 | Última opção da lista | Válido | Valor máximo do domínio |
| VL-23 | Opção inexistente | Inválido | Acima do máximo |

# JavaScript Básico

O **JavaScript (JS)** é uma linguagem de programação utilizada para adicionar interatividade e comportamento às páginas web.

Enquanto o HTML define a estrutura e o CSS controla a aparência, o JavaScript permite criar funcionalidades dinâmicas, como validação de formulários, animações e atualização de conteúdo sem recarregar a página.

Segundo **David Flanagan**, autor de *JavaScript: The Definitive Guide*, o JavaScript é a principal linguagem de programação para desenvolvimento de aplicações web.

---

# Conceito Fundamental

O JavaScript executa instruções que permitem manipular elementos da página e responder às ações do usuário.

Entre suas principais aplicações estão:

- Validar formulários;
- Manipular elementos HTML;
- Realizar cálculos;
- Consumir APIs;
- Atualizar conteúdo dinamicamente.

---

# Variáveis

As variáveis armazenam informações utilizadas durante a execução do programa.

No JavaScript moderno, as principais formas de declaração são:

- `let` → valor que pode ser alterado.
- `const` → valor constante.

## Exemplo

```javascript
let nome = "João";
const idade = 25;
```

---

# Estruturas Condicionais

As estruturas condicionais permitem executar diferentes ações conforme uma condição.

As mais utilizadas são:

- `if`
- `else`
- `else if`

## Exemplo

```javascript
if (idade >= 18) {
    console.log("Maior de idade");
}
```

---

# Estruturas de Repetição

As estruturas de repetição executam um bloco de código várias vezes.

As principais são:

- `for`
- `while`

## Exemplo

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

---

# Funções

Uma **função** é um bloco de código criado para executar uma determinada tarefa.

## Exemplo

```javascript
function somar(a, b) {
    return a + b;
}
```

As funções facilitam a reutilização do código e sua organização.

---

# JavaScript e o QA

Conhecer JavaScript auxilia o profissional de QA em diversas atividades.

Entre elas:

- Compreender a lógica da aplicação;
- Identificar erros no Console do navegador;
- Criar testes automatizados;
- Validar regras de negócio;
- Localizar e manipular elementos da página.

Esse conhecimento também é importante para ferramentas de automação como Cypress, Playwright e Selenium.

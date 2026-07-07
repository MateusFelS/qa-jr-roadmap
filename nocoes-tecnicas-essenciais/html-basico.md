# HTML Básico

O **HTML (HyperText Markup Language)** é a linguagem de marcação utilizada para estruturar o conteúdo de páginas web.

Segundo a **World Wide Web Consortium (W3C)**, o HTML define a estrutura semântica de documentos na Web, organizando textos, imagens, links, formulários e outros elementos.

Embora não seja uma linguagem de programação, o HTML é um conhecimento importante para profissionais de QA, especialmente em testes de aplicações web e automação.

---

# Conceito Fundamental

O HTML é composto por **elementos**, representados por **tags**, que definem a estrutura e o significado do conteúdo de uma página.

A maioria das tags possui:

- Tag de abertura;
- Conteúdo;
- Tag de fechamento.

## Exemplo

```html
<p>Olá, mundo!</p>
```

Nesse exemplo, a tag `<p>` representa um parágrafo.

---

# Estrutura Básica de uma Página HTML

Todo documento HTML possui uma estrutura básica.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página</title>
</head>
<body>
    <h1>Olá, mundo!</h1>
</body>
</html>
```

Os principais elementos são:

- `<!DOCTYPE html>` → informa que o documento utiliza HTML5.
- `<html>` → elemento raiz da página.
- `<head>` → contém informações sobre o documento.
- `<title>` → define o título exibido na aba do navegador.
- `<body>` → contém o conteúdo visível da página.

---

# Principais Tags

Algumas das tags mais utilizadas são:

| Tag | Função |
|------|--------|
| `<h1>` a `<h6>` | Títulos e subtítulos |
| `<p>` | Parágrafo |
| `<a>` | Link |
| `<img>` | Imagem |
| `<button>` | Botão |
| `<input>` | Campo de entrada |
| `<form>` | Formulário |
| `<table>` | Tabela |
| `<div>` | Agrupa elementos |
| `<span>` | Agrupa conteúdo em linha |

---

# Atributos

Os atributos fornecem informações adicionais aos elementos HTML.

Alguns exemplos são:

- `id`
- `class`
- `name`
- `type`
- `value`
- `href`
- `src`

## Exemplo

```html
<input type="text" id="nome" name="nome">
```

Os atributos são amplamente utilizados para identificação de elementos durante testes automatizados.

---

# HTML e o QA

Conhecer HTML auxilia o profissional de QA em diversas atividades.

Entre elas:

- Identificar elementos da página;
- Localizar IDs e classes para automação;
- Validar formulários;
- Investigar problemas de interface;
- Utilizar a Inspeção de Elementos do navegador.

Esses conhecimentos facilitam a criação de testes mais confiáveis e a análise de defeitos.

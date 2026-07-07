# CSS Básico

O **CSS (Cascading Style Sheets)** é a linguagem utilizada para definir a aparência e o layout de páginas web.

Enquanto o HTML estrutura o conteúdo, o CSS controla aspectos visuais como cores, fontes, espaçamentos, tamanhos e posicionamento dos elementos.

Segundo a **World Wide Web Consortium (W3C)**, o CSS separa a apresentação da estrutura do documento, facilitando a manutenção e a reutilização do código.

---

# Conceito Fundamental

O CSS é composto por **seletores** e **declarações**.

Cada regra define quais elementos serão estilizados e quais propriedades visuais serão aplicadas.

## Exemplo

```css
p {
    color: blue;
    font-size: 16px;
}
```

Nesse exemplo:

- `p` é o seletor;
- `color` e `font-size` são propriedades;
- `blue` e `16px` são os valores atribuídos.

---

# Principais Seletores

Os seletores identificam os elementos que receberão um estilo.

Os mais utilizados são:

| Seletor | Exemplo | Aplica-se a |
|----------|----------|-------------|
| Elemento | `p` | Todos os parágrafos |
| Classe | `.botao` | Elementos com a classe especificada |
| ID | `#login` | Elemento com o ID informado |
| Universal | `*` | Todos os elementos |

---

# Principais Propriedades

Algumas propriedades básicas do CSS são:

- `color` → cor do texto.
- `background-color` → cor de fundo.
- `font-size` → tamanho da fonte.
- `font-family` → tipo da fonte.
- `width` → largura.
- `height` → altura.
- `margin` → espaçamento externo.
- `padding` → espaçamento interno.
- `border` → borda do elemento.

---

# Box Model

Segundo o **MDN Web Docs**, todos os elementos HTML são representados como caixas (**Box Model**).

Cada caixa é composta por:

- Content (Conteúdo);
- Padding (Espaçamento interno);
- Border (Borda);
- Margin (Espaçamento externo).

Compreender o Box Model é essencial para identificar problemas de layout.

---

# CSS e o QA

Conhecer CSS auxilia o profissional de QA em diversas atividades.

Entre elas:

- Identificar classes utilizadas na interface;
- Investigar problemas de layout;
- Validar cores, fontes e espaçamentos;
- Localizar elementos para automação;
- Analisar defeitos visuais.

Esse conhecimento facilita a identificação de bugs relacionados à interface do usuário.

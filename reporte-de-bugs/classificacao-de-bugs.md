# Classificação de Bugs

Um **bug** pode ser classificado de diferentes maneiras para facilitar sua análise, tratamento e priorização durante o processo de desenvolvimento de software.

Embora existam diversas classificações, uma das mais utilizadas considera **a natureza do defeito**, ou seja, qual aspecto da aplicação foi afetado.

Segundo **Rex Black**, classificar corretamente um defeito melhora a comunicação entre as equipes e auxilia na identificação de padrões de qualidade ao longo do projeto.

---

# Conceito Fundamental

A classificação de um bug não altera sua gravidade, mas ajuda a compreender sua origem e seu impacto.

Um defeito pode ser, por exemplo:

- Funcional;
- De Usabilidade;
- Visual (Interface do Usuário).

Cada categoria representa um tipo diferente de problema encontrado durante os testes.

---

# Bugs Funcionais

Os **bugs funcionais** são defeitos que afetam diretamente o funcionamento da aplicação.

Nesses casos, o sistema executa uma ação diferente daquela especificada pelos requisitos ou regras de negócio.

## Características

- Funcionalidade não executa corretamente.
- Cálculos incorretos.
- Regras de negócio não respeitadas.
- Validações incorretas.
- Fluxos interrompidos.

## Exemplos

- Login não funciona.
- Botão Salvar não grava informações.
- Sistema aceita CPF inválido.
- Valor do desconto é calculado incorretamente.

---

# Bugs de Usabilidade

Os **bugs de usabilidade** dificultam a utilização do sistema, mesmo quando suas funcionalidades estão tecnicamente corretas.

Segundo **Jakob Nielsen**, problemas de usabilidade reduzem a eficiência, aumentam erros do usuário e prejudicam sua experiência.

## Características

- Fluxos confusos.
- Mensagens pouco claras.
- Navegação difícil.
- Informações mal organizadas.
- Interface pouco intuitiva.

## Exemplos

- Mensagem de erro não explica o problema.
- Processo de cadastro exige etapas desnecessárias.
- Campo obrigatório não é identificado.
- Botão importante fica escondido.

---

# Bugs Visuais

Também conhecidos como **UI Bugs (User Interface Bugs)**, são defeitos relacionados exclusivamente à aparência da aplicação.

Normalmente não afetam a lógica do sistema, mas prejudicam a apresentação e a experiência do usuário.

## Características

- Problemas de layout.
- Alinhamento incorreto.
- Fontes inconsistentes.
- Ícones ausentes.
- Cores incorretas.

## Exemplos

- Texto cortado.
- Botões desalinhados.
- Imagens distorcidas.
- Layout quebrado em dispositivos móveis.
- Elementos sobrepostos.

---

# Comparação entre os Tipos

| Tipo de Bug | Afeta regra de negócio? | Afeta experiência do usuário? | Exemplo |
|--------------|--------------------------|-------------------------------|----------|
| Funcional | Sim | Pode afetar | Login não funciona |
| Usabilidade | Não necessariamente | Sim | Fluxo confuso |
| Visual | Não | Sim | Botão desalinhado |

---

# Exemplos Comparativos

## Bug Funcional

**Problema:**

O sistema calcula incorretamente o valor do frete.

---

## Bug de Usabilidade

**Problema:**

O botão "Finalizar Compra" fica escondido abaixo da área visível da página.

---

## Bug Visual

**Problema:**

Os campos do formulário aparecem desalinhados apenas no navegador Firefox.

---

# Relação entre as Classificações

Um mesmo sistema pode apresentar diferentes tipos de defeitos ao mesmo tempo.

Por exemplo:

- Um botão pode estar desalinhado (**bug visual**);
- Possuir um texto pouco claro (**bug de usabilidade**);
- E não executar sua função corretamente (**bug funcional**).

Por isso, identificar corretamente a natureza do defeito facilita sua análise, comunicação e correção durante o processo de desenvolvimento de software.

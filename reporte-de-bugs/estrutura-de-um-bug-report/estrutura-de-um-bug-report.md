# Estrutura de um Bug Report

Um **Bug Report** (Relatório de Defeito) é um documento utilizado para registrar, comunicar, acompanhar e facilitar a correção de um defeito encontrado durante a execução de testes ou durante a utilização do software.

Seu principal objetivo é fornecer informações suficientes para que qualquer membro da equipe consiga **reproduzir o problema, compreender sua causa e validar posteriormente sua correção**.

Segundo o **ISTQB (CTFL - Foundation Level)**, um relatório de defeito deve conter informações claras, completas e objetivas, permitindo que o defeito seja reproduzido e tratado de maneira eficiente durante o ciclo de vida do desenvolvimento.

**Cem Kaner**, em *Testing Computer Software*, destaca:

> **"Um bom relatório de defeito contém todas as informações necessárias para que outra pessoa consiga reproduzir o problema sem depender do testador que o encontrou."**

**Rex Black**, em *Foundations of Software Testing*, complementa que a qualidade da comunicação entre testadores e desenvolvedores influencia diretamente a velocidade da correção dos defeitos.

---

# Conceito Fundamental

Um Bug Report deve responder, no mínimo, às seguintes perguntas:

- O que aconteceu?
- Onde aconteceu?
- Como reproduzir o problema?
- Qual comportamento era esperado?
- Qual comportamento realmente ocorreu?
- Qual o impacto do defeito?

Quanto mais completas forem essas respostas, menor será o tempo gasto pela equipe para investigar e corrigir o problema.

---

# Estrutura Básica de um Bug Report

Embora ferramentas como Jira, Azure DevOps, Bugzilla e Redmine utilizem nomenclaturas diferentes, praticamente todos os relatórios possuem campos semelhantes.

| Campo | Finalidade |
|--------|------------|
| **Título** | Resume o defeito de forma objetiva |
| **Descrição** | Contextualiza o problema |
| **Pré-condições** | Estado necessário antes da execução |
| **Passos para reprodução** | Sequência utilizada para reproduzir o defeito |
| **Resultado esperado** | Comportamento correto do sistema |
| **Resultado atual (Obtido)** | Comportamento realmente observado |
| **Evidências** | Prints, vídeos, logs ou mensagens de erro |
| **Ambiente** | Sistema operacional, navegador, dispositivo, versão da aplicação etc. |
| **Severidade** | Impacto técnico causado pelo defeito |
| **Prioridade** | Ordem ou urgência para correção |

---

# Severidade x Prioridade

Embora frequentemente utilizadas juntas, **Severidade** e **Prioridade** representam conceitos diferentes.

Segundo **Rex Black**, a severidade está relacionada ao impacto técnico do defeito, enquanto a prioridade representa a urgência de sua correção sob a perspectiva do negócio.

| Severidade | Prioridade |
|-------------|------------|
| Mede o impacto técnico do defeito | Mede a urgência da correção |
| Relacionada ao funcionamento do sistema | Relacionada ao planejamento do projeto |
| Geralmente definida pela equipe de testes | Geralmente definida pelo Product Owner, gerente ou equipe responsável |
| Pode ser alta e possuir baixa prioridade | Pode ser alta mesmo em defeitos pouco severos |

**Exemplo:**

| Situação | Severidade | Prioridade |
|----------|------------|------------|
| Sistema não permite login | Alta | Alta |
| Logotipo da empresa desatualizado na tela inicial | Baixa | Alta (campanha de marketing) |
| Erro em funcionalidade pouco utilizada | Alta | Baixa |

---

# Passos para Reprodução

Os **Passos para Reprodução** descrevem exatamente o caminho percorrido até que o defeito aconteça.

Seu objetivo é permitir que qualquer pessoa consiga reproduzir o problema seguindo a mesma sequência de ações.

Boas práticas:

- Informar a pré-condição, quando existir.
- Escrever cada ação em ordem cronológica.
- Não omitir etapas.
- Evitar descrições genéricas.

**Exemplo:**

1. Realizar login como administrador.
2. Acessar o menu **Cadastro > Usuários**.
3. Clicar em **Novo Usuário**.
4. Preencher todos os campos obrigatórios.
5. Deixar o campo **Telefone** vazio.
6. Clicar em **Salvar**.

---

# Resultado Esperado x Resultado Atual

Esses dois campos representam a comparação entre o comportamento especificado e o comportamento observado.

## Resultado Esperado

Descreve como o sistema deveria funcionar segundo os requisitos ou regras de negócio.

**Exemplo:**

> O sistema deve exibir uma mensagem informando que o telefone é obrigatório.

## Resultado Atual (Obtido)

Descreve exatamente o comportamento observado durante o teste.

**Exemplo:**

> A aplicação apresenta erro HTTP 500 e interrompe o processamento.

A descrição deve ser objetiva, baseada em fatos e livre de interpretações.

---

# Classificação dos Bugs

Os defeitos podem ser classificados de diversas maneiras. Uma classificação bastante utilizada considera a natureza do problema.

## Bugs Funcionais

São defeitos relacionados ao funcionamento da aplicação.

O sistema executa uma ação diferente daquela especificada pelos requisitos.

**Exemplos:**

- Login não funciona.
- Cálculo incorreto de impostos.
- Botão Salvar não grava informações.
- Validação aceita dados inválidos.

---

## Bugs de Usabilidade

São problemas que dificultam ou prejudicam a interação do usuário com o sistema, mesmo quando as funcionalidades executam corretamente.

Segundo **Jakob Nielsen**, problemas de usabilidade reduzem a eficiência, aumentam erros do usuário e prejudicam a experiência de utilização.

**Exemplos:**

- Fluxo de cadastro confuso.
- Mensagens de erro pouco claras.
- Navegação difícil.
- Campos importantes pouco visíveis.

---

## Bugs Visuais

Também chamados de **bugs de interface (UI Bugs)**, afetam apenas a apresentação da aplicação.

Normalmente não comprometem a lógica de negócio, mas podem prejudicar a experiência do usuário e a credibilidade do produto.

**Exemplos:**

- Texto cortado.
- Botões desalinhados.
- Cores incorretas.
- Ícones ausentes.
- Layout quebrado em dispositivos móveis.

---

# Relação entre os Conceitos

Durante a execução dos testes:

1. O testador identifica um defeito.
2. Classifica seu tipo (funcional, usabilidade ou visual).
3. Documenta os passos para reprodução.
4. Registra o resultado esperado.
5. Registra o resultado atual.
6. Define a severidade.
7. A equipe define a prioridade da correção.

Um Bug Report completo reduz ambiguidades, facilita a reprodução do problema e acelera o processo de correção.

Segundo **Boris Beizer**, em *Software Testing Techniques*:

> **"Um defeito bem documentado é significativamente mais fácil de reproduzir, analisar e corrigir do que um defeito descrito de maneira incompleta."**

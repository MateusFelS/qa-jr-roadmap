# Estrutura de um Bug Report

Um **Bug Report** (Relatório de Defeito) é um documento utilizado para registrar, comunicar e acompanhar um defeito encontrado durante a execução de testes ou durante a utilização de um software.

Seu principal objetivo é fornecer informações suficientes para que qualquer membro da equipe consiga **reproduzir o problema, compreender sua causa e validar posteriormente sua correção**.

Segundo o **ISTQB (CTFL - Foundation Level)**, um relatório de defeito deve ser claro, completo, objetivo e conter informações suficientes para permitir a reprodução do problema.

**Cem Kaner**, em *Testing Computer Software*, afirma:

> **"Um bom relatório de defeito contém todas as informações necessárias para que outra pessoa consiga reproduzir o problema sem depender do testador que o encontrou."**

**Rex Black**, em *Foundations of Software Testing*, destaca que a qualidade de um Bug Report influencia diretamente a eficiência da comunicação entre testadores e desenvolvedores, reduzindo o tempo necessário para diagnosticar e corrigir defeitos.

---

# Conceito Fundamental

Um Bug Report deve responder, no mínimo, às seguintes perguntas:

- O que aconteceu?
- Onde aconteceu?
- Como reproduzir o problema?
- Qual comportamento era esperado?
- Qual comportamento realmente ocorreu?
- Qual o impacto do defeito?

Quanto mais completas e objetivas forem essas respostas, maior será a facilidade para reproduzir e corrigir o defeito.

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
| **Prioridade** | Urgência da correção |

---

# Passos para Reprodução

Os **Passos para Reprodução** descrevem exatamente a sequência de ações necessária para reproduzir o defeito.

Seu objetivo é permitir que qualquer pessoa consiga repetir o problema seguindo o mesmo procedimento.

## Boas práticas

- Informar as pré-condições, quando existirem.
- Descrever cada ação em ordem cronológica.
- Não omitir etapas.
- Informar dados utilizados durante o teste.
- Evitar descrições genéricas.

**Exemplo:**

1. Realizar login como administrador.
2. Acessar **Cadastro > Usuários**.
3. Clicar em **Novo Usuário**.
4. Preencher todos os campos obrigatórios.
5. Deixar o campo **Telefone** vazio.
6. Clicar em **Salvar**.

---

# Resultado Esperado x Resultado Atual

Esses dois campos permitem comparar o comportamento previsto do sistema com o comportamento realmente observado.

## Resultado Esperado

Descreve como o sistema deveria funcionar de acordo com os requisitos.

**Exemplo:**

> O sistema deve informar que o campo Telefone é obrigatório.

## Resultado Atual

Descreve exatamente o comportamento observado durante o teste.

**Exemplo:**

> O sistema apresenta erro HTTP 500 e interrompe o processamento.

| Resultado Esperado | Resultado Atual |
|--------------------|-----------------|
| Baseado nos requisitos | Baseado na execução do teste |
| Representa o comportamento correto | Representa o comportamento observado |
| Define o que deveria acontecer | Define o que realmente aconteceu |

---

# Severidade x Prioridade

Embora frequentemente confundidos, esses conceitos possuem objetivos diferentes.

Segundo **Rex Black**, a severidade está relacionada ao impacto técnico do defeito, enquanto a prioridade representa a urgência de sua correção sob a perspectiva do negócio.

| Severidade | Prioridade |
|-------------|------------|
| Mede o impacto técnico do defeito | Mede a urgência da correção |
| Relacionada ao funcionamento do sistema | Relacionada ao planejamento do projeto |
| Geralmente definida pela equipe de testes | Geralmente definida pelo Product Owner, gerente ou equipe responsável |
| Pode ser alta e possuir baixa prioridade | Pode ser alta mesmo em defeitos pouco severos |

**Exemplos:**

| Situação | Severidade | Prioridade |
|----------|------------|------------|
| Sistema não permite login | Alta | Alta |
| Logotipo incorreto na tela inicial | Baixa | Alta |
| Erro em relatório pouco utilizado | Alta | Baixa |

---

# Boas Práticas na Elaboração de um Bug Report

Para facilitar a comunicação entre as equipes, recomenda-se:

- Utilizar títulos claros e objetivos.
- Descrever apenas fatos observados.
- Informar todos os passos para reprodução.
- Registrar claramente os resultados esperado e atual.
- Anexar evidências sempre que possível.
- Informar corretamente o ambiente de testes.
- Evitar linguagem subjetiva ou opiniões.

---

# Exemplo Simplificado de Bug Report

| Campo | Conteúdo |
|--------|----------|
| **Título** | Erro ao salvar usuário sem telefone |
| **Pré-condição** | Usuário autenticado como administrador |
| **Passos** | Cadastro → Novo Usuário → Deixar telefone vazio → Salvar |
| **Resultado esperado** | Sistema deve solicitar o preenchimento do telefone |
| **Resultado atual** | Aplicação apresenta erro HTTP 500 |
| **Severidade** | Alta |
| **Prioridade** | Média |

---

# Relação com o Processo de Testes

Após identificar um defeito, o testador registra todas as informações relevantes em um Bug Report. Esse documento é utilizado pela equipe de desenvolvimento para reproduzir, analisar, corrigir e posteriormente validar a solução implementada.

Segundo **Boris Beizer**, em *Software Testing Techniques*:

> **"Um defeito bem documentado é significativamente mais fácil de reproduzir, analisar e corrigir do que um defeito descrito de maneira incompleta."**

# Fundamentos de Qualidade

## Qualidade de Software

A **qualidade de software** é um dos pilares fundamentais da Engenharia de Software, pois está diretamente relacionada à aceitação e à satisfação dos usuários finais.

Segundo Ian Sommerville, em *Software Engineering*, a qualidade de software é definida como:

> **“Atributos essenciais que afetam a aceitação do software pelo usuário, incluindo confiabilidade, eficiência, facilidade de uso e manutenção.”**

Nesse contexto, um software de qualidade deve apresentar:
- funcionamento confiável;
- uso eficiente dos recursos disponíveis;
- facilidade de aprendizado e utilização;
- capacidade de manutenção e evolução ao longo do tempo.

Dessa forma, a aceitação por parte dos usuários torna-se um fator central para a efetiva qualidade do software.

---

## Papel do QA

A **garantia da qualidade de software** está diretamente relacionada à adoção de processos bem definidos e à prevenção de defeitos ao longo de todo o ciclo de vida do software.

Roger S. Pressman, em *Engenharia de Software: Uma Abordagem Profissional*, destaca que a garantia da qualidade de software consiste em um conjunto de atividades planejadas e sistemáticas que asseguram que os processos, métodos e padrões adotados durante o desenvolvimento sejam seguidos corretamente. Segundo o autor:

> **“A garantia da qualidade de software é uma atividade guarda-chuva que se aplica a todo o processo de desenvolvimento.”**

A partir dessa perspectiva, o papel do QA não se limita à execução de testes ao final do desenvolvimento. O QA atua de forma **contínua e preventiva**, colaborando com o time desde as fases iniciais de planejamento e definição de requisitos, acompanhando o desenvolvimento, apoiando a execução dos testes e contribuindo para a entrega de um produto que atenda aos padrões de qualidade e às expectativas dos usuários.

---

## SDLC (Ciclo de Vida do Desenvolvimento de Software) x STLC (Ciclo de Vida de Testes de Software)

O **SDLC** corresponde ao ciclo de vida completo do software, englobando todas as atividades necessárias para sua concepção, desenvolvimento, validação, implantação e manutenção.

Segundo Sommerville (2016):

> **“O ciclo de vida do software organiza os processos fundamentais de especificação, desenvolvimento, validação e evolução, garantindo que o produto atenda aos requisitos técnicos e às necessidades dos usuários.”**

Já o **STLC** refere-se ao ciclo de vida do processo de testes de software. Ele descreve, de forma estruturada, as atividades relacionadas ao planejamento, projeto, execução e encerramento dos testes, com o objetivo de verificar e validar a conformidade do sistema em relação aos requisitos definidos.

Conforme discutido por Myers, Sandler e Badgett (2011) e Rex Black (2009):

> **“O teste de software deve ser tratado como um processo sistemático e gerenciável, e não como uma atividade isolada ao final do desenvolvimento.”**

Dessa forma, enquanto o SDLC possui uma visão abrangente voltada à entrega e evolução do software, o STLC concentra-se especificamente na garantia da qualidade, organizando as atividades de teste que sustentam a confiabilidade e a aceitação do produto final.

## Erro, Defeito/Bug e Falha segundo a ISTQB

No contexto de testes de software, a ISTQB estabelece uma distinção clara entre erro, defeito (bug) e falha, conceitos fundamentais para a garantia da qualidade.

Segundo o ISTQB Glossary of Testing Terms: 

> **"Um erro é uma ação humana que produz um resultado incorreto. Quando esse erro é introduzido em um artefato do software, como código ou documentação, ele se manifesta como um defeito, também conhecido informalmente como bug. A falha, por sua vez, ocorre quando esse defeito é executado e resulta em um comportamento incorreto do sistema."**

Ou seja, o erro está relacionado a uma decisão ou interpretação equivocada realizada por um indivíduo durante atividades como levantamento de requisitos, projeto, codificação ou testes.

- **Exemplo:**
  
  Considere um sistema que deve aplicar desconto para compras a partir de R$ 100,00:  
  - **Erro:** o desenvolvedor interpreta incorretamente a regra de negócio e entende que o desconto deve ser aplicado apenas para valores estritamente maiores que R$ 100,00.
  - **Defeito/Bug:** o código é implementado utilizando a condição `valor > 100`, em vez de `valor >= 100`.
  - **Falha:** ao realizar uma compra exatamente no valor de R$ 100,00, o sistema não aplica o desconto esperado, apresentando um comportamento incorreto ao usuário.

Dessa forma, a ISTQB descreve a relação causal entre esses conceitos como:

> **Erro → Defeito/Bug → Falha**

## Tipos de Teste

A ISTQB classifica os testes de software em diferentes **tipos de teste**, de acordo com o objetivo da avaliação realizada sobre o sistema.

Os **testes funcionais** verificam se o software atende aos requisitos funcionais especificados, validando entradas, processamento e saídas esperadas. Os **testes não funcionais** avaliam atributos de qualidade, como desempenho, usabilidade, confiabilidade e segurança.

O **teste de regressão** tem como objetivo assegurar que alterações no software não introduzam defeitos em funcionalidades já existentes. O **teste exploratório** combina aprendizado, projeto e execução de testes de forma simultânea, sendo guiado pela experiência do testador.

- **Exemplo:**
  
  Em um sistema de login:
  - **Funcional**: verificar se o usuário consegue acessar com credenciais válidas.
  - **Não funcional**: avaliar o tempo de resposta do login.
  - **Regressão**: garantir que mudanças no cadastro não afetem o login.
  - **Exploratório**: explorar comportamentos inesperados com dados inválidos.

---

## Níveis de Teste

Os **níveis de teste** definem em qual etapa do desenvolvimento o software é avaliado, considerando o grau de integração dos componentes.

O **teste unitário** verifica unidades individuais do software de forma isolada. O **teste de integração** avalia a interação entre componentes integrados. O **teste de sistema** valida o sistema completo em relação aos requisitos especificados. O **teste de aceitação** confirma se o sistema atende às necessidades do negócio e aos critérios definidos pelos usuários.

- **Exemplo:**
  
  Em um sistema de compras:
  - **Unitário**: testar o cálculo do frete.
  - **Integração**: validar a comunicação entre carrinho e pagamento.
  - **Sistema**: testar o fluxo completo de compra.
  - **Aceitação**: confirmar se o sistema atende às regras do cliente.

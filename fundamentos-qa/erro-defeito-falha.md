# Erro, Defeito/Bug e Falha segundo a ISTQB

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

# Exercício – Relatório de Execução de Testes

## Contexto

Você executou testes em um sistema de login com os seguintes resultados:

- Total de casos de teste: **10**
- Testes aprovados: **7**
- Testes reprovados: **3**

### Defeitos encontrados:

1. Senha aceita com menos de 6 caracteres  
2. Mensagem incorreta para usuário inexistente  
3. Conta não bloqueia após 3 tentativas inválidas  

---

## Tarefa

👉 Monte um **relatório de execução de testes completo**, contendo:

- ID do relatório  
- Data de execução  
- Ambiente  
- Versão do sistema  
- Responsável  
- Casos executados  
- Casos aprovados  
- Casos reprovados  
- Taxa de sucesso  
- Taxa de falha  
- Defeitos encontrados  
- Observações  

---

## Desafio Extra (Opcional)

- Classifique os defeitos por **severidade** (Alta, Média, Baixa)  
- Escreva uma **conclusão recomendando ou não a liberação do sistema**

---

| Campo | Valor |
|------|-------|
| ID do relatório | RT-01 |
| Data de execução | 26/03/2026 |
| Ambiente | Homologação |
| Versão do sistema | 1.0.0 |
| Responsável | Mateus Santos |
| Casos executados | 10 |
| Casos aprovados | 7 |
| Casos reprovados | 3 |
| Taxa de sucesso | 70% |
| Taxa de falha | 30% |
| Defeitos encontrados | 1. Senha aceita com menos de 6 caracteres.<br>2. Mensagem incorreta para usuário inexistente.<br>3. Conta não bloqueia após 3 tentativas inválidas. |
| Observações | Foram identificadas falhas relacionadas à segurança no fluxo de autenticação.<br>Recomenda-se reexecução dos testes após correção dos defeitos<br>Necessário validar regras de negócio de autenticação |

### **Severidade:**

- Defeito 1: Alta
- Defeito 2: Baixa
- Defeito 3: Alta

### **Conclusão:**

Não é recomendada a liberação do sistema. Foram identificados defeitos de alta severidade relacionados à segurança, como:
  - Aceitação de senhas fracas.
  - Ausência de bloqueio após múltiplas tentativas inválidas.
Esses problemas podem comprometer a integridade e segurança dos dados dos usuários.
A liberação deve ocorrer somente após a correção dos defeitos críticos e nova validação dos testes.

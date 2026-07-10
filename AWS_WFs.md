# ☁️ Laboratório AWS Step Functions - Orquestração de Workflows

> Implementação de workflows automatizados utilizando **AWS Step Functions**, explorando a orquestração de serviços da AWS para criação de processos escaláveis, resilientes e orientados a eventos.

---

# 📖 Sobre o Projeto

Este repositório foi desenvolvido como parte do laboratório da **DIO (Digital Innovation One)** com o objetivo de consolidar os conhecimentos sobre o **AWS Step Functions**.

Durante o laboratório, foi possível compreender como criar e gerenciar **workflows automatizados**, coordenando a execução de múltiplos serviços da AWS de forma visual e controlada. O Step Functions permite definir fluxos de trabalho utilizando máquinas de estado (*State Machines*), facilitando a implementação de processos complexos sem a necessidade de gerenciar toda a lógica de orquestração na aplicação.

Além da implementação prática, este repositório reúne anotações, exemplos e aprendizados adquiridos durante o desafio, servindo como material de apoio para estudos futuros.

---

# 🎯 Objetivos

* Compreender o funcionamento do AWS Step Functions.
* Conhecer o conceito de máquinas de estado (*State Machines*).
* Criar workflows automatizados.
* Integrar diferentes serviços da AWS em um único fluxo.
* Entender como tratar falhas, exceções e retentativas.
* Documentar os conhecimentos adquiridos durante o laboratório.

---

# 🛠 Tecnologias Utilizadas

* AWS Step Functions
* AWS Lambda
* Amazon CloudWatch
* AWS IAM
* Amazon EventBridge *(quando aplicável)*
* Amazon S3 *(quando aplicável)*
* Amazon DynamoDB *(quando aplicável)*
* JSON (Amazon States Language)
* Git
* GitHub

---

# 📚 O que é o AWS Step Functions?

O **AWS Step Functions** é um serviço de orquestração que permite coordenar diferentes serviços da AWS por meio de **workflows baseados em máquinas de estado**.

Esses workflows são definidos utilizando a **Amazon States Language (ASL)**, um formato baseado em JSON que descreve cada etapa do processo e as transições entre elas.

Com o Step Functions é possível:

* Automatizar processos.
* Orquestrar funções AWS Lambda.
* Integrar diversos serviços da AWS.
* Implementar fluxos de aprovação.
* Criar pipelines de processamento.
* Tratar falhas automaticamente.

---

# 🏗 Conceitos Fundamentais

## State Machine

É o workflow completo que representa o processo automatizado.

Ela contém todas as etapas da execução e define como cada estado se conecta ao próximo.

---

## States

Cada etapa do workflow é chamada de **State**.

Os principais tipos são:

| Tipo     | Finalidade                                  |
| -------- | ------------------------------------------- |
| Task     | Executa uma ação (Lambda, ECS, Batch, etc.) |
| Choice   | Realiza decisões condicionais               |
| Pass     | Apenas encaminha dados                      |
| Wait     | Aguarda um tempo determinado                |
| Parallel | Executa fluxos simultaneamente              |
| Map      | Processa listas de itens                    |
| Succeed  | Finaliza o workflow com sucesso             |
| Fail     | Finaliza o workflow indicando erro          |

---

## Execução

Cada vez que um workflow é iniciado, o Step Functions cria uma nova **Execution**, responsável por acompanhar todo o fluxo até sua conclusão.

---

# 📂 Estrutura do Repositório

```text
.
├── README.md
├── state-machines/
│   └── workflow.json
├── lambda/
│   └── lambda_function.py
├── imagens/
│   ├── arquitetura.png
│   └── workflow.png
├── anotacoes/
│   └── observacoes.md
└── exemplos/
    └── input.json
```

---

# 🚀 Etapas Realizadas

Durante o laboratório foram executadas as seguintes atividades:

1. Criação da State Machine.
2. Definição dos estados do workflow.
3. Configuração das transições entre estados.
4. Integração com serviços AWS.
5. Execução do workflow.
6. Simulação de cenários de sucesso e erro.
7. Monitoramento da execução utilizando CloudWatch.
8. Validação dos resultados.

---

# 🔄 Fluxo de Funcionamento

```text
Evento Inicial
      │
      ▼
State Machine
      │
      ▼
Task
      │
      ▼
Choice
 ┌──────────────┐
 │              │
 ▼              ▼
Sucesso      Tratamento de Erro
 │              │
 ▼              ▼
Próxima      Retry / Catch
Etapa            │
 │               ▼
 └───────────────┘
        │
        ▼
Workflow Finalizado
```

---

# 📄 Exemplo de State Machine

```json
{
  "Comment": "Exemplo de Workflow",
  "StartAt": "ProcessarPedido",
  "States": {
    "ProcessarPedido": {
      "Type": "Task",
      "Resource": "arn:aws:lambda:REGIAO:CONTA:function:MinhaFuncao",
      "End": true
    }
  }
}
```

---

# 💡 Aprendizados

Durante este laboratório foi possível compreender:

* Como modelar workflows utilizando máquinas de estado.
* Como integrar diferentes serviços da AWS.
* Como implementar decisões utilizando estados **Choice**.
* Como tratar exceções utilizando **Retry** e **Catch**.
* Como monitorar execuções utilizando o CloudWatch.
* A importância da automação de processos na arquitetura em nuvem.

---

# 📈 Benefícios do AWS Step Functions

* Orquestração visual de processos.
* Escalabilidade automática.
* Alta disponibilidade.
* Integração nativa com diversos serviços da AWS.
* Monitoramento completo das execuções.
* Tratamento automático de falhas.
* Redução da complexidade do código da aplicação.

---

# 🔐 Boas Práticas

* Criar workflows pequenos e reutilizáveis.
* Utilizar nomes descritivos para estados.
* Implementar tratamento de exceções com **Retry** e **Catch**.
* Monitorar execuções utilizando CloudWatch.
* Utilizar permissões mínimas através do IAM.
* Evitar lógica excessivamente complexa em uma única State Machine.
* Documentar o fluxo de execução.

---

# 📌 Casos de Uso

O AWS Step Functions é amplamente utilizado para:

* Processamento de pedidos.
* Aprovação de documentos.
* Automação de processos corporativos.
* Pipelines de ETL.
* Integração entre microsserviços.
* Processamento de arquivos.
* Orquestração de funções AWS Lambda.
* Fluxos de Machine Learning.

---

# 📚 Conclusão

O AWS Step Functions simplifica a criação de workflows automatizados ao permitir a orquestração de diferentes serviços da AWS por meio de máquinas de estado. Sua abordagem visual facilita a compreensão dos processos, melhora a manutenção da solução e reduz a complexidade do código.

Este laboratório proporcionou uma visão prática sobre automação e orquestração de serviços na AWS, reforçando conceitos importantes para o desenvolvimento de arquiteturas escaláveis, resilientes e orientadas a eventos.

---

# 📖 Referências

* AWS Step Functions Documentation
* Amazon States Language Specification
* AWS Well-Architected Framework
* AWS Step Functions Developer Guide

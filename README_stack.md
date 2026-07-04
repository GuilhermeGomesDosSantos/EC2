# ☁️ Laboratório AWS CloudFormation - Primeira Stack

> Implementação da primeira **Stack** utilizando o **AWS CloudFormation**, com o objetivo de compreender os conceitos de Infraestrutura como Código (Infrastructure as Code - IaC) na AWS.

---

## 📖 Sobre o Projeto

Este repositório foi criado para documentar a implementação de uma **Stack** utilizando o **AWS CloudFormation**.

O laboratório faz parte do processo de aprendizagem em computação em nuvem e tem como objetivo apresentar os conceitos básicos de **Infraestrutura como Código (IaC)**, permitindo automatizar a criação e o gerenciamento de recursos da AWS por meio de arquivos declarativos.

Além da implementação prática, este repositório serve como material de consulta para futuras implementações e estudos.

---

## 🎯 Objetivos

* Compreender o conceito de **Infrastructure as Code (IaC)**.
* Aprender a criar uma Stack utilizando o AWS CloudFormation.
* Automatizar a criação de recursos na AWS.
* Entender o ciclo de vida de uma Stack.
* Documentar o processo de criação e os aprendizados obtidos durante o laboratório.

---

## 🛠 Tecnologias Utilizadas

* AWS CloudFormation
* AWS Management Console
* YAML
* Git
* GitHub

---

## 📚 O que é o AWS CloudFormation?

O **AWS CloudFormation** é um serviço que permite criar, provisionar e gerenciar recursos da AWS utilizando arquivos de configuração em formato **YAML** ou **JSON**.

Esses arquivos, chamados de **templates**, descrevem toda a infraestrutura necessária para uma aplicação, permitindo que ela seja criada de forma automática, repetível e padronizada.

Entre os benefícios do CloudFormation estão:

* Automação da infraestrutura;
* Padronização dos ambientes;
* Versionamento da infraestrutura;
* Redução de erros manuais;
* Facilidade para replicar ambientes.

---

## 📂 Estrutura do Repositório

```text
.
├── README.md
├── templates/
│   └── primeira-stack.yaml
├── imagens/
│   ├── stack-criada.png
│   └── recursos.png
└── anotacoes/
    └── observacoes.md
```

---

## 🚀 Etapas do Laboratório

Durante o laboratório foram realizadas as seguintes etapas:

1. Criação de um template CloudFormation.
2. Definição dos recursos da infraestrutura.
3. Validação do template.
4. Criação da Stack.
5. Acompanhamento da criação dos recursos.
6. Verificação dos recursos provisionados.
7. Atualização da Stack (quando necessário).
8. Exclusão da Stack para evitar custos desnecessários.

---

## 📄 Estrutura Básica de um Template

Um template CloudFormation geralmente é composto pelas seguintes seções:

| Seção                    | Descrição                                      |
| ------------------------ | ---------------------------------------------- |
| AWSTemplateFormatVersion | Versão do template                             |
| Description              | Descrição da Stack                             |
| Parameters               | Parâmetros de entrada                          |
| Resources                | Recursos que serão criados                     |
| Outputs                  | Informações retornadas após a criação da Stack |

Exemplo:

```yaml
AWSTemplateFormatVersion: "2010-09-09"

Description: Minha primeira Stack

Resources:

  MeuBucket:
    Type: AWS::S3::Bucket
```

---

## 💡 Aprendizados

Durante este laboratório foi possível compreender:

* O funcionamento do AWS CloudFormation.
* A importância da Infraestrutura como Código (IaC).
* Como organizar recursos utilizando templates.
* O ciclo de vida de uma Stack.
* Como reduzir configurações manuais utilizando automação.
* A facilidade de replicar ambientes por meio de templates reutilizáveis.

---

## ✅ Boas Práticas

* Utilizar templates em formato YAML para facilitar a leitura.
* Organizar templates em diretórios específicos.
* Versionar os templates utilizando Git.
* Documentar cada recurso criado.
* Validar o template antes da criação da Stack.
* Excluir recursos que não serão mais utilizados para evitar cobranças.

---

## 📌 Conclusão

A utilização do AWS CloudFormation simplifica o gerenciamento de infraestrutura na nuvem ao permitir que recursos sejam definidos como código. Essa abordagem proporciona maior padronização, escalabilidade e facilidade na manutenção dos ambientes, tornando o processo de provisionamento mais eficiente e confiável.

Este laboratório foi essencial para compreender os fundamentos da automação de infraestrutura na AWS e servirá como base para estudos mais avançados envolvendo arquiteturas em nuvem e práticas de DevOps.

---

## 📖 Referências

* Documentação Oficial da AWS CloudFormation
* Guia do AWS CloudFormation User Guide
* AWS Well-Architected Framework

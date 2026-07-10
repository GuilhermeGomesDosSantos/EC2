# ☁️ Laboratório AWS CloudFormation - Infraestrutura como Código (IaC)

> Implementação de uma infraestrutura automatizada utilizando **AWS CloudFormation**, aplicando os conceitos de **Infrastructure as Code (IaC)** para provisionamento e gerenciamento de recursos na AWS.

---

# 📖 Sobre o Projeto

Este repositório foi desenvolvido como parte do laboratório da **DIO (Digital Innovation One)** com o objetivo de consolidar os conhecimentos sobre o **AWS CloudFormation** e a automação de infraestrutura na nuvem.

Durante o laboratório, foi possível criar e gerenciar recursos da AWS por meio de **templates declarativos**, eliminando configurações manuais e tornando o processo de provisionamento mais rápido, padronizado e reproduzível.

Além da implementação prática, este repositório reúne anotações, exemplos e aprendizados obtidos ao longo do desafio, servindo como material de consulta para estudos futuros.

---

# 🎯 Objetivos

* Compreender o conceito de **Infrastructure as Code (IaC)**.
* Conhecer o funcionamento do AWS CloudFormation.
* Criar e gerenciar uma Stack na AWS.
* Automatizar o provisionamento de recursos utilizando templates.
* Entender o ciclo de vida de uma Stack.
* Documentar os aprendizados adquiridos durante o laboratório.

---

# 🛠 Tecnologias Utilizadas

* AWS CloudFormation
* AWS Management Console
* YAML
* AWS IAM
* Git
* GitHub

---

# 📚 O que é o AWS CloudFormation?

O **AWS CloudFormation** é um serviço da AWS que permite criar, atualizar e excluir recursos da nuvem utilizando arquivos de configuração chamados **templates**.

Esses templates descrevem toda a infraestrutura da aplicação em formato **YAML** ou **JSON**, permitindo que ambientes sejam criados de forma automatizada e consistente.

Entre os principais benefícios estão:

* Automação da infraestrutura;
* Padronização dos ambientes;
* Versionamento dos templates;
* Reutilização de configurações;
* Redução de erros manuais;
* Facilidade para replicar ambientes.

---

# 🏗 Conceitos Fundamentais

## Template

Arquivo responsável por definir toda a infraestrutura que será criada.

Pode ser escrito em:

* YAML
* JSON

---

## Stack

Uma **Stack** representa o conjunto de recursos criados a partir de um template CloudFormation.

Exemplos de recursos:

* Amazon EC2
* Amazon S3
* Amazon VPC
* Amazon RDS
* Security Groups
* IAM Roles

---

## Change Set

Permite visualizar as alterações que serão realizadas antes da atualização de uma Stack, reduzindo riscos durante modificações na infraestrutura.

---

# 📂 Estrutura do Repositório

```text
.
├── README.md
├── templates/
│   ├── infrastructure.yaml
│   └── parameters.yaml
├── imagens/
│   ├── stack.png
│   └── arquitetura.png
├── anotacoes/
│   └── observacoes.md
└── exemplos/
    └── template-exemplo.yaml
```

---

# 🚀 Etapas Realizadas

Durante o laboratório foram executadas as seguintes atividades:

1. Criação do template CloudFormation.
2. Definição dos recursos da infraestrutura.
3. Validação do template.
4. Criação da Stack.
5. Provisionamento automático dos recursos.
6. Verificação do status da Stack.
7. Atualização da infraestrutura utilizando o mesmo template.
8. Exclusão da Stack para evitar custos desnecessários.

---

# ⚙ Estrutura Básica de um Template

Um template CloudFormation normalmente possui as seguintes seções:

| Seção                    | Descrição                                      |
| ------------------------ | ---------------------------------------------- |
| AWSTemplateFormatVersion | Versão do template                             |
| Description              | Descrição da infraestrutura                    |
| Parameters               | Valores fornecidos pelo usuário                |
| Resources                | Recursos que serão criados                     |
| Outputs                  | Informações retornadas após a criação da Stack |

Exemplo:

```yaml
AWSTemplateFormatVersion: '2010-09-09'

Description: Exemplo de Stack utilizando CloudFormation

Resources:

  MeuBucket:
    Type: AWS::S3::Bucket
```

---

# 🔄 Fluxo de Funcionamento

```text
Template (YAML/JSON)
        │
        ▼
AWS CloudFormation
        │
        ▼
Criação da Stack
        │
        ▼
Provisionamento dos Recursos
        │
        ▼
Infraestrutura Disponível
```

---

# 💡 Aprendizados

Durante este laboratório foi possível compreender:

* Como funciona o conceito de Infrastructure as Code (IaC).
* Como criar templates reutilizáveis.
* Como provisionar recursos automaticamente.
* Como atualizar uma infraestrutura sem recriá-la manualmente.
* A importância do versionamento dos templates.
* Como reduzir erros operacionais utilizando automação.

---

# 📈 Benefícios do AWS CloudFormation

* Provisionamento automatizado.
* Padronização dos ambientes.
* Reprodutibilidade da infraestrutura.
* Facilidade para atualização dos recursos.
* Controle de mudanças através de templates versionados.
* Integração com diversos serviços da AWS.

---

# 🔐 Boas Práticas

* Utilizar templates em formato YAML para melhorar a legibilidade.
* Organizar templates em diretórios específicos.
* Utilizar parâmetros para tornar os templates reutilizáveis.
* Validar o template antes da criação da Stack.
* Documentar todos os recursos provisionados.
* Versionar os templates utilizando Git.
* Excluir recursos não utilizados para evitar cobranças.

---

# 📌 Casos de Uso

O AWS CloudFormation pode ser utilizado para automatizar a criação de:

* Infraestruturas completas na AWS.
* Ambientes de desenvolvimento, homologação e produção.
* Redes (VPC, Subnets e Security Groups).
* Servidores EC2.
* Buckets S3.
* Bancos de dados Amazon RDS.
* Funções AWS Lambda.
* Arquiteturas escaláveis e padronizadas.

---

# 📚 Conclusão

O AWS CloudFormation é uma das principais ferramentas da AWS para implementação de **Infrastructure as Code (IaC)**. Sua utilização permite criar, atualizar e gerenciar ambientes de forma automatizada, garantindo maior consistência, escalabilidade e segurança.

Este laboratório proporcionou uma visão prática sobre como automatizar o provisionamento de infraestrutura utilizando templates, reduzindo atividades manuais e facilitando a replicação de ambientes em diferentes cenários.

Os conhecimentos adquiridos servirão como base para estudos mais avançados envolvendo automação, DevOps e arquitetura em nuvem.

---

# 📖 Referências

* AWS CloudFormation Documentation
* AWS CloudFormation User Guide
* AWS Well-Architected Framework
* AWS Infrastructure as Code (IaC) Best Practices

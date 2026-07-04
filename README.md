# Amazon EC2 (Elastic Compute Cloud)

## 📖 Visão Geral

O **Amazon EC2 (Elastic Compute Cloud)** é um serviço da Amazon Web Services (AWS) que permite criar e gerenciar servidores virtuais na nuvem. Ele fornece capacidade computacional escalável, possibilitando que empresas e desenvolvedores executem aplicações sem a necessidade de investir em infraestrutura física.

Com o EC2, é possível criar instâncias sob demanda, configurar sistemas operacionais, instalar aplicações e ajustar recursos computacionais conforme a necessidade.

---

# 🚀 Principais Características

* Escalabilidade sob demanda.
* Pagamento baseado no consumo (*Pay-as-you-go*).
* Suporte a diversos sistemas operacionais (Linux, Windows, entre outros).
* Diversos tipos de instâncias para diferentes cargas de trabalho.
* Integração com outros serviços da AWS.
* Alta disponibilidade utilizando múltiplas Zonas de Disponibilidade (Availability Zones).

---

# 🏗️ Componentes do EC2

## Instâncias

Uma instância representa uma máquina virtual executada na infraestrutura da AWS.

Cada instância possui:

* CPU
* Memória RAM
* Armazenamento
* Interface de rede

---

## Amazon Machine Image (AMI)

A **AMI** é um modelo utilizado para criar novas instâncias.

Ela contém:

* Sistema operacional
* Aplicações pré-instaladas
* Configurações
* Permissões

Tipos comuns:

* Amazon Linux
* Ubuntu
* Red Hat
* Windows Server
* AMIs personalizadas

---

## Tipos de Instâncias

A AWS oferece diferentes famílias de instâncias.

| Família | Utilização                       |
| ------- | -------------------------------- |
| T       | Uso geral e baixo custo          |
| M       | Uso geral balanceado             |
| C       | Otimizada para processamento     |
| R       | Otimizada para memória           |
| P       | GPU para Machine Learning        |
| G       | Processamento gráfico            |
| I       | Alto desempenho de armazenamento |

Exemplo:

* t3.micro
* t3.small
* m5.large
* c6i.large

---

# 💾 Armazenamento

O EC2 pode utilizar diferentes tipos de armazenamento.

## Amazon EBS (Elastic Block Store)

Volumes persistentes.

Características:

* Dados permanecem mesmo após reinicialização.
* Snapshots.
* Criptografia.
* Alto desempenho.

---

## Instance Store

Armazenamento temporário.

Características:

* Muito rápido.
* Dados são perdidos caso a instância seja interrompida.

---

# 🔒 Segurança

## Security Groups

Funcionam como um firewall da instância.

Permitem controlar:

* Portas abertas
* Protocolos
* Endereços IP autorizados

Exemplo:

| Porta | Serviço |
| ----- | ------- |
| 22    | SSH     |
| 80    | HTTP    |
| 443   | HTTPS   |
| 3389  | RDP     |

---

## Key Pair

Para acessar instâncias Linux utiliza-se um par de chaves:

* Chave Pública
* Chave Privada (.pem)

Exemplo de acesso:

```bash
ssh -i minha-chave.pem ec2-user@IP_PUBLICO
```

---

# 🌐 Rede

As instâncias são executadas dentro de uma **VPC (Virtual Private Cloud)**.

Principais componentes:

* VPC
* Subnets
* Internet Gateway
* Route Tables
* Elastic IP
* Network ACL

---

# 📈 Escalabilidade

O EC2 suporta escalabilidade automática.

## Auto Scaling

Permite aumentar ou diminuir automaticamente o número de instâncias com base em métricas como:

* CPU
* Memória
* Tráfego de rede

Benefícios:

* Economia
* Alta disponibilidade
* Melhor desempenho

---

# ⚖️ Balanceamento de Carga

O **Elastic Load Balancer (ELB)** distribui requisições entre várias instâncias.

Tipos:

* Application Load Balancer (ALB)
* Network Load Balancer (NLB)
* Gateway Load Balancer (GWLB)

---

# 💰 Modelos de Cobrança

## On-Demand

Pagamento apenas pelo tempo utilizado.

Ideal para:

* Testes
* Desenvolvimento
* Aplicações temporárias

---

## Reserved Instances

Desconto mediante compromisso de uso.

Ideal para:

* Ambientes estáveis
* Produção

---

## Spot Instances

Utilizam capacidade ociosa da AWS.

Vantagens:

* Até 90% de desconto.

Desvantagem:

* A instância pode ser interrompida pela AWS.

---

## Savings Plans

Modelo flexível de economia para utilização contínua.

---

# 🛠️ Criando uma Instância EC2

1. Acesse o Console da AWS.
2. Navegue até **EC2**.
3. Clique em **Launch Instance**.
4. Defina um nome para a instância.
5. Escolha uma AMI.
6. Selecione o tipo de instância.
7. Configure um Key Pair.
8. Defina as regras do Security Group.
9. Configure o armazenamento.
10. Clique em **Launch Instance**.

---

# 📊 Monitoramento

O Amazon CloudWatch permite monitorar:

* Utilização de CPU
* Uso de memória (com agente)
* Tráfego de rede
* Disco
* Alarmes
* Logs

---

# 🔄 Backup

O backup pode ser realizado através de:

* Snapshots do EBS
* AMIs personalizadas
* AWS Backup

---

# 🏆 Boas Práticas

* Utilize o princípio do menor privilégio (IAM).
* Evite utilizar a conta root.
* Mantenha as instâncias atualizadas.
* Utilize Security Groups restritivos.
* Habilite criptografia em volumes EBS.
* Faça backups periódicos.
* Utilize Auto Scaling para aplicações críticas.
* Monitore recursos utilizando CloudWatch.
* Armazene credenciais utilizando AWS Secrets Manager ou Systems Manager Parameter Store.

---

# 📌 Casos de Uso

* Hospedagem de sites.
* APIs REST.
* Aplicações corporativas.
* Bancos de dados.
* Ambientes de desenvolvimento.
* Machine Learning.
* Containers.
* Servidores de jogos.
* Aplicações Big Data.

---

# ✅ Vantagens

* Escalabilidade.
* Alta disponibilidade.
* Flexibilidade.
* Integração com diversos serviços AWS.
* Diversos modelos de cobrança.
* Segurança robusta.
* Fácil gerenciamento.

---

# ⚠️ Desvantagens

* Custos podem aumentar caso não haja monitoramento.
* Exige conhecimento sobre redes e segurança.
* Instâncias Spot podem ser interrompidas.
* Configurações inadequadas podem expor recursos à Internet.

---

# 📚 Conclusão

O Amazon EC2 é um dos serviços centrais da AWS para computação em nuvem, permitindo criar ambientes altamente escaláveis, seguros e flexíveis. Sua integração com serviços como VPC, EBS, IAM, CloudWatch e Auto Scaling possibilita a construção de arquiteturas robustas para aplicações de diferentes portes, desde pequenos projetos até sistemas corporativos de missão crítica.

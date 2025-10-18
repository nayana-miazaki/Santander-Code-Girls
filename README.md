<h1> Conceitos Fundamentais AWS </h1>

---

# Introdução à AWS ▶️

A Amazon Web Services, lançada em 2006, é uma plataforma de nuvem robusta,
escalável e segura que oferece mais de 200 serviços gerenciados em todo o
mundo.

---

# Regions e Availability Zones 🗺️
- `Regions`: áreas geográficas que contêm várias Availability Zones e são 
isoladas umas das outras para garantir maior tolerância a falhas.
- `Availability Zones`: datacenters fisicamente separados mas logicamente
conectados, que garantem alta disponibilidade.

---

# Serviços Principais 🔨
1. **Amazon EC2 (Elastic Compute Cloud)**
O EC2 fornece máquinas virtuais na nuvem da AWS, funcionando como um serviço
tipo IaaS (Infraestrutura como Serviço) <br>
`Composição`: CPU, memória, disco, rede, sistema operacional <br>
`Tipos de instâncias`: General Purpose, Compute Optimised, Memory Optimised,
Accelerated Computing e Storage Optimised <br>

    **Valores:**
   - Sob demanda: ideal para cargas de trabalho irregulares e de curto prazo 
   com pagamento por hora.
   - Instâncias reservadas: geralmente mais baratas que as sob demanda, mas
   exigem um pagamento de uso anual.
   - Instâncias SPOT: oferecem desconto de até 90% em instâncias sob demanda,
   mas podem ser encerradas pela AWS a qualquer momento com um aviso de dois
   minutos.

2. **Amazon S3 (Simple Storage Service)**
O S3 é um serviço de armazenamento de objetos seguro e escalável, ideal para
armazenar, organizar e recuperar grandes volumes de dados. 

   **Classes de armazenamento**
   - `S3 Standard`: para dados de acesso frequente.
   - `S3 Intelligent-Tiering`: otimiza custos automaticamente movendo dados
   entre classes de acesso frequente e não frequente.
   - `S3 Standard-IA`: para dados que são acessados com menos frequência.
   - `S3 One Zone-IA`: para dados que são acessados com menos frequência e 
   não requerem disponibilidade de várias Availability Zones.
   - `S3 Glacier & Glacier Deep Archive`: para arquivamento de dados a longo
   prazo, com os menores custos de armazenamento.

3. **Amazon EBS (Elastic Block Store)**
O EBS oferece volumes de armazenamento de bloco que podem ser anexados à 
instâncias EC2 funcionando como um HD externo para a sua máquina virtual.
- Armazenamento para bancos de dados: `MySQL`, `PostgreSQL`, `Oracle`, etc.
- Armazenamento de dados para aplicativos web e logs de sistema.

---
# Otimização de Recursos ✅
Otimizar recursos na AWS significa poupar custos.

- **Desligar instâncias não utilizadas:** em ambientes de desenvolvimento e
teste, desligar instâncias durante a noite ou nos fins de semana.
- **Remover recursos ociosos:** recursos parados em seu ambiente continuam
gerando custos.
- **Escalar recursos:** aumentar ou diminuir a capacidade dos recursos para
processar cargas de trabalho específicas.
   - `Escala Vertical`: aumentar a capacidade de um único recurso.
   - `Escala Horizontal`: aumentar o número de recursos.
---

# AWS Lambda 🛠️
Tecnologia serverless onde os desenvolvedores não precisam se preocupar em
gerenciar servidores.

Principais Benefícios:
- `pagamento por requisição`: a cobrança é feita apenas quando o código é
executado.
- `integração`: com diversos serviços AWS e suporta várias linguagens de
programação
- `sem gerenciamento de servidores`: a AWS é responsável pelo gerenciamento,
liberando para o desenvolvedor focar apenas no código.

# Módulo de Redes na AWS ⚙️
## Amazon VPC (Virtual Private Cloud)
Permite o provisionamento de uma rede lógica isolada na AWS. A VPC é 
comparável a uma rede de datacenter tradicional mas com a escalabilidade
em nuvem. 

## Amazon Subnet
É uma subdivisão da VPC, sendo uma gama de endereços IP onde os recursos
AWS são criados (instâncias EC2). Cada sub-rede reside em uma únida Zona
de Disponiblidade e pode ser pública ou privada. São nelas que os Security 
Groups são criados.

## Amazon Security Group
Funciona como um firewall virtual para as instâncias EC2, controlando 
o tráfego de entrada e saída. Permite habilitar regras e portas para 
acessos específicos, como SSH e RDP.

## Amazon Route 53
Serviço de Sistema de Nomes de Domínio (DNS) que converte nomes de 
domínio em endereços IP. Ele é fundamental para registro e 
transferência de domínios.

## Amazon CloudFront
Um serviço de Content Delivery Network (CDN) que distribui conteúdo 
globalmente a partir de Edge Locations, garantindo baixa latência 
para o usuário final, independentemente de sua localização.

## Amazon Elastic Load Balancer (ELB)
Distribui o tráfego de forma eficiente e automática para um grupo 
de servidores, aumentando a velocidade e o desempenho das aplicações.

## Amazon RDS (Relational Database Service)
Serviço de banco de dados relacional gerenciado que simplifica as 
tarefas de configuração, operação e escalabilidade.

* **Mecanismos Suportados:** Amazon Aurora, SQL Server, MySQL, 
PostgreSQL, MariaDB e Oracle.
* **Benefícios:** Fácil de gerenciar, automação de backups e 
patches, rápida implantação.

## Amazon DynamoDB
Um banco de dados NoSQL totalmente gerenciado. É altamente 
escalável e focado em fornecer baixa latência e desempenho 
consistente para aplicativos que trabalham com dados não 
estruturados ou semiestruturados (ex: Netflix, Airbnb).

### Estratégias de Backup e Recuperação de Dados

O backup é essencial para garantir a continuidade dos negócios 
e reduzir o risco de perda de dados. <br> 
As estratégias na AWS envolvem:

1.  **Backups Automatizados:** Snapshots e logs de transação.
2.  **Replicação:** Copiar dados para outras Regiões/AZs.
3.  **Segurança:** Uso de criptografia (em trânsito e em repouso) 
e políticas IAM para controlar o acesso.

--- 

# Github 🗂️

| **Elemento** |                 **Sintaxe (Comando)**                 | 
|:-----------|:-----------------------------------------------------:|
| Cabeçalhos       |          # Título 1 ## Título 2 ### Título 3          |
| Negrito       |                **texto** ou __texto__                 |
| Itálico       |                  *texto* ou _texto_                   |
| Negrito e Itálico       |                      ***texto***                      |
| Tachado       |                       ~~texto~~                       |
| Citação em Bloco       |             > Este é um bloco de citação.             |
| Linha Horizontal       |       *** ou --- ou ___ (em uma linha separada)       |
| Links       |                 [Texto do Link](URL)                  |
| Imagens       |          ![Texto Alternativo](URL da Imagem)          |
| Listas Não Ordenadas       |                   * Item 1 - Item 2                   |
| Listas Ordenadas       |           1. Primeiro item 2. Segundo item            |
| Bloco de Código       |                ```linguagem código ```                |
| Código em Linha       |                       `código`                        |
| Quebra de Linha       | Adicionar dois espaços no final da linha ou usar <br> |
|   Listas de Tarefas  |       - [ ] Fazer algo - [x] Fazer outra coisa        |




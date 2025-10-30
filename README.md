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

# 🚀 Stack na AWS: CloudFormation Essentials

## 💡 CloudFormation: Primeiros Insights
| **Seção do CFN** | **Aprendizado**                                                                                                   | Anotação                                                                                                                 |
|:----------------|:------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| `Parameters`    | Permite tornar o template reutilizável, definindo valores que podem ser passados na criação/atualização da Stack. | Sempre use Type e Default. Use `NoEcho`: true para dados sensíveis como senhas.                                          |
| `Resources`     | É a única seção obrigatória. Define todos os recursos da AWS que serão criados                                    | O nome lógico do recurso (VPCPrincipal, WebSecurityGroup) deve ser exclusivo no template.                       |
|  `Outputs`  | Permite exportar valores dos recursos criados para serem usados em outras Stacks.                                 | Para usar em outras Stacks, use a função `Export: Name: [NomeDaExportacao]` e importe com `Fn::ImportValue`. |
|  `Mappings` | Útil para valores condicionais, como determinar o AMI ID correto baseado na região da AWS.                        |  Simplifica muito a lógica de `Region` e `InstanceType` sem usar muitas condições.    |

## 🛠️ Desafios e Soluções

| **Desafio Encontrado** | **Causa Raiz**                                                                                                      | **Solução**                                                             |
|:----------------|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| **ROLLBACK_COMPLETE (Stack falhou e reverteu)**    | O Security Group estava tentando referenciar uma VPC que ainda não havia sido criada.| Adicionei a propriedade DependsOn: VPCPrincipal no recurso AWS::EC2::SecurityGroup      |
|  **User data is too long**  |  Meu script de bootstrapping (UserData) para a EC2 estava muito extenso.  | Movi o script complexo para um S3 Bucket e fiz o UserData apenas baixar e executar esse script. |
|  **Atualização Impossível** | Tentei modificar uma propriedade do recurso (ex: o CidrBlock da VPC) que requer substituição (Replacement). | Algumas modificações no CFN não são atualizações, e sim a criação de um novo recurso e a exclusão do antigo. Isso causa downtime.  |

## 🔑 Segurança e Boas Práticas
1. IAM Roles e Instance Profiles
Sempre use **IAM Roles** com o conceito de menor privilégio para atribuir permissões à EC2, 
nunca use chaves de acesso no `UserData`.
 Para EC2, a Role deve ser associada via `AWS::IAM::InstanceProfile`.

2. `DeletionPolicy`
Utilizar o `DeletionPolicy: Retain` no meu Amazon S3 Bucket e no DynamoDB Table (se aplicável) 
para garantir que os dados não sejam excluídos se a Stack for deletada.

3. Ambiente de Desenvolvimento vs. Produção

Criar Tags nos recursos para facilitar a identificação e o gerenciamento de custos.

# Automação Assíncrona com S3 e AWS Lambda
A Automação Assíncrona com S3 e AWS Lambda funciona como um sistema de processamento
de eventos, onde o upload de um arquivo aciona automaticamente um código para 
trabalhar com ele, sem a necessidade de servidores contínuos.

**Fluxo de trabalho:** <br>

1. Um novo arquivo (objeto) é carregado em um Bucket do Amazon S3;
2. O S3 envia um evento de notificação para o AWS Lambda; 
3. A Função Lambda é executada, processando o novo arquivo
(ex: validação, transformação, ingestão de dados).

O CloudFormation garante que o Bucket, a Função Lambda, as permissões de execução 
(IAM Role) e a conexão do gatilho (Trigger) sejam provisionados de forma coesa e 
repetida.

**Vantagens:**
1. `Serveless`: O AWS Lambda escala automaticamente e você paga apenas pelo 
tempo de computação usado.
2. `Escalabilidade Elástica`: Milhares de arquivos podem ser carregados no 
S3 simultaneamente, e a Lambda criará instâncias paralelas da sua função 
para processar todos eles ao mesmo tempo.
3. `Baixa Latência`: O processamento começa quase instantaneamente após o 
upload, garantindo que o tempo de resposta do sistema seja rápido.
4. `Separação de Preocupações`: O S3 cuida de forma eficiente do 
armazenamento e a Lambda cuida da computação, cada serviço fazendo o que faz de melhor.

# ☁️ AWS CloudFormation

## O que é AWS CloudFormation?
O AWS CloudFormation é o serviço de Infraestrutura como Código (IaC) da AWS. 
Ele permite que você modele, provisione e gerencie recursos da AWS de forma segura, 
previsível e automatizada, tratando a infraestrutura como código versionado.

| **Conceito** | **Descrição** |
|--------------|---------------|
| Template     | Um arquivo de texto (YAML ou JSON) que descreve exatamente quais recursos da AWS você deseja provisionar (ex: uma VPC, um S3 Bucket, uma instância EC2). É a planta da sua infraestrutura.              |
| Stack        | A unidade de deployment. Uma Stack é a instância em execução de um Template. Quando você executa um Template, o CloudFormation cria uma Stack que contém todos os recursos definidos.              |
| Parameters   | Variáveis de entrada que permitem reutilizar o mesmo Template em diferentes ambientes ou regiões. (Ex: o tipo de instância EC2, a senha do banco de dados).              |
| Outputs      | Valores gerados pela Stack que podem ser referenciados por outras Stacks ou consumidos por aplicações. (Ex: o nome DNS de um Load Balancer recém-criado).              |



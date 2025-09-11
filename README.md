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

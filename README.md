# Resumo do Lab - Fundamentos da Computação em Nuvem com Microsoft Azure

## Entendendo o Desafio

Este repositório faz parte do desafio proposto pela DIO, com foco nos fundamentos da computação em nuvem utilizando a plataforma Microsoft Azure. O objetivo foi explorar os conceitos iniciais e compreender como a nuvem pode transformar a forma como empresas e desenvolvedores trabalham com tecnologia.

## O que eu aprendi

- **O que é computação em nuvem**: Aprendi que a nuvem permite acessar e gerenciar recursos de computação pela internet, com escalabilidade, segurança e alta disponibilidade.

- **Microsoft Azure**: Conheci a plataforma Azure, seus principais serviços e como criar uma conta gratuita para começar a utilizar os recursos disponíveis.

- **Modelos de Custo - OPEX vs CAPEX**:
  - **CAPEX (Capital Expenditure)**: Investimento inicial em infraestrutura física, típico de ambientes tradicionais.
  - **OPEX (Operational Expenditure)**: Custo operacional contínuo, mais comum em ambientes de nuvem, com pagamento conforme o uso.

- **Vantagens da Nuvem**:
  - Redução de custos com infraestrutura.
  - Escalabilidade sob demanda.
  - Rapidez na criação de ambientes.
  - Foco no core business, sem se preocupar com manutenção física.

- **Como criar uma conta no Azure**: Através de tutoriais e vídeos, entendi o passo a passo para registrar uma conta gratuita e começar a utilizar os serviços em nuvem da Microsoft.

## Primeiros Passos com Máquina Virtual (VM)

- Aprendi a criar uma **máquina virtual** no Azure, escolhendo o sistema operacional, região, tamanho e nome.
- Entendi o que é um **grupo de recursos**, e como ele organiza os serviços criados.
- Vi como configurar a **rede virtual** e permitir acesso remoto via RDP (Windows) ou SSH (Linux).
- Descobri como **ligar, parar e excluir** a máquina virtual pelo portal para evitar cobranças desnecessárias.
- Entendi que uma VM é como um "computador virtual" na nuvem, e pode ser usada para testes, desenvolvimento ou hospedagem de aplicações.

## Recursos Avançados de VM: SLA, Escalabilidade e Alta Disponibilidade

- **SLA (Acordo de Nível de Serviço)** define a garantia de disponibilidade fornecida pelo provedor de nuvem.
  - Exemplo: SLA de 99,9% permite até 43 minutos de indisponibilidade por mês.
  - Quanto maior o SLA, maior a confiabilidade do serviço.

- **Alta Disponibilidade**:
  - Aprendi que é possível criar VMs em **zonas diferentes** dentro da mesma região.
  - Isso garante que, se uma zona falhar, outra possa assumir e manter o sistema funcionando.

- **Escalabilidade**:
  - A nuvem permite escalar verticalmente (aumentar recursos de uma VM) ou horizontalmente (adicionar mais VMs).
  - Isso ajuda a manter o desempenho do sistema conforme a demanda cresce.

- **Tolerância a Falhas**:
  - A criação de VMs em múltiplas zonas e o uso de backups evitam perda de dados e paradas inesperadas.
  - Isso garante continuidade nos serviços mesmo em caso de falhas.

## Modelos de Computação em Nuvem

### IaaS (Infrastructure as a Service)
Você aluga a infraestrutura (servidores, rede, armazenamento) e gerencia o que roda nela.

- **Exemplo:** AWS EC2, Microsoft Azure, Google Compute Engine.
- **Analogia simples:** Alugar um terreno para construir sua casa — você decide tudo, mas precisa cuidar de tudo também.

### PaaS (Platform as a Service)
Você usa uma plataforma pronta para desenvolver e hospedar aplicações, sem se preocupar com servidores.

- **Exemplo:** Heroku, Google App Engine, Azure App Service.
- **Analogia simples:** Alugar uma casa pronta onde você só precisa decorar e morar.

### SaaS (Software as a Service)
Você usa um software pronto, acessado pela internet, sem se preocupar com nada técnico.

- **Exemplo:** Gmail, Google Docs, Microsoft 365.
- **Analogia simples:** Usar um hotel — tudo já está pronto e você só aproveita o serviço.

## Componentes de Arquitetura do Azure

### 🌍 Regiões, Pares de Regiões e Regiões Soberanas
- **Regiões**: São locais físicos espalhados pelo mundo onde ficam os datacenters.
- **Pares de regiões**: Regiões que trabalham em conjunto para oferecer redundância e recuperação de desastres.
- **Regiões soberanas**: Criadas para atender requisitos legais específicos, como as regiões da China ou dos EUA (Governo).

### 🏢 Zonas de Disponibilidade e Datacenters
- **Zonas de Disponibilidade**: São áreas físicas separadas dentro de uma mesma região, com infraestrutura própria.
- Isso permite **alta disponibilidade**, pois se uma zona falhar, outra pode assumir.
- Cada zona pode conter um ou mais **datacenters**.

### 🧱 Recursos e Grupos de Recursos
- **Recursos**: Tudo que criamos no Azure (VMs, redes, bancos de dados etc).
- **Grupos de recursos**: Organizam e agrupam os recursos para facilitar o gerenciamento, controle de acesso e monitoramento.

### 🔐 Assinatura e Grupos de Gerenciamento
- **Assinatura**: É onde os serviços são cobrados. Você pode ter mais de uma assinatura.
- **Grupo de gerenciamento**: Serve para organizar várias assinaturas em níveis mais altos de controle e políticas.

## 💻 Computação no Azure

### • Tipos de Computação
O Azure oferece diferentes formas de executar aplicações, dependendo das necessidades de escalabilidade, gerenciamento e desempenho.

### • Instâncias de Contêiner
- Executam aplicações empacotadas em contêineres (como Docker).
- Isolamento leve e rápido.
- Ótimo para microserviços.
- Ex: Azure Container Instances, Azure Kubernetes Service (AKS).

### • Máquinas Virtuais (VMs)
- Computadores virtuais completos na nuvem.
- Você controla o sistema operacional, software e configurações.
- Ideal para workloads tradicionais e personalizados.
- Ex: Azure Virtual Machines.

### • Funções (Azure Functions)
- Execução de código sob demanda (serverless).
- Você paga apenas pelo tempo de execução.
- Ideal para tarefas automatizadas e eventos, como responder a uploads ou mensagens.

---

## 🌐 Hospedagem de Aplicativos

### • Aplicativos Web do Azure (App Service)
- Plataforma gerenciada para hospedar sites e APIs.
- Suporta várias linguagens como .NET, Java, Node.js, Python.
- Fácil integração com CI/CD e escalonamento automático.

### • Contêineres
- Hospedagem de aplicações empacotadas em contêineres Docker.
- Utiliza serviços como Azure Container Apps ou AKS.
- Escalabilidade automática e fácil gerenciamento.

### • Máquinas Virtuais
- Para hospedagem de aplicativos que exigem controle total do ambiente.
- Você pode instalar qualquer software ou servidor de aplicação.

---

## 🌐 Redes Virtuais

### • Redes Virtuais (VNet)
- Permite que recursos do Azure se comuniquem entre si com segurança.
- Pode ser dividida em sub-redes para segmentação.

### • Sub-redes
- Dividem a VNet em partes menores.
- Facilitam a organização e segurança de recursos.

### • Emparelhamento de Rede (VNet Peering)
- Conecta VNets diferentes.
- Tráfego entre elas é privado e de alta velocidade.

### • DNS
- Configuração personalizada de nomes de domínio internos e externos.
- Ajuda a localizar recursos dentro e fora da rede.

### • Gateway de VPN
- Conecta sua rede local com a rede virtual do Azure via túnel criptografado.
- Permite comunicação segura com a nuvem.

### • ExpressRoute
- Conexão privada e dedicada entre sua infraestrutura local e o Azure.
- Mais rápida, confiável e segura do que conexões pela internet pública.


**Desenvolvido por:**  
| <img src="https://avatars.githubusercontent.com/u/127707049?v=4" width="100px"><br><sub>Rafael Feitosa Santos</sub> |  
| :---: |

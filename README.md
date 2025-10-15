# ☁️ Estudos AWS – Fernanda Cristina Cruz Onil

## 🧠 Sobre este repositório
Este repositório foi criado para registrar meu aprendizado e práticas sobre **Amazon Web Services (AWS)** durante o programa **Santander Code Girls – 2025**, em parceria com a **DIO**.  
Os estudos atuais estão **baseados nas aulas, exemplos e desafios práticos** apresentados ao longo do curso.

Aqui organizo meus **resumos, anotações, exercícios e projetos práticos** realizados em cada módulo.

## 🗂️ Resumo dos Tópicos – Visão Geral AWS

### 📖 1. Introdução à AWS e Conceitos Básicos
- História da **Amazon** e da criação da **AWS (2006)**.  
- A AWS é a principal **provedora de serviços em nuvem** do mercado.  
- Oferece mais de **200 serviços globais** que atendem desde startups até grandes corporações.  
- Enfatiza o aprendizado “**hands-on**” (prático) para domínio das ferramentas.

---

### 🌍 2. Infraestrutura Global
- A **infraestrutura da AWS** é composta por:
  - **Regiões (Regions):** áreas geográficas que agrupam vários data centers.
  - **Zonas de Disponibilidade (AZs):** data centers independentes, mas interligados para garantir alta disponibilidade.
- Atualmente, a AWS possui:
  - **33 regiões** e **105 zonas de disponibilidade**,  
  - com planos para expansão em **Alemanha, Malásia, Nova Zelândia e Tailândia**.
- Disponibiliza latência inferior a **10 milissegundos** em implantações locais.  
- 🌐 Mais detalhes: [Infraestrutura Global AWS](https://aws.amazon.com/pt/about-aws/global-infrastructure)

---

### 💰 3. Modelo de Negócio da AWS
- Baseado em **pagamento conforme o uso (Pay-as-you-go)**.  
- Transição do modelo **CAPEX** (investimento em infraestrutura própria) para **OPEX** (custos operacionais sob demanda).  
- Escalabilidade e flexibilidade: paga-se apenas pelos recursos utilizados.  
- Oferece serviços desde **computação e armazenamento** até **Machine Learning, IoT e Analytics**.

---

### 🧩 4. Modelos de Serviço em Nuvem
| Modelo | Nome | Responsabilidade do Usuário | Exemplo |
|:--|:--|:--|:--|
| **IaaS** | Infraestrutura como Serviço | Controle total sobre o ambiente (ex: EC2, VPC) | EC2 |
| **PaaS** | Plataforma como Serviço | A AWS gerencia a infraestrutura e o sistema operacional | Elastic Beanstalk |
| **SaaS** | Software como Serviço | Usuário apenas utiliza a aplicação | Amazon Chime, WorkMail |

Cada modelo oferece diferentes níveis de **controle, flexibilidade e responsabilidade**.

---

### 🚀 5. Diferenciais da AWS
- **Inovação constante** e atualização frequente de serviços.  
- **Escalabilidade global** e segurança avançada.  
- **Modelo flexível** que se adapta a qualquer porte de empresa.  
- Ecossistema robusto de **parceiros, certificações e treinamentos**.

🧠 Resumo – Computação em Nuvem com Amazon EC2
📍 Módulo 2 – EC2: Elastic Compute Cloud

Serviço da AWS que fornece máquinas virtuais (instâncias) com sistemas operacionais Windows ou Linux.

Cada instância EC2 é composta por CPU, memória, disco, rede e SO.

Classificação IaaS (Infraestrutura como Serviço) — o usuário é responsável pelos aplicativos, dados e conexões.

⚙️ Escolha da Instância

Escolher corretamente garante eficiência, escalabilidade e economia.

É essencial entender as necessidades da aplicação antes de definir o tipo de instância.

🔐 Configuração e Segurança

Utiliza imagens de máquina (AMIs) no momento da criação.

Segurança configurada por grupos de segurança (firewall), controlando portas, protocolos e IPs de origem.

💡 Otimização de Recursos na AWS
💰 Objetivo da Otimização

Reduzir custos e melhorar desempenho dos sistemas em nuvem.

Otimizar é sinônimo de poupar recursos sem comprometer a performance.

⏸️ Boas Práticas

Desligar instâncias não utilizadas, principalmente em ambientes de desenvolvimento e teste.

Remover recursos ociosos (como volumes, snapshots e IPs elásticos).

📈 Escalabilidade

Escalonamento vertical: aumentar/reduzir capacidade (vCPUs, memória, disco) dentro da mesma instância.

Escalonamento horizontal: adicionar/remover instâncias conforme a demanda.

💵 Modelos de Compra de Instâncias

Sob Demanda: Pagamento por hora, ideal para cargas irregulares ou testes.

Reservadas: Desconto maior, porém requer compromisso de uso por 1 ou 3 anos.

Spot: Até 90% mais baratas, mas podem ser interrompidas pela AWS a qualquer momento.

🚀 Conclusão

O EC2 é a base da computação em nuvem da AWS, oferecendo flexibilidade e controle total sobre os recursos.
O uso inteligente e otimizado das instâncias traz redução de custos, alta disponibilidade e escalabilidade eficiente.

## ✨ Próximos Passos

- Revisar **simulados e quizzes da DIO**  
- Aprofundar estudos de **segurança, faturamento e monitoramento**  
- Criar resumo visual com **principais ícones e serviços AWS**  
- Praticar comandos básicos no **AWS CLI**

---

> 💬 *“A nuvem não é o futuro — é o presente em constante evolução.”*  
> — *Fernanda Cristina Cruz Onil*

☁️ Estudos AWS – Fernanda Cristina Cruz Onil
🧠 Sobre este repositório

Repositório criado para documentar meu aprendizado e práticas sobre Amazon Web Services (AWS) durante o programa Santander Code Girls – 2025, em parceria com a DIO.

Aqui registro meus resumos, anotações, exercícios e projetos práticos desenvolvidos em cada módulo do curso, com foco em entendimento técnico e aplicação prática.

🗂️ Resumo dos Tópicos
📖 1. Introdução à AWS e Conceitos Básicos

História da Amazon e origem da AWS (2006).

A AWS é a maior provedora de serviços em nuvem do mundo.

Oferece mais de 200 serviços globais, atendendo desde startups até grandes corporações.

Enfatiza o aprendizado “hands-on” (prático), essencial para o domínio das ferramentas.

🌍 2. Infraestrutura Global

Estrutura composta por:

Regiões (Regions): agrupam vários data centers.

Zonas de Disponibilidade (AZs): data centers independentes, conectados para garantir alta disponibilidade.

Atualmente:

33 regiões e 105 zonas de disponibilidade,

com expansão prevista para Alemanha, Malásia, Nova Zelândia e Tailândia.

Latência inferior a 10 ms em implantações locais.

🔗 Infraestrutura Global AWS

💰 3. Modelo de Negócio da AWS

Baseado em pagamento conforme o uso (Pay-as-you-go).

Transição do modelo CAPEX → OPEX, reduzindo custos com infraestrutura física.

Escalabilidade e flexibilidade: paga-se apenas pelo que é consumido.

Serviços que vão de computação e armazenamento a Machine Learning, IoT e Analytics.

🧩 4. Modelos de Serviço em Nuvem
Modelo	Nome	Responsabilidade do Usuário	Exemplo
IaaS	Infraestrutura como Serviço	Controle total sobre o ambiente	EC2, VPC
PaaS	Plataforma como Serviço	AWS gerencia infraestrutura e SO	Elastic Beanstalk
SaaS	Software como Serviço	Usuário apenas consome o app	WorkMail, Chime

Cada modelo oferece níveis distintos de controle, flexibilidade e responsabilidade.

🚀 5. Diferenciais da AWS

💡 Inovação constante e atualizações frequentes.

🌍 Escalabilidade global e segurança avançada.

🔄 Modelo flexível, adaptável a empresas de qualquer porte.

🎓 Ecossistema robusto de parceiros, certificações e treinamentos.

☁️ Computação em Nuvem com Amazon EC2
📍 Módulo 2 – EC2: Elastic Compute Cloud

Serviço que disponibiliza máquinas virtuais (instâncias) com Windows ou Linux.

Cada instância EC2 possui CPU, memória, disco, rede e sistema operacional.

Classificada como IaaS — o usuário é responsável pelos dados, aplicativos e conexões.

⚙️ Escolha da Instância

A escolha correta garante eficiência, escalabilidade e economia.

Baseia-se nas necessidades específicas da aplicação.

🔐 Configuração e Segurança

Uso de AMIs (Amazon Machine Images) no momento da criação.

Controle de acesso via Security Groups (firewall), definindo portas, protocolos e IPs.

💡 Otimização de Recursos na AWS
💰 Objetivo

Reduzir custos e aumentar o desempenho das soluções na nuvem.
Otimizar = usar recursos de forma inteligente sem desperdiçar.

⏸️ Boas Práticas

Desligar instâncias não utilizadas (ambientes de teste/dev).

Remover recursos ociosos, como volumes e IPs elásticos.

📈 Escalabilidade

Vertical: ajustar capacidade (vCPU, RAM, disco) da instância.

Horizontal: adicionar/remover instâncias conforme a demanda.

💵 Modelos de Compra
Tipo	Descrição	Ideal Para
Sob Demanda	Pagamento por hora	Cargas irregulares e testes
Reservadas	Pagamento fixo anual com desconto	Uso contínuo
Spot	Desconto de até 90%, mas pode ser interrompida	Processos não críticos
🚀 Conclusão

O EC2 é a base da computação em nuvem da AWS.
Usar instâncias de forma otimizada permite redução de custos, alta disponibilidade e escalabilidade eficiente.

✨ Próximos Passos

🔒 Aprofundar estudos em segurança, faturamento e monitoramento.

🧭 Criar resumo visual com principais ícones e serviços AWS.

💻 Praticar comandos básicos no AWS CLI.

💬 “A nuvem não é o futuro — é o presente em constante evolução.”
— Fernanda Cristina Cruz Onil

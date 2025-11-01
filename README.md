☁️ Estudos AWS – Fernanda Cristina Cruz Onil

🧠 Sobre este repositório

Repositório criado para documentar meu aprendizado e práticas sobre Amazon Web Services (AWS) durante o programa Santander Code Girls – 2025, em parceria com a DIO.

🗂️ Resumo dos Tópicos

📖 1. Introdução à AWS e Conceitos Básicos

    História da Amazon e origem da AWS (2006).

🌍 2. Infraestrutura Global

    Estrutura composta por:
    
    Regiões (Regions): agrupam vários data centers.
    Zonas de Disponibilidade (AZs): data centers independentes, conectados para garantir alta disponibilidade

💰 3. Modelo de Negócio da AWS

     Baseado em pagamento conforme o uso (Pay-as-you-go).
     Transição do modelo CAPEX → OPEX, reduzindo custos com infraestrutura física.
     Escalabilidade e flexibilidade: paga-se apenas pelo que é consumido.
     Serviços que vão de computação e armazenamento a Machine Learning, IoT e Analytics.


🧩 4. Modelos de Serviço em Nuvem

      Modelo	Nome	                        Responsabilidade do Usuário          Exemplo
      IaaS	  Infraestrutura como Serviço	  Controle total sobre o ambiente	     EC2, VPC
      PaaS	  Plataforma como Serviço AWS     Gerencia infraestrutura e SO  	     Elastic Beanstalk
      SaaS	  Software como Serviço       	  Usuário apenas consome o app	         WorkMail, Chime

      Cada modelo oferece níveis distintos de controle, flexibilidade e responsabilidade.

🚀 5. Diferenciais da AWS

      💡 Inovação constante e atualizações frequentes.

      🌍 Escalabilidade global e segurança avançada.

      🔄 Modelo flexível, adaptável a empresas de qualquer porte.

      🎓 Ecossistema robusto de parceiros, certificações e treinamentos.



      🚀 Passo a Passo: Step Functions e AWS Lambda
O processo será dividido em duas partes principais: Criação da Função Lambda e Criação da Máquina de Estados (Step Functions).

Parte 1: Criar a Função AWS Lambda
Esta função será um passo no nosso fluxo de trabalho.

1.1. Acessar o Console Lambda e Criar a Função
Faça login no Console AWS e navegue até o serviço Lambda.

Clique em Criar função.

Selecione Autor do zero.

Na seção Informações básicas:

Nome da função: Digite um nome (ex: MyStepFunctionLambda).

Tempo de execução: Selecione um runtime (ex: Node.js 20.x ou Python 3.12).

Arquitetura: Mantenha o padrão (x86_64).

Clique em Criar função.

1.2. Inserir o Código da Função
Após a criação, você será redirecionado para a página da função.

Role para baixo até a seção Código-fonte.

Substitua o código de exemplo pelo código a seguir. Este código simplesmente pega o campo name da entrada e retorna uma saudação.

Exemplo de código (Node.js):

JavaScript

export const handler = async (event) => {
  const name = event.name || 'Mundo';
  const greeting = `Olá, ${name}, da Step Function!`;

  console.log(greeting);

  return {
    statusCode: 200,
    body: JSON.stringify({ message: greeting }),
    // Retorna a saudação como um campo 'greeting'
    greeting: greeting
  };
};
Clique em Deploy (Implantar) para salvar as alterações.

Anote o ARN da função: Você precisará do Nome do Recurso da Amazon (ARN), que está localizado no canto superior direito da página (ex: arn:aws:lambda:us-east-1:123456789012:function:MyStepFunctionLambda).

Parte 2: Criar e Executar a Máquina de Estados (Step Functions)
Agora vamos criar o fluxo de trabalho que invocará a Lambda.

2.1. Acessar o Console Step Functions e Criar o Fluxo
No Console AWS, navegue até o serviço Step Functions.

Clique em Criar máquina de estado.

Selecione Projetar seu fluxo de trabalho visualmente (Workflow Studio).

Selecione Padrão (Standard) ou Expresso (Express) como tipo. Padrão é adequado para a maioria dos casos de uso.

Clique em Próximo.

2.2. Definir o Fluxo de Trabalho no Workflow Studio
Na tela do Workflow Studio, à esquerda, arraste o estado Task (Tarefa) e solte-o entre Start e End.

Configurar o Estado Task:

Com o novo estado Task selecionado, no painel Inspector à direita, em Configuração, altere o Nome do estado (ex: InvocarLambda).

Em Tipo de ação, selecione AWS Lambda e em Operação da API, selecione Invoke.

Em Recurso Lambda, cole o ARN da função Lambda que você anotou na Parte 1.

Visual no Console: O diagrama no centro agora mostrará Start -> InvocarLambda -> End.

Clique em Próximo.

2.3. Configurar a Máquina de Estados
Nome da máquina de estado: Digite um nome (ex: MeuPrimeiroWorkflow).

Permissões:

Selecione Criar uma nova função do IAM (recomendado). O Step Functions criará a função de execução necessária e adicionará automaticamente a política para invocar sua função Lambda.

Mantenha as demais configurações como padrão e clique em Criar máquina de estado.

2.4. Executar o Workflow
Após a criação, você será direcionado para a página de detalhes da máquina de estado.

Clique em Iniciar execução.

Entrada: A entrada da execução é o JSON que será passado para o estado inicial e, em nosso caso, para a função Lambda.

Substitua o JSON padrão pelo seguinte:

JSON

{
  "name": "Usuário Step Functions"
}
Clique em Iniciar execução.

2.5. Verificar o Resultado
Após iniciar a execução, você verá a página de detalhes da execução. O status deve mudar rapidamente para Sucesso.

Diagrama Visual: A caixa correspondente ao estado InvocarLambda (ou o nome que você deu) ficará verde.

Detalhes da Etapa (Passos): Clique no estado InvocarLambda no diagrama.

Role para baixo e visualize as guias:

Input (Entrada): Mostrará {"name": "Usuário Step Functions"}.

Output (Saída): Mostrará o resultado completo retornado pela função Lambda, incluindo a saudação que criamos.

Saída esperada: Se você usou o código Node.js de exemplo, a saída do estado Task deve conter algo como:

JSON

{
  "statusCode": 200,
  "body": "{\"message\":\"Olá, Usuário Step Functions, da Step Function!\"}",
  "greeting": "Olá, Usuário Step Functions, da Step Function!"
}

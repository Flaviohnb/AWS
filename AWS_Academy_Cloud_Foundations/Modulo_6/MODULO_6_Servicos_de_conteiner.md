## Noções básicas de contêiner 

- Os contêineres são um método de virtualização do sistema operacional
- Benefícios
    - Repetível
    - Ambientes de execução autônomos
    - O software é executado da mesma forma em diferentes ambientes
        - Laptop, teste, produção do desenvolvedor
    - Lançamento e interrupção ou encerramento mais rápido do que máquinas virtuais

## O que é o Docker?

- O Docker é uma plataforma de softare que permite criar, testar e implantar aplicações rapidamente
- Você executa contêiners no Docker
    - Os contêiners são criados a partir de um modelo chamado imagem
- Um contêiner tem tudo o que é necessário para execução de um aplicativo

## Contêiners versus máquinas virtuais

- Uma diferença significativa é que as máquinas virtuais são executadas diretamente em um hipervisor, enquanto os contêiners são executados em qualquer sistema operacional se tiverem o recurso de kernel apropriado para oferecer suporte ao software de host do Docker e a seus pré-requisitos.

## Amazon Elastic Container Service (Amazon ECS)

- Amazon Elastic Container Service (Amazon ECS)
    - Um serviço de gerenciamento de contêineres altamente escalável e rápido
- Principais benefícios
    - Orquestra a execução de contêiners do Docker
    - Mantém a escala a frota de nós que executam seus contêineres
    - Remove a complexidade da criação de infraestrutura 
- Integrado a recursos que são familiares para usuários de serviços do Amazon EC2 
    - Elastic Load Balacing
    - Grupos de segurança do Amazon EC2
    - Volumes do Amazon EBS
    - Funções do IAM

## Opções de cluster do Amazon ECS

- Pergunta-chave: Deseja gerenciar o cluster do Amazon ECS que executa os contêiners?
    - Se sim, crie um clustr do Amazon ECS baseado no Amazon EC2 (fornece controle mais granular sobre a infraestrutura)
    - Se não, crie um cluster do Amazon ECS baseado no AWS Fargate (mais fácil de manter, com foco em seus aplicativos)

## O que é o Kubernetes?

- O Kubernetes é um software de código aberto para orquestração de contêineres
    - Implante e gerencie aplicativos usando contêiners em grande escala
    - O mesmo conjunto de ferramentas pode ser usado no local e na nuvem
- Complementa o Docker
    - O Docker permite que você execute vários contêiners em um único host do sistema operacional
    - O Kubernetes orquestra vários hosts do Docker (nós)
- Automatiza
    - Provisionamento de contêineres
    - Redes
    - Distribuição de carga
    - Escalabilidade

## Amazon Elastic Kubernetes Service (Amazon EKS)

- Amazon Elastic Kubernetes Service (Amazon EKS)
    - Permite executar o Kubernetes na AWS
    - Conformidade certificada com o Kubernetes (dá suporte à migração fácil)
    - Oferece suporte a contêineres Linux e Windows
    - Compatível com as ferramentas de comunidade do Kubernetes e dá suporte a complementos populares do Kubernetes
- Por que usar o Amazon EKS
    - Gerenciar clusters de instâncias de computação do Amazon EC2
    - Execute contêineres orquestrados pelo Kubernetes nessas instâncias

## Amazon Elastic Container Registry (Amazon ECR)

- O Amazon ECR é um registro de contêiner gerenciado do Docker que facilita o armazenamento, o gerenciamento e a implantação de imagensde contêineres do Docker.


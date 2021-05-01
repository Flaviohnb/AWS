## Serviços de computação da AWS

- A Amazon Web Services (AWS) oferece muitos serviços de computação. Esta módulo discutirá os serviços destacados:
    - Amazon EC2
        - `Fornece máquinas virtuais redimensionáveis`
    - Amazon EC2 Auto Escaling
        - `Oferece suporte à disponibilidade de aplicativos, permitindo que você defina condições que executarão ou encerrarão automaticamente instâncias do EC2`
    - Amazon Elastic Container Registry (Amazon ECR)
        - `Usado para armazenar e recuperar imagens de Docker `
    - Amazon Elastic Conatiner Service (Amazon ECS)
        - `É um serviço de orquestração de contêiners compatível com o Docker`
    - VMware Cloud na AWS
        - `Permite provisionar uma nuvem híbrida sem hardware personalizado`
    - AWS Elastic Beanstalk
        - `Oferece uma maneira simples de executar e geranciar aplicativos web`
    - AWS Lambda
        - `Solução de computação sem servidor, você paga apenas pelo tempo de computação utilizado`
    - Amazon Elastic Serviço Kubernetes (Amazon EKS)
        - `Permite executar Kubernetes gerenciados na AWS`
    - Amazon Lightsail
        - `Oferece um serviço simples de usar para criar um aplicativo ou um site `
    - AWS Batch
        - `Fornece uma ferramenta para executar trabalhos em lote em qualquer escala`
    - AWS Fargate
        - `Oferece uma maneira de executar contêiners que reduzem a necessidade de gerenciar servidores ou clusters`
    - AWS Outposts
        - `Oferece uma maneira de executar serviços da AWS selecionados no datacenter local`
    - AWS Serveless Application Repository
        - `Permitem que os clientes descubram, implantem e publiquem aplicativos sem servidor`

## Categorização de serviços de computação

- Serviço: 
    - `Amazon EC2`
- Principais Coneitos:
    - `Infraestrutura como um serviço IaaS`
    - `Baseado em instância`
    - `Máquinas virtuais`
- Caracteristicas:
    - `Provisione máquinas virtuais que você possa gerenciar como quiser`
- Facilidade de uso: 
    - `Um conceito familiar para muitos profissionais de TI`
---
- Serviço: 
    - `AWS Lambda` 
- Principais Coneitos:
    - `Computaçãosem servidor`
    - `Baseado em função`
    - `Baixo custo`
- Caracteristicas:
    - `Escrever e implantar código que seja executado por agendamento ou que possa ser acionado por eventos`
    - `Use quando possível (arquiteto para a nuvem)`
- Facilidade de uso:
    - `Um conceito relativamente novo para muitos membros da equipe de TI, mas fácil de usar depois de aprender como`
---
- Serviço: 
    - `Amazon ECS`
    - `Amazon EKS`
    - `AWS Fargate`
    - `Amazon ECR`
- Principais Coneitos:
    - `Computação baseada em contêiners`
    - `Baseado em instância`
- Caracteristicas:
    - `Gere e execute trabalhos mais rapidamente`
- Facilidade de uso:
    - `O AWS Fargate reduz a sobrecaga administrativa, mas você pode usar opções que oferecem mais controle`
---
- Serviço: 
    - `AWS Elastic Beanstalk`
- Principais Coneitos:
    - `Plataforma como serviço (PaaS)`
    - `Para aplicativos Web`
- Caracteristicas:
    - `Concentre-se no código (criação do aplicativo)`
    - `Pode ser facilmente vinculado a outros serviços - bancos de dados, Domain Name System (DNS) etc`
- Facilidade de uso:                
    - `Comece a usar com rapidez e facilidade`

## Escolher o serviço de computação ideal

- O serviço ou serviços de computação ideais que você usa dependerão do seu caso de uso
- Alguns aspectos a serem considerados
    - Qual é o design do seu aplicativo?
    - Quais são seus padrões de uso?
    - Quais definições de configuração você deseja gerenciar?
- Selecionar a solução de computação errada para uma arquitetura pode levar a uma menor eficiência de performance
    - Um bom ponto de partida - Entenda as opções de computação disponíveis
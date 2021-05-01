## Amazon Elastic Compute Cloud (Amazon EC2)

- Fornece máquinas virtuais onde você pode hospedar os mesmos aplicativos executados em servidores locais.
- Disponibiliza capacidade computacional segura e redimensionável na nuvem.
- Usos comuns para instâncias do EC2 incluem:
    - Servidores de aplicativos;
    - Servidor Web;
    - Servidor de banco de dados;
    - Servidor de jogos;
    - Servidor de e-mail;
    - Servidor de mídia;
    - Servidor de catálogo;
    - Servidor de arquivos;
    - Servidor de computação;
    - Servidor de proxy;

## Visão geral do Amazon EC2

- Amazon Elastic Compute Cloud (Amazon EC2)
    - Fornece máquinas virtuais chamadas de instâncias do EC2 na nuvem
    - Fornece controle total sobre o sistema operacional convidade (Windows e Linux) em cada instância
- Você pode executar instâncias de qualquer tamanho em uma zona de disponibilidade em qualquer lugar do mundo
    - Execute instâncias a partir de Imagens de máquina da Amazon (AMIs)
    - Execute instâncias com apenas alguns cliques ou uma linha de código, e elas estarão prontas em minutos
- Você pode controlar o tráfego de e para instâncias

## Executar uma instância do Amazon EC2

- Esta seção do módulo aborda nove decisões importantes a serem tomadas quando você criar uma instância do EC2 usando o Assistente de execução de instância do Console de Gerenciamento da AWS
- Durante o processo, conceitos essenciais do Amazon EC2 serão explorados
- Escolhas feitas usando o Assistente para executar instâncias:
    - AMI
    - Tipo de instância
    - Configurações de rede
    - Função do IAM
    - Dados de usuário
    - Opções de armazenamento
    - Tags
    - Grupo de segurança
    - Par de chaves

## 1. Selecionar uma AMI

- Imagem de máquina da Amazon (AMI)
    - É um modelo usado para criar uma instância do EC2 (que é uma máquina virtual, ou VM, executada na Nuvem AWS)
    - Contém um sistema operacional Windows ou Linux
    - Muitas vezes, ele também tem software pré-instalado

- Opções de AMI
    - Quick Start - AMIs do Linux e do Windows fornecidas pela AWS
    - Minhas AMIs - Todas as AMIs que você criou
    - AWS Marketplace - Modelos pré-configurados de terceiros
    - AMIs da comunidade - AMIs compartilhadas por outras pessoas; use por sua conta e risco

## Criação de uma nova AMI: exemplo

- 1: Inicie uma instância
- 2: Conecte-se à instância e modifique-a manualmente ou execute um script que modifique a instância (por exemplo, atualizar o software instalado)
- 3: Capture como uma nova AMI
- 4: Copie a AMI em qualquer outra região em que você deseje usa-la

## 2. Selecionar um tipo de instância

- Considere seu caso de uso
    - Como será usada a instância do EC2 que você criar?
- O tipo de instância que você escolher determinará
    - Memória (RAM)
    - Capacidade de processamento (CPU)
    - Espaço em disco e tipo de disco (armazenamento)
    - Performance de rede
- Categorias de tipo de instância 
    - Uso geral
    - Otimizada para computação
    - Otimizada para memória
    - Otimizada para armazenamento
    - Computação acelerada
- Os tipos de instância oferecem família, geração e tamanho

## Nomeação e tamanhos de tipo de instância do EC2

- Nomeação de tipo de instância
    - Exemplo: t3.large
        - T é o nome da familia
        - 3 é o número da geração
        - Large é o tamanho

- Exemplo de tamanhos de instância 
    ---       
    - Nome da instância: `t3.nano`
    - vCPU: `2`
    - Memória (GB): `0,5`
    - Armazenamento: `Somente EBS`
    ---   
    - Nome da instância: `t3.micro`
    - vCPU: `2`
    - Memória (GB): `1`
    - Armazenamento: `Somente EBS`
    ---   
    - Nome da instância: `t3.small`
    - vCPU: `2`
    - Memória (GB): `2`
    - Armazenamento: `Somente EBS`
    ---   
    - Nome da instância: `t3.medium`
    - vCPU: `2`
    - Memória (GB): `4`
    - Armazenamento: `Somente EBS`
    ---   
    - Nome da instância: `t3.large`
    - vCPU: `2`
    - Memória (GB): `8`
    - Armazenamento: `Somente EBS`
    ---       
    - Nome da instância: `t3.xlarge`
    - vCPU: `4`
    - Memória (GB): `16`
    - Armazenamento: `Somente EBS`
    ---       
    - Nome da instância: `t3.2xlarge`
    - vCPU: `8`
    - Memória (GB): `32`
    - Armazenamento: `Somente EBS`
    ---       

## Selecionar tipo de instância: com base no caso de uso

- Detalhes do tipo de instância
    - Tipo de instância: `a1, m4, m5, t2, t3`
    - Caso de uso: `Amplo`
    ---
    - Tipo de instância: `c4, c5`
    - Caso de uso: `Alta performance`
    ---
    - Tipo de instância: `r4, r5, x1, z1`
    - Caso de uso: `Bancos de dados na memória`
    ---
    - Tipo de instância: `f1, g3, g4, p2, p3`
    - Caso de uso: `Machine learning`
    ---
    - Tipo de instância: `d2, h1, i3`
    - Caso de uso: `Sistema de arquivos distribuídos`
    ---

## Tipos de instância: recursos de rede 

- A largura de banda de rede (Gbps) varia de acordo com o tipo de instância
    - Consulte 'Tipos de instância do Amazon EC2' para comparar
- Para maximizar a performance de redes e largura de banda do seu tipo de instância:
    - Se você tiver instâncias interdependentes, execute-as em um placement group de cluster
    - Habilite a rede avançada
- Os tipos de rede avançada são compatíveis com a maioria dos tipos de instância
    - Consulte a documentação 'recursos de redes e armazenamento' para obter detalhes
- Tipos de rede avançada 
    - Elastic Network Adapter (ENA): oferece suporte a velocidade de rede de até 100 Gbps
    - Interface Inter 82599 Virtual Function: oferece suporte a velocidades de rede de até 10 Gbps

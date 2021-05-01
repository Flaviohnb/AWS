## Modelo de responsabilidade compartilhada da AWS

- Cliente (Responsabilidade pela segurança "na" nuvem):
    - Dados do cliente;
    - Plataforma, aplicativos, gerenciamento de identidade e acesso;
    - Configuração de sistema operacional, rede e firewall;
        - Criptografia de dados no lado do cliente e autenticação da integridade dos dados;
        - Criptografia no lado do servidor (Sistema  de arquivos e/ou dados);
        - Proteção do tráfego de rede (Croptografia, integridade, identidade);

- AWS (Responsabilidade pela segurança "da" nuvem):
    - Software;
        - Computação;
        - Armazenamento;
        - Banco de dados;
        - Rede;
    - Infraestrutura global de hardware/AWS
        - Regiões;
        - Zonas;
        - Pontos de presença;

## Responsabilidade da AWS: segurança da nuvem

AWS

- Segurança física dos datacenter:
    - Acesso controlado e baseado em necessidade;
- Infraestrutura de hardware e software:
    - Desativação de armazenamento, registro em log de acesso ao sistema operacional (SO) do host e auditoria;
- Infraestrutura de rede:
    - Detecção de intrusão;
- Infraestrutura de virtualização:
    - Isolamento de instância;

Cliente

- <b>Sistema operacional</b> da instância do Amazon Elastic Compute Cloud (Amazon EC2):
    - Incluindo aplicação de patches, manuntenção;
- <b>Aplicações</b>:
    - Senhas, acessos baseado em função etc;
- Configurações <b>de rede</b>
- Gerenciamento de contas:
    - Configurações de permissão e login para cada usuário;

## Características do serviço e responsabilidade de segurança

- Infraestrutura como um serviço (IaaS):
    - O cliente tem mais flexibilidade em relação à configuração de rede e armazenamento;
    - O cliente é responsável por gerenciar mais aspectos da segurança;
    - O cliente configura os controles de acesso;

- Plataforma como serviço (PaaS):
    - O cliente não precisa gerenciar a infraestrutura subjacente;
    - A AWS gerencia o sistema operacional, a aplicação de patches de banco de dados, a configuração de firewall e a recuperação de desastres;
    - O cliente pode ser concentrar no gerenciamento de código ou dados;

- Software como serviço (SaaS):
    - O softare é hospedado de maneira centralizada;
    - Licenciado em um modelo de assinatura ou pagamento conforme o uso;
    - Os serviços normalmente são acessados por meio de um navegador Web, um aplicativo móvel ou uma interface de programação de aplicativos (API);
    - Os clientes não precisam gerenciar a infraestrutura que oferece suporte ao serviço;
    - Exemplos de SaaS:
        - AWS Trusted Advisor;
        - AWS Shield;
        - Amazon Chime;

- Exemplos de serviços gerenciados:

    - Cliente:
        - Amazon EC2;
        - Amazon Elastic Block Store (Amazon EBS);
        - Amazon Virtual Private Cloud (Amazon VPC);
    - AWS:
        - AWS Lambda;
        - Amazon Relational Database Service (Amazon RDS);
        - AWS Elastic Beanslalk;

 
## Recursos do Amazon EFS

- Armazenamento de arquivos na Nuvem AWS
- Funciona bem para big data e análise, fluxos de trabalho de processamento de mídia, gerenciamento de conteúdo, serviço na web e diretórios iniciais
- Sistema de arquivos em escala de petabytes e baixa latência
- Armazenamento compartilhado
- Capacidade elástica
- Oferece suporte ao Network File System (NFS) versões 4.0 e 4.1 (NFSv4)
- Compatível com todas as AMIs baseadas em Linux para o Amazon EC2

## Arquitetura do Amazon EFS

- Pense no Amazon EFS como armazenamento de arquivos na nuvem. 
- Com o Amazon EFS, você pode criar um sistema de arquivos, montar o sistema de arquivos em uma instância do Amazon EC2, ler e gravar dados de/para seu sistema de arquivos. 
- Você pode montar um sistema de arquivos do Amazon EFS em sua VPC. O Amazon EFS oferece suporte ao Network File System ou ao NFS versões 4.0 e 4.1. 
- Você pode acessar o sistema de arquivos do Amazon EFS simultaneamente por meio de várias instâncias do Amazon EC2 na VPC. 
- Aplicativos que escalam além de uma única conexão podem acessar um sistema de arquivos. 
- As instâncias do Amazon EC2 executadas em várias zonas de disponibilidade dentro da mesma região da AWS podem acessar o sistema de arquivos possibilitando que vários usuários acessem e compartilhem uma fonte de dados comum. 

## Implementação do Amazon EFS

- 1 - Crie seus recursos do Amazon EC2 e execute sua instância do Amazon EC2
- 2 - Crie um sistema de arquivos do Amazon EFS
- 3 - Crie seus destinos de montagem nas sub-redes apropriadas
- 4 - Conecte suas instâncias do Amazon EC2 aos destinos de montagem
- 5 - Verifique os recursos e a proteção da sua conta da AWS

## Recursos do Amazon EFS

- Sistema de arquivos 
    - Destino de montagem
        - ID da sub-rede
        - Grupos de segurança
        - Um ou mais por sistema de arquivos
        - Criar em uma sub-rede VPC
        - Uma por zona de disponibilidade
        - Deve estar na mesma VPC
    - Tags
        - Pares de chave-valor

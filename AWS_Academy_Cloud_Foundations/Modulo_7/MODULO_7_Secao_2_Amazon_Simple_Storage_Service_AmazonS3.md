## Visão geral do Amazon S3 

- Os dados são armazenados como objetos em buckets
- Armazenamento praticamente ilimitado
    - Um único objeto é limitado a 5 TB
- Projetado para oferecer uma durabilidade de 11 noves
- Acesso granular a buckets e objetos

## Classes de armazenamento do Amazon S3

- O Amazon S3 oferece uma variedade de classes de armazenamento no nível do objeto projetado para diferentes casos de uso:
    - Amazon S3 Standard
    - Amazon S3 Intelligent Tiering
    - Amazon S3 Standard-Infrequent Access (Amazon S3 Standard-IA)
    - Amazon S3 One Zone-Infrequent Access (Amazon S3 One Zone-IA)
    - Amazon S3 Glacier
    - Amazon S3 Glacier Deep Archive 

## URLs do bucket do Amazon S3 (dois estilos)

- Para fazer upload dos seus dados:
    - 1 - Crie um bucket em uma região da AWS
    - 2 - Faça upload de quase qualquer número de objetos para o bucket
- Endpoint de URL no estilo de caminho do bucket:
    - https://s3.ap-notheast-1.amazonaws.com/bucket-name
        - "ap-norheast-1": código da região
        - "bucket-name": Nome do bucket
- Endpoint de URL do estilo de hospedagem virtual do bucket:
    - https://bucket-name.s3-ap-northeast-1.amazonaws.com
        - "bucket-name": Nome do bucket
        - "ap-notheast-1": Código da região 

## Os dados são armazenados de modo redundante na região

- Quando você cria um bucket no Amazon S3, ele é associado a uma região específica da AWS. Ao armazenar dados no bucket, eles são armazenados de forma redundante em várias instalações da AWS dentro da região selecionada. Isso significa que seus dados são protegidos mesmo que haja perda simultânea de dados em duas instalações da AWS.

## Projetado para escala perfeita

- O Amazon S3 gerencia automaticamente o armazenamento do bucket enquanto os dados crescem. Você pode começar a usar imediatamente, e o armazenamento físico de dados crescerá de acordo com as necessidades dos aplicativos. O Amazon S3 também escala para lidar com um alto volume de solicitações. Você não precisa provisionar o armazenamento ou o throughput, e será cobrado apenas pelo que usar. 

## Acesse os dados em qualquer lugar 

- Console de Gerenciamento da AWS
- Interface da Linha de Comando da AWS
- SDK

## Cenários comuns do Amazon S3

- Backup e armazenamento
- Hospedagem de aplicações
- Hospedagem de mídia
- Entrega de software

## Definição de preço do Amazon S3 

- Pague somente pelo que usar, incluindo
    - GBs por mês
    - Transferência para FORA, para outras regiões
    - Solicitações PUT, COPY, POST, LIST, GET
- Você não paga por
    - Transferência para DENTRO do Amazon S3
    - Transferência para FORA do Amazon S3 para o Amazon CloudFront ou para o Amazon EC2 na mesma região

## Amazon S3: definição de preço de armazenamento

- Para uma estimativa de custos do Amazon S3, considere o seguinte:
    - 1 - Tipo de classe de armazenamento
        - O armazenamento padrão foi projetado para:
            - 11 noves de durabilidade
            - Quatro noves de disponibilidade
        - O S3 Standard-Infrequent Access (S-IA) foi projetado para:
            - 11 noves de durabilidade
            - Três noves de disponibilidade
    - 2 - Quantidade de armazenamento 
        - Número e tamanho dos objetos
    - 3 - Solicitações 
        - O número e o tipo de solicitações (GET, PUT, COPY)
        - Tipo de solicitações:
            - Taxas diferentes para solicitações GET com relação às outras solicitações
    - 4 - Transferência de dados
        - A definição de preço é baseada na quantidade de dados transferidos para fora da região do Amazon S3
            - A transferência de dados para dentro é gratuita, mas você é cobrado pelos dados transferidos para fora.
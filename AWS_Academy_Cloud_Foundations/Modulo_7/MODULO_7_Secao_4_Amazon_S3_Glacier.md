## Análise do Amazon S3 Glacier

- O Amazon S3 Glacier é um serviço de arquivamento de dados projetado para oferecer segurança, durabilidade e um custo extremamente baixo.
- Ele oferece suporte à criptografia de dados em trânsito e ociosos por meio de Secure Sockets Layer (SSL) ou Transport Alayer Security (TLS)
- O recurso Vault Lock impõe a conformidade por meio de uma política
- O design de custo extremamente baixo funciona bem para arquivamento de longo prazo
    - Fornece três opções de acesso a arquivos: expresso, padrão e em massa. Os tempos de recuperação variam de alguns minutos a várias horas.

## Amazon S3 Glacier

- Serviço de armazenamento para arquivamento de dados de baixo custo e backup de longo prazo
- É possível configurar o arquivamento do ciclo de vida do conteúdo do Amazon S3 no Amazon S3 Glacier
- Opções de recuperação
    - Padrão: de 3 a 5 horas
    - Em massa: de 5 a 12 horas
    - Expressa: de 1 a 5 minutos 

## Casos de uso do Amazon S3 Glacier

- Arquivamento de ativos de mídia
- Arquivamento de informações de saúde
- Arquivamento para fins normativos e de conformidade
- Arquivamento de dados cientificos
- Preservação digital
- Substituição da fita magnética

## Uso do Amazon S3 Glacies

- Serviços da web RESTful
- SDKs JAva ou .NET
- Amazon S3 com políticas de ciclo de vida 

## Políticas de ciclo de vida

- As políticas de ciclo de vida do Amazon S3 permitem que você exclua ou mova objetos com base na idade.

## Classes de armazenamento do Amazon S3 

- Classe de armazenamento   
    - S3 Standard
        - Maior ou igual a três zonas de disponibilidade
    - S3 Standard - Infrequent Access (AI)
        - A taxa de recuperação está associada a objetos
        - Mais adequado para dados acessados com pouca frequência
    - Camadas inteligentes do S3
        - Move automaticamente objetos entre níveis com base em padrões de acesso
        - Maior ou igual a três zonas de disponibilidade 
    - S3 One Zone - IA
        - Uma zona de disponibilidade
        - Custa menos que o Amazon S3 Standard-IA
    - S3 Glacier
        - Não está disponível para acesso em tempo real
        - É necessário restaurar objetos antes de acessá-los
        - A resturação de objetos pode levar de 1 minuto a 12 horas
    - S3 Glacier Deep Archive
        - Armazenamento de menor custo para retenção em longo prazo (7 a 10 anos)
        - Maior ou igual a três zonas de disponibilidade
        - Tempo de recuperação de até 12 horas

## Comparação de armazenamento

- Amazon S3 
    - Volume de dados: Sem limite
    - Latência média: ms
    - Tamanho do item: Máximo de 5 TB
    - Custo/GB por mês: Custos mais altos
    - Solicitações faturadas: PUT, COPY, POST, LIST, GET
    - Definição de preço de recuperação: Por solicitação
- Amazon S3 Glacier
    - Volume de dados: Sem limite
    - Latência média: minutos/horas
    - Tamanho do item: Máximo de 40 TB
    - Custo/GB por mês: Custos mais baratos
    - Solicitações faturadas: UPLOAD e retrieval
    - Definição de preço de recuperação: Por solicitação e por GB

## Criptografia no lado do servidor

- Outra diferença importante entre o Amazon S3 e o Amazon S3 Glacier, é como o dado é criptografado. 
- Servidor se concentra na proteção de dados em repouso. Com ambas as soluções, você pode transferir seus dados com segurança por HTTPS. Todosos dados arquivados no Glacier são criptografados por padrão.
- Com o Amazon S3, seu aplicativo deve iniciar a criptografia no lado do servidor. Há várias maneiras de habilitar a criptografia no lado do servidor no Amazon S3. Primeiro, você pode usar a criptografia no lado do servidor com chaves de criptografia gerenciadas do Amazon S3 SSE S3. 
- O Amazon S3 criptografa cada objeto com uma chave exclusiva. Como uma proteção adicional, ele criptografa a chave com uma chave mestra que é alterada regurlamente. 
- A criptografia no lado do servidor do Amazon S3 usa uma das cifras de bloco mais fortes disponíveis, o padrão de criptografia avançada de 256 bits ou AES-256 para criptografar seus dados.
- Em seguida, você pode usar a criptografia no lado do servidor com chaves de criptografia fornecidas pelo cliente, o que é conhecido como SSE-C. Essa opção pérmite que você defina suas próprias chaves de criptografia. Você inclui a chave de criptografia como parte da solicitação e o Amazon S3 gerencia a criptografia à medida que grava em discos e a descriptografia quando você acessa seus objetos. Por fim, você pode usar a criptografia no lado do servidor com o AWS Key Mangement Service ou o AWS KMS
- O AWS KMS é um serviço que combina hardware e software altamente disponíveis e seguros para fornecer um sistema de gerenciamento de chaves escalado para a nuvem. O AWS KMS usa chaves mestras de cliente para criptografar objetos do Amazon S3. Você acessa o KMS por meio da seção de chaves de criptografia no console do IAM. Você também pode acessar o AWS KMS por meio da API para criar centralmente chaves de criptografia, definir as políticas que controlam como as chaves podem ser usadas e auditar o uso de chaves para provar que elas estão sendo usadas corretamente. 

## Segurança com o Amazon S3 Glacier

- Controlar o acesso com o IAM
- O Amazon S3 Glacies criptografa seus dados com AES-256
- O Amazon S3 Glacier gerencia suas chaves para você

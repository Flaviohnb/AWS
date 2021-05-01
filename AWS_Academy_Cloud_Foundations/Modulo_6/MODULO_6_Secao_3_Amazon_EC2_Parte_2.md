## 3. Especificar configurações de rede

- Onde a instância deve ser implantada?
    - Identificar a VPC e, opcionalmente, a sub-rede
- Um endereço IP público deve ser atribuído automaticamente?
    - Para torná-lo acessível à Internet

## 4. Anexar função do IAM (opcional)

- O software na instância do EC2 precisará interagir com outros serviços da AWS?
    - Em caso afirmativo, anexe uma função do IAM apropriada.
- Uma função do AWS Indentity and Access Management (IAM) anexada a uma instância do EC2 é mantida em um perfil de instância.
- Você não está restrito a anexar uma função apenas na execução da instância.
    - Você também pode anexar uma função a uma instância que já existe.

- Exemplo:
    - Função que concede permissões de acesso ao bucket do Amazon Simple Storage Service (Amazon S3) ->
    - -> `Anexado a` ->
    - -> Instância ->
    - -> `O aplicativo na instância pode acessar` ->
    - -> Bucket do S3 com objetos 

## 5. Script de dados do usuário (opcional)

- Opcionalmente, especifique um script de dados do usuário na execução da instância
- Use scripts de dados do usuário para personalizar o ambiente de tempo de execução de sua instância
    - O script é executado na primeira vez que a instância é iniciada
- Pode ser usado estrategicamente
    - Por exemplo, reduza o número de AMIs personalizadas que você cria e mantém

## 6. Especificar armazenamento

- Configurar o volume raiz 
    - Onde o sistema operacional convidade está instalado
- Anexar volumes de armazenamento adicionais (opcional)
    - A AMI já pode incluir mais de um volume
- Para cada volume, especifique:
    - O tamanho do disco (em GB)
    - O tipo de volume
        - Diferentes tipos de unidades de estado sólido (SSDs) e unidades de disco rígido (HDDs) estão disponíveis
    - Se o volume for excluído quando a instância for encerrada
    - Se a criptografia precisar ser usada

## Opções de armazenamento do Amazon EC2

- Amazon Elastic Block Store (Amazon EBS) 
    - Volumes de armazenamento em nível de bloco duráveis
    - Você pode interromper a instância e iniciá-la novamente; os dados ainda estarão lá;
- Armazenamento de instâncias do Amazon EC2
    - O armazenamento é fornecido em discos anexados ao computados host em que a instância do EC2 está em execução 
    - Se a instância for interrompida, os dados armazenados aqui serão excluídos
- Outras opções de armazenamento (não para o volume raiz)
    - Monte um sistema de arquivos do Amazon Elastic File System (Amazon EFS) 
    - Conecte-se ao Amazon Simple Storage Service (Amazon S3)

## Exemplo de opções de armazenamento

- Características da instância 1 
    - Ele tem um tipo de volume raiz do Amazon EBS para o sistema operacional
    - O que acontecerá se a instância for interrompida e reiniciada?
- Característica da instância 2 
    - Ele tem um tipo de volume raiz de armazenamento de instâncias para o sistema operacional
    - O que acontecerá se a instância for interrompida (devido a um erro do usuário ou uma falha no sistema)?
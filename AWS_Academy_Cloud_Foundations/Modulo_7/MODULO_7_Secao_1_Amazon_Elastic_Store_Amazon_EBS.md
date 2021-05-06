## Armazenamento

- Amazon EBS
    - Disponibiliza volumes de armazenamento persistente em blocos para uso com instâncias do Amazon EC2. Armazenamento persistente é qualquer dispositivo de armazenamento físico de dados que retém dados após a alimentação desse dispositivo ser desligada. Ele também é chamado de armazenamento não volátil
    - Cada volume do Amazon EBS é replicado automaticamente dentro da sua zona de disponibilidade para proteger você contra falhas de componente. Ele foi projetado para oferecer alta disponibilidade e durabilidade. Os volumes do Amazon EBS oferecem a performance consistente e de baixa latência necessárioa para executar suas cargar de trabalho. 
    - Você pode ajustar a escala do seu uso em poucos minitos, pagando um preço baixo apenas pelo que você provisiona.

## Opções de armazenamento da AWS: armazenamento em bloco vesus armazenamento de objetos

- E se você quiser alterar um caractere em um arquivo de 1 GB?
    - Armazenamento em bloco 
        - Alterar um bloco (parte do arquivo) que contém o caractere
    - Armazenamento de objetos
        - Todo o arquivo deve estar atualizado
    
## Amazon EBS

- O Amazon EBS permite criar volumes de armazenamento individuais e anexá-los a uma instância do Amazon EC2:
    - O Amazon EBS oferece armazenamento em nível de blocos.
    - Os volumes são replicados automaticamente dentro de sua zona de disponibilidade.
    - O backup pode ser feito automaticamente no Amazon S3 por meio de snapshots.
    - Os usos incluem
        - Volumes de inicialização e armazenamento para instâncias do Amazon Elastic Compute Cloud (Amazon EC2)
        - Armazenamento de dados com um sistema de arquivos
        - Hosts de banco de dados
        - Aplicações empresariais

## Tipos de volume do Amazon EBS

- Unidades de estado sólido (SSDs)
    - Uso geral 
        - Tamanho máximo do volume: 16 TiB
        - Máximo de IOPS por volume: 16.000
        - Taxa de transferência máxima/volume: 250 MiB/s
    - IOPS provisionadas
        - Tamanho máximo do volume: 16 TiB
        - Máximo de IOPS por volume: 64.000
        - Taxa de transferência máxima/volume: 1000 MiB/s
- Unidades de disco rígido (HDD)
    - Otimizados para throughtput
        - Tamanho máximo do volume: 16 TiB
        - Máximo de IOPS por volume: 500
        - Taxa de transferência máxima/volume: 500 MiB/s
    - Inativos
        - Tamanho máximo do volume: 16 TiB
        - Máximo de IOPS por volume: 250
        - Taxa de transferência máxima/volume: 250 MiB/s

## Recursos do Amazon EBS

- Snapshots
    - Snapshots pontuais
    - Recriar um novo volume a qualquer momento
- Criptografia
    - Volumes criptografados do Amazon EBS
    - Sem custo adicional
- Elasticidade 
    - Aumentar a capacidade
    - Alteração para diferentes tipos

## Amazon EBS: volumes, IOPS e definição de preço

- 1 - Volumes
    - Os volumes do Amazon EBS persistem independentemente da instância
    - Todos os tipos de volume são cobrados pela quantidade provisionada por mês
- 2 - IOPS
    - General Purpose SSD
        - Cobrado pela quantidade provisionada em GB por mês até que o armazenamento seja liberado.
    - Magnético
        - Cobrado pelo número de solicitações para o volume.
    - Provisioned IOPS SSD
        - Cobrado pela quantidade provisionada em IOPS (mmultiplicada pela porcentagem de dias provisionados no mês).

## Amazon EBS: Snapshots e tranferência de dados

- 3 - Snapshots 
    - O custo adicional dos snapshots do Amazon EBS para o Amazon S3 é por GB-mês de dados armazenados
- 4 - Transferência de dados
    - A transferência de dados de entrada é gratuita
    - A transferência de dados de saída entre regiões gera cobrança

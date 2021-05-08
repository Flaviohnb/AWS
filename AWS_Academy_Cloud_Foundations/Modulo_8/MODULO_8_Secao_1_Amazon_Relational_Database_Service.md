## Serviços não gerenciados vesus serviços gerenciados

- Não gerenciados:
    - Escalabilidade, tolerância a falhas e disponibilidade são gerenciadas por você.
- Gerenciados:
    - Normalemtne, escalabilidade, tolerância a falhas e disponibilidade são incorporados ao serviço.

## Desafios dos bancos de dados relacionais

- Manuntenção do servidor e consumo de energia
- Instalação de software e patches
- Backups de banco de dados e alta disponibilidade
- Limites de escalabilidade
- Segurança de dados
- Instalação e patches do sistema operacional (SO)

## Amazon RDS

- Serviço gerenciado que configura e opera um banco de dados relacional na nuvem.

## Responsabilidade de serviços gerenciados

- Você gerencia:
    - Otimização de aplicativos
- A AWS gerencia:
    - Instalação e patches do SO
    - Instalação e patches de software de banco de dados
    - Backups de banco de dados
    - Alta disponibilidade
    - Escalabilidade
    - Energia e servidores em rack e pilha
    - Manutenção do servidor

## Instâncias de banco de dados do Amazon RDS

- Amazon RDS
    - Instâncias principal de banco de dados do Amazon RDS
        - Classe da instância de banco de dados
            - CPU
            - Memória
            - Desempenho de rede
        - Armazenamento de instâncias de banco de dados
            - Magnético
            - De uso geral (unidades de estado sólido ou SSD)
            - IOPS provisionadas

- Mecanismos de banco de dados
    - MySQL
    - Amazon Aurora
    - Microsoft SQL Server
    - PostgreSQL
    - MariaDB
    - Oracle

## Amazon RDS em uma virtual private cloud (VPC)

- Há muitas maneiras diferentes de configurar sua implementação do RDS. 
    - Por exemplo, você pode executar uma instância em uma Amazon VPC. Ao usar, uma VPC, você tem controle sobre o ambiente de rede virtual. Você pode selecionar seu próprio intervalo de endereços IP, criar sub-redes e configurar listas de controle de acesso e roteamento para controlar o acesso ao seu banco de dados.
- A funcionalidade básica do Amazon RDS é a mesma, independentemente de você executá-la ou não em uma VPC.
- Geralmente, a instância de banco de dados fica isolada em uma sub-rede privada, e só fica diretamente acessóvel aos aplicativos que você escolher.

## Alta disponibilidade com implantação Multi-AZ

- Um dos recursos mais eficientes do Amazon RDS é a capacidade de configurar sua instância de banco de dados para alta disponibilidade com uma implantação Muti-AZ. 
- Ao configuara uma implantação Multi-AZ, o Amazon RDS gera automaticamente uma cópia esperada da instância de banco de dados em outra zona de disponibilidade dentro da mesma VPC. Após a propagação da cópia do banco de dados as transações são replicadas de forma síncrona para a cópia em espera. 
- A execução de uma instância de banco de dados em uma implantação multi-AC pode aumentar a disponibilidade durante a manuntenção planejada do sistema. E pode ajudar a proteger sua instância de banco de dados se houver alguma interrupção dentro da zona de disponibilidade.
- Se a instância de banco de dados principal falahr em uma implantação Multi-AZ, o Amazon RDS autoamticamente coloca a instância de banco de dados em espera online como a nova instância principal. A replicação síncrona minimiza o pontenicial de perda dos dados. Como aplicativos fazem referência ao banco de dados por nome usando o endpoint do domínio de DNS, não é necessário alterar nada no código do seu aplicativo para usar a cópia em espera para o failover.

## Réplicas de leitura do Amazon RDS 

- Recursos 
    - Oferece replicação assíncrona 
    - Pode ser promovida a mestre, se necessário
- Funcionalidade
    - Use para cargas de trabalho do banco de dados com uso intenso de leitura
    - Descarregar consultas de leitura

## Casos de uso

- Aplicativos web e móveis
    - Alto vazão
    - Escalabilidade de armazenamento massiva
    - Alta disponibilidade
- Aplicativos de comércio eletrônico
    - Banco de dados de baixo custo
    - Segurança de dados
    - Solução totalmente gerenciada
- Jogos para dispositivos móveis e online 
    - Aumente a capacidade rapidamente
    - Escalabilidade automática
    - Monitoramnteo do banco de dados

## Quando usar o Amazon RDS 

- Use o Amazon RDS quando seu aplicativo exigir:
    - Transações ou consultas comlpexas
    - Uma taxa de consulta ou gravação média a alta - Até 30.000 IOPS (15.000 leituras + 15.000 gravações)
    - Não mais do que um único nó de operdor ou fragmento 
    - Alta durabilidade

- NÃO USE o Amazon RDS quando seu aplicativo exigir:
    - Taxas massivas de leitura/gravação (por exemploi, 150.000 gravações/segundo)
    - Fragmentação devido a altas demandas de throughput ou de volume de dados
    - Solicitações e consultas GET ou PUT simples que um banco de dados NoSQL pode processar
    - Personalização de sistema de gerenciamento de banco de dados relacional (RDBMS)

## Amazon RDS: características de banco de dados e faturamento por hora

- Faturamento por hora 
    - Os recursos geram cobranças quando estão em execução 

- Características do banco de dados
    - Capacidade física do banco de dados:
        - Mecanismo 
        - Tamanho
        - Classe de memória

## Amazon RDS: tipo de compra de banco de dados e várias instâncias de banco de dados

- Tipo de compra de banco de dados
    - Instâncias sob demanda
        - Capacidade de computação por hora
    - Instâncias reservadas
        - Pagamento único baixo para instâncias de banco de dados reservados com prazos de 1 ano ou de 3 anos

- Número de instâncias de banco de dados
    - Provisione várias instâncias de banco de dados para lidar com picos de carga

## Amazon RDS: armazenamento 

- Armazenamento provisionado
    - Gratuito
        - Armazenamento de backup de até 100% para um banco de dados ativo
    - Cobrança (GB/mês)
        - Armazenamento de backup para instâncias de banco de dados encerradas
- Armazenamento adicional 
    - Cobrança (GB/mês)
        - Armazenamento de backup além do armazenamento provisionado
    
## Amazon RDS: tipo de implantação e transferência de dados

- Solicitações 
    - O número de solicitações de entrada e saída que são feitas ao banco de dados
- Tipo de implantação "As cobranças de armazenamento e E/S variam, dependendo de você implantar em: 
    - Uma zona de disponibilidade única
    - Várias zonas de dispnibilidade
- Transferência de dados
    - Não há cobrança pela transferência de dados de entrada
    - Faixas de cobrança para transferência de dados de saída

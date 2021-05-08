## Amazon Redshift

- É um data warehouse rápido e gerenciado que torna simples e econômica a análise de todos os seus dados usando ferramentas SQL padrão.

## Introdução ao Amazon Redshift

- Data warehouse pode levar meses e recursos financeiros significativos para ser configurado. 
- O Amazon Redshift é um data warehouse rápido e totalmente gerenciado que é simples e econômico de configurar, usar e escalar.
- O serviço permite executar consultas complexas de análise em petabytes de dados estruturados, usando otimização de consultas sifisticadas, armazenamento colunar em disco locais de alta performance e execução paralela massiva.
- A maioria dos resultados é disponibilizado em alguns segundos.

## Arquitetura de processamento paralelo

- Uma implementação do Amazon Redshift consiste em:
    - Cluster de nós líderes;
    - Cluster de computação;
- O nó líder:
    - Gerencia a comunicação com programas cliente e toda a comunicação com nós de computação.
    - Ele analisa e desenvolve planos de execução para executar a série de etapas necessárias para obter resultados de consultas complexas. 
    - Compila código de elementos individuais do plano de execução e atribui o código aos nós de computação individuais. 
- O nó de computação:
    - Executam o código compilado e reenviam resultaos intermediários ao nó líder para agregação final.
- Assim como em outros serviços da AWS, o Amazon Redshift você paga apenas pelo 

## Automação e escalabilidade 

- Escalabilidade: É possivel escalar os recursos a medida que for utilizando 
- Segurança: É integrada e projetada para fornecer criptografia forte de dados ociosos e em trânsito.

## Compatibilidade 

- É compatível:
    - SQL 
    - Banco de dados Java de alto desempenho
    - Conectores de conectividade de banco de dados abertos
- Você pode fazer essa conexão pela interface de linha de comandos da AWS ou por meio do console da AWS.

## Casos de uso do Amazon Redshift

- Data warehouse corporativo (EDW)
    - Migre a um ritmo confortável para os clientes
    - Experimente sem grandes custos iniciais ou compromissos
    - Responda mais rapidamente às necessidades empresariais
- Big data
    - Preço baixo para clientes pequenos
    - Serviço gerenciado para facilidade de implantação e manutenção 
    - Concentre-se mais nos dados e menos no gerenciamento do banco de dados

## Casos de uso do Amazon Redshift 2

- Sofware como serviço (SaaS):
    - Escale a capacidade do data warehouse à medida que precisar
    - Adicione funcionalidade analítica a aplicativos
    - Reduza os custos de hardware e software
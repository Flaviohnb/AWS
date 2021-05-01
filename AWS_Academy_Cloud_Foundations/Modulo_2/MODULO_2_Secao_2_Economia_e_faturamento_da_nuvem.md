# Economia e Faturamento da nuvem

### O que é o custo total de propriedade (TCO)?

- Custo total de propriedade (TCO) é a estimativa financeira para ajudar a identificar custos diretos e indiretos de um sistema.

- Por que usar o TCO?

    - Para comparar os custos da execução de um ambiente de infraestrutura inteiro ou de um carga de trabalho específica no local em comparação com a AWS;
    - Para criar um orçaento e um caso de negócios para migrar para a nuvem;

- Considerações sobre TCO

    - Custos de servidor:
        - Hardware: servidor, unidades de distribuição de energia (PDUs) do chassi de rack, switches top-of-rack (TOR) (e manuntenção)
        - Software: sistema operacional (SO). licenças de virtualização (e manuntenção)
        - Custos de instalação: Espaço; Energia elétrica; Refrigeração;
    
    - Custos de armazenamento:
        - Hardware: discos de armazenamento, rede de área de armazenamento (SAN) ou switches de canal de fibra (FC);
        - Custos de administração de armazenamento;
        - Custos de instalação: Espaço; Energia elétrica; Refrigeração;
    
    - Custos de rede:
        - Hardware de rede: switches de rede local (LAN), custos de largura de banda do load balancer;
        - Custos de administração de rede;
        - Custos de instalação: Espaço; Energia elétrica; Refrigeração;
    
    - Custo de mão de obra de TI:
        - Custos de administração de servidores;

### Local versus tudo na nuvem

- Você pode economizar até 96% ao ano migrando sua infraestrutura para a AWS. Sua economia totral de 3 anos seria de 159.913 USD.

- Custo de propriedade durante 3 anos:

    - Ambiente Local:
        - Servidor          |   91.922 USD
        - Armazenamento     |   67.840 USD
        - Rede              |   7.660  USD
        - TI - Mão de Obra  |   ------ USD
    - AWS:
        - Servidor          |   2.547  USD
        - Armazenamento     |   4.963  USD
        - Rede              |   ------ USD
        - TI - Mão de Obra  |   ------ USD

    - O custo da AWS inclui suporte de nível empresarial e uma instância PURI de EC2 de 3 anos.

### Calcularoda Mensal da AWS

- http://calculator.s3.amazonaws.com/index.html
    - Estimar custos mensais;
    - Identificar oportunidades para reduzir custos mensais;
    - Use modelos para comparar serviços e modelos de implantação;

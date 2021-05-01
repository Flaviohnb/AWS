# Infraestrutura Global da AWS

- A infraestrutura global da AWS foi projetada e criada para oferecer um ambientede computação em nuvem <b>flexível, confiável, escalável</b> e <b>seguro</b> com <b>desempenho de rede global</b> de alta qualidade.

- Este mapa de <u>infrastructure.aws</u> mostra as regiões atuais da AWS e outras que serão disponibilizados em breve.

## Regiões da AWS

- Uma região da AWS é uma área geográfica.
    - A replicação de dados entre regiões é controlada por você.
    - A comunicação entre regiões usa a infraestrutura de rede backbone da AWS.
- Cada região fornece redundância total e conectividade com a rede.
- Uma região normalmente consiste em duas ou mais zonas de disponibilidade.

## Seleção de uma região 

- Determine a região certa para seviços, aplicativos e dados com base nesses fatores:
    - Governança de dados, requisitos legais;
    - Proximidade com os clientes (latência);
    - Serviços disponíveis na região;
    - Custos (variam por região);

## Zonas de disponibilidade

- Cada <b>região</b> tem várias zonas de disponibilidade.
- Cada <b>zona de disponibilidade</b> pe uma partição totalmente isolada da infraestrutura da AWS.
    - No momento, existem 69 zonas de disponibilidade em todo o mundo;
    - As zonas de disponibilidade consistem em <b>datacenters</b> distintos;
    - Elas são projetadas para isolamento de falhas;
    - Elas são interconectadas a outras zonas de disponibilidade usando redes privadas de alta velocidade;
    - Você escolhe suas zonas de disponibilidade;
    - <b>A AWS recomenda a replicação de dados e recursos entre zonas de disponibilidade</b> para fins de resiliência. 

## Datacenters da AWS

- Os datacenters da AWS são <b>projetados para segurança.</b>
- Os datacenteres são onde os dados residem e o processamento de dados ocorre.
- Cada datacenter tem energia, redes e conectividade redundantes e está hospedado em uma instalação separada.
- Normalmente, um datacenter tem de 50.000 a 80.000 servidores físicos.

## Pontos de presença

- A AWS fornece uma rede global de 187 <b>pontos de presença</b>
- Consiste em 176 pontos de <b>presença e 11 pontos</b> de presença de <b>caches regionais</b>
- Usada com o Amazon CloudFront
    - Uma Content Delivery Network (CDN - Rede de entrega de conteúdo) global que entrega conteúdo aos usuários finais com latência reduzida.
- Os pontos de presença de caches regionais usados para conteúdo com acesso pouco frequente.

## Recursos de infraestrutura da AWS

- Elasticidade e estabilidade
    - Infraestrutura elástica; adaptação dinâmica da capacidade;
    - Infraestrutura escalável; adapta-se para acomodar o crescimento;
- Tolerância a falhas
    - Continua funcionando corretamente na presença de uma falha;
    - Redundância integrada de componentes;
- Alta disponibilidade
    - Alto nível de desempenho operacional;
    - Tempo de inatividade mínimo;
    - Sem intervenção humana;
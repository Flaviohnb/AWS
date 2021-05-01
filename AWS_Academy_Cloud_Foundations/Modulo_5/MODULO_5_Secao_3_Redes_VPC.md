## Gateway da Internet

- Um gateway da Internet é um componente da VPC escalável, redundante e altamente disponível que permite a comunicação entre instâncias na VPC e a internet pública. 

- Tem duas finalidades.
    1. Fornecer um destino nas tabelas de rotas da VPC para tráfego de Internet;
    2. Para executar a conversão de endereços de rede para instâncias que receberam endereços IPv4 públicos;

- Para tornar uma sub-rede pública, anexe um gateway da Internet à VPC e adicione uma entrada de rota à tabela de rotas associada à sub-rede.

- Um gateway de conversão de endereços de rede, ou NAT, permite que instâncias em uma sub-rede privada se conectem à Internet ou a outros serviços da AWS. Mas isso impede que a Internet pública inicie uma conexão com essas instâncias.

- Para criar um gateway NAT é necesspario especificar a sub-rede pública em que ele ficará ativo. É também necessário especificar um endereço IP elástico para associá-lo ao gateway NAT ou criá-lo. 

- Depois de criar um gateway NAT, você deverá atualizar a tabela de rotas associada a uma ou mais de suas sub-redes privadas para apontar o tráfego vinculado à Internet para o gateway NAT. Isso permitirá que as instâncias em suas sub-redes privadas se comuniquem com a Internet. Você também pode usar uma instância NAT em uma sub-rede pública em sua VPC, em vez de uma gateway NAT. No entando, a AWS recomenda que você use um gateway NAT em vez de uma instância NAT pois um gateway NAT é um serviço gerenciado que fornece melhor disponibilidade, maior largura de banda e menos esforço administrativo. 

## Compartilhamento da VPC

- Permite que clientes compartilhem sub-redes com outras contas da AWS na mesma organização.

- Permite que várias contas da AWS criem recursos de aplicativos como instâncias do Amazon EC2, Amazon Relational Database Services, clusters do Amazon Redshift e funções do AWS Lambda em uma VPC compartilhada e gerenciada centralmente. 

- Nesse modelo, a conta proprietária da VPC compartilha uma ou mais sub-redes com outras contas chamadas de participantes que pertencem à mesma organização. Depois que uma sub-rede é compartilhada, os participantes podem visualizar, criar, modificar e excluir seus recursos de aplicativo nas sub-redes compartilhadas 

## Emparelhamento de VPC

- Você pode conectar VPCs em sua própria conta da AWS, entre contas da AWS ou entre regiões da AWS

- Restrições
    - Espaços IP não podem ser sobrepor;
    - O emparelhamento transitivo não é compatível;
    - Você pode ter apenas um recurso de emparelhamento entre as mesmas duas VPCs;

## AWS Site-to-Site VPN

- Por padrão, as instâncias que você executa em uma Amazon VPC não podem ser comunicar com sua própria rede remota. 

- Você pode habilitar o acesso à rede remota a partir da VPC anexando um gateway privado virtual à VPC, criando uma tabela de rotas personalizada, atualizando as  regras do grupo de segurança, criando uma conexão VPN de site a site da AWS e configurando o roteamento para passar o tráfego para a conexão.

## AWS Direct Connect

- Um dos desafios da rede na comunicação é o desempenho da rede.

- Performance:
    - Consequencia negativa: O datacenter estiver localizado longe da região da AWS. Como solução a AWS oferece o AWS Direct Connect permite estabelecer uma conexão privada dedicada entre a rede e um dos locais de conexão direta. Essa conexão privada pode aumentar a largura de banda e o throughput, além de fornecer uma experiência de rede mais consistente do que as conexões baseadas na Internet ou as conexões VPN. 

- O Direct Connect usa redes de área local virtuais 802.1q padrão aberto.

## VPC Endpoints

- Às vezes, você precisará conectar os recursos da VPC a serviços regionais da AWS, como Amazon S3 e DynamoDB.

- VPC endpoint é um dispositivo virtual que permite que você conecte sua VPC de forma privada a esses serviços da AWS compatíveis

- Dois tipos de endpoints:
    - Endpoints da interface (desenvolvidos pelo AWS PrivateLink);
    - Endponits do gateway (Amazon S3 e Amazon DynamoDB);

- AWS PrivateLink
    - Ele requer um endponint de interface VPC. Ele simplifica a segurnaça dos dados compartilhados com aplicativos baseados na nuvem, eliminando a exposição dos dados à Internet pública. 
    - Fornece conectividade privada entre VPCs, serviços da AWS e aplicativos locais.

## AWS Transit Gateway

- 
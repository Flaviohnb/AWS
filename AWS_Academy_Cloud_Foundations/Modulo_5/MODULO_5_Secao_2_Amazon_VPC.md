## Amazon VPC

- Permite provisionar uma seção isolada logicamente da Nuvem AWS onde você pode executar recursos da AWS em uma rede virtual que você mesmo define;

- Fornece controle sobre seus recursos de rede virtual, incluindo:
    - Seleção do intervalo de endereços IP;
    - Criação de sub-redes;
    - Configuração de tabelas de rotas e gateways de rede;

- Permite personalizar a configuração de rede para sua VPC;

- Permite usar várias camadas de segurança;

## VPCs e sub-rede 

- VPCs:
    - Logicamente isoladas de outras VPCs;
    - Dedicadas à sua conta da AWS;
    - Pertencem a uma única região da AWS e podem abranger várias zonas de disponibilidade;

- Sub-redes:
    - Intervalo de endereços IP que dividem uma VPC;
    - Pertencem a uma única zona de disponibilidade;
    - Classificadas como públicas (acesso direto a internet) ou privadas;

## Endereçamento IP

- Ao criar uma VPC, você a atribui um bloco CIDR IPv4 (intervalo de endereços IPv4 privados).
- Você não pode alterar o intervalo de endereços depois de criar a VPC;
- O maior tamanho de bloco CIDR IPv4 é /16;
- O menor tamanho de bloco CIDR IPv4 é /28;
- O IPv6 também é compatível (com um limite de tamanho de bloco diferente);
- Os blocos CIDR de sub-redes não podem se sobrepor.

x.x.x.x/16 ou 65.536 endereços (máximo) to x.x.x.x/28 ou 16 endereços (mínimo)

## Endereços IP reservados

- Exemplo: uma VPC com um bloco CIDR IPv4 de 10.0.0.0/16 tem 65.536 endereços IP no total. A VPC tem quatro sub-redes de tamanho igual. Somente 251 endereços IP estão disponíveis para uso por cada sub-rede.

VPC -> 10.0.0.0/16

Sub-rede 1 (10.0.0.0/24) 251 endereços IP -> Reservado para: Endereço de rede 
Sub-rede 2 (10.0.1.0/24) 251 endereços IP -> Reservado para: Comunicação interna
Sub-rede 3 (10.0.2.0/24) 251 endereços IP -> Reservado para: Resolução do Domain Name System (DNS)
Sub-rede 4 (10.0.3.0/24) 251 endereços IP -> Reservado para: Endereço de transmissão de rede

## Tipos de endereços IP públicos

- Endereço IPv4 público
    - Atribuído manualmente por meio de um endereço IP elástico
    - Atribuído automaticamente por meio das configurações de endereço IP público de atribuição automática no nível da sub-rede

- Endereço IP elástico
    - Associado a uma conta da AWS
    - Pode ser alocado e remapeado
    - Custos adicionais podem ser aplicados

## Interface de rede elástica

- Uma interface de rede elástica é uma interface de rede virtual que você pode:
    - Anexar a uma instância
    - Separar da instância e anexar a outra instância para redirecionar o tráfego de rede
- Seus atributos a seguem quando são reanexadas a uma nova instância
- Cada instância em sua VPC tem um interface de rede padrão que recebe um endereço IPv4 privado do intevalo de endereços IPv4 de sua VPC

## Tabelas de rotas e rotas

- Uma tabela de rotas contém um conjunto de regras (ou todas) que você pode configurar para direcionar o tráfego de rede da sub-rede
- Cada rota especifica um destino e um destino
- Por padrão, toda tabela de rotas contém uma rota local para comunicação dentro da VPC
- Cada sub-rede deve estar associada a uma tabela de rotas (no máximo uma)

## 
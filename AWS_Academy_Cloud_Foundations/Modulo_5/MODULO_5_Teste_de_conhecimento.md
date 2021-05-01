## 1 - Com a Amazon Virtual Private Cloud (Amazon VPC), qual é a menor sub-rede que você pode ter em uma VPC? (Selecione a melhor resposta.)

- A. /24
- B. /30
- C. /26
- <u>D. /28</u> 

R: A menor sub-rede que você pode ter em uma VPC é /28.

## 2 - Com a Amazon Virtual Private Cloud (Amazon VPC), qual é o maior intervalo de endereços IP que você pode ter em uma VPC? (Selecione a melhor resposta.)

- A. /30
- B. /28
- <u>C. /16</u>
- D. /24

R: O maior intervalo de endereços IP que você pode ter em uma VPC é /16

## 3 - Você precisa permitir que os recursos em uma sub-rede privada acessem a Internet. Qual das opções a seguir deve estar presente para permitir esse acesso? (Selecione a melhor reposta.)

- <u>A. Gateway NAT</u>
- B. Tabelas de rotas
- C. Listas de controle de acesso de rede
- D. Grupos de segurança 

R: Se você precisa permitir que os recursos em uma sub-rede privada acessem a Internet, um gateway NAT deve estar presente para permitir esse acess.

## 4 - Qual serviço de rede da AWS permite que uma empresa crie uma rede virtual dentro da AWS? (Selecione a melhor reposta.)

- <u>A. Amazon Virtual Private Cloud (Amazon VPC)</u>
- B. AWS Direct Connect
- C. Amazon Route 53
- D. AWS Config

R: O Amazon Virtual Private Cloud permite que uma empresa crie uma rede virtual dentro da AWS.

## 5 - Verdadeiro ou Falso? Sub-redes privadas têm acesso direto à Internet.

- A. Verdadeiro
- <u>B. Falso</u>

R: Sub-redes privadas não têm acesso direto à Internet.

## 6 - Qual componente da Infraestrutura global da AWS o Amazon CloudFront usa para garantir a entrega de baixa latência? (Selecione a melhor reposta.)

- A. Regiões da AWS
- <u>B. Pontos de presença da AWS</u>
- C. Zonas de disponibilidade da AWS
- D. Amazon Virtual Private Cloud (Amazon VPC)

R: Para garantir a entrega de baixa latência, o Amazon CloudFront usa pontos de presença da AWS.

## 7 - Qual das opções a seguir é um controle de segurança opcional que pode ser aplicado na camada de sub-rede de uma VPC? (Selecione a melhor reposta.)

- <u>A. Network ACL</u>
- B. Firewall de aplicativos Web
- C. Grupo de segurança
- D. Firewall

R: Uma network ACL é um controle de segurança opcional que pode ser aplicado na camada de sub-rede de uma VPC.

## 8 - O que acontece quando você usa a Amazon Virtual Private Cloud (Amazon VPC) para criar uma nova VPC? (Selecione a melhor reposta.)

- A. Três sub-redes são criadas por padrão em uma zona de disponibilidade.
- B. Três sub-redes são criadas por padrão: um para cada zona de disponibilidade.
- <u>C. Uma tabela de rotas principal é criada por padrão.</u>
- D. Um gateway da Internet é criado por paddrão.

R: Quando você cria uma VPC, uma tabela de rotas é criada por padrão. Você deve criar manualmente sub-redes e um gateway da Internet.

## 9 - Qual das opções a seguir pode ser usada para proteger instâncias do Amazon Elastic Compute Cloud (Amazon EC2) hospedadas na AWS? (Selecione a melhor reposta.)

- A. AMI
- B. Todas as opções anteriores
- C. Gateway da Internet
- <u>D. Grupo de segurança</u>

R: Um grupo de segurança atua como um firewall virtual da instância para controlar o tráfego de entrada e saída. 

## 10 - Você é um arquiteto de soluções que trabalha em uma grande empresa de varejo que está migrando a infraestrutura existente para a AWS. Você recomenda que eles usem uma VPC personalizada. Ao criar uma VPC, você a atribui a um bloco de roteamento entre domínios sem classe (CIDR) IPv4 10.0.1.0/24 (que tem um total de 256 endereços IP). Quantos endereços IP estão disponíveis? (Selecione a melhor reposta.)

- <u>A. 251</u>
- B. 256
- C. 250
- D. 246

R: A sub-rede tem 256 endereços IP, mas apenas 251 estão disponíveis porque 5 estão reservados.

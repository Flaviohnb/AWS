## Adicionar tags

- Uma tag é um rótulo que você atribui a um recurso da AWS
    - Consiste em uma chave e um valoropcional
- A marcação é como você pode anexar metadados a uma instância do EC2
- Benefícios potenciais da marcação: filtragem, automação, alocação de custos e controle de acesso

## 8 Configurações do grupo de segurança

- Um grpo de segurança é um conjunto de regras de firewall que controlam o tráfego para a instância
    - Ele existe fora do sistema operacional convidade da instância
- Crie regras que especifiquem a origem e as portas que comunicações de rede podem usar
    - Especifique o número da porta e o protocolo, como Transmission Control Protocol (TCP), User Datagram Protocol (UDP) ou Internet Control Message Protocol (ICMP).
    - Especifique a origem (por exemplo, um endereço IP ou outro grupo de segurança) com permissão para usar a regra

## 9 Identificar ou criar o par de chaves

- Na execução da instância, você especifica um par de chaves existente ou cria um novo par de chaves
- Um par de chaves consiste em
    - Uma chave pública que a AWS armazena
    - Um arquivo de chave privada que você armazena
- Ele permite conexões seguras com a instância
- Para AMIs do Windows
    - Use a chave privada para obter a senha de administrados necessária para fazer login em sua instância
- Para AMIs do Linux
    - Use a chave privada para usar SSH para se conectar com segurança à sua instância

## Outra opção: executar uma instância do EC2 com a interface de linha de comando da AWS

- As instância do EC2 também podem ser criadas de forma programática
- Esta exemplo mostra como o comando pode ser simples
    - Esse comando pressupõe que o par de chaves e o grupo de segurança já existem
    - É possível especificar mais opções. Consulte a "referência de comandos da CLI da AWS" para obter detalhaes

- Exemplo de comando:
`aws ec2 run-instances --image-id ami-1a2b3c4d --count 1 --instance-type c3.large --key-name MyKeyPair --security-groups MySecurityGroup --region us-east-1`

## Considere o uso de um endereço IP elástico

- A reinicialização de uma instância não alterará endereços IP ou nomes de host DNS.
- Se você precisar de um endereço IP público persistente
    - Associe um endereço IP elástico à instância
- Quando uma instância é interrompida e, em seguida, reiniciada
    - O endereço IPv4 público e o nome do host DNS externo serão alterados
    - O endereço IPv4 privado e o nome do host DNS interno não são alterados
- Características do endereço IP elástico
    - Pode ser associado a instâncias na região, conforme necessário
    - Permanece alocado à sua conta até que você opte por liberá-la

## Metadados da instância do EC2

- Metadados da instância são dados sobre sua instância
- Enquanto estiver conectado à instância, você poderá visualizá-la
    - Em um navegador: `http://169.254.169.254/latest/meta-data/`
    - Em uma janela de terminal: `curl http://169.254.169.254/latest/metada-data/`
- Exemplo de valores recuperáveis
    - Endereço IP público, endereço IP privado, nome de host público, ID de instância, grupos de segurança, região, zona de disponibilidade
    - Todos os dados do usuário especificados na execução da instância também podem ser acessados em: `http://169.254.169.254/latest/user-data/`
- Ele pode ser usado para configurar ou gerenciar uma instância em execução
    - Por exemplo, crie um script de configuiração que leia os metadados e use-o para definir aplicativos ou configurações de sistema operacional

## Amazon CloudWatch para monitoramento

- Use o Amazon CloudWatch para monitorar instâncias do EC2
    - Fornece métricas quase em tmpo real
    - Fornece gráficos na guia Monitoramento do console do Amazon EC2 que você pode visualizar 
    - Mantém 15 meses de dados históricos
- Monitoramento básico
    - Padrão, sem custo adicional
    - Dados de métrica enviados para o CloudWacth a cada 5 minutos
- Monitoramento detalhado
    - Taxa mensal fixa para sete métricas pré-selecionadas
    - Dados de métricas entregues a cada 1 minuto

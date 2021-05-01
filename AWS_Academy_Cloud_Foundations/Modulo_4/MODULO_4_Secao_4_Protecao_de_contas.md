## AWS Organizations

- O AWS Organizations permite consolidar várias contas da AWS para que você as gerencie de maneira centralizada

- Recursos de segurança do AWS Organizations
    - Agrupe contas da AWS em unidades organizacionais (OUs) e anexe políticas de acesso diferentes a cada OU
    - Integração e suporte para o IAM
        - As permissões para um usuário são a interseção do que é permitido pelo AWS Organizations e o que é concedido pelo IAM nessa conta
    - Use políticas de controle de serviço para estabelecer controle sobre os serviços da AWS e as ações de API que cada conta da AWS pode acessar

## AWS Organizations: políticas de controle de serviço

- As políticas de controle de serviço (SCPs) oferecem controle centralizado sobre contas
    - Limite as permissões disponíveis em uma conta que faça parte de uma organização

- Garante que as contas estejam em conformidade com as diretrizes de controle de acesso

- As SCPs são semelhantes às políticas de permissões do IAM
    - Elas usam uma sintaxe semelhante
    - No entanto, uma SCP nunca concede permissões
    - Em vez disso, as SCPs especificam as permissões máximas para uma organização

## AWS Key Management Service (AWS KMS)

- Recursos do AWS Key Management Service (AWS KMS)
    - Permite criar e gerenciar chaves de criptografia
    - Permite controlar o uso da criptografia nos serviços da AWS e nos aplicativos
    - Integra-se ao AWS CloudTrail para registrar todo o uso de chaves
    - Usa módulos de segurança de hardware (HSMs) validados pelo Federal Information Processing Standards (FIPS) 140-2 para proteger chaves

## Amazon Cognito 

- Recursos do Amazon Cognito
    - Adicionar inscrição, login e controle de acesso de usuários a aplicativos Web e móveis
    - Ajusta a escala até milhões de usuários
    - Oferece suporte a login com provedores de identidade social, como Facebook, Google e Amazon, e provedores de identidade corporativa, como o Microsoft Active Directory por meio do Security Assertion Markup Language (SAML) 2.0.

## AWS Shield

- Recursos do AWS Shield
    - É um serviço gerenciado de proteção contra negação de serviço dstribuída (DDoS)
    - Protege aplicativos executados na AWS
    - Fornece detecção sempre ativada e mitigações automáticas em linha
    - AWS Shiel Standard habilitdo sem custo adicional. O AWS Shield Advanced é um serviço pago opcional.

- Use-o para minimizar o tempo de inatividade e a latência do aplicativo


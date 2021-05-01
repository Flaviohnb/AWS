## Criptografia de dados em repouso

- A criptografia codifica dados com uma chave secreta, o que os torna ilegíveis
    - Somente quem tem a chave secreta pode decodificar os dados
    - O AWS KMS pode gerenciar suas chaves secretas

- A AWS oferece suporte à criptografia de dados em repouso
    - Dados em repouso = dados armazenados fisicamente (em disco ou fita)
    - Você pode criptografar dados armazenados em qualquer serviço compatível com o AWS KMS, incluindo:
        - Amazon S3
        - Amazon EBS
        - Amazon Elastic File System (Amazon EFS)
        - Bancos de dados gerenciados do Amazon RDS

## Criptografia de dados em trânsito

- Criptografia de dados em trânsito (dados em movimentação por uma rede)
    - Transport Layer Security (TLS), anteriormente SSL, é um protocolo de padrão aberto
    - AWS Certificate Manager oferece uma maneira de gerenciar, implantar e renovar certificados TSL ou SSL

- O HTTP seguro (HTTPS) cria um túnel seguro
    - Ele usa TSL ou SSL para a troca bidirecional de dados

- Os serviços da AWS oferecem suporte à criptografia de dados em trânsito
    - Exemplo:
        - [Nuvem AWS - Amazon EC2] <- Tráfego de dados, criptografado com TSL-> [Nuvem AWS - Amazon EFS]
        - [Datacenter corporativo - AWS Storage Gateway] <- TSL ou SSL criptografado -> [Nuvem AWS - Amazon S3]
    
## Proteção de buckets e objetos do Amazon S3

- Os buckets e objetos do S3 recém-criados são privados e protegidos por padrão

- Quando os casos de uso exigem o compartilhamento de objetos de dados no Amazon S3
    - É essencial gerenciar e controlar o acesso aos dados
    - Siga as permissões que respeitam o princípio do privilégio do mínimo e considere o uso da criptografia do Amazon S3

- Ferramentas e opções para controlar o acesso aos dados do S3 incluem
    - Recurso Amazon S3 Block Public Access: simples de usar
    - Políticas do IAM: uma boa opção quando o usuário pode autenticar usando o IAM
    - Políticas de buckets
    - Listas de controle de acesso (ACLs): um mecanismo de controle de acesso herdado
    - Verificação de permissão de bucket do AWS Trusted Advisor: um recurso gratuito

## 
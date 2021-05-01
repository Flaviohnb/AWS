## AWS Identity and Access Management (IAM)

- Use o IAM para gerenciar o acesso aos recursos da AWS:
    - Um recurso é uma entidade em uma conta da AWS com a qual você pode trabalhar; 
    - Exemplo de recursos: uma instância do Amazon EC2 ou um bucket do Amazon S3;

- Exemplo: controle quem pode encarrar instâncias dos Amazon EC2;

- Defina direitos de acesso refinados:
    - Quem pode acessar o recurso;
    - Quais recursos podem ser acessados e o que o usuário pode fazer com o recurso;
    - Como os recursos podem ser acessados;

- O IAM é um recurso de conta da AWS gratuito;

## IAM: Componentes essenciais

- Uma pessoa ou aplicativo que pode se autenticar com uma conta da AWS;
- Uma coleção de usuários do IAM que recebem autorização idêntica;
- O documento que define quais recursos podem ser acessados e o nível de acesso a cada recurso;
- Mecanismo útil para conceder um conjunto de permissões para fazer solicitações de serviço da AWS;

## Autenticar como um usuário do IAM para obter acesso

- Acesso programático:
    - Autentique usando:
        - ID ou chave de acesso;
        - Chave de acesso secreta;
    - Fornece acesso à CLI e ao SDK da AWS;

- Acesso ao Console de Gerenciamento da AWS:
    - Autentique usando:
        - ID ou alias da conta com 12 dígitos;
        - Nome de usuário do IAM;
        - Senha do IAM;
    - Se ativada, a Multi-Factor Authentication (MFA) solicita um código de autenticação.

## MFA do IAM

- A MFA oferece maior segurança;
- Além do nome de usuário e da senha, a MFA requer um código de autenticação exclusivo para acessar os serviços da AWS;

## Autorização: quais ações são permitidas

- Depois que o usuário ou o aplicativo estiver conectado à conta da AWS, o que ele poderá fazer?
    
    - Usuário do IAM, grupo do IAM ou função do IAM 
        - Acesso total     
            - Instâncias do EC2
        - Somente leitura  
            - Bucket do S3

## IAM: autorização

- Atribua permissões criando uma política do IAM;
- As permissões determinam quais recrusos e operações são permitidos:
    - Todas as permissões são implicitamente negadas por padrão;
    - Se algo for explicitamente negado, nunca será permitido;
- <b>Prática recomendada:</b> siga o princípio do privilégio mínimo;

*OBS: o escopo das configurações de serviço do IAM  é global. As configurações se aplicam a todas as regiões da AWS;
    
## Políticas do IAM

- Uma política do IAM é um documento que define permissões
    - Habilita um controle de acesso refinado;
- Dois tipos de políticas: baseadas em identidade e em recurso
- Políticas baseadas em identidade
    - Anexe uma política a qualquer entidade do IAM
        - Um usuário do IAM, um grupo do IAM ou uma função do IAM
    - As políticas especificam:
        - Ações que podem ser executadas pela entidade;
        - Ações que não podem ser executadas pela entidade;
    - Uma única política pode ser anexada a várias entidades;
    - Uma única entidade pode ter várias políticas anexadas a ela;
- Políticas baseadas em recursos
    - Anexadas a um recurso (como um bucket do S3);

## Exemplo de política do IAM

```
{
    "Version": "2012-10-17",
    "Statement":[{
        "Effect":"Allow",
        "Action":["DynamoDB:*","s3:*"],
        "Resource":[
            "arn:aws:dynamodb:region:account-number-witout-hyphens:table/table-name",
            "arn:aws:s3:::bucket-name",
            "arn:aws:s3:::bucket-name/*]
        },
        {
            "Effect":"Deny",
            "Action":["dynamodb.*","s3:*"],
            "NotResource":["arn:aws:dynamodb:region:account-number-without-hyphens:table-name",
                "arn:aws:s3:::bucket-name",
                "arn:aws:s3:::bucket-name/*]
        }
    ]
}
```

- Uma permissão explícita (`"Effect":"Allow"`) oferece aos usuários acesso a uma tabela específica (`/table-name`) do DynamoDB e...
- Uma negação explícita (`"Effect":"Deny"` e `"NotResource"`) garante que os usuários não possam usar nenhuma outra ação ou recurso da AWS que não seja essa tabela e esses buckets;
- Uma instrução de negação explícita tem precedência sobre uma instrução de permissão;

## Políticas baseadas em recursos

- As políticas baseadas em identidade são anexadas a um usuário, um grupo ou uma função;
- As políticas baseadas em recursos são anexadas a um recurso (não a um usuário, um grupo ou uma função);
- Características das políticas baseadas em recursos:
    - Especificam quem tem acesso ao recurso e quais ações podem ser executadas nele;
    - As políticas são apenas em linha, não gerenciadas;
- As políticas baseadasd em recursos são compatíveis apenas com alguns serviços da AWS;

## Permissões do IAM

- A permissão é explicitamente negada?
    - Sim -> Negação
    - Não
        - A permissão é explicitamente permitida?
            - Sim -> Permissão
            - Não -> Negação (negação implícita)

## Grupos do IAM

- Um grupo do IAM é um conjunto de usuários do IAM;
- Um grupo é usado para conceder as mesmas permissões a vários usuários
    - Permissões concedidas ao anexar política ou políticas do IAM ao grupo;
- Um usuário pode pertencer a vários grupos;
- Não há grupo padrão;
- Os grupos não podem ser aninhados;

## Funções do IAM 

- Uma função do IAM é uma identidade do IAM com permissões específicas 
- Semelhante a um usuário do IAM
    - Anexe políticas de permissões a ela
- Diferente de um usuário do IAM
    - Não associada exclusivamente a uma pessoa
    - Destinada a ser assumida por uma pessoa, um aplicativo ou um serviço
- A função fornece credenciais de segurança temporárias
- Exemplos de como as funções do IAM são usadas para delegar acesso
    - Usada por um usuário do IAM na mesma conta da AWS que a função
    - Usada por um serviço da AWS, como o Amazon EC2, na mesma conta que a função
    - Usada por um usuário do IAM em uma conta da AWS diferente da função

## Exemplo de uso de uma função do IAM

- Cenário:
    - Um aplicativo executado em uma instância do EC2 precisa de acesso a um bucket do S3

- Solução:
    - Defina uma política do IAM que conceda acesso ao bucket do S3;
    - Anexe a política a uma função;
    - Permita que a instância do EC2 assuma a função;

    
## Acesso de usúario raiz da conta da AWS em comparação ao acesso do IAM

- Práticas recomendada: não use o usuário raiz da conta da AWS, exceto quando necessário.
    - O acesso ao usuário raiz da conta requer o login com o endereço de e-mail (e a senha) que você usou para criar a conta.

- Ações para criar a conta
    - Atualizar a senha do usuário raiz da conta
    - Alterar o plano do AWS Support
    - Restaurar as permissões de um usuário do IAM
    - Alterar as configurações da conta (por exemplo, informações de contato, regiões permitidas)

## Proteção de novas contas da AWS: usuário raiz da conta

- Etapa 1: Parar de usar o usuário raiz da conta o mais rápido possível
    - O usuário raiz da conta tem acesso irrestrito a todos os seus recursos

- Para parar de usar o usuário raiz da conta:
    1. Enquanto estiver conectado como o usuário raiz da conta, crie um usuário do IAM para você mesmo. Salve as chaves de acesso, se necessário
    2. Crie um grupo do IAM, atribua a ele permissões completas de administrador e adicione o usuário do IAM do grupo
    3. Desabilite e remova as chaves de acesso do usuário raiz da conta, se elas existirem
    4. Habilite uma política de senha para usuários
    5. Faça login com as convas credenciais de usuário do IAM
    6. Armazene as credenciais de usuário raiz da sua conta em um local seguro

## Proteção de novas contas da AWS: MFA

- Etapa 2: Habilitar Multi-Factor Authentication (MFA)
    - Exija MFA para o usuário raiz da sua conta e para todos os usuários do IAM
    - Você também pode usar a MFA para controlar o acesso às APIs de serviço da AWS

- Opções para recuperar o token de MFA 
    - Aplicativos compatíveis com MFA virtual
        - Google Authenticator
        - Authy Autheticator (aplicativo Windows Phone)
    - Dispositivos de chave de segurança U2F
        - Por exemplo, YubiKey
    - Opções de MFA de hardware
        - Chaveiro ou cartão de exibição oferecido pela Gemalto

## Proteção de novas conta da AWS: AWS CloudTrail

- Etapa 3: Usar o AWS CloudTrail
    - O CloudTrail rastreia as atividades dos usuarios em sua conta
        - Ele registra todas as solicitações de API para recursos em todos os serviços compativeis da sua conta
    - O historico basico de eventos da AWS CloudTrail é habilitado por padrão e gratuito
        - Ele tambem contem todos os dados de eventos de gerenciamento nos ultimos 90 dias de atividade da conta

- Para acessar o CloudTrail
    1. Faça login con Console de Gerenciamento da AWS e escolha os serviço CloudTrail
    2. Clique em Event history (Historico de eventos) para visualizar, filtrar e pesquisar os ultimos 90 dias de eventos

- Para habilitar logs alem de 90 dias e habilitar alertas de eventos especificados, crie uma trilha
    1. Na pagina CloudTrail Console trails (Trilhas do console do CloudTrail), clique em Create trail (criar trilha)
    2. Atribua um nome a ela, aplique-a todas as regiões e crie um novo bucket do Amazon S3 para armazenamento de logs
    3. Configure restrições de acesso no bucket do S3 (por exemplo, somente usuários admin devem ter acesso)

## Proteção de novas contas da AWS: relátorios de faturamento 

- Etapar 4: Habilitar um relatório de faturamento, como o relatório de custos e uso da AWS
    - Os relatórios de faturamento oferecem informações sobre o uso dos recursos da AWS e os curstos estimados para esse uso
    - A AWS entrega os relatórios para o bucket do Amazon S3 que você especifica
        - O relatório é atualizado pelo menos uma vez por dia
    - O relatório de custos e uso da AWS monitora seu uso da AWS e fornece cobrnaças estimadas associadas à sua conta da AWS por hora ou por dia

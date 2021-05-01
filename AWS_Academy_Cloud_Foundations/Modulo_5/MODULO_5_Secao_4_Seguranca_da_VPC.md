## Grupos de segurança

- Os grupos de segurança atuam no nível da instância;
- Os grupos de segurança têm regras que controlam o tráfego de instâncias de entreda e saída;
- Os grupos de segurança padrão negam todo o tráfego de entrada e permitem todo o tráfego de saída;
- Os grupos de segurança são stateful;

## Listas de controle de acesso à rede (ACLs de rede)

- As ACLs de rede atuam no nível da sub-rede;

## ACLs de rede 

- Uma ACL de rede tem regras de entrada e saída separadas, e cada regra pode permitir ou rejeitar tráfego;
- As ACLs de rede padrão permitem todo o tráfego IPv4 de entrada e saída;
- As ACLs de rede são stateless;

## Comparação entre grupos de segurança a ACLs de rede

- Atributo: Escopo
    - Grupo de segurança: Nível de instância 
        - ACLs de rede: Nível de sub-rede
- Atributo: Regras compatíveis 
    - Grupo de segurança: Permitir somente regras
        - ACLs de rede: Regras de permissão e negação
- Atributo: Estado
    - Grupo de segurança: Stateful (o tráfego de retorno é permitido automaticamente, independentemente das regras)
        - ACLs de rede: Stateless ( o tráfego de retorno deve ser explicitamente permitido pelas regras)
- Atributo: Ordem das regras
    - Grupo de segurança: Todas as regras são avaliadas antes da decisão de permitir o tráfego
        - ACLs de rede: As regras são avaliadas em ordem numérica antes da decisão de permitir tráfego                
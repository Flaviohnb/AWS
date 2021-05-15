## Porque a escalabilidade é importante?

- Escalabilidade é a capacidade de aumentar ou diminuir a capacidade computacional de seu aplicativo.

## Amazon EC2 Auto Scaling

- Ajuda a manter a disponibilidade do aplicativo
- Permite adicionar ou remover automaticamente instâncias do EC2 de acordo com as condições que você define
- Detecta instâncias do EC2 danificadas e aplicativos não íntegros e substitui as instâncias sem sua intervenção
- Fornece várias opções de escalabilidade 
    - Manual
    - Programada
    - Dinâmica
    - Sob demanda 
    - Preditiva

## Grupos de Auto Scaling

- Um grupo de Auto Scaling é um conjunto de instâncias do EC2 que são tratadas como um agrupamento lógico para fins de escalabilidade automática e gerenciamento.

## Comoo funciona o Amazon EC2 Auto Scaling

- 1º Especifica "O QUE"
    - Configuração de execução
        - AMI
        - Tipo de instância 
        - Função do IAM
        - Grupos de segurança
        - Volumes do EBS
- 2º "ONDE"
    - Grupo de Auto Scaling
        - VPC e sub-redes
        - Load Balancer
- 3º "QUANDO"        
    - Manter o número
        - Verificações de integridade
    - Escalabilidade manual
        - Capacidade mínima, máxima e desejada
    - Escalabilidade programada
        - Ações programadas
    - Escalabiliade dinâmica
        - Políticas de escalabilidade
    - Escalabilidade preditiva
        - AWS Auto Scaling

## AWS Auto Scaling

- Monitora os aplicativos e ajusta automaticamente a capacidade para manter uma performance constante e previsível pelo menor custo possível
- fornece uma interface de usuário simples e eficiente que permite criar planos de escalabilidade para recursos do, incluindo:
    - Instâncias do Amazon EC2 e frotas spot
    - Tarefas do Amazon Elastic Container Service (Amazon ECS)
    - Índices e tabelas do Amazon DynamoDB
    - Réplicas do Amazon Aurora

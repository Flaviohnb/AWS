## Monitoramento de recursos da AWS

- Para usar a AWS com eficiência, você precisa de informações sobre seus recrusos da AWS:
    - Como você sabe quando deve executar mais instâncias do Amazon EC2?
    - A performance ou a disponibilidade do seu aplicativo estão sendo afetadas por falta de capacidade suficiente?
    - Quanto da infraestrutura está realmente sendo usada?

## Amazon CloudWatch

- Monitora
    - recursos da AWs
    - Apliativos executados na AWs
- Coleta e rastreia
    - Métricas padrão
    - Métricas personalizadas
- Alarmes
    - Enviar notificações para um tópico do Amazon SNS
    - Executar ações do Amazon EC2 Auto Scaling ou do Amazon EC2
- Eventos 
    - Definir regras de acordo com as alterações no ambiente da AWS e rotear esses eventos para um ou mais fluxos ou funções de destino para processamento

## Alarmes do CloudWatch

- Criar alarmes com base no 
    - Limite estático
    - Detecção de anomalias
    - Expressão matemática de métricas
- Especificar
    - Namespace
    - Métrica
    - Estatística
    - Período
    - Condições
    - Configuração adicional
    - Ações

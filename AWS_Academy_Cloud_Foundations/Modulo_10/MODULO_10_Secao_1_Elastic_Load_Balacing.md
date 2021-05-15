## Elastic Load Balancing

- Distribui o tráfego de entrada do aplicativo ou da rede entre vários destinos em uma única zona de disponibilidade ou em várias zonas de disponibilidade.
- Escala seu load balancer à medida que o tráfego para seu aplicativo muda com o tempo.

## Tipos de load balancers


- Application Load Balancer
    - Balanceamento de carga avançado de tráfego HTTP e HTTPS
    - Roteia o tráfego para os destinos co mbase no conteúdo da solicitação
    - Fornece roteamento avançado de solicitações direcionado para a entrega de arquiteturas de aplicativos modernas, incluindo microserviços e contêineres
    - Opera na camada de aplicativo (camada 7 do modelo OSI)
- Network Load Balancer
    - Balanceamento de carga de tráfego TCP, UDP e TLS em que haja necessidade de uma performance exepcional
    - Roteia o tráfego para os destinos com base nos dados do protocolo IP
    - Pode processar milhões de solicitações por segundo e ainda manter latências ultrabaixas
    - É otimizado para lidar com padrões de tráfego súbitos e voláteis
    - Opera na camada de transporte (camada 4 do modelo OSI)
- Classic Load Balancer (geração anterior)
    - Balanceamento de carga de tráfego HTTP, HTTPS, TCP e SSL
    - Balancemento de carga entre várias instâncias do EC2
    - Opera nas camas de aplicativo e transporte

## Como o Elastic Load Balancing funciona

- Com Application Load Balancers e Network Load Balancers, você registra destinos em grupos de destino, e roteia o tráfego para os grupos de destino.
- Com Classic Load Balancers, você registra instâncias com o load balancer.

## Casos de uso de Elastic Load Balancing

- Aplicativos altamente disponíveis e tolerantes a falhas
- Aplicativos em contêineres
- Elasticidade e escalabilidade
- Virtual Private Cloud (VPC)
- Ambientes híbridos
- Invocar funções do Lambda por HTTP(S)

## Monitoramento do load balancer

- Métricas do Amazon CloudWatch
    - Usadas para verificar se o sistema está funcionando conforme o esperado e cria um alarme para iniciar uma ação se uma métrica sair de um intervalo aceitável.
- Logs de acesso 
    - Capture informações detalhadas sobre solicitações enviadas ao load balancer
- Logs AWS CloudTrail
    - Capture quem, o que, quando e onde das interações de API nos serviços da AWS

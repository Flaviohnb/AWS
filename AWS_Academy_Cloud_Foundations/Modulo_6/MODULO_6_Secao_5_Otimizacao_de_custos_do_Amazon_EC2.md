## Modelos de definição de preço do Amazon EC2

- Instâncias sob demanda
    - Pagamento por hora
    - Não há compromissos em longo prazo
    - Qualificado para o nível gratuito AWS
- Instâncias reservadas
    - Pagamento integral, parcial ou nenhum pagamento adiantado para a instância reservada
    - Desconto na cobrança por hora para essa instância 
    - Prazo de 1 ou 3 anos
- Instâncias spot
    - As instâncias são executadas desde que estejam dosponíveis e sua sugestão de preço esteja acima do preço da instância spot
    - Elas podem ser interrompidas pela AWS com uma notificação de 2 minutos
    - As opções de interrupção incluem encerrado, interrompido ou hibernado
    - Os preços podem ser bem menores em comparação às instâncias sob demanda
    - Boa escolha quando você tem flexibilidade no momento em que seus aplicativos podem ser executados
- Host dedicados
    - Um servidor físivo com capacidade de instância do EC2 totalmento dedicada a seu uso
- Instâncias dedicadas
    - Instâncias que são executadas em uma VPC de um harware dedicado a um único cliente
- Instâncias reservadas programadas
    - Compre uma reserva de capacidade que esteja sempre disponível em uma programação recorrente que você especificar

## Modelos de definição de preço do Amazon EC2: benefícios

- Instâncias sob demanda
    - Baixo custo e flexibilidade
- Instâncias spot
    - Carga de trabalho dinâmica e em grande escala
- Instâncias reservadas
    - A previsibilidade garante que a capacidade computacional esteja disponível quando necessário
- Hosts dedicados
    - Economize dinheiro com custos de licenciamento
    - Ajude a cumprir os requisitos regulatórios e de conformidade

## Modelos de definição de preço do Amazon EC2: casos de uso

- Instâncias sob demanda
    - Cargas de trabalho de curto prazo, com picos ou imprevisíveis
    - Desenvolvimento ou teste de aplicativos
- Instâncias spot
    - Aplicações com horários de início e término flexíveis
    - Aplicações que são viáveis somente por preços computacionais muito baixos
    - Usuários com necessidades computacionais urgentes para grandes quantidades de capacidade adicional
- Instâncias reservadas 
    - Carga de trabalho de uso constante ou previsível
    - Aplicativos que exigem capacidade reservada, incluindo recuperação de desastres
    - Os usuários podem fazer pagamentos prévios pra reduzir ainda mais o total dos custos computacionais
- Hosts dedicados
    - Traga a sua própria licença (BYOL)
    - Conformidade e restrições normativas
    - Rastreamento de uso e licenciamento
    - Controlar posicionamento de instâncias

## Os quatro pilares da otimização de custos

- Tamanho certo
- Aumente a elasticidade
- Modelo de definição de preço ideal
- Otimizar opções de armazenamento

## Pilar 1: Tamanho certo

- Provisione instâncias de acordo com a necessidade
    - Taxa de transferência de CPU, memória, armazenamento e rede
    - Selecione os tipos de instância apropriados para seu uso
- Métricas do Amazon CloudWatch
    - Até que ponto as instâncias estão ociosas? Quando?
    - Reduzir instâncias
    - Prática recomenada: tamanho certo e reserva

## Pilar 2: Aumentar a elasticidade

- Interrompa ou hiberne instâncias baseadas no Amazon EBS que não estã em uso ativamente 
    - Exemplo: instâncias de desenvolvimento ou teste que não sejam de produção
- Use a escalabilidade automática para atender às necessidades com base no uso
    - Elasticidade automatizada e baseada em tempo

## Pilar 3: Modelo de definição de preço ideal

- Aproveite o modelo de definição de preço correto para seu caso de uso
    - *Considere seus padrões de uso
- Otimizar e combinar tipos de compra
- Exemplo:
    - Usar instância sob demanda e instâncias spot para cargas de trabalho variáveis
    - Usar instância reservada para cargas de trabalho previsíveis
- Considere soluções sem servidor (AWS Lambda)

## Pilar 4: otimizar opções de armazenamento

- Reduza custos e mantenha a performance e a disponibilidade do armazenamento
- Redimensionar volumes do EBS
- Alterar tipos de volume do EBS
    - Você pode atender aos requisitos de performance com armazenamento mais barato?
    - Exemplo: o armazenamento HDD otimizado para throughput (st1) do Amazon EBS normalmente custa metade do que a opção de armazenamento padrão General Purpose SSD (gp2)
- Excluir snapshots do EBS que não são mais necessários
- Identificar o destino mais apropriado para tipos específicos de dados
    - O aplicativo precisa que a instância resida no Amazon EBS?
    - As opções de armazenamento do Amazon S3 com políticas de ciclo de vida podem reduzir custos

## Meça, monitore e melhore

- A otimização de custo é um esforço permanente
- Recomendações
    - Defina e imponha a marcação de alocação de custos
    - Defina métricas, defina destinos e revise regularmente
    - Incentive as equipes a projetar custos
    - Atribua a responsabilidade da otimização a um indivíduo ou a uma equipe

## AWS Lambda: execute código sem servidores

- O AWS Lambda é um serviço de computação sem servidor.

- 1
   - Faça upload do seu código
- 2 
   - O código que você executa é uma função Lambda
   - Execute seu código em uma programação ou em reposta a eventos
- 3 
   - Seu código é executado somente quando é acionado
- 4
   - Pague somente pelo tempo de computação que você usar

## Benefícios do Lambda

- Oferece suporte a várias linguagens de programação
- Administração totalmente automatizada
- Tolerância a falaes integrada
- Oferece suporte à orquestração de várias funções
- Pay-per-use a definição de preço

## Fontes de eventos do AWS Lambda

- Configure outros serviços da AWS como fontes de eventos para invocar sua função, conforme mostrado aqui. 
- Como alternativa, invoque uma função do Lambda no console do Lambda, no SDK da AWS ou na CLI da AWS

## Configuração da função do AWS Lambda

- Ao usar o Console de Gerenciamento da AWS para criar uma função do Lambda
- 1º - o primeiro passo é atribuir um nome a ela
- 2º - especifique o ambiente de tempo de execução
- 3º - você configura a funação, e as configurações incluem a adição de um trigger que é onde você especifica uma fonte de evento disponível
- 4º - você também precisa adicionar o código da função, use o editor de código fornecido o Lambda ou você também pode fazer upload de um arquivo que contenha seu código. Você deve especificar a memória em megabytes a ser alocada à sua função, e isso é de até 3.008 megabytes. Opcionalmente vocÊ também pode adicionar variaveis de ambiente como tempos limite, a VPC específica na qual executar a função e outras  
- Todas as confuguyrações recém-mencionadas são colocadas em um pacote de implantação do Lambda, que é um arquivo zip que contém o código da função e as dependências. Quando você uso o console do Lambda para criar sua função, o console gerencia o pacote para você. No entando, se você precisar criar um pacote de implantação se usar a API do Lambda para gerenciar as funçõs, precisará fazer isso por conta própria.

## Exeplo de função Lambda baseada em programção: Iniciar e interromper instância do EC2

- Exemplo de interrupção de instâncias:
    - 1º. Evento do CloudWatch baseado em tempo
    - 2º. Função do Lambda acionada
    - 3º. Instâncias EC2 interrompidas
- Exemplo de iniciar instâncias:
    - 4º. Evento do CloudWatch
    - 5º. Função do Lambda acionada
    - 6º. Instâncias do EC2 iniciadas

## Exemplo de função Lambda baseada em eventos: Criar imagens em miniatura

- 1º. Usuário
- Nuvem AWS
    - 2º. Bucket de origem
    - 3º. Lambda
    - 4º Função de execução
    - Política de acesso
    - 5º. Função Lambda
    - 6º. Bucket de destino

## Limites do AWS Lambda

- Limites flexíveis por região
    - Execuções simultâneas = 1.000
    - Função e armazenamento de camadas = 75 GB
- Limites rígidos para funções individuais
    - Alocação máxima de memória da função = 3.008 MB
    - Tempo limite da função = 15 minutos
    - Tamanho do pacote de implantação = 250 MB descompactados, incluindo camadas
- Limites adicionais também existem. Os detalhes estão na documentação de limites do AWS lambda

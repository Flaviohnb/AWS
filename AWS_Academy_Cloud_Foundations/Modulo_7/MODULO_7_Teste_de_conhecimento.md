## Exemplo de pergunta do exame - Uma empresa deseja armazenar dados que `não são acessados com frequência.` Qual é a melhor `solução econômica` que deve ser considerada?

- A. AWS Storage Gateway
- `B. Amazon Simple Storage Service Glacier`
- C. Amazon Elastic Block Storage (Amazon EBS)
- D. Amazon Simple Storage Service (Amazon S3)

## 1 - Verdadeiro ou Falso? O Amazon Simple Storage Service (Amazon S3) é um armazenamento de objetos adequado para o armazenamento de arquivos simples, como documentos do Microsoft Word, fotos, etc.

- `Verdadeiro` 
- False

R: É verdadeiro que o S3 é um armazenamento de objetos adequado para arquivos "simples", como documentos do Word, fotos, etc.

## 2 - O Amazon S3 replica todos os objetos ______. (Selecione a melhor reposta)

- em vários volumes dentro de uma zona de disponibilidade
- `em várias zonas de disponibilidade na mesma região`
- entre várias regiões para maior durabilidade
- em vários buckets do S3

R: O S3 replica todos os objetos em várias zonas de disponibilidade dentro da mesma região.

## 3 - Qual das opções a seguir pode ser usada como uma classe de armazenamento para uma política de ciclo de vida de objetos do S3? (Escolha três alternativas)

- `S3 - Acesso padrão` 
- AWS Storage Gateway
- `S3 - Acesso infrequente`
- `Simple Storage Service Glacier`
- S3 - Armazenamento de redundância reduzida 
- Amazon Dynamo DB

R: Glacier, S3 Acesso infrequente e S3 Acesso padrão podem ser usados como uma classe de armazenamento para uma política de ciclo de vida de objetos do S3.

## 4 - O nome de um bucket do S3 deve ser exclusivo ____________.

- `em todo o mundo e em todas as contas da AWS.`
- dentro de uma região 
- em todas as suas contas da AWS
- em sua conta da AWS

R: O nome de um bucket do S3 deve ser exclusivo em todo o mundo em todas as contas da AWS.

## 5 - Você pode usar o Amazon Elastic File System (Amazon EFS) para: (Selecione a melhor reposta)

- fornece armazenamento de arquivos simples, escalável e elástico para uso apenas na AWS.
- `implementar armazenamento para instâncias do Amazon EC2 que várias máquinas virtuais podem acessar ao mesmo tempo.`
- hospedar uma CDN robusta para entregar sites inteiros com conteúdo dinâmico, estático e de streaming.
- gerar conteúdo específico do usuário.

R: Você pode usar o EFS para implementar armazenamento em instâncias do EC2 que várias máquians virtuais podem acessar ao mesmo tempo.

## 6 - O Amazon Elastic Block Store (Amazon EBS) é recomendado quando os dados _____ e _____. (Escolha duas alternativas.)

- requerem armazenamento no nível do objeto.
- `devem ficar rapidamente acessíveis, exigindo persistência de longo prazo.`
- `requerem uma solução de criptografia.`
- precisam ser armazenados em uma zona de disponibilidade diferente daquela em que a instância do EC2 está 

R: O Amazon EBS é recomendade quando os dados devem ser acessíveis rapidamente, exigindo persistência de longo prazo e uma solução de criptografia.

## 7 - Verdadeiro ou Falso? Por padrão, todos os dados armazenados no Amazon S3 podem ser visualizados pelo público.

- Verdadeiro
- `Falso`

R: Por padrão, todos os dados armazenados no S3 não podem ser visualizados pelo público.

## 8 - Em relação ao Amazon S3 Glacier, o que é um cofre? (Selecione a melhor reposta)

- As regras que determinam quem pode (ou não) acessar arquivos
- Um objeto (fotos, vídeos, arquivos ou documentos)
- `Um contêiner para armazenar arquivos`
- Uma política que identifica quem pode acessar o conteúdo armazenado no Glacier

R: O cofre no Amazon Glacier é um contâiner para armazenar arquivos.

## 9 - Verdadeiro ou Falso? Quando você cria um bucket no Amazon S3, ele é associado a uma região específica da AWS.

- `Verdadeiro`
- Falso

R: Quando você cria um bucket no Amazon S3, ele é associado a uma região específica da AWS.

## 10 - Quais das opções a seguir são recursos do Amazon Elastic Block Store (Amazon EBS)? (Escolha duas alternativas.)

- `Os volumes do Amazon EBS podem ser criptografados de forma transparente para workloads na instância anexada.`
- `Os dados armazenados no Amazon EBS são replicados automaticamente dentro de uma zona de disponibilidade`
- Os dados do Amazon EBS são copiados automaticamente em fite
- Os dados em um volume do Amazon EBS são perdidos quando a instância anexada é interrompida

R: Os volumes do Amazon EBS persistem quando a instância é interrompida. Os dados são replicados automaticamente dentro de uma zona de disponibilidade, podem ser criptografados na criação e usados por uma instância, como se não tivessem sido criptografados.




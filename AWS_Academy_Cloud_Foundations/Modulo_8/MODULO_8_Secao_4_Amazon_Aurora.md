## Amazon Aurora 

- Banco de dados relacional de nível empresarial
- Compatível com MySQL ou PostgreSQL
- Automatize tarefas demoradas: 
    - provisionamento
    - correção
    - backup
    - recuperação
    - detecção de falhas
    - reparo

## Benefícios do serviço Amazon Aurora

- Serviço gerenciado
- Veloz e confiável
- Simples
- Compatível
- Pagamento conforme o uso

## Alta disponibilidade

- Aurora atinge alta disponibilidade armazenando várias cópias de seus dados em diferentes zonas de disponibilidade.
- O backup dos dados é feito continuamente no Amazon S3.
- Você pode usar até 15 réplicas de leitura com o Amazon Aurora para melhorar significativamente o desempenho de casos de uso de leitura elevados. Isso também reduz a possibilidade de perder seus dados.

## Projeto resiliente 

- Foi projetado para recuperação instantânea de falhas se o banco de dados principal se tornar não íntegro.
- Após uma falha no banco de dados, o Amazon Aurora não precisa reproduzir o log do último ponto de verificação do banco de dados. Em vez disso, ele executa isso em cada operação de leitura. Isso reduz o tempo de reinicialização após uma falha de banco de dados para menos de 60 segundos na maioria dos casos. 
- A arquitetura remove o cache do buffer do processo do banco de dados, é por isso que o buffer fica disponível imediatamente após uma reinicialização. Isso significa que você não precisa controlar o acesso após uma falha enquanto aguarda que o cache seja preenchido novamente.

## Bancos de dados relacionais versus não relacionais

- Relacional (SQL)
    - Armazenamento de dados: Linhas e colunas
    - Esquema: Fixo
    - Consulta: Usa SQL
    - Escalabilidade: Vertical
    - Exemplo: 
        - ISBN: 3111111223439
            - Título: Withering Depths
            - Autor: Jackson, Mateo
            - Formato: Brochura
        - ISBN: 3122222223439
            - Título: Wily Wily
            - Autor: Wang, Xiulan
            - Formato: Ebook
- Não relacional
    - Armazenamento de dados: Chave-valor, documento, grafo
    - Esquemas: Dinâmico
    - Consulta: Focado na coleta de documentos
    - Escalabilidade: Horizontal
    - Exemplo: 
        {
            ISBN: 3111111223439,
            Título: "Withering Depths",
            Autor: "Jackson, Mateo",
            Formato: "Brochura"
        }

## O que é o Amazon DynamoDB?

- Serviço de banco de dados NoSQL rápido e fléxivel para qualquer escala
    - Tabelas de banco de dados NoSQL
    - Armazenamento praticamente ilimitado
    - Os itens podem ter atributos diferentes
    - Consultas de baixa latência
    - Vazão de leitura/gravação escalável

## Componentes principais do Amazon DynamoDB

- Tabelas, itens e atributos são os principais componentes do DynamoDB
- O DynamoDB oferece suporte a dois tipos diferentes de chaves primárias: 
    - Chave de partição 
    - Chave de partição e de classificação

## Os itens em uma tabela devem ter uma chave 

- Chave única
    - Chave de partição + Atributos 

- Chave composta
    - Chave de partição + Chave de classificação + Atributos

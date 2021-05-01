## Resolução de DNS do Amazon Route 53

- Processo de converter um nome interno para o endereço IP correspondente;
- O protocoo DNS significa Domain Name System (Sistema de nome de domínio) e funciona como uma agenda telefônica em que os nomes da Internet são substituídos pelos endereços IP das máquinas correspondentes;

## Amazon Route 53 

- É um servidor Web do Domain Name System (DNS) altamente disponível e escalável;
- É usado para rotear usuários finais para aplicativos da Internet ao traduzir nomes (como www.exemplo.com) em endereços IP numéricos (como 192.0.2.1) que os computadores usam para se conectarem uns aos outros;
- É totalmente compatível com IPv4 e IPv6;
- Conecta solicitações de usuários à infraestrutura executada na AWS e também fora da AWS;
- É usado para verificar a integridade de seus recursos;
- Recursos de fluxo de tráfego;
- Permite registrar nomes de domínio;

## Roteamento compatível com o Amazon Route 53

- Roteamento simples: use em ambientes de servidor único;
- Roteamento ponderado Round Robin: atribua pesos a conjuntos de registros de recursos para especificar a frequência;
- Roteamento de latência: ajude a melhorar seus aplicativos globais;
- Roteamento de localização geográfica: roteie o tráfego com base na localização de seus usuários;
- Roteamento de geoproximidade: roteie o tráfego com base na localização de seus recursos;
- Roteamento de failover: faça failover para um site de backup se o site principal se tornar inacesível;
- Roteamento de resposta com valores múltiplos: responda a consultas DNS com até oito registro íntegros selecionados aleatoriamente;

## Failover de DNS do Amazon Route 53

- Melhore a disponibilidade dos aplicativos executados na AWS:
    - Configurando cenários de backup e failover para seus próprios aplicativos;
    - Habilitando arquiteturas multirregião altamente disponíveis na AWS;
    - Criação de verificações de integridade;

## 
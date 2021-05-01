## Redes 

- Um rede de computadores são duas ou mais máquinas conectadas juntas para se comunicar;
- Uma rede pode ser particionada logicamente em sub-redes;
- A rede requer um dispositivo de rede como um roteador ou um switch. Isso conecta todas as máquinas e permite a comunicação entre elas;

## Endereços IP

192.0.2.0 - IPv4 (32 bits)

192 -> 11000000
0   -> 00000000
2   -> 00000010
0   -> 00000000

2600:1f18:22ba:8c00:ba86:a05e:a5ba:00FF - IPv6 (128 bits)

- Cada máquina na rede tem um endereço exclusivo de Internet Protocol atribuído a uma máquina para identificá-la de forma exclusiva;
- Um endereço de IP é semelhante a um número de telefone. Ele precisa ser exclusivo;
- Cada numero é representado por um valor máximo de 8 bits, significa que um dos 4 números pode ser de 0 a 255, combinando um endereço de (32 bits - IPv4), também existem endereços (128 bits - IPv6); 

## Roteamento sem classe entre domínios (CIDR)

`192.0.2.0/24`

- Identificador de rede (prefixo de roteamento)
    - 192   -> 11000000 -> FIXO
    - 0     -> 00000000 -> FIXO
    - 2     -> 00000010 -> FIXO

- Identificador do host
    - 0     -> 00000000 para 11111111 -> FLÉXIVEL

- Informa quantos bits estão fixos
    - 24
               
##  Modelo Open System Interconnection (OSI - Interconexão de sistemas abertos)

- Camada: Aplicativo
    - Número: 7 
        - Função: Meios para um aplicativo acessar uma rede de computadores
            - Protocolo/endereço: HTTP(S), FTP, DHCP, LDAP
- Camada: Apresentação
    - Número: 6
        - Função: Garante que a camada do aplicativo possa ler os dados; Criptografia
            - Protocolo/endereço: ASCI, ICA
- Camada: Sessão
    - Número: 5
        - Função: Permite a troca ordenanda de dados
            - Protocolo/endereço: NetBIOS, RPC
- Camada: rede/
    - Número: 4 
        - Função: Fornece protocolos para oferecer suporte à comunicação host a host
            - Protocolo/endereço: TCP, UDP
- Camada: Rede
    - Número: 3
        - Função: Roteamento e encaminhamento de pacotes (roteadores)
            - Protocolo/endereço: IP
- Camada: Link de dados
    - Número: 2 
        - Função: Transferir dados na mesma rede LAN (hubs e switches)
            - Protocolo/endereço: MAC
- Camada: Físico
    - Número: 1
        - Função: Transmissão e recepção de fluxo de bits bruts em um meio físico
            - Protocolo/endereço: Sinais (1s e 0s)


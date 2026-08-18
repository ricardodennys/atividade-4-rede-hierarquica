# Atividade 4 — Rede Hierárquica no Cisco Packet Tracer
## Descrição da configuração

A rede foi organizada em três camadas: núcleo, distribuição e borda/acesso.

A camada de núcleo é formada pelos switches CORE_1 e CORE_2. A camada de distribuição é formada pelos switches DIST_1 e DIST_2. A camada de borda/acesso é formada pelos switches EDGE-1, EDGE-2, EDGE-3 e EDGE-4.

O roteador Router0 possui duas interfaces FastEthernet. A interface FastEthernet 0/0 está conectada ao CORE_1 e a interface FastEthernet 0/1 está conectada ao CORE_2.

Os switches de núcleo estão conectados aos switches de distribuição, formando caminhos redundantes para uma futura agregação de links. Os switches de distribuição estão conectados aos switches de borda sem redundância na camada de acesso.

Foram conectados quatro computadores desktop, quatro notebooks e um servidor, todos por cabos de rede. O servidor está conectado ao EDGE-4.

## Endereçamento IP

Foi utilizada a rede 192.168.10.0/24, com máscara 255.255.255.0. Os dispositivos finais receberam endereços IP individuais e a comunicação foi testada com o comando ping.

O teste realizado entre o PC0 e o Server0 apresentou 0% de perda de pacotes.

## Arquivos do repositório

- Arquivo da topologia física do Packet Tracer.
- Arquivo da topologia com endereçamento IP.
- Imagem do diagrama da rede.

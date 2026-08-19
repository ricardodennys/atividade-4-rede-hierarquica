Avaliação 04 – Prática de Simulação de Ambiente Hierárquico
Aluno: Ricardo Dennys Soares de Souza
Disciplina:  Comutação de redes locais
Atividade: Avaliação 04 (trabalho)
Data: 19/08/2026

1. Objetivo
Esta atividade apresenta a configuração inicial de uma rede hierárquica desenvolvida no Cisco Packet Tracer. A topologia foi organizada em três camadas: núcleo, distribuição e borda/acesso, de acordo com as características funcionais de cada camada.

Nesta etapa foram realizadas somente as ligações físicas entre os equipamentos. Não foram configurados endereços IP, VLANs, roteamento ou agregação de links.

2. Estrutura hierárquica
A rede foi dividida da seguinte forma:

Camada
Equipamentos
Função na topologia
Núcleo
CORE_1 e CORE_2
Formar o núcleo de alta velocidade e concentrar as ligações principais
Distribuição
DIST_1 e DIST_2
Interligar o núcleo aos switches de borda/acesso
Borda/Acesso
EDGE_1, EDGE_2, EDGE_3 e EDGE_4
Conectar os dispositivos finais à rede
3. Equipamentos utilizados
Foram utilizados os seguintes equipamentos:

    • 1 roteador Cisco 2811;
    • 2 switches Cisco 3650-24PS na camada de núcleo;
    • 2 switches Cisco 3650-24PS na camada de distribuição;
    • 4 switches Cisco 2960-24TT na camada de borda/acesso;
    • 4 computadores desktop;
    • 4 notebooks;
    • 1 servidor.

4. Ligações do roteador
O roteador Router0 foi conectado aos dois switches de núcleo por meio de suas duas interfaces FastEthernet:

Router0 FastEthernet0/0 ↔ CORE_1
Router0 FastEthernet0/1 ↔ CORE_2

As conexões foram realizadas com cabos de cobre apropriados para a ligação entre o roteador e os switches. O roteador possui uma ligação individual para cada switch de núcleo, conforme solicitado no enunciado.

5. Ligação entre os switches de núcleo
Os switches CORE_1 e CORE_2 foram interligados por quatro enlaces físicos utilizando interfaces GigabitEthernet. Esses enlaces foram preparados para uma futura agregação de links com capacidade planejada de 4 Gbps.

A agregação não foi configurada nesta etapa, pois a atividade solicita apenas a montagem física do cenário.

CORE_1 GigabitEthernet ↔ CORE_2 GigabitEthernet
CORE_1 GigabitEthernet ↔ CORE_2 GigabitEthernet
CORE_1 GigabitEthernet ↔ CORE_2 GigabitEthernet
CORE_1 GigabitEthernet ↔ CORE_2 GigabitEthernet

6. Ligações entre núcleo e distribuição
Os switches de núcleo foram conectados individualmente aos switches correspondentes da camada de distribuição por meio de interfaces ópticas:

CORE_1 ↔ DIST_1: dois enlaces físicos de fibra óptica
CORE_2 ↔ DIST_2: dois enlaces físicos de fibra óptica

Os dois enlaces em cada par foram preparados para uma futura agregação de links com capacidade planejada de 2 Gbps. A configuração do link aggregation não foi realizada nesta etapa.

7. Ligações da camada de borda/acesso
Os quatro switches de borda foram conectados à camada de distribuição sem utilização de redundância:

DIST_1 ↔ EDGE_1
DIST_1 ↔ EDGE_2
DIST_2 ↔ EDGE_3
DIST_2 ↔ EDGE_4

Cada switch de borda possui somente um enlace de subida para a camada de distribuição, atendendo ao requisito de não utilizar recurso de redundância nesta atividade.

8. Dispositivos finais
Os dispositivos finais foram distribuídos entre os switches de borda e conectados por cabos de rede:

Switch
Dispositivos conectados
EDGE_1
PC0 e Laptop0
EDGE_2
PC1 e Laptop1
EDGE_3
PC2 e Laptop2
EDGE_4
PC3, Laptop3 e Server0
Ao todo, foram conectados quatro computadores desktop, quatro notebooks e um servidor.

9. Configurações não realizadas
Para atender ao escopo desta etapa, não foram realizados:

    • endereçamento IP;
    • criação ou configuração de VLANs;
    • configuração de roteamento;
    • configuração de EtherChannel ou outro mecanismo de agregação;
    • configuração de redundância nos switches de borda.

Foram realizadas apenas as ligações físicas necessárias para deixar a topologia preparada para as próximas etapas.

10. Diagrama da rede



11. Arquivo do Packet Tracer
O arquivo da simulação está disponível neste repositório:

## 11. Arquivos do Packet Tracer

O arquivo principal da simulação, contendo a topologia física, está disponível abaixo:

arquivo da topologia física (Atividade4_Rede_Hierarquica_fisica.pkt)

Como etapa complementar, também foi disponibilizada a versão com endereçamento IP:

(Atividade4_Rede_Hierarquica_ip.pkt)
https://github.com/ricardodennys/atividade-4-rede-hierarquica/blob/main/Atividade4_Rede_Hierarquica_fisica.pkt 


12. Conclusão
A topologia construída apresenta uma organização hierárquica visível, com separação entre as camadas de núcleo, distribuição e borda/acesso. A estrutura física foi preparada para futuras agregações de 4 Gbps entre os switches de núcleo e de 2 Gbps entre os pares núcleo–distribuição, mantendo os dispositivos finais conectados com fio e os switches de borda sem redundância.

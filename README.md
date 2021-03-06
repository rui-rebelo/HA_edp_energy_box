# Âmbito

A integração entre os contadores inteligentes com sistemas de domótica permite potenciar automações, controlo e análises com base na informação disponível das grandezas elétricas. Nomeadamente, tensão, intensidade de corrente, potência ativa, fator de potência, frequência, estado do disjuntor controlador de potência, *et al*.

A EDP Distribuição S.A. surge neste contexto enquanto Operadora da Rede de Distribuição de baixa tensão. Independentemente do comercializador de energia elétrica com quem tem contrato de fornecimento e de estar em mercado regulado ou liberalizado.


# Objetivo

Pretende-se partilhar uma prova de conceito da possível integração entre dispositivos EDP Energy Box marca Janz, modelo C3801, com um HUB de domótica a executar [Home Assistant Core](https://www.home-assistant.io/).

Esta integração é possível, graças à porta de comunicação HAN que está disponível internamente nos contadores inteligentes.

**`A porta de comunicação HAN está no interior das EDP Energy Box. A manipulação ou acesso não autorizado a esta porta é da total responsabilidade do próprio.`**

É proposto neste repositório um procedimento para requisitar formalmente o acesso a esta porta.

# Conteúdos

1. [A Energy Box e a sua porta HAN](Energy%20Box/README.md)
   1. [Pedido de acesso](Energy%20Box/README.md#pedido-de-acesso)
   2. [Interface físico](Energy%20Box/README.md#interface-físico)
   3. [Impedância de linha](Energy%20Box/README.md#impedância-de-linha)
   4. [Ligações](Energy%20Box/LIGACOES.md)
   5. [Comunicação](Energy%20Box/COMUNICACAO.md)
2. [Home Assitant Core e a sua configuração](Home%20Assistant/README.md)
   1. [Ficheiro de configuração](Home%20Assistant/README.md#configuração-do-home-assistant-core) 
   2. [Personalizar as entidades geradas](Home%20Assistant/README.md#personalizar-as-entidades-geradas) 
   3. [Aplicação das configurações](Home%20Assistant/README.md#aplicação-das-configurações) 

# Requisitos mínimos

- Acesso exterior à porta HAN, previamente instalado pela EDP Distribuição S.A.;
- Raspberry Pi 3 B+ ou superior (alternativamente, Home Assistant Core em PC, máquina física ou virtualizada em Proxmox);
- Home Assistant Core instalado (versão de prova de conceito: 0.106.6. Recomendada a versão 0.109.6.);
- Conversor USB - TTL vs RS-485;
- Cabo extensor USB (recomendado);
- Acessórios de ligação variados.

# Fontes

[EDP Box - HAN protocol specification (DEF-C44-509/N)](https://www.edpdistribuicao.pt/sites/edd/files/normative_docs/DEF-C44-509.pdf)

[Descrição dos requisitos e respetiva aplicabilidade em função do tipo de módulo HAN](https://www.edpdistribuicao.pt/sites/edd/files/2019-06/Requisitos%20dos%20m%C3%B3dulos%20HAN_2019.05.31.pdf?fbclid=IwAR1txmKfYIbwCae6eR5njlblvvBMB1xiLvp5ynURi9qAW4rsOut3WFfJNQM)

[Contadores de energia elétrica - Especificação funcional (DEF-C44-506/N)](https://www.edpdistribuicao.pt/sites/edd/files/normative_docs/DEF-C44-506N.pdf)

[Novos Equipamentos](https://www.edpdistribuicao.pt/sites/edd/files/2019-04/Novos_Equipamentos.pdf?fbclid=IwAR3zNpBId8BMqrSVaPoekoUvqt-xxstLua4iqZN2qz-8Xf2hvRQqtU8g2xo)


# A fazeres

- [ ] Potência ativa
- [ ] Totalizadores de energia
- [ ] Religação do DCP

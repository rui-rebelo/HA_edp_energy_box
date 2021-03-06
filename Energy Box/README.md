# A porta HAN

## Pedido de acesso

`ATENÇÃO: Não se conhece qualquer obrigação legal ou regulatória do Operador de Rede de Distribuição ter de providenciar este acesso. Portanto, considere como uma eventual cortesia.`

Em primeiro lugar, verifique se o seu contador de energia elétrica consta da seguinte lista de equipamentos com porta HAN: [Novos Equipamentos](https://www.edpdistribuicao.pt/sites/edd/files/2019-04/Novos_Equipamentos.pdf?fbclid=IwAR3zNpBId8BMqrSVaPoekoUvqt-xxstLua4iqZN2qz-8Xf2hvRQqtU8g2xo)

### Caso o seu modelo `NÃO` corresponda exatamente a algum dos supracitados:

Deverá aguardar pela substituição programada do seu contador de energia elétrica, aquando da sua obsolescência total.

### Se o seu modelo `corresponde exatamente` a algum dos supracitados:

O acesso a esta porta requerá um pedido formal à EDP Distribuição S.A., através do endereço: apoiocliente@edpdistribuicao.pt.

Deverá indicar no pedido:

1. Identificação pessoal do titular do contrato de energia elétrica (Nome, NIF, Morada);
2. Código do Ponto de Entrega (CPE). Consta na sua fatura de eletricidade;
3. Questões sobre eventuais custos, condições e procedimentos.

Haverá uma provável deslocação de um técnico especializado à sua instalação para deselagem, instalação de um chicote exterior e nova selagem do contador inteligente.

## Interface físico

Esta prova de conceito é baseada numa Energy Box da marca Janz, modelo C3801 (R4LRFGPRS), com a sua porta HAN ativada e disponível externamente. Exemplo:

![janz_c3801](./img/janz_c3801.png)
> Fonte: edpdistribuicao.pt

A porta de comunicação tem um formato físico RJ12, de 6 pinos e 6 coneções (6P6C):


![rj-12](https://upload.wikimedia.org/wikipedia/commons/3/3c/Rj25_connector.jpg)
> Fonte: wikipedia.com


| # do pino | Função |
|----------|----------|
| 1| GND |
| 2| A+ (não usada) |
| 3| B- |
| 4| B- (não usada) |
| 5| A+ |
| 6| +5 Volt |

A disponibilidade de alimentação a partir da porta HAN está limitada a uma intensidade de corrente máxima de 150 mA. Considerando também que a função primordial da porta HAN é providenciar comunicação de dados, **é altamente recomendável que seja utilizada alimentação dos dispositivos a conectar a partir de uma fonte de alimentação externa.**

## Impedância de linha

A linha de comunicação, representada pelo chicote exterior a instalar pela EDP Distribuição S.A., deverá ser terminada com uma resistência de 120 Ohm, por forma a balancear todo o cirtuito com a impedância do cabo. Essa resistência será em paralelo com os terminais `A+` e `B-` do conversor TTL vs RS-485.

## Mais info

[Voltar](../README.md)

[Como se ligar à porta HAN](./LIGACOES.md)

[Como se comunica com a Energy Box](./COMUNICACAO.md)


# Registradores

Conjunto de flip-flops, são armazenadores de informação. Se armazena 4 bits, possui 4 flip-flops.

Um registrador consiste em um grupo de flip-flops tipo D que atualiza a informação a cada ciclo de clock.

## Registrador de deslocamento

Consiste em inserir os dados na entrada do registrador, respeitando o número de bits, e efetuar o número de pulsos de clock necessários para que todo o dado seja inserido no registrador.  
N ciclos de clock para N números (síncronos ao clock).

**Exemplo:**

Dado 110:

- Din: 1, armazenado: 0, 0, 0 (clock)
- Din: 1, armazenado: 1, 0, 0 (clock)
- Din: 0, armazenado: 1, 1, 0 (clock)
- Din: x, armazenado: 0, 1, 1. (x = próximo dado)

Dado entra serial e termina paralelo.

## Registrador de carga paralela

N bits em 1 pulso de clock. 3 flip-flops e 3 linhas simultâneas.

Pode possuir um controle de clock, pois em um pulso perde-se a informação. Logo, insere-se um controle (*load*) em um mux entre a nova entrada e a antiga, podendo manter uma informação por mais tempo até que *load* mude.

## Conversor paralelo/série (para registrador de deslocamento)

Apresenta PRE e CLEAR, tendo como controle um *enable* que ativa ou não o *preset*. Quando o *enable* estiver ligado, as entradas PRE assumem o valor das entradas paralelas de cada flip-flop.  
Esse controle é feito por um NAND entre o *enable* e a entrada paralela.

Na CPU será necessário o registrador de carga paralela.

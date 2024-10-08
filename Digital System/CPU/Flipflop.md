# Circuitos combinacionais

A saída depende apenas da entrada.

## Circuitos sequenciais

A saída depende das entradas presentes e da história das entradas passadas (armazenadas pelo flip-flop).

## Clock

Um trem de pulsos de onda quadrada, que coloca circuitos sequenciais em sincronismo.

* Flip-flop não sincroniza no patamar pois o período de subida é quase instantâneo, e ele deve acontecer nesse tempo rapidamente. Já no patamar, levaria uma eternidade para o computador.

## Flip-flop

Um tipo de componente eletrônico que guarda um certo dado, funcionando por nível, ou seja, na mudança do clock de 0 para 1, ou de 1 para 0, podendo até mesmo funcionar em ambos.

### D Flip-flop

Armazena em um pulso de clock (ciclo).  
É formado pela entrada de dados (D), o clock (CLK) e a saída.  

**Borda de subida:** !!!Sinal de subida (0 -> 1)!!!  
Obs: não tem bolinha.

Quando o clock está em zero, a saída independe do D, mantendo o que já está naquela posição.  
Porém, com CLK = 1, a saída corresponde ao D, logo:

- Q = 1 se D = 1 
- Q = 0 se D = 0.

!!!Usado para fazer registrador!!!

### T Flip-flop

Chamado assim pois possui modo de comutação.  
Se T = 0 e há borda de subida, mantém-se o dado.  
Porém, se T = 1 e o clock sobe, ele troca a saída:

- Q = Q`
- Q` = Q.

!!!Essencial para construir um contador!!!

## Controles assíncronos dos flip-flops

Flip-flops possuem pinos de controle assíncronos, ou seja, não dependem do clock.  
Exemplos:

- **PRESET ou SET** -> ativado com 1 (PRE/SET = 0)
- **CLEAR** -> ativado com 0 (CLR = 0)

## Aviso

É necessário filtrar os sinais com o *debouncer*, pois esse filtro garante a estabilidade do exercício, absorvendo aproximadamente $2^16$ pulsos em apenas 1. Ele também é utilizado para verificar se a chave está funcionando corretamente.

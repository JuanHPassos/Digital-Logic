# Circuitos Combinacionais e Sequenciais

**Circuitos combinacionais**: A saída depende apenas da entrada.

**Circuitos sequenciais**: Depende das entradas presentes e da história das entradas passadas (armazenadas pelo flip-flop).

## Clock

O clock é um trem de pulsos de onda quadrada que coloca os circuitos sequenciais em sincronismo.

* Flip-flop não sincroniza no patamar pois o período de subida é quase instantâneo, e ele deve acontecer nesse tempo rapidamente. Já no patamar levaria uma eternidade para o computador.

**Flip-flop** é um tipo de componente eletrônico que guarda um certo dado e seu funcionamento se dá por nível, ou seja, na mudança do clock de zero para um, ou de 1 para zero, podendo ser até mesmo para ambos.

### D Flip-flop

Armazena em um pulso de clock (ciclo). É formado pela entrada de dados (D), o clock (CLK) e a saída. 

- **Borda de subida**: !!!Sinal de subida (0 -> 1)!!! obs: não tem bolinha.
- Quando o clock está em zero, a saída independe do D, mantendo o que já está naquela posição. Porém, com CLK = 1, a saída corresponde ao D, logo, Q = 1 se D = 1 e Q = 0 se D = 0.
- !!!Usado para fazer registrador!!!

### T Flip-flop

T porque possui modo de comutação. Se T = 0 e borda de subida, mantém-se o dado, porém se T = 1 e o clock sobe, ele troca a saída Q = Q complemento e Q complemento = Q. 

- !!!Essencial para construir um contador!!!

Flip-flops possuem pinos de controles assíncronos, ou seja, não dependem do clock.

- Exemplo: **PRESET** ou **SET** -> 1 (ativado com 0)
- **CLEAR** -> 0 (ativado com 0)

**Aviso**: É necessário filtrar os sinais com o debouncer, pois esse filtro vai garantir a estabilidade do circuito, absorvendo aproximadamente 2^16 pulsos em apenas 1. Ele também é utilizado para saber se a chave está boa.

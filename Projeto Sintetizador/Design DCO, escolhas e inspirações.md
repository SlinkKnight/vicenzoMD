Nossa jornada começa com O DCO (Digital controlled oscillator), que é, basicamente, um VCO sem aparte de conversão de tensão para corrente. Para este design, vamos utilizar como modelo o DCO do juno-106 da Roland, que é meu preferido.
Como base, foi utilizado o artigo https://blog.thea.codes/the-design-of-the-juno-dco/, que descreve exatamente o funcionamento do DCO, todos os flaws no design e como resolver.


*Figura 1* - Diagram de blocos do Juno-106, extremamente simplificado.
![](../MEDIA/Pasted%20image%2020260322121556.png)
*Fonte:* Artigo que foi mencionado.

Como podemos ver, o CPU tem o feed de um clock, e decide a matemática da frequência com base no input das teclas. Essa frequência é passada por um gerador de rampa analógico, que mistura a precisão digital com a junção analógica. Essa rampa então vai para os waveshapers, que decidem o formato final de maneira analógica.



## O CPU

## O gerador de rampa

*Figura 1* - Arquitetura do gerador de rampa Juno-106
![](../MEDIA/Pasted%20image%2020260322121051.png)
*Fonte:* Manual de serviço do juno-106 (anexo 1), 1984.
*Descrição:* Diagrama de circuito original do oscilador.

Tudo funciona com base naquele amplificador operacional, que funciona em modo 
integrador, ou seja, tende a gerar uma onda linear com uma Vi constante.

![](../MEDIA/Pasted%20image%2020260322123104.png)

Como o intuito do projeto é gerar uma onda dente de serra, e não uma triangular, colocaremos um reset

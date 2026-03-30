-**Tags:** `DCO` `VCO` `juno-106` `roland` `síntese-analógica`

---

## Visão Geral

O **DCO** (Digital Controlled Oscillator) é, basicamente, um VCO sem a parte de conversão de tensão para corrente. Para este design, foi utilizado como modelo o DCO do **Juno-106** da Roland.

O funcionamento do DCO, seus flaws de design e as soluções adotadas estão descritos em detalhes na referência [1].

*Figura 1 — Diagrama de blocos do Juno-106 (simplificado)*
![Diagrama de blocos simplificado do Juno-106](../_MEDIA/Pasted%20image%2020260322121556.png)
*Fonte: [1]*

O CPU recebe o feed de um clock e calcula a frequência com base no input das teclas. Essa frequência é passada por um **gerador de rampa analógico**, que combina a precisão digital com a geração analógica. A rampa resultante segue para os **waveshapers**, que definem o formato final de onda de maneira analógica.

---
## O CPU

*(a preencher)*

---

## O Gerador de Rampa

*Figura 2 — Arquitetura do gerador de rampa do Juno-106*
![Diagrama de circuito do oscilador do Juno-106](../_MEDIA/Pasted%20image%2020260322121051.png)
*Fonte: Manual de serviço do Juno-106 [2], 1984.*

O circuito é baseado em um **amplificador operacional em modo integrador**, que gera uma onda linear a partir de uma tensão de entrada `Vi` constante.

![Diagrama do integrador](../_MEDIA/Pasted%20image%2020260322123104.png)

Como o objetivo é gerar uma **onda dente de serra** (e não triangular), é necessário adicionar um circuito de reset — que descarrega o capacitor do integrador no momento certo, reiniciando a rampa.

---

## Referências

[1] CODES, Thea. *The Design of the Juno DCO*. Disponível em: <https://blog.thea.codes/the-design-of-the-juno-dco/>

[2] ROLAND. *Juno-106 Service Manual*. 1984. Disponível em: <http://www.analoguerenaissance.com/D80017A/juno-serv.pdf>

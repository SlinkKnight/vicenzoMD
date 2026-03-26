**Professor:** Maicon Bandeira
**Tags:** `ladder` `CLP` `portas-lógicas` `timers` `contadores`

---

## Portas Lógicas no MasterTools

### Porta AND

![Diagrama porta AND](../_MEDIA/Pasted%20image%2020260226103621.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   1   |

### Porta OR

![Diagrama porta OR](../_MEDIA/Pasted%20image%2020260226103659.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   1   |

### Porta NOR

![Diagrama porta NOR](../_MEDIA/Pasted%20image%2020260226103804.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   0   |

### Porta NAND

![Diagrama porta NAND](../_MEDIA/Pasted%20image%2020260226103845.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |

### Porta XOR

![Diagrama porta XOR](../_MEDIA/Pasted%20image%2020260226103949.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |

### Porta XNOR

![Diagrama porta XNOR](../_MEDIA/Pasted%20image%2020260226104819.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   1   |

---

## Timers em LADDER

### Timer Delay On (TON)

![Animação Timer Delay On](../_MEDIA/MToolIEC_zEwN1JuMH4.gif)

Timer que **espera** um tempo antes de elevar a saída `Q` ao nível alto.

- **`IN`:** Pulso que inicia o timer.
- **`PT`:** Tempo de preset — formato `T#5S`.
- **`ET`:** Variável de tempo interno (elapsed time).
- **`Q`:** Saída lógica — vai a nível alto após `PT`.

### Timer Delay Off (TOF)

![Animação Timer Delay Off](../_MEDIA/MToolIEC_Z3sKk8gRie.gif)

Timer que **espera** um tempo antes de abaixar a saída `Q`.

- **`IN`:** Pulso que inicia o timer.
- **`PT`:** Tempo de preset — formato `T#5S`.
- **`ET`:** Variável de tempo interno.
- **`Q`:** Saída lógica — vai a nível baixo após `PT`.

### Timer Pulse (TP)

![Animação Timer Pulse](../_MEDIA/MToolIEC_E72H33xe09.gif)

Timer que gera um **pulso de duração fixa** `PT` a partir de um sinal em `IN`.

- **`IN`:** Pulso que inicia o timer.
- **`PT`:** Duração do pulso — formato `T#5S`.
- **`ET`:** Variável de tempo interno.
- **`Q`:** Saída lógica — fica ativa pelo tempo definido em `PT`.

---

## Contadores em LADDER

### Contador UP (CTU)

![Diagrama Contador UP](../_MEDIA/Pasted%20image%2020260312111626.png)

- **`CU`:** Pulso de incremento do contador.
- **`RESET`:** Zera `CV`.
- **`PV`:** Valor limite (threshold) — quando `CV >= PV`, `Q = 1`.
- **`CV`:** Contagem interna.
- **`Q`:** Saída lógica.

### Contador DOWN (CTD)

![Diagrama Contador DOWN](../_MEDIA/Pasted%20image%2020260312111636.png)

- **`CD`:** Pulso de decremento do contador.
- **`LOAD`:** Carrega o valor de `PV` em `CV`.
- **`PV`:** Valor inicial (tipo `INT`).
- **`CV`:** Contagem interna.
- **`Q`:** Saída lógica — nível alto quando `CV = 0`.

### Contador UP/DOWN (CTUD)

![Diagrama Contador UP/DOWN](../_MEDIA/Pasted%20image%2020260312111657.png)

- **`CU`:** Pulso de incremento.
- **`CD`:** Pulso de decremento.
- **`RESET`:** Zera `CV`.
- **`LOAD`:** Carrega o valor de `PV` em `CV`.
- **`PV`:** Valor de referência (tipo `INT`).
- **`CV`:** Contagem interna.
- **`QU`:** Saída incremental — nível alto quando `CV >= PV`.
- **`QD`:** Saída decremental — nível alto quando `CV = 0`.

---

## Exercícios

![PDF Exercícios Contadores e Temporizadores](../_MEDIA/8%20-%20Exercícios%20Contadores%20e%20Temporizadores.pdf)

### A)

![Resolução exercício A](../_MEDIA/Pasted%20image%2020260319090608.png)

### B)

![Resolução exercício B](../_MEDIA/Pasted%20image%2020260319090448.png)

---

## Ligação com o CLP

A declaração de variáveis abaixo indica uma ligação com o CLP, podemos ver o uso da estrutura  **`AT %IX0.3`**, onde `AT = atribuição` e `%IX0.3` indica uma entrada (Input) no "GPIO" 0.3. A saída é indicada pelo `%IQ1.4`, onde Q significa saída no endereço 1.4:

---

![Diagrama de ligação CLP — parte 1](../_MEDIA/Pasted%20image%2020260319101539.png)

![Diagrama de ligação CLP — parte 2](../_MEDIA/Pasted%20image%2020260319101554.png)

> Usamos `Baudrate = 115200` no CLP Altus

---

## Semáforo 2 Tempos

![Diagrama semáforo 2 tempos](../_MEDIA/Pasted%20image%2020260319113410.png)

---
## Semáforo 4 Tempos

![](../MEDIA/Pasted%20image%2020260326110008.png)


![](../MEDIA/Pasted%20image%2020260326105239.png)


![](../MEDIA/MToolIEC_rb10Zgg2tL.gif)

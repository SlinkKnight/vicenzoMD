## Portas lógicas no MasterTools

### Porta AND

![](../MEDIA/Pasted%20image%2020260226103621.png)

| A   | B   | Saída |
| --- | --- | ----- |
| 0   | 0   | 0     |
| 0   | 1   | 0     |
| 1   | 0   | 0     |
| 1   | 1   | 1     |
### Porta OR

![](../MEDIA/Pasted%20image%2020260226103659.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   1   |
### Porta NOR

![](../MEDIA/Pasted%20image%2020260226103804.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   0   |
### Porta NAND

![](../MEDIA/Pasted%20image%2020260226103845.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |
### Porta XOR

![](../MEDIA/Pasted%20image%2020260226103949.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |
### Porta XNOR

![](../MEDIA/Pasted%20image%2020260226104819.png)

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   1   |
## Timer em LADDER

### Timer delay on

![](../MEDIA/MToolIEC_zEwN1JuMH4.gif)

* **TON:** Timer que ESPERA para elevar Q ao alto.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
### Timer delay off!

![](../MEDIA/MToolIEC_Z3sKk8gRie.gif)

* **TON:** Timer que ESPERA para abaixar.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
### Timer pulse

![](../MEDIA/MToolIEC_E72H33xe09.gif)

* **TON:** Timer que faz um pulso de X segundos.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
## Contadores em LADDER

### Contador UP

![](../MEDIA/Pasted%20image%2020260312111626.png)

* **CU:** Pulso de incremento do contador.
* **RESET:** Leva CV a 0.
* **PV:** Threshold, quando CV >= a PV, Q = 1.
* **CV:** Contagem interna.
* **Q:** Saida lógica.

### Contador DOWN

![](../MEDIA/Pasted%20image%2020260312111636.png)

* **CD:** Pulso de decremento do contador.
* **LOAD:** Passa o valor de PV para CV.
* **PV:** Valor INT.
* **CV:** Contagem interna.
* **Q:** Saida lógica, nível alto quando CV = 0.
### Contador UP and Down

![](../MEDIA/Pasted%20image%2020260312111657.png)

* **CU:** Pulso de incremento do contador.
* **CD:** Pulso de decremento do contador.
* **RESET:** Leva CV a 0.
* **LOAD:** Passa o valor de PV para CV.
* **PV:** Valor INT.
* **CV:** Contagem interna.
* **QU:** Saida lógica incremental, nível alto quando CV >= PV.
* **QD:** Saida lógica decremental, nível alto quando CV = 0.

### Exercícios

![](../MEDIA/8%20-%20Exercícios%20Contadores%20e%20Temporizadores.pdf)

#### a
![](../MEDIA/Pasted%20image%2020260319090608.png)

#### b

![](../MEDIA/Pasted%20image%2020260319090448.png)
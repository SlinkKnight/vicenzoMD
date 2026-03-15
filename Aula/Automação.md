## Portas lógicas no MasterTools

### Porta AND

![[Pasted image 20260226103621.png|283]]

| A   | B   | Saída |
| --- | --- | ----- |
| 0   | 0   | 0     |
| 0   | 1   | 0     |
| 1   | 0   | 0     |
| 1   | 1   | 1     |
### Porta OR

![[Pasted image 20260226103659.png]]

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   1   |
### Porta NOR

![[Pasted image 20260226103804.png]]

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   0   |
### Porta NAND

![[Pasted image 20260226103845.png]]

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |
### Porta XOR

![[Pasted image 20260226103949.png]]

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |
| 0 | 1 |   1   |
| 1 | 0 |   1   |
| 1 | 1 |   0   |
### Porta XNOR

![[Pasted image 20260226104819.png]]

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   1   |
| 0 | 1 |   0   |
| 1 | 0 |   0   |
| 1 | 1 |   1   |
## Timer em LADDER

### Timer delay on

![[MToolIEC_zEwN1JuMH4.gif]]

* **TON:** Timer que ESPERA para elevar Q ao alto.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
### Timer delay off!

![[MToolIEC_Z3sKk8gRie.gif]]

* **TON:** Timer que ESPERA para abaixar.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
### Timer pulse

![[MToolIEC_E72H33xe09.gif]]

* **TON:** Timer que faz um pulso de X segundos.
* **IN:** Pulso que inicia o timer.
* **PT:** Entrada em tempo, formato _T#5S.
* **ET:** Variável de tempo interno
* **Q:** Saida lógica.
## Contadores em LADDER

### Contador UP

![[Pasted image 20260312111626.png|211]]

* **CU:** Pulso de incremento do contador.
* **RESET:** Leva CV a 0.
* **PV:** Threshold, quando CV >= a PV, Q = 1.
* **CV:** Contagem interna.
* **Q:** Saida lógica.

### Contador DOWN

![[Pasted image 20260312111636.png]]

* **CD:** Pulso de decremento do contador.
* **LOAD:** Passa o valor de PV para CV.
* **PV:** Valor INT.
* **CV:** Contagem interna.
* **Q:** Saida lógica, nível alto quando CV = 0.
### Contador UP and Down

![[Pasted image 20260312111657.png]]

* **CU:** Pulso de incremento do contador.
* **CD:** Pulso de decremento do contador.
* **RESET:** Leva CV a 0.
* **LOAD:** Passa o valor de PV para CV.
* **PV:** Valor INT.
* **CV:** Contagem interna.
* **QU:** Saida lógica incremental, nível alto quando CV >= PV.
* **QD:** Saida lógica decremental, nível alto quando CV = 0.
**Professor:** Maicon Bandeira
**Tags:** `plano-de-numeração` `DDD` `DDI` `decibéis` `codificação` `modulação`

---

## Plano de Numeração

![PDF Plano de Numeração](../_MEDIA/Aux1%20-%20Plano%20de%20Numeração.pdf)

### 1. Divisão por DDD (Código de Área)

- **11 a 38 — Sudeste:** Rio de Janeiro, Minas Gerais, Espírito Santo, São Paulo.
- **41 a 55 — Sul:** Paraná, Santa Catarina, Rio Grande do Sul.
- **61 a 69 — Centro-Oeste:** Distrito Federal, Mato Grosso, Mato Grosso do Sul, Goiás, Tocantins, Rondônia, Acre.
- **63 a 99 — Norte/Nordeste:** Pará, Amapá, Amazonas, Roraima, Bahia, Sergipe, Alagoas, Pernambuco, Paraíba, Rio Grande do Norte, Ceará, Piauí, Maranhão.

### 2. Significado do Segundo Algarismo do DDD

O segundo algarismo do **DDD** (Código Nacional ou Código de Área) define a **subárea geográfica dentro de um estado**, geralmente baseando-se no desenvolvimento econômico e na densidade populacional da região.

### 3. Estrutura do Número Telefônico

- **`ABCD` — Prefixo:** Identifica a central local ou área telefônica (estação comutadora).
- **`MCDU` — Sufixo:** Número individual do assinante — **M**ilhar, **C**entena, **D**ezena, **U**nidade.

### 4. Códigos de País (DDI)

| País | Código |
|------|--------|
| Estados Unidos | +1 |
| Alemanha | +49 |
| México | +52 |
| Suécia | +46 |
| Brasil | +55 |
| China | +86 |
| Japão | +81 |
| Itália | +39 |

### 5. Centrais Duplas

Existem duas centrais para suportar a quantidade de assinantes da área.

### 6. Tipos de Chamada

- **Local:** Ligação interna na mesma rede (ex: CIMOL → CIMOL).
- **DDD:** Ligação interurbana dentro do território nacional.
- **DDI:** Ligação internacional.

---

## Ganho e Atenuação

### Ganho em dB — Potência

$$dB = 10 \log_{10}\!\left(\frac{P_{out}}{P_{in}}\right)$$

### Ganho em dB — Tensão

$$dB = 20 \log_{10}\!\left(\frac{V_{out}}{V_{in}}\right)$$

### dBV (referência 1 V)

$$dBV = 20 \log_{10}\!\left(\frac{V_{out}}{1\,\text{V}}\right)$$

### dBmV (referência 1 mV)

$$dBmV = 20 \log_{10}\!\left(\frac{V_{out}}{1\,\text{mV}}\right)$$
### Atividades

![Atividade 1](../_MEDIA/IMG_1225%201.png)

![Resposta Atividade 1](../_MEDIA/IMG_1224.png)



---

## Codificação I

![PDF Codificação I](../_MEDIA/6%20-%20Codificação%20I.pdf)

![PDF Exercícios Codificação I](../_MEDIA/6%20-%20Exercícios%20Codificação%20I.pdf)

![Resolução Codificação I](../_MEDIA/WhatsApp%20Image%202026-03-19%20at%2008.25.09.jpeg)

---

## Codificação II

![PDF Codificação II](../_MEDIA/7%20-%20Codificação%20II%201.pdf)

![PDF Exercícios Codificação II](../_MEDIA/7%20-%20Exercícios%20Codificação%20II.pdf)

---

## Modulação

![PDF Modulação](../_MEDIA/8%20-%20Modulação-1.pdf)

![PDF Exercícios Modulação](../_MEDIA/8%20-%20Exercícios%20Modulação.pdf)

![Resolução Modulação](../_MEDIA/WhatsApp%20Image%202026-03-19%20at%2008.28.27.jpeg)

---

## Trabalho modulação

![](../MEDIA/Atv_TK_Telecom-1.pdf)

### 1)

![](../MEDIA/Pasted%20image%2020260326212954.png)

`int i, j=1,z, dados[10];
float freq=0.5,phase=0,tempo=0,senoide=0;
const float pi = 3.1415;
unsigned long inter=50;
unsigned long tin, tend;
void setup()
{
Serial.begin(9600);
}
void loop()
{
if (Serial.available() >= 10)
{
for (i=0; i < 10 ; i++)
{
dados[i] = Serial.read();
if(dados[i]==49)
dados[i]=1;
else if(dados[i]==48)
dados[i]=0;
}
j=0;
}
if(j==0)
{
for (i=0;i<10;i++)
{
for (z=0; z<40;z++)
{
tempo = (float)z*((float)inter/1000);
senoide= 1.00 * sin(2*pi*((float)dados[i] + 1.00)*tempo +
phase);
Serial.println(senoide);
tin = millis();
tend=tin+inter;
while(tin<tend)
{
tin=millis();
}
}
}
j=1;
}
}`


![](../MEDIA/Pasted%20image%2020260326213136.png)
### 2)

![](../MEDIA/Pasted%20image%2020260326212506.png)

`int i, j=1,z, dados[10];
float freq=0.5,phase=0,tempo=0,senoide=0;
const float pi = 3.1415;
unsigned long inter=50;
unsigned long tin, tend;
void setup()
{
Serial.begin(9600);
}
void loop()
{
if (Serial.available() >= 10)
{
for (i=0; i < 10 ; i++)
{
dados[i] = Serial.read();
if(dados[i]==49)
dados[i]=1;
else if(dados[i]==48)
dados[i]=0;
}
j=0;
}
if(j==0)
{
for (i=0;i<10;i++)
{
for (z=0; z<40;z++)
{
tempo = (float)z*((float)inter/1000);
senoide= (float)dados[i] * sin(2*pi*1.00*tempo +
phase);
Serial.println(senoide);
tin = millis();
tend=tin+inter;
while(tin<tend)
{
tin=millis();
}
}
}
j=1;
}
}`

![](../MEDIA/Pasted%20image%2020260326212723.png)

### 3)

![](../MEDIA/Pasted%20image%2020260326212140.png)

`int i, j=1,z, dados[10];
float freq=0.5,phase=1.0,tempo=0,senoide=0;
const float pi = 3.1415;
unsigned long inter=50;
unsigned long tin, tend;
void setup()
{
Serial.begin(9600);
}
void loop()
{
if (Serial.available() >= 10)
{
for (i=0; i < 10 ; i++)
{
dados[i] = Serial.read();
if(dados[i]==49)
dados[i]=1;
else if(dados[i]==48)
dados[i]=0;
}
j=0;
}
if(j==0)
{
for (i=0;i<10;i++)
{
phase = (dados[i] == 1)? pi:0.0;
for (z=0; z<40;z++)
{
tempo = (float)z*((float)inter/1000);
senoide= 1.0 * sin(2*pi*freq*tempo +
phase);
Serial.println(senoide);
tin = millis();
tend=tin+inter;
while(tin<tend)
{
tin=millis();
}
}
}
j=1;
}
}`

![](../MEDIA/Pasted%20image%2020260326212403.png)

### 4)



### 5)
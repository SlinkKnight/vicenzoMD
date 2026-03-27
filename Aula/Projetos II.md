**Professor:** Tiago Ulrich
**Tags:** `ampop` `logaritmos` `slew-rate`

---

## Amplificadores Operacionais (AmpOp)

A tensão diferencial de entrada é definida como:

$$V_{dif} = V^+ - V^-$$

O AmpOp sempre opera com aproximadamente **2V a menos na saída** em relação ao rail de alimentação, exceto em configurações *rail-to-rail*.

### Slew Rate

O **Slew Rate** (`Sr`) define a taxa máxima de variação da tensão de saída:

$$S_r = 2\pi F V_p$$

---

## Propriedades Logarítmicas

| Propriedade            | Expressão                                                 |
| ---------------------- | --------------------------------------------------------- |
| Definição              | $\log_b(a) = x \;\Rightarrow\; b^x = a$                   |
| Produto                | $\log_b(xy) = \log_b x + \log_b y$                        |
| Quociente              | $\log_b\!\left(\dfrac{x}{y}\right) = \log_b x - \log_b y$ |
| Potência               | $\log_b(x^n) = n\log_b x$                                 |
| Mudança de base        | $\log_b x = \dfrac{\log_k x}{\log_k b}$                   |
| Base da própria base   | $\log_b b = 1$                                            |
| Logaritmo de 1         | $\log_b 1 = 0$                                            |
| Identidade exponencial | $\log_b b^x = x$                                          |
| Identidade inversa     | $b^{\log_b x} = x$                                        |

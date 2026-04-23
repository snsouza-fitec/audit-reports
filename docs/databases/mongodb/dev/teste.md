# Formulário de Elementos de Máquinas I

## Material Dúctil

### Tensão Equivalente de Von Mises

$$\sigma' = \sqrt{\sigma_1^2 - \sigma_1\sigma_2 + \sigma_2^2}$$

### Coeficiente de Segurança

$$N = \frac{S_y}{\sigma}$$

### Cisalhamento Puro

$S_{ys} = 0,577 S_y$

### Na Máxima Tensão de Cisalhamento

$S_{ys} = 0,5 S_y$

$$N = \frac{S_{ys}}{\tau_{max}}$$

### Tensões Normais

$$\sigma_1 = \frac{\sigma_x + \sigma_y}{2} + \tau_{max}$$

$$\sigma_2 = 0$$

$$\sigma_3 = \frac{\sigma_x + \sigma_y}{2} - \tau_{max}$$

$$\tau_{max} = \sqrt{\left(\frac{\sigma_x - \sigma_y}{2}\right)^2 + \tau_{xy}^2}$$

## Materiais Frágeis

### Teoria de Mohr Modificada

Pontos A e B = $S_{ut}$ ou $S_{uc}$

Ponto C = $S_{ut}$

$$C_1 = \frac{1}{2} \cdot \left[ |\sigma_1 - \sigma_2| + \frac{2S_{ut} - |S_{uc}|}{-|S_{uc}|} \cdot (\sigma_1 + \sigma_2) \right]$$

$$C_2 = \frac{1}{2} \cdot \left[ |\sigma_2 - \sigma_3| + \frac{2S_{ut} - |S_{uc}|}{-|S_{uc}|} \cdot (\sigma_2 + \sigma_3) \right]$$

$$C_3 = \frac{1}{2} \cdot \left[ |\sigma_3 - \sigma_1| + \frac{2S_{ut} - |S_{uc}|}{-|S_{uc}|} \cdot (\sigma_3 + \sigma_1) \right]$$

$$\tilde{\sigma} = \text{MAX}(C_1, C_2, C_3, \sigma_1, \sigma_2, \sigma_3)$$

$$\tilde{\sigma} = 0 \quad \text{se} \quad \text{MAX} < 0$$

Coeficiente de segurança:

$$N = \frac{S_{ut}}{\tilde{\sigma}}$$

## Limite de Fadiga

![alt text](image-10.png)

### Fatores de Correção

$S_e = C_L C_G C_S C_T C_R S_e'$

$C_L$: Fator de Carregamento
$C_G$: Fator de Tamanho
$C_S$: Fator de Superfície
$C_T$: Fator de Temperatura
$C_R$: Fator de Confiabilidade

### Critérios para Estimar Falha por Fadiga

**FLEXÃO**: $C_{carga} = 1$

**FORÇA NORMAL**: $C_{carga} = 0,7$

**TORÇÃO**: $C_{carga} = 1$

## Critério de Tamanho

Para $d \le 0,3 \text{ in (8 mm)}$: $C_{tamanho} = 1$

Para $0,3 \text{ in} < d \le 10 \text{ in}$: $C_{tamanho} = 0,869 d^{-0,097}$

Para $8 \text{ mm} < d \le 250 \text{ mm}$: $C_{tamanho} = 1,189 d^{-0,097}$

Para tamanhos maiores: $C_{tamanho} = 0,6$

### Área da Seção Transversal Não Circular

Para uma peça que se encontra sujeita a uma tensão superior a 95% da tensão máxima:

$$A_{85} = \pi \left[\frac{d^2 - 0,95d^2}{4}\right] = 0,0766 d^2$$


### Diâmetro Equivalente

$$d_{equiv} = \sqrt{\frac{A_{95}}{0,0766}}$$

![alt text](image-7.png)

## Critério da Superfície

### Ferros Fundidos

$C_{superfície} = 1$

$$C_{superfície} = A (S_{ut})^b$$

Se $C_{superfície} > 1$, utilize $C_{superfície} = 1$

## Temperatura

Para $T \le 450^\circ C (840^\circ F)$: $C_{temp} = 1$

Para $450^\circ C < T \le 550^\circ C$: $C_{temp} = 1 - 0,0058 (T - 450)$

Para $840^\circ F < T \le 1020^\circ F$: $C_{temp} = 1 - 0,0032 (T - 840)$

## Coeficientes para a equação do fator de superfície

**Tabela 6-3 Coeficientes para a equação do fator de superfície**


![alt text](image-6.png)

## Fatores de confiabilidade

**Tabela 6-4 Fatores de confiabilidade para $S_e = 0,08 \mu$**

| Confiabilidade % | $C_{conf}$ |
|---|---|
| 50 | 1,000 |
| 90 | 0,897 |
| 95 | 0,868 |
| 99 | 0,814 |
| 99,9 | 0,753 |
| 99,99 | 0,702 |
| 99,999 | 0,659 |
| 99,9999 | 0,620 |

## Desenho do diagrama S-N estimado

* As Equações mostradas trazem informações a respeito da resistência dos materiais na região de alto-ciclo.
* Com informações similares para a região de baixo-ciclo, pode-se construir um diagrama S-N para materiais e aplicações
* $S_m$ - a resistência do material a $10^3$ ciclos – baixo ciclo.

![Diagrama S-N](https://files.manuscdn.com/user_upload_by_module/session_file/310519663052738814/sGTVKqOmtCSMpNYs.png)


### Flexão

$S_m = 0,9 S_{ut}$

### Força Normal

$S_m = 0,75 S_{ut}$

### Equações do Diagrama S-N

$$S(N) = a N^b$$

$$\log S(N) = \log a + b \log N$$

$$b = \frac{1}{z} \log \left(\frac{S_m}{S_e}\right) \quad \text{onde} \quad z = \log N_1 - \log N_2$$

$$\log(a) = \log(S_m) - b \log(N_1) = \log(S_e) - 3b$$


![alt text](<Captura de tela 2026-04-23 144349.png>)

![alt text](image-5.png)

## Dimensionamento de Parafusos

### Área sob tração

Testes de barra rosqueadas submetidas à tração pura mostram que sua resistência à tração é melhor definida pelas médias dos diâmetros menor e primitivo.

$$A_t = \frac{\pi}{4} \left(\frac{d_p + d_r}{2}\right)^2$$

Para roscas UNS:

$$d_p = d - \frac{0,649519}{N}$$

$$d_r = d - \frac{1,299038}{N}$$

Para roscas ISO:

$d_p = d - 0,649519 p$

$d_r = d - 1,299038 p$

### Tabela 15-1 - Principais dimensões de roscas de parafusos UNS

![alt text](image-3.png)

## Resistência dos parafusos

### Tabela 15-6 - Especificações métricas e resistências de parafusos de aço

![alt text](image-2.png)

### Tabela 15-7 - Especificações métricas e resistências de parafusos de aço

![alt text](image-1.png)

### Força tensora e aperto de juntas aparafusadas

* Em condições comerciais comuns, $K = 0,15$ se houver qualquer tipo de lubrificação;
* Para roscas limpas e secas, $K = 0,20$;

## Dimensionamento de Chaveta

### Cisalhamento

![alt text](<Captura de tela 2026-04-23 141245.png>)

$$\tau = \frac{F_t}{A_{cis}} = \frac{F_t}{b \cdot l}$$

### Pressão de Contato

![Chaveta em Pressão de Contato](https://files.manuscdn.com/user_upload_by_module/session_file/310519663052738814/SEqGyVFHgIRWqNJc.png)

$$\sigma_d = \frac{F_t}{A_{esm}} = \frac{F_t}{l (h - t_1)}$$

### Tabela de dimensões de chaveta

![alt text](image-11.png)

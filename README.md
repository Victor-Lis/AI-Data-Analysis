# AI-Data-Analysis
Esse é o repositório de explicação de como as IAs podem ser analisadas e com quais métodos, antes de tudo, vamos para uma explicação

## Como uma IA de Regressão funciona?
Ela basicamente vai se assemelhar bastante a uma função matématica ou uma função das linguagens de programação.
Temos várias características e valores que são o **X** que através de uma fórmula gerarão o **Y**, a IA basicamente vai descobrir essa fórmula.
Em resumo, termos X como o Preditor(Predictor) e Y como o Alvo(Target)

## Exemplo | Dados de treinamento(Training Data)

Supondo que tenhamos os seguintes valores:
```
Predict | Target
x: 1    | y: 3
x: 2    | y: 5 
x: 3    | y: 7 
x: 4    | y: 9 
x: 5    | y: 11
x: 6    | y: 13
x: 7    | y: 15
x: 8    | y: 17
x: 9    | y: 19
```

A **IA** vai traçar um **model** (uma espécie de função que sirva para obtermos os respectivos valores), no caso o **model** que **IA** iria traçar seria (em JS):
```js
const f = (x) => console.log(`x: ${x} | y: ${(x*2)+1}`)
```

## Como qualificar a qualidade dos resultados?
Para isso existem alguns métodos, vamos ver:

### Exemplo | Dados de treinamento(Training Data)
Nesse exemplo, vamos supor que fossemos avaliar o valor de uma casa(y) através de alguns valores(x), por exemplo: área_quadrada e num_de_quartos.

Supondo que tenhamos os seguintes valores:
```
      |               X                |       Y       | 
Index | area_quadrada | num_de_quartos | valor_da_casa |
1     |      091      |       04       |   5.500,000   |
2     |      082      |       04       |   5.345,000   |
3     |      075      |       03       |   4.978,000   |
```

Além disso temos uma equação estimada:
```
valor_casa1 = 3.000,000 + (peso1 * area_quadrada) + (peso2 * num_de_quartos)
valor_casa2 = 3.000,000 + (peso1 * area_quadrada) + (peso2 * num_de_quartos)
valor_casa3 = 3.000,000 + (peso1 * area_quadrada) + (peso2 * num_de_quartos)
```

Para os valores já conhecidos podemos apenas subistituir:
```
valor_casa1 = 3.000,000 + (peso1 * 91) + (peso2 * 4)
valor_casa2 = 3.000,000 + (peso1 * 82) + (peso2 * 4)
valor_casa3 = 3.000,000 + (peso1 * 75) + (peso2 * 3)
```

Agora os nossos únicos valores desconhecidos são:
```
peso1 = ?
peso2 = ?
```

Precisamos encontrar uma **valor** para eles que se encaixe em **ambas situações** ao mesmo tempo.
Começando então por um valor aleatório.

Exemplo:
Obs: Poderia ser qualquer outro valor, foi escolhido apenas de maneira aleatória.
```
peso1: 27,000;
peso2: 27,000
```

Subistituindo agora nas nossas formulas os valores gerados aleatóriamente:
```
valor_casa1 = 3.000,000 + (27 * 91) + (27 * 4)
valor_casa2 = 3.000,000 + (27 * 82) + (27 * 4)
valor_casa3 = 3.000,000 + (27 * 75) + (27 * 3)
```

Agora temos uma fórmula para **estimar o valor**
Os resultados no exemplo acima seriam:
```
valor_casa1 = 5.565,000;
valor_casa2 = 5.322,000;
valor_casa3 = 5.106,000;
```

Agora fazendo a comparação com os valores reais:
```
Valores Reais | Valores Estimados |
  5.500,000   |     5.565,000     |
  5.345,000   |     5.322,000     |
  4.978,000   |     5.106,000     |        
```

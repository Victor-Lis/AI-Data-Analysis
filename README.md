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
Index | area_quadrada | num_de_quartos | valor_da_casa
1     |      091      |       04       |   5.500,000
2     |      082      |       04       |   5.345,000
3     |      075      |       03       |   4.978,000
```

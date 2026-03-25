# Aplicação Parcial de Função

----------------

O que é?

A aplicação parcial de função acontece quando você fornece apenas parte dos argumentos de uma função, gerando uma nova função que espera os argumentos restantes.

Em vez de:

`soma x y = x + y` 

Você pode fazer:

`soma10 = soma 10`

Agora soma10 é uma nova função:

`soma10 5 -- resultado: 15`

-----------------

Motivação
Reutilizar código de forma mais simples
Criar funções mais específicas a partir de funções genéricas
Facilitar programação funcional (código mais limpo e declarativo)

-----------------

Exemplos

Ex1:

`multiplica x y = x * y`

`dobro = multiplica 2`

`dobro 4 -- 8`

Ex2:

`maiorQue x y = y > x`

`maiorQue10 = maiorQue 10`

`maiorQue10 15 -- True`

-----------------

Em outra linguagem (JavaScript)

JavaScript não faz isso automaticamente, mas dá pra simular:

```javascript

function soma(x) {
  return function(y) {
    return x + y;
  };
}
const soma10 = soma(10);
console.log(soma10(5)); // 15
```

------------------

Uso em código real

Aplicação parcial é muito usada em:

funções como map, filter
pipelines funcionais
bibliotecas como lodash/fp

Exemplo:

`map (multiplica 2) [1,2,3]
-- [2,4,6]`

-----------------



# Array Methods

> Lista de métodos, que utilizo com frequência, para manipular arrays contendo objetos :rocket:

### // Array

```javascript
const beers = [
  {
    id: '1',
    name: 'Heineken',
    price: 6.0,
    quantity: 202
  },
  {
    id: '2',
    name: 'Budweiser',
    price: 5.5,
    quantity: 121
  },
  {
    id: '3',
    name: 'Eisenbahn',
    price: 5.0,
    quantity: 2
  },
  {
    id: '4',
    name: 'Antarctica Original',
    price: 6.0,
    quantity: 24
  },
  {
    id: '5',
    name: 'Bohemia',
    price: 7.0,
    quantity: 139
  }
];
```

### // Array.filter()

```javascript
// Array.filter()
// retorna todos os itens que satisfação a função de teste provida

beers.filter((beer) => {
  return beer.name.toLowerCase().indexOf('origi') !== -1
})

beers.filter((beer) => {
  return beer.price < 6.0
})

beers.filter((beer) => {
  return beer.quantity < 50
})
```

### // Array.find()

```javascript
// retorna o primeiro item que satisfaça a função de teste provida

beers.find((beer) => {
  return beer.id == '2'
})
```

### // Array.map()

``` javascript
// retorna um novo array contendo os itens multados

beers.map((beer) => {
  if (beer.price == 6.0) {
    beer.price = 5.5
  }

  return beer
})
```

### // Array.some()

```javascript
// retorna true caso algum item satisfaça a função de teste provida

beers.some((beer) => {
  return beer.quantity < 50
})
```

### // Array.reduce()

```javascript
// retorna o valor acumulado durante a iteração

beers.reduce((quantity, beer) => {
  return quantity + beer.quantity
}, 0)
```

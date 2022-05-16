Dada una cantidad de dinero en euros (número positivo, si no mostrar el mensaje "error") calcule el número mínimo de billetes y monedas necesario, sabiendo que disponemos de billetes de 500, 200, 100, 50, 20, 10 y 5 euros, y monedas de 1 y 2 euros,  y 50, 20, 10, 5, 2 y 1 céntimo. Las monedas o billetes que NO se necesiten para el cálculo NO deben mostrarse. Si se necesita más de una moneda o billete se debe mostrar el plural ("3 monedas" en lugar de "3 moneda") .

Por ejemplo, si introducimos la cantidad 342.78 €, la salida del algoritmo será:

1 billete de 200€

1 billete de 100€

2 billetes de 20€

1 moneda de 2 €,

1 moneda de 50 céntimos

1 moneda de 20 céntimos

1 moneda de 5 céntimos

1 moneda de 2 céntimos

1 moneda de 1 céntimo 

# Bateria de test 

```javascript
case = Test 1
Grade reduction = 20%
input =342.78
output = 1 billete de 200 euros
1 billete de 100 euros
2 billetes de 20 euros
1 moneda de 2 euros
1 moneda de 50 céntimos
1 moneda de 20 céntimos
1 moneda de 5 céntimos
1 moneda de 2 céntimos
1 moneda de 1 céntimo 

case = Test 2
Grade reduction = 20%
input =900
output = 1 billete de 500 euros
2 billetes de 200 euros

case = Test 3
Grade reduction = 20%
input =-900
output = error

case = Test 4
Grade reduction = 20%
input =10.25
output = 1 billete de 10 euros
1 moneda de 20 céntimos
1 moneda de 5 céntimos

case = Test 5
Grade reduction = 20%
input =200.69
output = 1 billete de 200 euros
1 moneda de 50 céntimos
1 moneda de 10 céntimos
1 moneda de 5 céntimos
2 monedas de 2 céntimos
```


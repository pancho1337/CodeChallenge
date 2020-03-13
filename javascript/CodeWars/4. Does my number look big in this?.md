Un número narcisista es un número que es la suma de sus propios dígitos, cada uno elevado a la potencia del número de dígitos.
Por ejemplo, 153 (3 dígitos totales que formarán al potencia):
```
1 ^ 3 + 5 ^ 3 + 3 ^ 3 = 1 + 125 + 27 = 153
```
y 1634 (4 dígitos totales que formarán al potencia):
```
1 ^ 4 + 6 ^ 4 + 3 ^ 4 + 4 ^ 4 = 1 + 1296 + 81 + 256 = 1634
```
 
### El Desafío:
Su código debe devolver verdadero o falso dependiendo de si el número dado es un número narcisista.
No se requiere la comprobación de errores para cadenas de texto u otras entradas no válidas, sólo se pasarán números enteros válidos a la función.

### Mi Razonamiento 

1.Tengo que convertir el número en un arreglo para iterar
2. Creó un resultado que tenga mis suma 
3. Itero por cada elemento en el arreglo sumando al resultado el poder del elemento a lo largo del arreglo. 
4. Comparó que mi total y con mi valor inicial regresando true or false.

### Solución

```js
function narcissistic(valor) {
  const arrCopia = valor+"".split('');

  let sumaTotal = 0;

  for (caracterIndividual of arrCopia) {
    const numeroActual = Number(caracterIndividual)

    sumaTotal += Math.pow(numeroActual, arrCopia.length);
  }

  return sumaTotal === valor;
}
```

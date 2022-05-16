# Para crear una tarea en VPL
1) Crear una actividad VPL. Como cualquier tarea de moodle se deberá indicar: 
    * Nombre y descripción
    * Fecha límite
    * Restricciones
    * Puntuación máxima
    * Restricciones Acceso
2) Configurar las opciones de ejecución. En este apartado se deberá establecer si se permite: ejecutar, depurar, evaluar, evaluar al entregar y calificación automática.
    * Basado en: permite establecer otra actividad VPL de la que tomar referencias.
    * Ejecutar script y Script de depuración: permite establecer un script determinado de entre la lista.
    * Ejecutar, Depurar y Evaluar: establecen que se puede usar durante la edición de la entrega. Esto sólo afecta a los estudiante. 
    * Evaluar al entregar: Si al subir los ficheros, se evalua automáticamente. 
    * Calificación automática: Si el resultado anterior se toma como nota definitiva.
3) Establecer los ficheros requeridos: Se establece los nombres y contenido inicial de los ficheros requeridos para los estuidantes. 
4) Establecer la batería de test: Una vez creada la actividad, se debe establecer la bateria de prueba que deberá pasar el código fuente. Se debe completar el fichero "vpl_evaluate.cases". 

# Batería de Prueba (vpl_evaluate.cases) 
Los principales comandos son:
* **Case** = Name Case: Todos los casos de uso deben tener un nombre identificativo
* **Input** = Text|Number. Los valores de entrada pudiendo establecerse en una única línea o varias. Este apartado termina cuando se define otra instrucción.
* **Output** = Text|Number|Regex. Salida esperada a partir de los inputs.
  * Números: solo se escriben números. Solo se extraen números, el resto del texto se ignora.
  * Texto: solo se verifican las palabras, la comparación no distingue entre mayúsculas y minúsculas y los demás caracteres se ignoran.
  * Texto exacto: el texto está entre comillas dobles.
  * Expresiones regulares: Empieza con / y termina con / y opcionalmente uno o varios modificadores. El formato es POSIX
* **Grade reduction** = Grade Reduction.  Porcentaje de reducción cuando las salidas no se corresponden con la esperada. 
* **Fail Message**. Mensaje de error. Establece el texto para mostrar cuando falla el caso. Se omite la información de entrada y salida.
* **Program to run**: Programa a ejecutar: Reemplaza, el programa del estudiante por otro. Por ejemplo, puede utilizar esta instrucción para ejecutar un análisis estático / dinámico del código del alumno.
* **Program arguments**. Argumentos del programa. Permite enviar información al programa del estudiante
* **Expected exit code**. Código de salida esperado. Establece el código de salida esperado de la ejecución del caso del programa (return)
    
# Ejemplo 1. Hola Mundo. 

Se quiere realizar un batería que compruebe que la salida es Hola Mundoooo. Como se puede comprobar no necesita ningún input (pues no hay entrada) y la salida se ha puesto entre comillas para comprobar que la salida es exacta. 

```javascript
case = Primer Caso
Grade reduction = 100%
output = "Hola Mundoooo"
```

# Ejemplo 2. Menor de Tres. 
En este caso vamos a leer tres números por entrada y mostraremos el menor de los tres. 

```javascript
case = Test 1
grade reduction = 30%
input =3
5
10
Output = 3

case = Test 2
grade reduction = 30%
input =3
3
3
Output = 3

case = Test 3
grade reduction = 40%
input =1000
-1000
2000
output = -1000
```



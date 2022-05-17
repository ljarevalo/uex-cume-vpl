En este directorio se incluirán nuevos ejemplos de tareas VPL pero que necesitan de un proceso de configuración. En primer lugar se detalla cómo funciona VPL para compresnder las distintas opciones que pueden llevarse a cabo y posteriormente se clasifican y se incluyen en un subdirectorio cada una de ellas. 

# Como funciona VPL 
Para ello será necesario saber cómo funciona mejor este plugins. Cuando un estudiante realiza un proceso de evaluación se realizan los siguientes pasos: 
* Los ficheros subidos por el estudiante son enviados al servidor Jaula (Jail) donde se ejecutan. 
* La ejecución, depuración o evaluación se hace mediante un conjunto de script (.sh). Estos ficheros será los que aprenderemos a modificar en este apartado. **Es necesario conocimiento de shell script** Concretamente: 
  * Ejecución (vpl_run.sh)
  * Depuración (vpl_debug.sh)
  * Evaluación (vpl_evaluate.sh)  * 
* La ejecución de cualquiera de estos scripts debe generar un fichero denominado vpl_execution o vpl_wexecution que puede ser un binario o un fichero script.

# Tipos de Casos
* Ejemplos con modificación en los ficheros de ejecución: En este caso será necesario modificar los ficheros vpl_run.sh o vpl_evaluate.sh
* Ejemplos con ficheros a mantener durante de la ejecución
* Ejemplos con generación del código en los resultados de ejecución
* Ejemplos Ejecución de vpl_evaluate.cpp


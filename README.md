# Matlab

MATLAB (abreviatura de _MATrix LABoratory_, «laboratorio de matrices») es un sistema de cómputo numérico que ofrece un entorno de desarrollo integrado (IDE) con un lenguaje de programación propio (_lenguaje M_). Está disponible para las plataformas Unix, Windows, macOS y GNU/Linux.

Entre sus prestaciones básicas se hallan la _manipulación de matrices_, la representación de datos y funciones, la implementación de algoritmos, la creación de interfaces de usuario (GUI) y la comunicación con programas en otros lenguajes y con otros dispositivos hardware. El paquete MATLAB dispone de dos herramientas adicionales que expanden sus prestaciones, a saber, _Simulink (plataforma de simulación multidominio)_ y GUIDE (editor de interfaces de usuario - GUI). Además, se pueden ampliar las capacidades de MATLAB con las cajas de herramientas (_toolboxes_); y las de Simulink con los paquetes de bloques (blocksets).

Es un software muy usado en universidades y centros de investigación y desarrollo. En los últimos años ha aumentado el número de prestaciones, como la de programar directamente procesadores digitales de señal o crear código VHDL.

## Ventanas de MATLAB

- **Barra de Herramientas**
  La barra de herramientas de MATLAB vamos a encontrar tres pestañas HOME/PLOTS/APPS cada una tendrá funcionalidades especificas para usar en nuestro proyecto.

- **Current Folder (Carpeta Actual)**
  Nos muestra los archivos de la carpeta donde MATLAB se encuentra ubicado actualmente. Quiere decir que todo lo que haga matlab, desde el llamado de funciones o códigos script, MATLAB va a buscar primero en esa carpeta para ver si encuentra lo que él necesita.

- **Workspace (Área de Trabajo)**
  En esta parte, vas a ver todas las variables que has creado en el software, podras ver el tipo de variable, el valor, el minimo, máximo entre otras informaciones útiles.

- **Command Windows (Ventana de Comandos)**
  Es la ventana principal de MATLAB, donde podrás ingresar todos los cálculos numéricos como si fuera una calculadora. Además aqui podrás visualizar los resultados de la operaciones que hagas con el Software.
  - Para asignar variables simplemente se usa con el signo **`=`**
  - Para evitar imprimir el resultado debes finalizar con **`:`** (punto y coma).
  - Para crear comentários basta con colocar el el signo de porcentaje **`%`** al comienzo o usar **`%{ comentario multilinea %}`** para multiples líneas. Este texto MATLAB no lo va a interpretar.

## Cómo nombrra las variables

1. Todos los nombres deben comenzar con una letra
2. Los nombres pueden tener una longitud máxima de 63 caracteres a partir de Matlab 7
3. Los únicos caracteres permitidos con letras, números y guión bajo, al igual que el nombre a los _scripts_ y las _funciones_.
4. Los nombres son sensibles a mayúsculas y minúsculas (Case sensitive)
5. Las palabras reservadas no pueden usarsen (Usar **iskeyword** para conocerlas).
6. Matlab permite resignar nombres de funciones internas como nombres de variables. (Tener cuiado con eso, para limpiar la variable se usa **clear sin** donde _sin_ sería la variable).

## Crear Vectores

Existen dos tipos de vectores que podemos ingresar en Matlab:

- Vector fila
- Vector columna

Para crear un **vector Fila**, asignamos una variable con el nombre que queramos y colocamos los elementos del vector dentro de _corchetes_ `[]`, cada elemento puede ir separado por comas (,) o espacios.

```M
x=[4 6.5 -3 3 10.5 11] %Separado con espacio
x=[4,6.5,-3,3,10.5,11] %Separado con coma
```

Para crear un **vector Columna**, asignamos una variable con el nombre que queramos y colocamos los elementos del vector dentro de corchetes, cada elemento separado por punto y coma (;)

```M
x=[4;6.5;-3;3;10.5;11] %Separado con punto y coma
```

**Vectores con intervalos regulares** se pueden ingresar mucho más fácilmente, basta solo con colocar la variable y asignarla al valor con intervalo regular colocando el primer valor, luego dos puntos, el incremento, dos puntos y el ultimo valor.

**`Variable= Primer Valor : Incremento : Ultimo Valor`**

```M
% Crea un vector x1=[1 2 3 4 5 6]
x1=1:6
% Crea un vector x2=[6 5 4 3 2 1]
x2=6:-1:1
% Crea un vector x3=[0 2 4 6 8 10]
x3=0:2:10
% Crea un vector x4=[10.5 10 9.5 9 8.5 8 7.5]
x4=10.5:-0.5:7.5
```

Matlab también posee algunas funciones para crear vectores con determinadas características

- **`linspace (a,b,c)`** genera un vector linealmente espaciado entre los valores a y b con c elementos.
- **`linspace (a,b)`** genera un vector linealmente espaciado entre los valores a y b con 100 elementos.
- **`logspace (a,b,c)`** genera un vector logarítmicamente espaciado entre los valores 10^a y 10^b con c elementos.
- **`logspace (a,b)`** genera un vector logarítmicamente espaciado entre los valores 10^a y 10^b con 50 elementos.

## EXTRAER Datos de un Vector en MATLAB

Para acceder a los elementos individuales de un vector lo haremos utilizando subíndices, así **`x(n)`** sería el _n-ésimo_ elemento del _vector x_. Si queremos acceder al último podemos indicarlo usando **`end`** como subíndice

- [x] Para acceder a un bloque de elementos a la vez, se usa la notación dos puntos (:) como **`x(m:n)`**

```M
%crea el Vector
x=[4 6.5 -3 3 10.5 11]
%Toma el tercer elemento
x(3) %asi puedo obtener el valor -3 que está en la tercera posicion
%toma del tercero al quinto
x(3:5)
%Toma las datos espaciados de 2 en 2
x(1:2:end)
%Toma el ultimo valor
x(end)
%Toma el primero, cuarto y quinto valor
x([1 4 5])
```

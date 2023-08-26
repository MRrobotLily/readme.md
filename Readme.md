## Documentación del algoritmo *conversión de unidades* escrito en los siguientes lenguajes
> Pseint
> C++
> Python 
##
## Pseint
En la parte de abajo estará el código fuente del la tarea **Conversión de Unidades de Longitud** creado en pseudocódigo. Se definió las variables necesarias para almacenar valores de entrada como lo que son *Centímetros* y los valores convertidos a otras unidades como:  *opción, metros, yardas, varas, pulgadas y pies.*

Hay una solicitud de entrada, el cual le solicita al usuario ingresar los centímetros a convertir. Luego de tomar el dato, al usuario se le presentan las opciones disponibles de conversión que están enumeradas del 1 al 5, el usuario deberá seleccionar la opción deseada y esto deberá ser capturado en la variable opción. 

Se utilizo una estructura de control *"Según"* que toma la opción seleccionada por el usuario y ejecuta el caso correspondiente, para cada caso se realiza la conversión especifica multiplicando el valor del centímetro por el factor de conversión correspondiente para obtener la unidad deseada.  Luego se muestra el caso de conversión. **De otro modo:** Si la opción seleccionada no coincide con las opciones presentadas, se mostrar un mensaje:  *Opción inválida. Por favor, vuelva a intentarlo* 
**Fin Según** marca  el final de la estructura *según* y **FinAlgoritmo** indica el final del algoritmo.

**CODIGO FUENTE:**

//Algoritmo ConversionUnidadesLongitud

	Definir centimetros, opcion, metros, yardas, varas, pulgadas, pies como Real
		
		Escribir "Ingrese la longitud en centímetros: "
		Leer centimetros
		
		Escribir "Opciones de conversión:"
		Escribir "1. Metros"
		Escribir "2. Yardas"
		Escribir "3. Varas"
		Escribir "4. Pulgadas"
		Escribir "5. Pies"
		
		Escribir "Seleccione la unidad a la que desea convertir (1-5): "
		Leer opcion
		
		Segun opcion Hacer
			Caso 1:
				metros <- centimetros * 0.01
				Escribir centimetros, " centímetros equivale a ", metros, " metros."
			Caso 2:
				yardas <- centimetros * 0.0109361
				Escribir centimetros, " centímetros equivale a ", yardas, " yardas."
			Caso 3:
				varas <- centimetros * 0.835905
				Escribir centimetros, " centímetros equivale a ", varas, " varas."
			Caso 4:
				pulgadas <- centimetros * 0.393701
				Escribir centimetros, " centímetros equivale a ", pulgadas, " pulgadas."
			Caso 5:
				pies <- centimetros * 0.0328084
				Escribir centimetros, " centímetros equivale a ", pies, " pies."
			De Otro Modo:
				Escribir "Opción inválida. Por favor, vuelva a intentarlo."
		Fin Segun
FinAlgoritmo 

##
## C++

Abajo encontrara el código fuente de conversor de unidades hecho en el lenguaje de C++. 

Primero se incluye la librería *"iostream"* para manejar la entrada y salida estándar. Se utilizó la función *"main()"*, se declararan variables como *"opción"* de tipo entero, para almacenar la opción seleccionada por el usuario. y el tipo de dato utilizado es double porque se utilizaran decimales. 

El usuario podrá seleccionar una conversión que desea del un menú en pantalla. El número seleccionado por el usuario será almacenado en la variable*"opción"*. 

Se utilizo una estructura switch en donde leerá la variable *"opción"*.  La estructura switch muestra 5 casos y si la opción ingresada por el usuario esta dentro de estos 5 casos lograra mostrar el resultado deseado.

En cada caso se muestra un encabezado solicitando al usuario la cantidad de centímetros a convertir. Se realiza la conversión correspondiente utilizando las formulas proporcionadas.

En caso que el usuario seleccione un numero que no este dentro del rango del 1 al 5 se agrego un *"default"* que le mostrara el siguiente mensaje: *"Opción invalida, por favor seleccione una opción del 1 al 5"* hasta finalizar en return 0. 

Este programa permite realizar conversiones de unidades de longitud según la opción elegida por el usuario, mostrando resultados en diferentes unidades.
 
**CODIGO FUENTE:**

#include <iostream<iostream>>

using namespace std;

int main() {
	
	int opcion;
	double centimetros, metros, yardas, varas, pulgadas, pies;
	
	cout << "Ingrese una opcion: " << endl;
	cout << "1. Centimetros a metros " << endl;
	cout << "2. Centimetros a yardas " << endl;
	cout << "3. Centimetros a varas " << endl;
	cout << "4. Centimetros a pulgadas " << endl;
	cout << "5. Centimetros a pies " << endl;
	cin >> opcion;
	
	switch (opcion){
		
		case 1:
			cout << "**Centimetros a metros**" << endl;
			cout << "Ingrese cantidad de centimetros a convertir" << endl;
			cin >> centimetros;
			metros = centimetros * 0.01;
			cout << centimetros << " centimetros equivalen a " << metros << " metros." << endl;
			break; 
		case 2:
			cout << "**Centimetros a Yardas**" << endl;
			cout << "Ingrese cantidad de centimetros a convertir" << endl;
			cin >> centimetros;
			yardas = centimetros * 0.0109361;
			cout << centimetros << " centimetros equivalen a " << yardas << " yardas." << endl;
			break; 
		case 3:
			cout << "**Centimetros a varas**" << endl;
			cout << "Ingrese la cantidad de centimetros a convertir " << endl;
			cin >> centimetros;
			varas = centimetros * 83.59;
			cout << centimetros << " centimetros equivalen a " << varas << " varas. " << endl;
			break;
		case 4:
			cout << "**Centimetros a pulgadas**" << endl;
			cout << "Ingrese la cantidad de centimetros a convertir";
			cin >> centimetros;
			pulgadas = centimetros * 0.393701;
			cout << centimetros << " centimetros equivalen a " << pulgadas << " pulgadas. " << endl;
			break;
		case 5: 
			cout << "**Centimetros a pies**" << endl;
			cout << "Ingrese la cantidad de centimetros a convertir";
			cin >> centimetros;
			pies = centimetros * 0.0328084;
			cout << centimetros << " centimetros equivalen a " << pies << " pies. " << endl;
			break;
		default:
			cout << "Opcion invalida, por favor seleccione una opcion del 1 al 5." << endl;
			break;
	}
return 0;
}
##
## Python

Se define la función *"main()"* que será el punto de entrada del programa. Se le solicitara al usuario ingresar los centímetros a convertir.
El usuario ingresa la cantidad de centímetros a convertir y a continuación se le presentaran 5 opciones de unidad de conversión. 

El usuario selecciona una opción y usando las declaraciones *"if"* y *"elif"* el programa realiza la conversión correspondiente según la opción seleccionada. 
>Se calcula la conversión utilizando las fórmulas proporcionadas.
>Muestra el resultado de la conversión en la unidad deseada.

Si el usuario ingresa una opción que no esta en el rango del 1 al 5 se le mostrara el siguiente mensaje: *"Opción inválida, por favor vuelva a intentarlo"* 
La ultima sección del código "`if  __name__  ==  "__main__":"` asegura la función `"main()"`se ejecute cuando el programa inicie. 

**CODIGO FUENTE:**

def main():
    # Solicitar la longitud en centimetros
    centimetros = float(input("Ingrese la longitud en centimetros: "))

    # Solicitar la unidad de conversión
    print("Opciones de conversión:")
    print("1. Metros")
    print("2. Yardas")
    print("3. Varas")
    print("4. Pulgadas")
    print("5. Pies")

    option = int(input("Seleccione la unidad a la que desea convertir: "))

    # Realizar la conversión según la opción seleccionada
    if option == 1:
        metros = centimetros * 0.01
        print(f"{centimetros} centímetros equivalen a {metros} metros.")
    elif option == 2:
        yardas = centimetros * 0.0109361
        print(f"{centimetros} centímetros equivalen a {yardas} yardas.")
    elif option == 3:
        varas = centimetros * 83.59
        print(f"{centimetros} centimetros equivalen a {varas} varas.")
    elif option == 4:
        pulgadas = centimetros * 0.393701
        print(f"{centimetros} centimetros equivalen a {pulgadas} pulgadas.")
    elif option == 5:
        pies = centimetros * 0.0328084
        print(f"{centimetros} centimetros equivalen a {pies} pies. ")
    else:
        print("Opcion invalida, por favor vuelva a intentarlo.")
    if  __name__  ==  "__main__":
	    main()


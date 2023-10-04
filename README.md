# Aplicación de Consulta de Datos por Departamento

Esta aplicación permite a los usuarios ingresar un nombre de departamento y un número de registros que desean obtener de una consulta. La consulta se realiza en una fuente de datos externa y se muestra en la pantalla en un formato específico.

## Capturas de Pantalla

A continuación se muestran algunas capturas de pantalla de la aplicación en funcionamiento:
![Datos](https://github.com/Max1mus5/Proyecto-API/assets/75461653/b3778a6c-2d1c-4ac6-8ddb-db34e600138e)
*Ingresaer los datos por consola*

![Obtener](https://github.com/Max1mus5/Proyecto-API/assets/75461653/facdc027-11fa-4e43-a766-7e78919271b3)
*mostrar los datos filtrados por departamento*

![Interfaz Grafia](https://github.com/Max1mus5/Proyecto-API/assets/75461653/e66366f2-5a87-47f1-8afc-44cc12ab827b)
*visualizacion de resultados en interfaz grafica*


## Instrucciones de Uso

Para utilizar la aplicación, siga estos pasos:

1. Ejecute el script `main.py` en su entorno de Python.

2. Ingrese el nombre del departamento que desea consultar cuando se le solicite.

3. Ingrese el número de registros que desea ver. Tenga en cuenta que un número grande de registros puede ralentizar la consulta.

4. Los resultados de la consulta se mostrarán en la pantalla en un formato de tabla que incluye las siguientes columnas: Ciudad de ubicación, Departamento, Edad, Tipo, Estado y País de procedencia.

## Dependencias

La aplicación utiliza las siguientes bibliotecas de Python:

- `sodapy`: Para acceder a la fuente de datos externa (www.datos.gov.co).
- `pandas`: Para el procesamiento de datos y la presentación en forma de tabla.
- `tkinter`: Para la interfaz gráfica de usuario (GUI).

Asegúrese de tener estas bibliotecas instaladas antes de ejecutar la aplicación.

## Configuración

Antes de ejecutar la aplicación, asegúrese de configurar las credenciales necesarias en el archivo `main.py` para acceder a la fuente de datos externa.

```python
# Configuración de la fuente de datos externa
client = Socrata("www.datos.gov.co",
                "axzd54LGExmtlbjuS4Zl3l8zY",
                username="j.riveros1@utp.edu.co",
                password="7E1088ro239515?")

## Advertencia

Tenga en cuenta que si selecciona un número grande de registros, la consulta puede llevar tiempo y ralentizar la aplicación. Asegúrese de elegir un número razonable de registros para evitar problemas de rendimiento.

Si elige un número de registros que excede el tamaño total de la fuente de datos, la aplicación mostrará un mensaje de advertencia y le proporcionará todos los datos disponibles en lugar del número especificado.

```python
if n > len(departamento_data):
    print(f"-------------------------------------------------------------------------------------\n¡ADVERTENCIA!\nEl DataFrame solo tiene {len(departamento_data)} filas. No se pueden seleccionar {n} filas.\nSe mostrarán los {len(departamento_data)} datos disponibles.\n-------------------------------------------------------------------------------------")
    n = len(departamento_data)

## Autor

Este código fue desarrollado por [Jeronimo Riveros].

Si tiene alguna pregunta o necesita ayuda adicional, no dude en ponerse en contacto conmigo:

- Correo electrónico: [J.riveros1@utp.edu.co]


# Aplicación de Consulta de Datos por Departamento

Esta aplicación permite a los usuarios ingresar un nombre de departamento y un número de registros que desean obtener de una consulta. La consulta se realiza en una fuente de datos externa y se muestra en la pantalla en un formato específico.

## Capturas de Pantalla

A continuación se muestran algunas capturas de pantalla de la aplicación en funcionamiento:

![Captura de Pantalla 1](https://postimg.cc/Wt6FYzJst)
*Ingresaer los datos por consola*

![Captura de Pantalla 2](https://postimg.cc/BXS8r3xH)
*mostrar los datos filtrados por departamento*

![Captura de Pantalla 3](https://postimg.cc/ZCw9ZQcg)
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


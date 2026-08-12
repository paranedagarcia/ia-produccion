# Plan de Compras 2025

## Descripción del proyecto

Este proyecto tiene como objetivo realizar un análisis exploratorio de datos (EDA) sobre la planilla del Plan de Compras 2025, utilizando Python y Pandas.

El análisis permite conocer la estructura de los datos, identificar valores faltantes, revisar las principales características de la información y generar tablas de resumen.

## Datos utilizados

La fuente de datos utilizada corresponde al archivo:

plan_de_compras_2025.xlsx

El archivo contiene 831 registros y 26 columnas relacionadas con proyectos, unidades de compra, tipos de proyecto, estados, montos y órdenes de compra.

## Actividades realizadas

### 1. Carga de la planilla de compras 2025

Se realizó la carga del archivo Excel utilizando la biblioteca Pandas y se verificó la cantidad de filas y columnas del dataset.

### 2. Análisis Exploratorio de Datos (EDA)

Se realizó un análisis exploratorio de los datos, considerando:

- Revisión de las dimensiones del dataset.
- Revisión de los nombres de las columnas.
- Revisión de los tipos de datos.
- Revisión de la información general.
- Identificación de valores nulos.
- Revisión de registros duplicados.
- Obtención de estadísticas descriptivas.
- Análisis de los tipos de proyectos.
- Análisis del estado de los proyectos.
- Análisis de los tipos de compra.
- Análisis de las unidades de compra.

### 3. Tablas de resumen

Se generaron tablas de resumen para analizar la información del Plan de Compras 2025, considerando:

- Resumen por Tipo de Proyecto.
- Resumen por Estado del Proyecto.
- Resumen por Unidad de Compra.
- Resumen por Tipo de Compra.

Las tablas de resumen consideran la cantidad de registros y el monto total asociado a cada categoría.

### 4. Limpieza de Registros Columna Teléfono

Al revisar la mencionada columna se encuentran 96 valores únicos, lo que merma la calidad de análisis, para ello se genera limpieza de la columna, con los siguientes pasos:

- Se convierte la columna en string.
- Se dejean sólo números eliminando guiones u otro tipo de expresión regular.
- Se reemplazan las columnas con digitos 0 por vacía (NA)
- Posteriormente, se eliminan 14 registros con filas NA.


## Principales resultados

El dataset contiene 831 registros y 26 columnas.

En el análisis de los tipos de proyecto se identificaron:

- 613 proyectos operacionales.
- 218 proyectos estratégicos.

Respecto al estado de los proyectos:

- 648 registros corresponden a proyectos actualizados.
- 183 registros corresponden a proyectos publicados.

La unidad de compra con mayor cantidad de registros corresponde al Ministerio de Vivienda y Urbanismo(766), con 684 registros.

Se identificaron valores faltantes en las siguientes columnas:

- Código presupuestario: 1 registro.
- OC Asociada Item 2025: 123 registros.
- Meses envio OC de Arraste: 648 registros.

## Estructura del proyecto

```text
ia-produccion-4/
│
├── plan_de_compras_2025.xlsx
├── requirements.txt
├── README.md
│
├── notebooks/
│   ├── cargar_pvd_ipynb
│   ├── 02_EDA.ipynb
│   └── 03_tablas_resumen.ipynb
│   └── 04_limpieza_telefono_dcc.ipynb
│   └── 05_filtrado_25_dcc.ipynb
│
└── .venv/
# Optimización del Secuestro de Carbono en Viñedos de La Rioja

Este repositorio contiene el código, datos y análisis utilizados en el estudio sobre la optimización del secuestro de carbono en viñedos de La Rioja. Se incluyen scripts de simulación, procesamiento y modelado, así como los conjuntos de datos generados y analizados.

## Estructura del Proyecto


```bash
carbonSequestration/
├── 📂 Scripts                # Código fuente en Python
│   ├── simulacionDatos.py    
│   ├── concatDatos.py        
│   ├── rothCvineyards.py     
│   ├── dfFinales.ipynb       
│   ├── analisisFinal.ipynb  
└── 📄 requirements.txt 
└── 📄 datosLaRioja.xls 
└── 📄 README.md              

```

## Instalación y Requisitos

Para ejecutar este proyecto, es necesario contar con:

- **Python 3.x**
- **Un editor de código** (recomendado: VSCode, PyCharm o Jupyter Notebook)
- **Librerías necesarias** (pueden instalarse con el siguiente comando):

```sh
pip install -r requirements.txt
```

## Desarrollo del proyecto 

1. **Generación de datos sintéticos**: Este script simula condiciones meteorológicas y de suelo para generar los datos de entrada requeridos por el modelo RothC. Incluye factores como temperatura media mensual, precipitación, evaporación y características del suelo.
```sh
python Scripts/simulacionDatos.py

```
2. **Prprocesamiento**: Agrupa y limpia los datos generados para obtener una estructura homogénea, lista para ser usada por el modelo.
```sh
python Scripts/concatDatos.py
```
3. **Simulación del Modelo RothC**: Ejecuta la simulación del modelo RothC adaptado al contexto del proyecto. Genera las salidas de carbono orgánico del suelo (SOC) en función del tiempo y de las estrategias agrícolas utilizadas (tradicional, intensiva y orgánica).
```sh
python Scripts/rothCvineyards.py
```
3. **Análisis de resultados**: Los notebooks permiten visualizar, analizar y comparar los resultados obtenidos, incluyendo:

    - Evolución temporal del SOC.
    - Comparativa entre tipos de manejo agrícola.
    - Gráficos de tendencias y correlaciones.
    - Aplicación de modelos estadísticos (regresión, ARIMA, SARIMA).

```sh
jupyter nbconvert --to notebook --execute Scripts/dfFinales.ipynb --output Scripts/dfFinales_output.ipynb
jupyter nbconvert --to notebook --execute Scripts/analisisFinal.ipynb --output Scripts/analisisFinal_output.ipynb
```

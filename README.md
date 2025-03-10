## Ejecutar en Binder
Haz clic en el siguiente botón para ejecutar el notebook en un entorno interactivo:

[![Binder](https://mybinder.org/badge_logo.svg)](https://hub.2i2c.mybinder.org/user/vincesmandres-pruebatecnica-jjsx8zef/doc/workspaces/auto-n/tree/Reto_Tecnico.ipynb)

# Reto de Minería

Este proyecto presenta una simulación para calcular la cantidad de **mineral valioso** extraído a partir de datos aleatorios. El objetivo es ayudar a estimar la producción minera considerando factores como tonelaje extraído, ley de cabeza, dilución y recuperación metalúrgica.

## Características Principales
- ✅ Cálculo preciso de mineral valioso en kilogramos.
- ✅ Validación de entradas para evitar valores negativos.
- ✅ Simulación aleatoria de condiciones mineras en 5 bloques.
- ✅ Fórmula basada en principios metalúrgicos reales.

## Instalación
1. Clona el repositorio:

```bash
git clone https://github.com/vincesmandres/PruebaTecnica.git
cd PruebaTecnica
```

2. Instala las dependencias necesarias (en caso de haberlas):

```bash
pip install -r requirements.txt
```

## Uso
1. Abre el notebook `Reto_Tecnico.ipynb` en Jupyter Notebook o en cualquier entorno compatible.
2. Ejecuta las celdas para visualizar la simulación de extracción minera.

### Ejemplo de Código

```python
import random

def calcular_mineral_valioso(tonelaje_extraido, ley_cabeza, dilucion, recuperacion):
    """
    Calcula la cantidad de mineral valioso extraído en kilogramos.
    """
    if any(param < 0 for param in [tonelaje_extraido, ley_cabeza, dilucion, recuperacion]):
        raise ValueError("Los valores no pueden ser negativos.")

    # Cálculo del mineral valioso
    ley_cabeza /= 100
    dilucion /= 100
    recuperacion /= 100

    mineral_valioso = tonelaje_extraido * (1 - dilucion) * ley_cabeza * recuperacion * 1000
    
    return round(mineral_valioso, 2)
```

## Tecnologías Utilizadas
- Python 3.x
- Jupyter Notebook

## Contribución
Las contribuciones son bienvenidas. Para colaborar:
1. Realiza un fork del repositorio.
2. Crea una rama con tu nueva funcionalidad (`git checkout -b nueva-funcionalidad`).
3. Realiza un commit con tus cambios (`git commit -m 'Agrega nueva funcionalidad'`).
4. Envía un Pull Request.

## Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo `LICENSE` para más información.

## Contacto
**Nombre del Desarrollador:** VinceS Mendoza Miakel Andres  
**Email:** vincesmandres@gmail.com  
**LinkedIn:** [https://www.linkedin.com/in/vincesmandres/](https://www.linkedin.com/in/vincesmandres/)

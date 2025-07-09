# 📚 Trabajo de Fin de Título – Comunicación Política en redes sociales

## 🎓 Contexto académico

Este proyecto forma parte de un **Trabajo de Fin de Título (TFT)** cuyo objetivo principal no es el desarrollo de herramientas, sino la **investigación en comunicación política a través de las redes sociales y, en concreto, de X/Twitter**.

El código almacenado en los distintos módulos del trabajo —aunque incluye componentes software funcionales (recolector, clasificadores, app de análisis)— **sirve de apoyo a la investigación**, permitiendo recolectar, procesar y visualizar los datos necesarios para el análisis posterior.

> 🧩 Las herramientas desarrolladas cumplen un rol vital dentro del TFT, pero **la finalidad del proyecto es puramente analítica**.

---

Este repositorio agrupa las tres piezas principales de un sistema para la recolección, análisis y visualización de mensajes políticos publicados en la red social X (anteriormente Twitter), centrado en la actividad de políticos españoles. Se compone de:

* 🛰️ `recolector`: recolección, limpieza y traducción de publicaciones y comentarios.
* 🧠 `clasificador_analisis`: entrenamiento y evaluación de modelos para clasificar el contenido político por **tema** y **tono**.
* 📊 `analisis-politico-x-twitter`: aplicación interactiva en Streamlit para explorar los resultados de forma visual.

---

## 🔧 Repositorios incluidos como submódulos

| Módulo                                                                                     | Descripción                                                                                             |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| [`recolector`](https://github.com/jabado2701/recolector)                                   | Extrae metadatos, publicaciones y comentarios de políticos en X. Limpia y traduce los datos a español.  |
| [`clasificador_analisis`](https://github.com/jabado2701/clasificador_analisis)             | Entrena clasificadores temáticos y de tono político usando modelos preentrenados BERT. Incluye notebooks de análisis. |
| [`analisis-politico-x-twitter`](https://github.com/jabado2701/analisis-politico-x-twitter) | App en Streamlit para analizar y visualizar la actividad política y el resultado de los clasificadores. |

---

## 🗂️ Estructura del repositorio principal

```
TFG-Comunicacion-Politica/
├── recolector/                  # Submódulo: recolección y procesamiento
├── clasificador_analisis/       # Submódulo: modelos de clasificación
├── analisis-politico-x-twitter/ # Submódulo: app de visualización
├── .gitmodules                  # Referencias a subrepositorios
├── README.md                    # Este archivo
└── .gitignore
```

---

## 🚀 Cómo clonar y preparar el proyecto completo

```bash
# 1. Clonar el repositorio con submódulos
git clone --recurse-submodules https://github.com/jabado2701/TFG-Comunicacion-Politica.git
cd TFG-Comunicacion-Politica

# 2. Instalar los requisitos de cada módulo (uno por uno)
cd recolector
pip install -r requirements.txt

cd ../clasificador_analisis
pip install -r requirements.txt

cd ../analisis-politico-x-twitter
pip install -r requirements.txt
```

---

## 🧠 Notas

* Algunos archivos pesados (`.xlsx`) y modelos exportados (`safetensors`) han sido excluidos por tamaño. Deben colocarse manualmente en las carpetas indicadas en cada módulo.
* Toda la información tratada en el proyecto es **pública**, extraída de fuentes oficiales como el Congreso de los Diputados, Wikipedia o X (Twitter).
* Los clasificadores se pueden regenerar si se dispone de los datos etiquetados y los pesos de modelos.

---

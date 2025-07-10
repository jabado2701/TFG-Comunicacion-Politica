# 📚 Trabajo de Fin de Título – Comunicación Política en redes sociales
---

## 🎓 Contexto académico

Este proyecto forma parte de un **Trabajo de Fin de Título (TFT)** cuyo objetivo principal es la **investigación en comunicación política en las redes sociales y, en concreto, en X/Twitter**. Para dar soporte a los objetivos del proyecto se han desarrollado algunas herramientas de software, cuyo código se incluye en este repositorio.

Las herramientas desarrolladas —el recolector, los clasificadores y la aplicación de análisis— cumplen un rol importante dentro del TFT, aunque la finalidad principal del trabajo es el análisis de datos.

> 📄 El proceso completo y los resultados del análisis se recogen en la memoria del TFT, que estará disponible de forma pública en la web de la Biblioteca de la ULPGC.

---


Este repositorio agrupa las tres herramientas principales de un sistema para la recolección, análisis y visualización de mensajes políticos publicados en la red social X (anteriormente Twitter), centrado en la actividad de políticos españoles. Se compone de:

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

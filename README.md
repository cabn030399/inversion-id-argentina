# Análisis de inversión en I+D en Argentina (2004–2024)

## Descripción

Análisis exploratorio de la evolución de la inversión en Investigación y Desarrollo (I+D) en Argentina entre 2004 y 2024.

El proyecto analiza la evolución de los recursos destinados a I+D y su distribución por sector ejecutor, provincia y disciplina científica. El objetivo es identificar cambios relevantes en la composición y evolución de la inversión, manteniendo un enfoque descriptivo y documentando las limitaciones de los datos.

---

## 1. Información general

**Nombre del proyecto:**
Análisis de inversión en I+D en Argentina (2004–2024)

**Especialidad:**
Data Analytics (DA)

**Fuente del proyecto:**
Dataset de inversión en Investigación y Desarrollo (I+D) de Argentina.

**Fuente original:**
Dataset inversion.xlsx proporcionado para el desarrollo del proyecto. No se dispone de información adicional para validar el enlace de publicación original o la documentación metodológica del dataset.

**Proyecto publicado:**
https://github.com/cabn030399/inversion-id-argentina
---

## 2. Objetivo

Analizar cómo evolucionó la inversión en Investigación y Desarrollo (I+D) en Argentina entre 2004 y 2024 y cómo cambió su distribución entre sectores, provincias y disciplinas.

El análisis busca aportar información descriptiva que pueda servir como punto de partida para comparar la evolución de la inversión y apoyar el análisis de instituciones públicas, investigadores u otros interesados en el comportamiento de la inversión en I+D.

---

## 3. Plan de trabajo

### 1. Exploración inicial

* Revisión de las cuatro hojas del dataset.
* Identificación de dimensiones, indicadores y períodos disponibles.
* Revisión de tipos de datos, valores nulos y duplicados.
* Identificación de posibles claves para cada tabla.

### 2. Preparación y control de calidad

* Verificación de la estructura de los datos.
* Revisión de duplicados y valores faltantes.
* Comparación de los totales financieros con los desgloses por sector, provincia y disciplina.
* Identificación y documentación de discrepancias sin realizar ajustes artificiales.

### 3. Análisis

* Análisis de la evolución de los indicadores financieros entre 2004 y 2024.
* Construcción de índices con base 2004 = 100 para las series monetarias.
* Análisis de la participación de cada sector ejecutor.
* Análisis de la distribución territorial de la inversión.
* Análisis de la distribución por disciplina científica.

### 4. Evaluación e interpretación

* Comparación de cambios entre distintos períodos.
* Identificación de variaciones relevantes en la composición de la inversión.
* Revisión de la consistencia entre las distintas hojas del dataset.
* Documentación de limitaciones y discrepancias detectadas.

### 5. Conclusiones

* Resumen de los principales hallazgos.
* Identificación de las principales limitaciones del análisis.
* Propuesta de posibles líneas de análisis posteriores.

---

## 4. Preguntas clave

Antes de considerar terminado el análisis se plantearon las siguientes preguntas:

1. ¿De dónde provienen exactamente los datos y qué tan vigente y documentada es su metodología?
2. ¿Las distintas hojas del dataset utilizan las mismas definiciones y unidades para representar la inversión?
3. ¿Cómo deben interpretarse las diferencias encontradas entre el total financiero y algunos de sus desgloses?

Estas preguntas son especialmente relevantes porque algunas discrepancias no pueden explicarse únicamente a partir del dataset disponible.

---

## 5. Qué se hizo y cómo

El análisis se realizó utilizando Python y Pandas, complementados con NumPy y Matplotlib para las transformaciones y visualizaciones.

El dataset contiene cuatro hojas:

* **Recursos Financieros:** indicadores agregados anuales.
* **Sector:** inversión por sector ejecutor.
* **Provincias:** inversión por provincia.
* **Disciplinas:** inversión por disciplina científica.

Las cuatro hojas contienen información correspondiente al período 2004–2024.

### Control de calidad

Se revisaron:

* dimensiones de las tablas;
* nombres y tipos de variables;
* valores faltantes;
* filas duplicadas;
* posibles claves únicas;
* consistencia entre los totales financieros y los distintos desgloses.

No se realizaron imputaciones ni modificaciones destinadas a forzar la conciliación de los datos.

### Análisis financiero

Se analizaron las series disponibles de:

* inversión en pesos corrientes;
* inversión en pesos constantes;
* inversión en dólares corrientes;
* inversión en dólares PPC, según la etiqueta del archivo;
* inversión en I+D como proporción del PBI;
* participación pública y privada como proporción del PBI.

Para las series monetarias también se calcularon índices tomando 2004 como año base = 100.

### Análisis sectorial

Se calculó la participación porcentual de cada sector ejecutor sobre la inversión total y se comparó su composición entre 2004 y 2024.

Entre los cambios observados se encuentra un aumento de la participación de las empresas y una reducción de la participación relativa de las universidades públicas.

### Análisis territorial

Se analizó la distribución de la inversión por provincia, incluyendo su participación sobre el total y las diferencias observadas entre territorios.

### Análisis por disciplina

Se revisó la distribución de la inversión entre disciplinas científicas y su relación con el total financiero.

Debido a que la suma por disciplinas no coincide completamente con el total financiero, esta diferencia se mantiene documentada como una limitación y no se atribuye a una causa que no pueda demostrarse con los datos disponibles.

---

## 6. Resultados principales

El análisis muestra cambios importantes en la evolución y composición de la inversión en I+D durante el período estudiado.

Entre los principales resultados:

* La serie de pesos corrientes presenta un crecimiento nominal muy pronunciado, especialmente en los últimos años.
* La serie en pesos constantes presenta una evolución diferente: crecimiento hasta 2015, retrocesos posteriores, recuperación hasta 2023 y una caída en 2024.
* Las series expresadas en dólares presentan períodos de crecimiento y retroceso, con una disminución en 2024.
* La inversión en I+D como proporción del PBI pasa de 0.59 en 2023 a 0.49 en 2024, según los valores disponibles en el dataset.
* La participación de las empresas aumenta de 32.98% en 2004 a 47.52% en 2024.
* La participación de los organismos públicos de ciencia pasa de 39.61% a 35.04%.
* La participación de las universidades públicas pasa de 22.97% a 14.45%.

En la revisión de consistencia se identificó además una diferencia en 2023 entre el total financiero y la suma de los sectores de aproximadamente 6,984 unidades, equivalente a alrededor de 0.61% del total financiero de ese año.

La suma de las inversiones por disciplina también queda por debajo del total financiero, por lo que este resultado se presenta como una limitación del dataset y no como una categoría adicional cuya naturaleza pueda afirmarse sin documentación complementaria.

---

## 7. Conclusiones

El análisis permitió describir la evolución de la inversión en I+D en Argentina entre 2004 y 2024 desde diferentes dimensiones: financiera, sectorial, territorial y científica.

Uno de los principales aprendizajes fue la importancia de realizar controles de calidad antes de interpretar los resultados. La comparación entre hojas permitió detectar diferencias que no deberían ignorarse al presentar las conclusiones.

También se observó que una variación nominal de la inversión no necesariamente representa un crecimiento real, por lo que las series en pesos corrientes deben interpretarse con precaución.

Con más tiempo y documentación metodológica sería posible profundizar en la definición de las unidades, validar la fuente original y explicar las diferencias encontradas entre algunos desgloses y el total financiero.

La parte que destacaría en una entrevista es el proceso de control de calidad y reconciliación de los datos: antes de sacar conclusiones, se verificó la consistencia entre las diferentes tablas y se documentaron las discrepancias en lugar de corregirlas sin evidencia.

---

## 8. Limitaciones

* La fuente original y la documentación metodológica deben validarse antes de realizar interpretaciones más profundas.
* No se confirmaron completamente las definiciones de todas las unidades y siglas utilizadas por el dataset.
* La discrepancia observada en el desglose por sector para 2023 no pudo ser explicada con la información disponible.
* La suma por disciplina no coincide con el total financiero y su causa no está determinada.
* La serie de pesos corrientes no debe interpretarse como crecimiento real.
* El análisis es descriptivo y no busca establecer relaciones causales.
* No se realizaron imputaciones ni ajustes para forzar la conciliación entre tablas.

---

## 9. Estructura del proyecto

```text
inversion-id-argentina/
│
├── README.md
│
├── notebooks/
│   └── 01_exploracion_inversion.ipynb
│
├── data/
│   └── README.md
│
└── .gitignore
```

El dataset original no se incluye en el repositorio cuando su distribución no corresponde al proyecto. El notebook utiliza una estructura de archivos relativa al proyecto.

---

## 10. Herramientas utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook

---

## 11. Próximos pasos posibles

Como extensión del análisis, sería posible:

* validar la fuente y documentación metodológica;
* investigar las discrepancias encontradas;
* profundizar en la evolución territorial;
* ampliar el análisis de las disciplinas científicas;
* incorporar información adicional que permita interpretar los cambios observados.

Estas extensiones quedan fuera del alcance de esta primera versión del proyecto.

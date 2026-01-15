# CASO DE ÉXITO: Base de datos del proyecto Regulus Divulgación (ejemplo anonimizando)

## Contexto
**Regulus Divulgación** es un proyecto personal de divulgación científica creado en **julio de 2024**, enfocado principalmente en **talleres en línea de matemáticas y astronomía**. Desde su creación, ha impartido **talleres de forma mensual hasta la actualidad**, con el objetivo de acercar el conocimiento científico a públicos diversos, fomentar el pensamiento crítico y vocaciones científicas a jóvenes estudiantes. Se busca que aprender sea una experiencia cercana, clara y estimulante.

La **Comunidad Regolita** es el nombre con el que se identifica a las personas que se registran y participan en los talleres de **Régulus Divulgación**. El término hace referencia al *regolito*, el material que cubre la superficie de cuerpos como la Luna o Marte. Este concepto representa a una comunidad en crecimiento, formada por personas curiosas que exploran el conocimiento paso a paso y que son invitadas a **continuar registrándose en futuros talleres**, fortaleciendo su formación y su vínculo con la ciencia.

Este repositorio presenta un **ejemplo de control de flujo y gestión de actividades** utilizado en el proyecto *Regulus Divulgación*. El objetivo es mostrar la **estructura de datos**, la lógica de seguimiento y la organización operativa de un proyecto de divulgación científica, sin exponer información sensible (seguridad de datos). Los datos incluidos son **ficticios y anonimizados**, pero conservan la **estructura, relaciones y dinámica** del flujo real de trabajo.

---

## Objetivo del repositorio

- Mostrar un ejemplo realista de **gestión y seguimiento de actividades** en una hoja de cálculo.
- Ilustrar cómo se organiza el flujo de proyectos, tareas y estados dentro de una iniciativa de divulgación científica.
- Servir como base para **análisis exploratorio de datos**, visualización y automatización.
- Evidenciar buenas prácticas en el **manejo responsable de datos**.

---

## Sobre los datos

El archivo principal del repositorio es una **tabla en formato Excel**, diseñada para registrar y dar seguimiento a:

- Actividades y cursos del proyecto.
- Estados del flujo de trabajo (planeación, ejecución y cierre).
- Participación y asistencia de personas (anonimizadas).
- Indicadores de desempeño y métricas de seguimiento.

La base está organizada siguiendo una **estructura relacional**, en la que distintas hojas se vinculan mediante identificadores comunes. Esta organización permite **combinar información sin duplicar datos**, facilitando la generación de métricas consistentes y **gráficos dinámicos** para análisis y reporte.

### Importante
- **No contiene nombres reales, correos, teléfonos ni información personal.**
- Los valores han sido **modificados o generados con fines demostrativos**.
- La estructura refleja fielmente el flujo de trabajo original.

El archivo `regulus_database.xlsx` fue **descargado a partir de una hoja de cálculo en Google Sheets**, utilizada originalmente como herramienta de trabajo colaborativo. El formato en Excel conserva la **estructura, relaciones y fórmulas clave** del documento original, adaptado para su análisis y distribución en este repositorio. Para consultar el **estilo original de la base de datos** (diseño visual y organización del flujo), puede accederse a la versión en Google Sheets en el siguiente enlace:

👉 *https://docs.google.com/spreadsheets/d/1J9cqWRFYp_ysqLqXJ4zxWrdxEGE70V-UZlzsJaDjpE0/edit?usp=sharing*

---

## Procesos clave desde el enfoque de análisis de datos

El diseño del archivo permite implementar procesos relevantes para un analista de datos, tales como:

- Seguimiento de participación y asistencia por actividad.
- Análisis temporal por año y mes.
- Comparación de desempeño entre cursos o temáticas.
- Generación de indicadores agregados a partir de datos granulares.
- Preparación de la información para visualización y dashboards.

---


## Estructura general del archivo

El archivo está compuesto por las siguientes hojas:

## Hoja: `CURSOS`

Contiene el **catálogo principal de cursos y actividades**.

### Estructura
- Cada **fila representa un curso o actividad**.
- Incluye información descriptiva (nombre, temática, tipo).
- Incluye variables temporales (año y mes).
- Contiene métricas agregadas de desempeño:
  - Total de sesiones
  - Personas inscritas
  - Porcentaje de asistencias
  - Porcentaje de reconocimientos

### Uso analítico
- Análisis de desempeño por curso.
- Comparaciones por temática, periodo o tipo de actividad.
- Base para agregaciones y dashboards.

---

## Hoja: `REGOLITOS`

Contiene el **registro de participantes**.

### Estructura
- Cada **fila representa una persona única**.
- Incluye variables demográficas y de clasificación:
  - Edad
  - Ocupación
  - Procedencia
  - Grupo de edad
- Incluye campos de control administrativo (tutor, año de ingreso).

### Uso analítico
- Segmentación por grupos de edad.
- Análisis de procedencia y perfiles.
- Relación con cursos mediante identificadores.

---

## Hoja: `ASISTENCIAS`

Es la hoja **más granular y central para el análisis**.

### Estructura
- Cada **fila representa la participación de una persona en un curso**.
- Contiene:
  - Identificadores de curso y persona
  - Variables demográficas
  - Registro de asistencia por sesión (`S1`, `S2`, ..., `S11`)
  - Porcentaje de asistencia calculado
  - Indicador de reconocimiento

### Uso analítico
- Cálculo automático de porcentajes de asistencia.
- Evaluación de compromiso por curso o grupo.
- Análisis longitudinal de participación.
- Base para métricas agregadas en otras hojas.

---

## Hoja: `TEMATICA`

Contiene un **resumen agregado por temática**.

### Estructura
- Cada **fila representa una temática** (por ejemplo, Astronomía, Matemáticas).
- Incluye métricas promedio de:
  - Porcentaje de asistencia
  - Porcentaje de reconocimientos

### Uso analítico
- Comparación de impacto entre áreas temáticas.
- Soporte para reportes ejecutivos.

---

## Hojas de visualización y análisis gráfico

Además de las hojas de datos, el archivo incluye hojas dedicadas exclusivamente a **visualización**, construidas a partir de la estructura relacional de la base de datos. Estas hojas permiten interpretar de forma rápida el comportamiento de la audiencia y el desempeño de los cursos.

---

### Hoja: `GRUPOS_DE_EDAD`

Contiene un **gráfico circular** que muestra la distribución de la audiencia por grupos de edad.

**Uso analítico:**
- Identificar los rangos de edad con mayor participación.
- Definir un **perfil o audiencia ideal** para la toma de decisiones estratégicas.

---

### Hoja: `PROCEDENCIA`

Incluye un **histograma** que representa la procedencia geográfica de la audiencia, ya sea por estados de la República o por países.

**Uso analítico:**
- Visualizar la distribución territorial de la audiencia.
- Identificar regiones con mayor o menor alcance.
- Evaluar la expansión geográfica del proyecto.

---

### Hoja: `%ASISTENCIA`

Presenta un **gráfico de barras** con los porcentajes de asistencia correspondientes a cada curso.

**Uso analítico:**
- Comparar el nivel de participación entre cursos.
- Detectar actividades con alta o baja retención.
- Es un KPI para evaluar la efectividad del diseño de los cursos.

---

### Hoja: `%RECONOCIMIENTOS`

Presenta un **gráfico de barras** con el porcentaje de personas que reciben reconocimiento en cada curso.

**Uso analítico:**
- Es un KPI para evaluar el nivel de finalización de los cursos.
- Comparar el desempeño entre distintas actividades.
- Identificar cursos con mayor impacto formativo.

## Automatización y análisis de datos

El diseño del archivo permite el uso eficiente de funciones de Excel como:

- `CONTAR.SI` para conteos automáticos por curso, temática o periodo.
- `BUSCARX` / `XLOOKUP` para vincular información entre hojas sin duplicar datos.
- Cálculo automático de porcentajes y métricas agregadas.

Esto reduce errores manuales y mejora la trazabilidad del análisis.

---

## Estructura del repositorio

```text
regulus/
│
├── regulus_database.xlsx    Archivo de ejemplo con datos anonimizados
│
├── README.md                         Descripción del repositorio
│
└── LICENSE

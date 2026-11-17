# Trabajo Final Integrador – Grupo 42
## Detección de cáncer de mama con Machine Learning

**Universidad Provincial del Sudoeste (UPSO)**
Materia: Elementos de Aprendizaje de Máquina y Big Data
Docentes: Ing. Valentín Barco – Dr. Claudio A. Delrieux
Carrera: T.U. Tecnologías de Programación
Integrante: Leonardo Fiz

---

### ¿De qué se trata?

En este trabajo quise predecir si un tumor de mama es benigno o maligno usando las medidas de las células de **569 pacientes** (dataset *Breast Cancer Wisconsin – Diagnostic*, que viene incluido en scikit-learn).

### ¿Qué hay en el repositorio?

| Archivo | Contenido |
|---|---|
| `Trabajo_Final_Grupo_42.ipynb` | Notebook con todo el código, paso a paso y con explicaciones. |
| `Trabajo_Final_Grupo_42.pdf` | Informe del trabajo con gráficos, tablas y conclusiones. |

### ¿Qué se hizo?

1. Carga de los datos en un DataFrame de pandas.
2. Validación y limpieza (faltantes y duplicados).
3. Estadística descriptiva, gráficos, mapa de calor de correlación y prueba de hipótesis (t de Student).
4. Separación en entrenamiento (80%) y testeo (20%), y escalado de los datos.
5. Comparación de 4 modelos de clasificación: KNN, Naive Bayes, SVM y Árbol de Decisión, con matriz de confusión, curva ROC y validación cruzada.
6. Reducción de dimensionalidad con PCA.
7. Clustering con K-medias.

### Resultados principales

| Modelo | Exactitud | Sensibilidad | AUC |
|---|---|---|---|
| SVM | **0,974** | **0,929** | **0,995** |
| KNN (K=3) | 0,939 | 0,857 | 0,982 |
| Naive Bayes | 0,921 | 0,857 | 0,989 |
| Árbol de Decisión | 0,912 | 0,810 | 0,877 |

El mejor modelo fue el SVM: acertó el 97,4% de los pacientes de testeo y no dio ninguna falsa alarma.

### ¿Cómo correrlo?

**Opción 1 – Google Colab (no hace falta instalar nada):**
1. Entrar a [colab.research.google.com](https://colab.research.google.com).
2. *Archivo → Subir notebook* y elegir `Trabajo_Final_Grupo_42.ipynb`.
3. *Entorno de ejecución → Ejecutar todas*.

**Opción 2 – En la compu:**
```bash
pip install pandas numpy matplotlib scipy scikit-learn jupyter
jupyter notebook Trabajo_Final_Grupo_42.ipynb
```

Los datos se cargan solos desde scikit-learn, no hace falta descargar ningún archivo.

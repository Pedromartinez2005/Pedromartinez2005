# 👋 Hola, soy Pedro Álvaro Martínez Gutiérrez

Estudiante de último curso del **Grado en Ciencia de Datos e Inteligencia Artificial** (Universidad Politécnica de Madrid). Lo que más me interesa de este campo no es solo entrenar el modelo con la mejor métrica, sino entender **qué decisión de negocio hay detrás de cada proyecto**: qué error cuesta más caro, qué estrategia se prioriza, qué es mantenible de verdad en producción.

En cada uno de mis proyectos vas a encontrar la misma estructura: primero el objetivo de negocio, después los resultados, y por último por qué elegimos lo que elegimos — que no siempre es lo que "gana" en la métrica.

---

## 🧠 Cómo enfoco un proyecto

- **El objetivo de negocio se define antes de tocar ningún modelo** — qué tipo de error pesa más, qué se prioriza, qué riesgo compensa asumir.
- **La métrica más alta no siempre gana.** Prefiero el modelo (o la decisión) que mejor encaja con ese objetivo, aunque no sea el número más vistoso de la tabla.
- **Documentar lo que no funcionó** es tan importante como lo que sí — tanto para las siguientes mejoras técnicas como para poder justificar una decisión ante alguien que no ha visto el código.
- **Un análisis solo vale si se puede llevar a la práctica** — por eso varios de mis proyectos incluyen explícitamente un apartado de "para qué serviría esto en un negocio real".

---

## 🛠️ Stack técnico

**Lenguajes:** Python · SQL · R · MATLAB

**Machine Learning:** Scikit-learn · Deep Learning (TensorFlow) · GridSearchCV / validación cruzada · SMOTE (imbalanced-learn) · Bagging, Random Forest, AdaBoost, Gradient Boosting, Stacking · PCA / SelectKBest / Mutual Information

**Datos:** Pandas · NumPy · Web scraping (Selenium) · EDA (análisis exploratorio) · preprocesamiento y escalado (QuantileTransformer, StandardScaler) · limpieza e integración de datos multi-fuente

**Visualización:** Matplotlib · Seaborn

**Cloud & Despliegue:** Docker · AWS · APIs / REST · PyInstaller

**Otros:**  Git / control de versiones · Jupyter / Google Colab

---

## 📂 Proyectos destacados

### 💳 [Riesgo de crédito](https://github.com/Pedromartinez2005/credit-risk-classification)
Comparativa de 4 modelos de clasificación para decidir si conceder crédito a un cliente. El modelo final no lo decide la accuracy más alta: definimos primero qué tipo de error (rechazar un buen cliente vs. aprobar uno malo) encajaba con una estrategia de crecimiento, y elegimos según ese criterio de negocio.

### 🚗 [Depreciación de coches de ocasión en 4 mercados europeos](https://github.com/Pedromartinez2005/coches)
Web scraping de 7 portales en España, Francia, Alemania y Holanda para cuantificar cómo se deprecia un coche según el kilometraje, mercado por mercado. Esa tasa de depreciación real (€ por cada 10.000 km) es justo el dato que una empresa de renting necesita para fijar la cuota mensual según el kilometraje contratado: a más depreciación por km, mayor debería ser la cuota si el cliente pide más kilómetros incluidos o gestión de flotas decidiendo en qué país vender sus vehículos.

### 🧩 [Clasificación con métodos de Ensemble](https://github.com/Pedromartinez2005/ensemble-classification)
Comparativa sistemática de 7 familias de clasificadores (Bagging, Random Forest, AdaBoost, Gradient Boosting, Stacking...). Ante un empate técnico entre dos modelos, elegimos el más simple — la misma pregunta que hay que hacerse antes de llevar un modelo a producción: ¿esa décima de más justifica el coste de mantener algo más complejo?

### 🚇 [Planificador de rutas — Subte de Buenos Aires](https://github.com/Pedromartinez2005/buenos-aires-metro-route-planner)
Aplicación de escritorio que calcula la ruta óptima entre estaciones con el algoritmo A*, usando horarios y frecuencias reales por línea. Trabajo en equipo de 6 personas, empaquetado como ejecutable para que fuera utilizable de verdad, no solo un script de laboratorio.

---

## 📫 Contacto

📧 pedromartinezgutierrez@gmail.com

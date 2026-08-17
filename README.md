# 👋 Hola, soy Pedro Álvaro Martínez Gutiérrez

Estudiante de último curso del **Grado en Ciencia de Datos e Inteligencia Artificial** (Universidad Politécnica de Madrid). Lo que más me interesa de este campo no es solo entrenar el modelo con la mejor métrica, sino entender **qué decisión de negocio hay detrás de cada proyecto**: qué error cuesta más caro, qué estrategia se prioriza, qué es mantenible de verdad en producción — y, cada vez más, cómo llevar eso a sistemas que funcionan solos, no solo a notebooks.

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

**APIs y automatización:** API de Anthropic (Claude) · APIs REST · GitHub Actions (CI/CD) · pytest (mocking de servicios externos)

**Cloud & Despliegue:** Docker · AWS · PyInstaller

**Otros:** Git / control de versiones · Jupyter / Google Colab

---

## 🤖 Proyectos con LLMs y automatización

### 📈 [Informe diario BTC/ETH/S&P 500](https://github.com/Pedromartinez2005/daily-market-report-v2)
Antes hacía esto a mano: abría un chat nuevo cada día y le pasaba precios a un LLM para que opinara. El problema es que sin datos estructurados un LLM no calcula indicadores de forma fiable, y cada día parte de cero. Este proyecto separa las dos cosas: un motor de reglas explicable (tendencia + RSI + contexto macro del S&P 500) calcula la recomendación, y la API de Claude solo la redacta. La decisión de diseño que más vale la pena explicar: un RSI en sobreventa **no** significa lo mismo según el contexto — en una tendencia alcista es un pullback sano (oportunidad), en una bajista es solo inercia de la caída (no se premia). La primera versión no distinguía esto; el test que lo cubre está en el repo.

### 💧 [Optimizador de rango — pool de liquidez ETH/USD](https://github.com/Pedromartinez2005/eth-lp-range-optimizer)
En una posición de liquidez concentrada (estilo Uniswap v3) el trade-off es directo: rango estrecho = más comisiones pero rebalanceos frecuentes; rango ancho = menos comisiones pero más estable. En vez de fijar el ancho a ojo, lo calculo a partir de la volatilidad realizada de ETH y una probabilidad objetivo de seguir dentro del rango. La matemática de liquidez concentrada la verifiqué contra la fórmula clásica de Uniswap v2 en su caso límite — y ahí encontré un fallo real: mi primer cálculo de pérdida impermanente confundía el capital que no encajaba en la proporción del rango con pérdida real, cuando en realidad ese sobrante se queda simplemente fuera de la pool. Incluye un backtester para medir, sobre histórico, qué fracción del tiempo se habría mantenido el precio dentro del rango recomendado.

### 💶 [Gastos personales con Claude + Excel](https://github.com/Pedromartinez2005/gastos-claude-excel)
Caso de estudio, no código: uso Claude conectado directamente a mi Excel personal como interfaz en lenguaje natural para registrar gastos sin abrir la hoja ni recordar en qué pestaña va cada categoría. La parte interesante no es el Excel — es que Claude traduce una frase suelta y ambigua ("he pagado 42€ del súper") a una fila estructurada, sin romper ninguna fórmula del resto de la hoja, y prefiero que pregunte ante la ambigüedad a que asuma mal y meta ruido en el resumen mensual.

---

## 📂 Proyectos de Machine Learning

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

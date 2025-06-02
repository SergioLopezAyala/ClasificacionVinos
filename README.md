# Clasificación Binaria con Perceptrón y Redes Neuronales Profundas usando Keras

Este proyecto implementa modelos de redes neuronales para resolver un problema de **clasificación binaria** usando `TensorFlow` y `Keras`. Se exploran tres arquitecturas diferentes: un perceptrón simple, una red neuronal con una capa oculta, y una red profunda con múltiples capas ocultas.

## 📁 Estructura del Proyecto

├── README.md
├── requirements.txt
├── data/
│ ├── train.csv
│ └── test.csv
├── models/
│ ├── model1_perceptron.py
│ ├── model2_simple_nn.py
│ └── model3_deep_nn.py
├── utils/
│ └── preprocessing.py
└── main.py

shell
Copiar
Editar

## 📌 Objetivo

Construir y comparar diferentes modelos de redes neuronales para un problema de clasificación binaria, evaluando su desempeño y comportamiento con distintas arquitecturas.

## 🧠 Modelos Implementados

### 1. Perceptrón Simple (`model1_perceptron.py`)
- Una sola neurona con activación sigmoide.
- Arquitectura equivalente a una regresión logística.

### 2. Red Neuronal con Capa Oculta (`model2_simple_nn.py`)
- Una capa oculta con tantas neuronas como características de entrada.
- Act. sigmoide en capa oculta y salida.

### 3. Red Neuronal Profunda (`model3_deep_nn.py`)
- Tres capas ocultas con 3 neuronas cada una.
- Activaciones sigmoides en cada capa.

## 🛠️ Tecnologías Usadas

- Python 3.8+
- TensorFlow/Keras
- NumPy
- Pandas
- Matplotlib (para visualización)
- Scikit-learn (para métricas y preprocesamiento)

## 🚀 Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/tu_usuario/tu_repo.git
cd tu_repo
Instala los requisitos:

bash
Copiar
Editar
pip install -r requirements.txt
🧪 Ejecución del Proyecto
bash
Copiar
Editar
python main.py
Este script realiza:

Carga y preprocesamiento de datos.

Entrenamiento de los tres modelos.

Evaluación y comparación con métricas de validación.

Gráficas de entrenamiento.

📊 Resultados
Se registran las métricas de accuracy y loss para los tres modelos y se grafican para comparación. La idea es observar cómo la profundidad afecta la capacidad de aprendizaje del modelo.

📈 Ejemplo de gráfico de entrenamiento
python
Copiar
Editar
plt.plot(history1.history['val_accuracy'], label='Perceptrón')
plt.plot(history2.history['val_accuracy'], label='Red Simple')
plt.plot(history3.history['val_accuracy'], label='Red Profunda')
plt.xlabel('Épocas')
plt.ylabel('Precisión de Validación')
plt.title('Comparación de Precisión')
plt.legend()
plt.show()
📌 Consideraciones
Las funciones de activación sigmoid fueron utilizadas en todas las capas ocultas para comparar con un perceptrón clásico, aunque ReLU puede ser más eficiente en redes profundas.

Si el modelo sobreajusta, se recomienda añadir técnicas de regularización como Dropout o L2.

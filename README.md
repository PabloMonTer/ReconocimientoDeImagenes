# Reconocimiento De Imagenes

Este proyecto se centra en el reconocimiento de imágenes de prendas de vestir utilizando la base de datos Fashion MNIST. Para lograr una predicción precisa, se utilizaron redes neuronales convolucionales (CNN), junto con el modelo avanzado ResNet, que se entrenó para clasificar correctamente las imágenes de diversas categorías de ropa. Además, se aplicó una técnica de aumento de datos para mejorar la robustez y precisión del modelo, incrementando la diversidad de las imágenes de entrenamiento.

## Metodología
El proceso de desarrollo de este proyecto se dividió en varias etapas clave:

### 1. Preparación de los Datos
La base de datos utilizada en este proyecto es Fashion MNIST, que contiene 60,000 imágenes de entrenamiento y 10,000 imágenes de prueba, cada una representando una prenda de vestir diferente, distribuida en 10 clases, tales como camisetas, pantalones, zapatos, etc.

Aumento de Datos (Data Augmentation): Para mejorar la capacidad del modelo de generalizar a nuevas imágenes y reducir el sobreajuste, se implementó un aumento de datos en las imágenes. Esto incluyó técnicas como:
Rotación de imágenes para crear variaciones angulares.
Desplazamiento y escalado de las imágenes.
Reflejo horizontal de las imágenes.
Estas transformaciones ayudan a simular variaciones en las imágenes que pueden ocurrir en escenarios del mundo real, lo que mejora el rendimiento del modelo en datos no vistos previamente.

### 2. Construcción del Modelo

- 2.1 Redes Neuronales Convolucionales (CNN)
Las redes neuronales convolucionales (CNN) son especialmente adecuadas para el reconocimiento de imágenes. Se construyó una arquitectura CNN básica con varias capas convolucionales y de pooling, seguida de capas densas para la clasificación. Esta arquitectura permite extraer características espaciales de las imágenes y aprender patrones complejos.

- 2.2 Modelo ResNet
Además de la CNN básica, se implementó un modelo ResNet (Residual Network), una arquitectura avanzada que utiliza bloques residuales para permitir un entrenamiento más profundo y eficiente. ResNet es conocido por su capacidad para entrenar redes muy profundas sin sufrir de desvanecimiento o explosión de gradientes. Esto lo hace ideal para este tipo de problemas de clasificación, ya que puede aprender representaciones más complejas y generales.

El modelo ResNet fue preentrenado en un conjunto de datos similar, lo que permitió aprovechar el aprendizaje transferido y mejorar la precisión en nuestro conjunto de datos de Fashion MNIST.

### 3. Entrenamiento del Modelo
El modelo se entrenó utilizando la base de datos de Fashion MNIST aumentada, con las imágenes transformadas mediante las técnicas de aumento de datos. Durante el entrenamiento, se utilizó la función de entropía cruzada como función de pérdida y el optimizador Adam, que es adecuado para tareas de clasificación.

### 4. Evaluación del Modelo
Para evaluar el rendimiento del modelo, se utilizaron las siguientes métricas:

- Precisión: La proporción de predicciones correctas entre todas las predicciones.
- Pérdida: El valor de la función de pérdida en el conjunto de prueba.
- Matriz de confusión: Para ver cómo el modelo clasificó cada clase de prendas de vestir.
El modelo final fue capaz de identificar correctamente las prendas de vestir en las imágenes de prueba con un alto nivel de precisión.

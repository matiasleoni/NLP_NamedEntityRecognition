# Description (English)

NER is ``Named-Entity recognition'', one of the basic tasks of Natural Language Processing. It consists of the task of identifying people, locations, organizations and other entities in an arbitraty text.

In this Jupyter notebook we have a custom Named Entity Recognition (NER) model implemented using PyTorch. The model is defined as a subclass of `nn.Module` and consists of an embedding layer, an LSTM layer, a dropout layer, and a linear layer. The code includes training and evaluation loops. The model is trained using the Adam optimizer with cross-entropy loss. Training is performed for a specified number of epochs, and the loss and gradient norm are logged using `SummaryWriter` from TensorBoard.

At the end of the notebook there are utility functions such as `simplify_entities` which simplifies identified entities by combining consecutive elements, and `identificar_entidades` which uses the trained model to identify named entities in a given text.

Overall, the code implements a custom NER model, training loop, evaluation metrics, and utility functions for entity simplification and identification. All the code is intended to work with spanish language.

_This notebook was developed for the NLP course in UDESA (Buenos Aires, Argentina) under the guidance and correction of Professor Juan Manuel Pérez. If you are an UDESA student, please do not copy this code for homework._

# Descripción (Español)

NER es el reconocimiento de entidades nombradas ("Named Entity Recognition"), una de las tareas básicas del Procesamiento del Lenguaje Natural. Consiste en identificar personas, ubicaciones, organizaciones y otras entidades en un texto arbitrario.

En este Jupyter Notebook, tenemos un modelo personalizado de Reconocimiento de Entidades Nombradas (NER) implementado utilizando PyTorch. El modelo se define como una subclase de `nn.Module` y consta de una capa de embedding, una capa LSTM, una capa de dropout y una capa lineal. El código incluye bucles de entrenamiento y evaluación. El modelo se entrena utilizando el optimizador Adam con pérdida de entropía cruzada. El entrenamiento se realiza durante un número especificado de épocas y se registran la pérdida y la norma del gradiente utilizando `SummaryWriter` de TensorBoard.

Al final del cuaderno, hay funciones de utilidad como `simplify_entities`, que simplifica las entidades identificadas combinando elementos consecutivos, y `identificar_entidades`, que utiliza el modelo entrenado para identificar entidades nombradas en un texto dado.

En resumen, el código implementa un modelo personalizado de NER, bucle de entrenamiento, métricas de evaluación y funciones de utilidad para la simplificación e identificación de entidades. Todo el código está diseñado para trabajar con el idioma español.

_Este Notebook fue desarrollado para el curso de NLP en UDESA (Buenos Aires, Argentina) bajo la guía y correción del Profesor Juan Manuel Pérez. Si sos alumno de UDESA por favor no copies este código para completar las tarea requerida._
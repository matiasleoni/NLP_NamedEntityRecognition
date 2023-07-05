# Description (English)

NER is "Named-Entity recognition", one of the basic tasks of Natural Language Processing. It consists of the task of identifying people [PER], locations [LOC], organizations [ORG] and other entities [MISC] in an arbitraty text.

In this Jupyter notebook we have a custom Named Entity Recognition (NER) model implemented using PyTorch. The model is defined as a subclass of `nn.Module` and consists of an embedding layer, an LSTM layer, a dropout layer, and a CRF layer. The code includes training and evaluation loops. The model is trained using the Adam optimizer with cross-entropy loss. Training is performed for a specified number of epochs, and the loss and gradient norm are logged using `SummaryWriter` from TensorBoard. The model is trained in SPANISH.

At the end of the notebook there are utility functions such as `simplify_entities` which simplifies identified entities by combining consecutive elements, and `identificar_entidades` which uses the trained model to identify named entities in a given text.

As an illustrative example of the trained model and the utility functions, take an arbitrary article form Argentine constitution:
```python
text = "Las denominaciones adoptadas sucesivamente desde 1810 hasta el presente, a saber: Provincias Unidas del Río de la \
Plata, República Argentina, Confederación Argentina, serán en adelante nombres oficiales indistintamente para la \
designación del Gobierno y territorio de las provincias, empleándose las palabras Nación Argentina en la formación \
y sanción de las leyes."
identificar_entidades(model, tokenizer, text)
```
the utility function `identificar_entidades` returns:
```python
[{'entidad': 'LOC', 'texto': 'Río de la Plata'},
 {'entidad': 'LOC', 'texto': 'República Argentina'},
 {'entidad': 'ORG', 'texto': 'Confederación Argentina'},
 {'entidad': 'ORG', 'texto': 'Gobierno'},
 {'entidad': 'ORG', 'texto': 'Argentina'}]
```

Overall, the code implements a custom NER model, training loop, evaluation metrics, and utility functions for entity simplification and identification. All the code is intended to work with spanish language.

_This notebook was developed for the NLP course in UDESA (Buenos Aires, Argentina) under the guidance and correction of Professor Juan Manuel Pérez. If you are an UDESA student, please do not copy this code to complete your homework._

# Descripción (Español)

NER es el reconocimiento de entidades nombradas, una de las tareas básicas del Procesamiento del Lenguaje Natural. Consiste en identificar personas [PER], ubicaciones [LOC], organizaciones [ORG] y otras entidades [MISC] en un texto arbitrario.

En este cuaderno de Jupyter, tenemos un modelo personalizado de Reconocimiento de Entidades Nombradas (NER) implementado usando PyTorch. El modelo se define como una subclase de `nn.Module` y consta de una capa de incrustación, una capa LSTM, una capa de abandono y una capa CRF. El código incluye bucles de entrenamiento y evaluación. El modelo se entrena utilizando el optimizador Adam con una pérdida de entropía cruzada. El entrenamiento se realiza durante un número específico de épocas, y la pérdida y la norma del gradiente se registran utilizando `SummaryWriter` de TensorBoard. El modelo se entrena en ESPAÑOL.

Al final del notebook, hay funciones de utilidad como `simplify_entities`, que simplifica las entidades identificadas combinando elementos consecutivos, e `identificar_entidades`, que utiliza el modelo entrenado para identificar entidades nombradas en un texto dado.

Como ejemplo ilustrativo del modelo entrenado y las funciones de utilidad, tomemos un artículo arbitrario de la constitución argentina:
```python
text = "Las denominaciones adoptadas sucesivamente desde 1810 hasta el presente, a saber: Provincias Unidas del Río de la \
Plata, República Argentina, Confederación Argentina, serán en adelante nombres oficiales indistintamente para la \
designación del Gobierno y territorio de las provincias, empleándose las palabras Nación Argentina en la formación \
y sanción de las leyes."
identificar_entidades(model, tokenizer, text)
```
la función de utilidad `identificar_entidades` devuelve:
```python
[{'entidad': 'LOC', 'texto': 'Río de la Plata'},
 {'entidad': 'LOC', 'texto': 'República Argentina'},
 {'entidad': 'ORG', 'texto': 'Confederación Argentina'},
 {'entidad': 'ORG', 'texto': 'Gobierno'},
 {'entidad': 'ORG', 'texto': 'Argentina'}]
```

En resumen, el código implementa un modelo personalizado de NER, bucle de entrenamiento, métricas de evaluación y funciones de utilidad para la simplificación e identificación de entidades. Todo el código está diseñado para trabajar con el idioma español.

_Este Notebook fue desarrollado para el curso de NLP en UDESA (Buenos Aires, Argentina) bajo la guía y correción del Profesor Juan Manuel Pérez. Si sos alumno de UDESA por favor no copies este código para completar las tarea requeridas._
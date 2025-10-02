# Proyecto Final:

## Modelo de Machine learning para predecir Alteración del Orden en el Sistema Penitenciario Argentino

Grupo M: 
- Lucia Cortes, María Fernanda Farias, Favio Ruggieri, Alejandro Gomez, Sergio Salanitri, Karina Calvo_DS_GrupoM
  
______________________________________________________________________________________________________________________
## Modelos probados: LGBM y/o CatBoost
- 1er_Prueba_Diplomatura_CDyAA_ Proyecto Final_Grupo_M_Cuaderno(COLAB): LGBM solamente:
  - Estratificación (70/30), se dividió los datos en conjuntos de entrenamiento y prueba en esa proporción.
  - Este es un modelo muy básico que no consideró validación, por lo que se decidió continuar con un modelo de temporal Holdout y validación mediante K-fold:

- 2da Prueba_Diplomatura_CDyAA_Proyecto Final_Grupo_M_Cuaderno(COLAB): LGBM y CatBoost aplicando:
    - Temporal Holdout: train 2002-2021 y test en 2022
    - Validación con K-fold (n=5)

- 3er_Prueba_Diplomatura_CDyAA_Proyecto Final_Grupo_M_Cuaderno(COLAB): LGBM y CatBoost aplicando:
    - Temporal Holdout: train 2010-2021 y test en 2022
    - Validación con Rolling window 2019-2021
    - Optimización de hiperparámetros con GridSearchCV

Notas: 
- Utilizando incluso un subdataset balanceado con el 20% del dataset original, el modelo de LGBM tardo aproximadamente en correr 4hs y CatBoost se tilda cuando comienza con la optimización de hiperparámetros. LGBM no mejoró significativamente con la optimización de hiperparámetros por lo que en la siguiente prueba (Archivo Final) no se realizó optimización de hiperparámetros.
- Archivo Final Diplomatura_CDyAA_Proyecto Final_Grupo_M_Cuaderno(COLAB):
LGBM y CatBoost aplicando:
- Para el entrenamiento dataset procesado se utilizó 2010-2018 (60% del dataset), para validación Rolling window de 2019-2021 (30% del dataset) y para el testeo 2022 (10%).

# Proyecto de ciencia de datos:
Precios de las viviendas en Boston

## Dataset
Dataset obtenido desde Kaggle: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

## Pasos a seguir
1. Definición del problema
2. Recolección de datos
3. Análisis exploratorio de datos
4. Preparación de los datos
5. Modelado
6. Evaluación
7. Conclusiones

## Definición del problema

En el siguiente problema hay que predecir el precio de las casas en función de las características que tienen. 

Para ello se cuenta con un dataset de entrenamiento y otro de test. 
- El dataset de entrenamiento cuenta con 81 variables y 1460 observaciones. 
- El dataset de test cuenta con 80 variables y 1459 observaciones. 
- La variable a predecir es el precio de las casas. (SalePrice)

## Las Variables

- SalePrice: el precio de venta de la propiedad en dólares. Esta es la variable objetivo.
- MSSubClass: La clase de edificio
- MSZoning: La clasificación de zonificación general
- LotFrontage: Pies lineales de calle conectados a la propiedad
- LotArea: Tamaño del lote en pies cuadrados
- Street: Tipo de acceso a la carretera
- Alley: Tipo de acceso al callejón
- LotShape: Forma general de la propiedad
- LandContour: Planitud de la propiedad
- Utilities: Tipo de servicios disponibles
- LotConfig: Configuración del lote
- LandSlope: Pendiente de la propiedad
- Neighborhood: Ubicaciones físicas dentro de los límites de la ciudad de Ames
- Condition1: Proximidad a carretera principal o vía férrea
- Condition2: Proximidad a carretera principal o vía férrea (si hay una segunda presente)
- BldgType: Tipo de vivienda
- HouseStyle: Estilo de vivienda
- OverallQual: Calidad general de material y acabado
- OverallCond: Calificación general de condición
- YearBuilt: Fecha de construcción original
- YearRemodAdd: Fecha de remodelación
- RoofStyle: Tipo de techo
- RoofMatl: Material del techo
- Exterior1st: Revestimiento exterior de la casa
- Exterior2nd: Revestimiento exterior de la casa (si hay más de un material)
- MasVnrType: Tipo de revestimiento de mampostería
- MasVnrArea: Área de revestimiento de mampostería en pies cuadrados
- ExterQual: Calidad del material exterior
- ExterCond: Condición actual del material exterior
- Foundation: Tipo de cimiento
- BsmtQual: Altura del sótano
- BsmtCond: Condición general del sótano
- BsmtExposure: Paredes del sótano al nivel del jardín o salida
- BsmtFinType1: Calidad del área terminada del sótano tipo 1
- BsmtFinSF1: Pies cuadrados terminados de tipo 1
- BsmtFinType2: Calidad del segundo área terminada (si está presente)
- BsmtFinSF2: Pies cuadrados terminados de tipo 2
- BsmtUnfSF: Pies cuadrados sin terminar del área del sótano
- TotalBsmtSF: Pies cuadrados totales del área del sótano
- Heating: Tipo de calefacción
- HeatingQC: Calidad y condición de calefacción
- CentralAir: Aire acondicionado central
- Electrical: Sistema eléctrico
- 1stFlrSF: Pies cuadrados del primer piso
- 2ndFlrSF: Pies cuadrados del segundo piso
- LowQualFinSF: Pies cuadrados terminados de baja calidad (todos los pisos)
- GrLivArea: Pies cuadrados de área habitable sobre el nivel del suelo
- BsmtFullBath: Baños completos en el sótano
- BsmtHalfBath: Medios baños en el sótano
- FullBath: Baños completos sobre el nivel del suelo
- HalfBath: Medios baños sobre el nivel del suelo
- Bedroom: Número de habitaciones sobre el nivel del sótano
- Kitchen: Número de cocinas
- KitchenQual: Calidad de la cocina
- TotRmsAbvGrd: Total de habitaciones sobre el nivel del suelo (no incluye baños)
- Functional: Calificación de funcionalidad del hogar
- Fireplaces: Número de chimeneas
- FireplaceQu: Calidad de la chimenea
- GarageType: Ubicación del garaje
- GarageYrBlt: Año en que se construyó el garaje
- GarageFinish: Acabado interior del garaje
- GarageCars: Tamaño del garaje en capacidad de autos
- GarageArea: Tamaño del garaje en pies cuadrados
- GarageQual: Calidad del garaje
- GarageCond: Condición del garaje
- PavedDrive: Entrada pavimentada
- WoodDeckSF: Área de la terraza de madera en pies cuadrados
- OpenPorchSF: Área del porche abierto en pies cuadrados
- EnclosedPorch: Área del porche cerrado en pies cuadrados
- 3SsnPorch: Área del porche de tres estaciones en pies cuadrados
- ScreenPorch: Área del porche con pantalla en pies cuadrados
- PoolArea: Área de la piscina en pies cuadrados
- PoolQC: Calidad de la piscina
- Fence: Calidad de la cerca
- MiscFeature: Característica miscelánea no cubierta en otras categorías
- MiscVal: Valor en dólares de la característica miscelánea
- MoSold: Mes de venta
- YrSold: Año de venta
- SaleType: Tipo de venta
- SaleCondition: Condición de venta

## Conclusiones

Basándonos en los resultados de validación:

* El modelo que mejor predice es el Gradient Boosting Regressor con:
    - El error cuadrático medio es: 700592596.7181544
    - El error absoluto medio es: 16483.64310252916
    - El r2 score es: 0.9086619554639415
    
* El modelo que peor predice es la RandomForest con:
    - El error cuadrático medio es: 833370133.8312945
    - El error absoluto medio es: 17661.579178082193
    - El r2 score es: 0.891351409142101


* El Error Absoluto Medio (MAE) es la diferencia entre las predicciones y los valores reales. Un MAE de 0 significa que no hay error, por lo que cuanto más cercano a 0 mejor es el modelo. Los modelos mantenian un MAE entre 16.000 - 18.000 aprox. Este dato debe ser interpretado con los valores de la variable objetivo:

    - El valor minimo de la variable SalePrice es: 34900
    - El valor maximo de la variable SalePrice es: 755000
    - El rango de la variable SalePrice es: 720100

Si analizamos el dataset de Test, nos damos cuenta que hay una diferencia entre los distintos modelos.
- Si miramos el gráfico de las predicciones, podemos ver los diferentes valores que cada modelo entrega.

Por el momento no se puede saber que tan bien estaban los valores de Test, ya que no se cuenta con la variable objetivo real.

El dataset fue creado por Kaggle para una competencia de Machine Learning, por lo que no se cuenta con la variable objetivo real.
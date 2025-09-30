# ENEI-2025-ML1 - Tarea 1

## Integrante
- Yudith Diana Chalco Cerezo

## Comparación de modelos
- **OLS**: Modelo base, sensible a multicolinealidad. R² más bajo (~0.38).  
- **Ridge**: Manejó bien multicolinealidad, mejoró el ajuste (R² hasta ~0.54).  
- **Lasso**: Similar a Ridge, pero con regularización L1 anuló más variables y empeoró en polinomiales.

## Efecto de la tasa de aprendizaje en Gradiente Descendente
- Con **learning rate pequeño**, la convergencia fue más lenta.  
- Con **learning rate mayor**, la función de costo bajó más rápido, pero si era demasiado grande podía volverse inestable.

## Validación cruzada (k-Fold)
- La validación cruzada permitió elegir los mejores valores de regularización (alpha) en Ridge y Lasso.  
- **Ridge** fue más estable con muchas variables correlacionadas.  
- **Lasso** es más útil cuando buscamos seleccionar pocas variables relevantes.


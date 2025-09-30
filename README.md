# ENEI-2025-ML1 - Tarea 1

## Integrante
- Yudith Diana Chalco Cerezo

---

## Comparación de modelos

- **OLS (Closed-form)**  
  Modelo base sin regularización. Fue sensible a la multicolinealidad y mostró el desempeño más bajo con un R² ≈ 0.38.

- **Ridge**  
  Manejó bien la multicolinealidad introducida por las variables correlacionadas y los polinomios. Mejoró el ajuste con R² ≈ 0.54, mostrando mayor robustez.

- **Lasso**  
  Tuvo un desempeño similar a Ridge (R² ≈ 0.54), pero al aplicar penalización L1 eliminó variables, lo que puede ser útil cuando buscamos selección de características. En espacios muy grandes fue más inestable.

---

## Efecto del learning rate en Gradient Descent

Se observó que:  
- Con un **learning rate demasiado alto**, la función de costo no converge (diverge rápidamente).  
- Con un **learning rate demasiado bajo**, la convergencia es muy lenta.  
- Un **valor intermedio** permitió un descenso más estable y eficiente de la función de costo.

---

## Influencia de k-Fold Cross Validation

El uso de validación cruzada con **k=5** fue clave para:  
- Seleccionar los mejores valores de regularización.  
  - Ridge: α = 100  
  - Lasso: α ≈ 0.22  
- Evitar el sobreajuste al no depender de una sola partición train/test.  
- Mejorar la capacidad de generalización de los modelos en el conjunto de prueba.

---

## Conclusión

- OLS funciona como punto de partida, pero es limitado frente a multicolinealidad.  
- Ridge resultó ser el más robusto en escenarios con muchas variables correlacionadas.  
- Lasso es más útil cuando se necesita **selección de variables**.  
- La validación cruzada permitió elegir correctamente la fuerza de regularización.  
- Ajustar bien el learning rate es fundamental para lograr una convergencia eficiente en gradient descent.


-> Eine der am weitesten verbreiteten **Kostenfunktionen**.

Mit dem **MSE** wird das **Quadrat der durchschnittlichen Fehler**, also der Durchschnittswert der Differenz der Werte und korrekten Werte, geschätzt. Dieser ist immer **positiv**. Je kleiner der Wert, desto besser.

# Vorgehensweise

1. Finde die Formel der Regressionslinie
   
$$
\hat{Y}_i = \beta_0 + \beta_1X_i + \hat{\epsilon}_i
$$

2. Füge die $X$-Werte in obige Formel ein. um das neue $\hat{Y}_i$ zu errechnen.
   
3. Subtrahiere nun den neuen Wert $\hat{Y}_i$ vom alten.

4. Setze zum Quadrat
   $$
	   (Y_i - \hat{Y}_i)²
$$

5. Summiere alle Quadrate $$
   \sum_{i=1}^{n}(Y_i - \hat{Y}_i)²
   $$
   6. Dividiere den Wert aus Schritt 5 durch die Gesamtanzahl der Observationen. Es ergibt sich diese Formel:

$$
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_{\text{true},i} - y_{\text{pred},i})^2
$$




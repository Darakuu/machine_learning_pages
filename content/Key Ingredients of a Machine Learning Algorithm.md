---
tags:
  - MachineLearning
---
# Algoritmo di Machine Learning: Componenti Base

- Modello e funzione parametrizzata che risolve un task $t$
- Funzione di costo $J$;
- Parametri del modello $v$;
- Framing Algorithms: cioè che 'aggiustano' i parametri;
- Dataset X:
	- X.Train: Training Sets;
	- X.Val: Validation Sets;
	- X.Test: Test Sets;
	- Importante che:
		- $X_{\text{TRAIN}}\bigcap X_{TEST}=\emptyset$
		- $X_{TRAIN}\bigcap X_{VAL}=\emptyset$
		- $X_{VAL}\bigcap X_{TEST}=\emptyset$
		- X è l'unione di tutti questi set.


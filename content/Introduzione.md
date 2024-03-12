---
tags:
  - MachineLearning
---
# Machine Learning

Il machine learning va oltre la normale concezione degli algoritmi classici, in quanto abbiamo a che fare con una categoria di problemi con due caratteristiche tanto particolari quanto fondamentali:

- Incertezza (Uncertainty);
- Variabilità

Quando si presentano problemi di questo tipo non abbiamo la possibilità di osservare tutti i possibili campioni di un evento.


> [!example] Distinguere una mail Spam / Non Spam



> [!def] Definizione Formale di Machine Learning (Tom Mitchell)
> "A computer is said to learn from Experience $E$ with regards to a task $t$ and a performance measure $P$ if its performance at task $t$, as measured by $P$, improves with experience $E$"

In generale, è il machine learning è il campo di studi che dà la capacità ai computer di imparare senza essere esplicitamente programmati a risolvere un determinato problema.

Dato un task, dobbiamo trovare un'approssimazione della funzione che risolve il problema (che è analiticamente difficile).

L'esperienza $E$ può essere tradotta in dati: $E \implies X$

E ci servono delle label con cui etichettare il problema: $Y$

Otteniamo così un set di item (o campione):

$\{ (x^{(i)}, y^{(i)}) \}^m_{i}$

Se voglio che il mio algoritmo impari da solo, dobbiamo migliorare $P$.

Per farlo, dobbiamo avere una funzione che valuta la bontà della performance tenuto conto dell'esperienza $E$.

Data la funzione $\hat{y}=ArgMax_{y}=H(Y|mail)$ (nel nostro esempio), vogliamo valutare appunto la bontà di H.

Valutiamo le coppie: $P(\{ y^{(i)} \}, \{ \hat{y}^{(i)} \})$, usando la Delta Function (dà 1 se $A=B$):

$\displaystyle\sum_{i}\delta(y^{(i)},\hat{y}^{(i)}) \implies \delta(A,B)=1 \text{ se } A=B$.

Sappiamo inoltre che H è una funzione parametrizzata: $H_{\alpha}$

![[Key Ingredients of a Machine Learning Algorithm#Algoritmo di Machine Learning Componenti Base]]

**Ci interessa che l'algoritmo dia buoni risultati su dati che non ha mai visto.**

Generalizziamo l'algoritmo con Iper-Parametri.

## IperParametri

$(1-\lambda)A+\lambda B\ ,\ \lambda \in[0,1]$

Usa due risposte da due modelli diversi, per generalizzare. Si deve usare il validation set per testare accuracy degli iperparametri.

## Input

L'input può avere una certa dimensionalità $n=d_{1},d_{2},\dots,d_{n}$

### Vettore

Input:
- $x \in \mathbb{R}^d$
	- $x=(x_{1},x_{2},\dots,x_{d})$ (feature vector)

Output, di dimensionalità k:
- $y \in \mathbb{R}^k$


### Matrici

Esempio: Immagine.

- $x \in \mathbb{R}^{d_{1}+d_{2}}$

### Tensori

"Matrici" tridimensionali:

- $x \in \mathbb{R}^{d_{1},d_{2},d_{3}}$

Ogni componente del dato è un valore numerico detto:

## Feature

$x_{j}^{(i)}$


Noi effettuiamo un processo di Feature Extraction, dal quale otteniamo delle label tramite la funzione di rappresentazione dei dati raw:

$x=\mathcal{L}(email)$

$\mathcal{L}$ di solito era progettata manualmente dall'uomo, ma negli ultimi anni grazie al Deep Learning, questa funzione viene appresa automaticamente.

### Tipi di Feature

- Categorical: es. colori (rosso, blu, giallo...)
- Continuous: insieme di numeri. Comprende anche gli interi.


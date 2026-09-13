# 📐 Equazioni Irrazionali — Formulario ed Eserciziario
> **Corso di Matematica — Terzo Anno Liceo Scientifico**  
> *Guida teorico-metodologica: equivalenze logiche, condizioni necessarie, condizioni superflue ed esercizi graduati.*

---

## 📌 Indice dei Contenuti
1. [Obiettivi Didattici](#-obiettivi-didattici)
2. [Quadro Teorico ed Equivalenze Logiche](#-quadro-teorico-ed-equivalenze-logiche)
3. [Focus Teorico: Il Falso Problema del Modulo e la Ridondanza delle C.E.](#-focus-teorico-il-falso-problema-del-modulo-e-la-ridondanza-delle-ce)
4. [La Regola del Trasporto nelle Differenze](#-la-regola-del-trasporto-nelle-differenze)
5. [Struttura del Repository](#-struttura-del-repository)
6. [Eserciziari Graduati](#-eserciziari-graduati)
   - [Livello 1: Indice dispari](#livello-1-indice-dispari)
   - [Livello 2: Forma base e confronto tra due radicali](#livello-2-forma-base-e-confronto-tra-due-radicali)
   - [Livello 3: Radicali multipli (somme e differenze)](#livello-3-radicali-multipli-somme-e-differenze)
   - [Livello 4: Metodo di sostituzione ed equazioni fratte](#livello-4-metodo-di-sostituzione-ed-equazioni-fratte)
7. [Istruzioni per la Compilazione LaTeX](#-istruzioni-per-la-compilazione-latex)

---

## 🎯 Obiettivi Didattici
Questo percorso è progettato per sviluppare il rigore logico-deduttivo degli studenti del terzo anno, superando l'approccio meccanico del "calcolo a macchinetta":
- Comprendere la differenza tra **implicazione algebrica** ($a = b \implies a^2 = b^2$) ed **equivalenza logica** ($\iff$).
- Distinguere rigorosamente le **condizioni necessarie** dalle **condizioni superflue/ridondanti**.
- Evitare errori concettuali sistematici (confusione tra $\sqrt{x^2}=\vert{}x\vert{}$ e $(\sqrt{x})^2=x$).
- Impostare strategie di calcolo efficienti prima di elevare a potenza (trasporto dei termini negativi, variabili ausiliarie).

---

## 🧠 Quadro Teorico ed Equivalenze Logiche

| Forma dell'Equazione | Modello Risolutivo Corretto | Condizioni Superflue da **NON** porre | Motivazione Logica |
| :--- | :--- | :--- | :--- |
| $\sqrt[2n+1]{A(x)} = B(x)$ | $A(x) = [B(x)]^{2n+1}$ | Nessuna C.E., nessun vincolo di segno | L'indice dispari conserva l'equivalenza in tutto $\mathbb{R}$. |
| $\sqrt{A(x)} = k \quad (k < 0)$ | $S = \emptyset$ (impossibile a vista) | Calcoli algebrici inutili | Una radice aritmetica reale è sempre non negativa. |
| $\sqrt{A(x)} = B(x)$ | $\begin{cases} B(x) \ge 0 \\ A(x) = [B(x)]^2 \end{cases}$ | **NON** porre $A(x) \ge 0$ | $A(x) = [B(x)]^2 \ge 0$ è garantito dall'equazione stessa. |
| $\sqrt{A(x)} = \sqrt{B(x)}$ | $\begin{cases} A(x) \ge 0 \quad (\text{oppure } B(x) \ge 0) \\ A(x) = B(x) \end{cases}$ | **NON** porre entrambi i radicandi $\ge 0$ | Se $A(x)=B(x)$, la positività di uno implica quella dell'altro. |
| $\sqrt{A(x)} + \sqrt{B(x)} = C(x)$ | $\begin{cases} A(x) \ge 0 \\ B(x) \ge 0 \\ C(x) \ge 0 \\ \dots \end{cases}$ | **Nessuna condizione è superflua** | Il doppio prodotto $2\sqrt{AB}$ richiede l'esistenza contemporanea di entrambi. |

---

## 🔍 Focus Teorico: Il Falso Problema del Modulo e la Ridondanza delle C.E.

Uno degli errori concettuali più comuni riguarda la presenza del modulo e della condizione di esistenza quando si risolve $\sqrt{A(x)} = B(x)$.

### Dimostrazione formale della riduzione minimale
Consideriamo l'impostazione "massimale" che include esplicitamente sia la condizione di esistenza sia l'eventuale valore assoluto derivante dall'elevamento:

$$\begin{cases} B(x) \ge 0 & \text{(concordanza del segno)} \\ A(x) \ge 0 & \text{(condizione di esistenza del radicale)} \\ \vert{}A(x)\vert{} = [B(x)]^2 & \text{(elevamento al quadrato con valore assoluto)} \end{cases}$$

1. **Risoluzione del modulo:**  
   Poiché la seconda riga impone $A(x) \ge 0$, per definizione di valore assoluto $\vert{}A(x)\vert{} \equiv A(x)$. Il sistema si riscrive immediatamente come:
   $$\begin{cases}    B(x) \ge 0 \\    A(x) \ge 0 \\    A(x) = [B(x)]^2    \end{cases}$$

2. **Assorbimento logico della C.E.:**  
   L'equazione $A(x) = [B(x)]^2$ vincola $A(x)$ a coincidere con un quadrato reale, il quale è **intrinsecamente non negativo** ($[B(x)]^2 \ge 0$).  
   Ne consegue che qualsiasi soluzione dell'equazione soddisfa automaticamente la disequazione $A(x) \ge 0$.  

La condizione $A(x) \ge 0$ è dunque **ridondante** e il modello minimale rigoroso è:
$$\sqrt{A(x)} = B(x) \iff \begin{cases} B(x) \ge 0 \\ A(x) = [B(x)]^2 \end{cases}$$

---

## ⚡ La Regola del Trasporto nelle Differenze

Quando compare una differenza tra radicali con termine noto:
$$\sqrt{A(x)} - \sqrt{B(x)} = k \qquad (k > 0)$$

> ⚠️ **Non elevare mai al quadrato con il segno meno al primo membro!**  
> Il segno della differenza $\sqrt{A} - \sqrt{B}$ non è noto a priori ed elevare produce un insidioso doppio prodotto col segno meno.

**Procedura corretta (Trasporto):**
1. Trasporta il radicale negativo al secondo membro:
   $$\sqrt{A(x)} = \sqrt{B(x)} + k$$
2. Entrambi i membri sono ora **garantiti non negativi** ($\sqrt{B} \ge 0$ e $k > 0$), eliminando la necessità di porre condizioni di concordanza sul primo elevamento.
3. Risolvi imponendo le C.E. simultanee iniziali ($A(x) \ge 0 \land B(x) \ge 0$) e isola il radicale superstite per il secondo elevamento.

---

## 📂 Struttura del Repository

```text
├── README.md                                  # Questo documento introduttivo
├── formulario-equazioni-irrazionali.tex       # Sorgente LaTeX del formulario sintetico (2 facciate)
├── eserciziario-irrazionali-base.tex         # Esercizi: indice dispari, radice isolata, due radici
└── eserciziario-irrazionali-avanzato.tex     # Esercizi: somme, differenze, fratte e sostituzione

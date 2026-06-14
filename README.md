# Quantum Fourier Transform (QFT)

Projet réalisé dans le cadre du Master 2 Ingénierie Mathématique.

## Auteur

Réalisé en groupe.

---

# Présentation

Ce projet explore plusieurs applications fondamentales de la Transformée de Fourier Quantique (QFT).

L'objectif est de comprendre comment la QFT intervient dans certains des algorithmes quantiques les plus importants :

- Analyse fréquentielle de signaux
- Recherche de période (principe utilisé dans l'algorithme de Shor)
- Estimation de phase quantique (Quantum Phase Estimation)

Les implémentations ont été réalisées avec **Python** et **myQLM**.

---

# Contenu du projet

## Exercice 1 : Analyse d'un signal classique avec la QFT

### Objectif

- Encoder un signal classique dans un registre quantique.
- Appliquer la Transformée de Fourier Quantique.
- Comparer les résultats obtenus avec la FFT classique (`numpy.fft`).

### Travaux réalisés

- Implémentation de la QFT (version séquentielle).
- Implémentation de la QFT récursive.
- Encodage d'amplitudes quantiques à l'aide de rotations `RY`.
- Généralisation de l'encodage à un signal de taille `2^n`.
- Comparaison entre QFT et FFT classique.

### Concepts abordés

- State Encoding
- Amplitude Encoding
- Quantum Fourier Transform
- Analyse fréquentielle

---

## Exercice 2 : Recherche de période

### Objectif

Utiliser la QFT pour retrouver la période d'une fonction périodique.

La fonction étudiée est de la forme :

\[
f(x)=a^x \mod N
\]

avec de petits paramètres afin de reproduire le principe utilisé dans l'algorithme de Shor.

### Travaux réalisés

- Construction d'une fonction périodique discrète.
- Détermination classique de la période.
- Construction d'un oracle quantique.
- Création d'une superposition uniforme.
- Application de la QFT.
- Extraction de la période à partir des résultats de mesure.

### Concepts abordés

- Oracle quantique
- Interférences quantiques
- Recherche de période
- Algorithme de Shor

---

## Exercice 3 : Quantum Phase Estimation (QPE)

### Objectif

Estimer la phase d'un opérateur unitaire :

\[
U|\psi\rangle=e^{2i\pi\phi}|\psi\rangle
\]

où \(|\psi\rangle\) est un vecteur propre de \(U\).

### Travaux réalisés

- Implémentation de la QFT inverse.
- Vérification numérique que QFT⁻¹(QFT(|ψ⟩)) = |ψ⟩.
- Construction du circuit QPE.
- Estimation de différentes phases.
- Analyse de la précision en fonction du nombre de qubits.

### Concepts abordés

- Quantum Phase Estimation
- QFT inverse
- Opérateurs unitaires
- États propres
- Mesure quantique

---

# Technologies utilisées

- Python
- NumPy
- Matplotlib
- myQLM
- Jupyter Notebook

---

# Structure du dépôt

```text
.
├── QFT2.ipynb
├── Projet_QFT_state_encoding.pdf
└── README.md
```

---

# Résultats

Le projet met en évidence :

- l'équivalence mathématique entre FFT classique et QFT ;
- l'utilisation de la QFT pour la détection de périodicité ;
- le rôle central de la QFT dans l'algorithme d'estimation de phase ;
- les fondements théoriques de l'algorithme de Shor.

---

# Références

- Nielsen & Chuang, Quantum Computation and Quantum Information.
- Documentation myQLM.
- Quantum Fourier Transform.
- Quantum Phase Estimation.
- Algorithme de Shor.

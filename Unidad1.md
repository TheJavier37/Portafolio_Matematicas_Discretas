➡️ [Regresar al Portafolio Principal](index.md)


# 📂 Unidad 1 – Contenidos y Tareas  

---

# 📘 Recapitulación: Lógica Proposicional

## 1. ¿Qué es la lógica proposicional?

La lógica proposicional (o lógica sentencial) estudia proposiciones —enunciados que son verdadero (V) o falso (F)— y las relaciones entre ellas mediante operadores (conectores) lógicos. Es la base formal para razonar sobre afirmaciones compuestas y para construir demostraciones.

---

## 2. ¿Qué es una proposición?

Una **proposición** es una oración declarativa que tiene un valor de verdad bien definido (V o F).

* Ejemplos: `p: "Hoy llueve"`, `q: "2+2=4"`.
* No son proposiciones: preguntas, órdenes, o expresiones con ambigüedad de verdad.

---

## 3. Conectores lógicos (símbolos y significado)

* **Negación**: `¬p` — "no p". Invierte el valor de verdad.
* **Conjunción**: `p ∧ q` — "p y q". Verdadero solo si ambos son V.
* **Disyunción inclusiva**: `p ∨ q` — "p o q (o ambos)". Verdadero si al menos uno es V.
* **Disyunción exclusiva (XOR)**: `p ⊕ q` — "p o q (pero no ambos)".
* **Implicación material**: `p → q` — "si p entonces q".
* **Bicondicional / equivalencia**: `p ↔ q` — "p si y solo si q" (mismos valores de verdad).

---

## 4. Jerarquía de los conectores (precedencia)

Orden típico de evaluación (de mayor a menor prioridad):

1. `¬` (negación)
2. `∧` (conjunción)
3. `∨`, `⊕` (disyunciones)
4. `→` (implicación)
5. `↔` (bicondicional)

Siempre que haya ambigüedad, usar paréntesis `()` para fijar el orden.

---

## 5. Tablas de verdad (principales)

### Negación

|  p |  ¬p |
| -: | :-: |
|  V |  F  |
|  F |  V  |

### Conjunción (`p ∧ q`)

|  p |  q | p ∧ q |
| -: | -: | :---: |
|  V |  V |   V   |
|  V |  F |   F   |
|  F |  V |   F   |
|  F |  F |   F   |

### Disyunción inclusiva (`p ∨ q`)

|  p |  q | p ∨ q |
| -: | -: | :---: |
|  V |  V |   V   |
|  V |  F |   V   |
|  F |  V |   V   |
|  F |  F |   F   |

### Disyunción exclusiva (`p ⊕ q`)

|  p |  q | p ⊕ q |
| -: | -: | :---: |
|  V |  V |   F   |
|  V |  F |   V   |
|  F |  V |   V   |
|  F |  F |   F   |

> Observación: `p ⊕ q` es equivalente a `(p ∨ q) ∧ ¬(p ∧ q)`.

### Implicación (`p → q`)

|  p |  q | p → q |
| -: | -: | :---: |
|  V |  V |   V   |
|  V |  F |   F   |
|  F |  V |   V   |
|  F |  F |   V   |

> Nota: `p → q` solo es falsa cuando `p` es V y `q` es F.

### Bicondicional (`p ↔ q`)

|  p |  q | p ↔ q |
| -: | -: | :---: |
|  V |  V |   V   |
|  V |  F |   F   |
|  F |  V |   F   |
|  F |  F |   V   |

---

## 6. Tautología, contradicción y contingencia

* **Tautología**: fórmula verdadera en todas las asignaciones de verdad (ej.: `p ∨ ¬p`).
* **Contradicción**: fórmula falsa en todas las asignaciones (ej.: `p ∧ ¬p`).
* **Contingencia**: fórmula que es verdadera en algunas asignaciones y falsa en otras (ej.: `p ∧ q`).

---

## 7. Leyes/identidades fundamentales de las proposiciones

(Esquema: `⇔` muestra equivalencia lógica)

* **Idempotencia**

  * `p ∨ p ⇔ p`
  * `p ∧ p ⇔ p`

* **Asociativa**

  * `(p ∨ q) ∨ r ⇔ p ∨ (q ∨ r)`
  * `(p ∧ q) ∧ r ⇔ p ∧ (q ∧ r)`

* **Conmutativa**

  * `p ∨ q ⇔ q ∨ p`
  * `p ∧ q ⇔ q ∧ p`

* **De Morgan**

  * `¬(p ∧ q) ⇔ ¬p ∨ ¬q`
  * `¬(p ∨ q) ⇔ ¬p ∧ ¬q`

* **Complemento / Negación**

  * `p ∨ ¬p ⇔ T` (ley del tercero excluido)
  * `p ∧ ¬p ⇔ F` (contradicción)

* **Distributiva**

  * `p ∧ (q ∨ r) ⇔ (p ∧ q) ∨ (p ∧ r)`
  * `p ∨ (q ∧ r) ⇔ (p ∨ q) ∧ (p ∨ r)`

* **Identidad**

  * `p ∨ F ⇔ p`
  * `p ∧ T ⇔ p`

* **Absorción**

  * `p ∨ (p ∧ q) ⇔ p`
  * `p ∧ (p ∨ q) ⇔ p`

* **Doble negación**

  * `¬(¬p) ⇔ p`

* **Equivalencias útiles**

  * `p → q ⇔ ¬p ∨ q`
  * `p ↔ q ⇔ (p → q) ∧ (q → p)`
  * `p ⊕ q ⇔ (p ∨ q) ∧ ¬(p ∧ q)`

---

## 8. Reglas de inferencia (formas válidas de razonamiento)

Para cada regla se muestra el **esquema** y un **ejemplo**.

* **Modus Ponens (MP)** — *modus ponendo ponens*

  * Esquema: `p → q, p  ⊢  q`.
  * Ejemplo: `Si llueve, la calle se moja. Está lloviendo. ⇒ La calle se moja.`

* **Modus Tollens (MT)** — *modus tollendo tollens*

  * Esquema: `p → q, ¬q  ⊢  ¬p`.
  * Ejemplo: `Si hay electricidad, la lámpara enciende. La lámpara no enciende. ⇒ No hay electricidad.`

* **Silogismo hipotético (SH)**

  * Esquema: `p → q, q → r  ⊢  p → r`.
  * Ejemplo: `Si estudio, apruebo; si apruebo, entro al curso. ⇒ Si estudio, entro al curso.`

* **Modus Tollendo Ponens (MTP)** — *disyunctive syllogism / modus tollendo ponens*

  * Esquema: `p ∨ q, ¬p  ⊢  q`.
  * Ejemplo: `O estudio o salgo; no estudio. ⇒ Salgo.`

* **Ley/Regla de absorción** *(también vista como equivalencia)*

  * Esquema: `p → (p ∨ q)` y `p → (p ∧ (p ∨ q))` (la forma usada en deducciones: de `p` inferir `p ∨ q`).
  * Uso habitual: simplificar expresiones durante transformaciones.

* **Dilema constructivo**

  * Esquema: `p → q, r → s, p ∨ r  ⊢  q ∨ s`.
  * Ejemplo: `Si estudio, apruebo; si trabajo, gano dinero; estudio o trabajo. ⇒ apruebo o gano dinero.`

* **Dilema destructivo**

  * Esquema: `p → q, r → s, ¬q ∨ ¬s  ⊢  ¬p ∨ ¬r`.

* **Simplificación (Simp)**

  * Esquema: `p ∧ q  ⊢  p`  (y simétricamente `⊢ q`).
  * Ejemplo: `Tengo tarea y tengo tiempo. ⇒ Tengo tarea.`

* **Conjunción (Conj)**

  * Esquema: `p, q  ⊢  p ∧ q`.
  * Ejemplo: `Tengo hambre. Tengo dinero. ⇒ Tengo hambre y tengo dinero.`

* **Adición (Add)**

  * Esquema: `p  ⊢  p ∨ q`.
  * Ejemplo: `Hace frío. ⇒ Hace frío o está nublado.`

* **Conmutación (Commutativity as inference/form rewriting)**

  * `p ∨ q ⇔ q ∨ p`, `p ∧ q ⇔ q ∧ p`. Útil para reordenar premisas.

---

---

## 9. Ejemplo corto (deducción)

Premisas:

1. `p → q`
2. `q → r`
3. `p`

Derivación:

* De (1) y (3) por **MP** obtenemos `q`.
* De (2) y `q` por **MP** obtenemos `r`.
* Conclusión: `r` (por **silogismo hipotético** y **MP**).

---

## 📦 Tareas Entregadas  

  [Ver carpeta anexa en Google Drive](https://drive.google.com/drive/folders/1plFObZEaFtJjhQ2voPTFkw8JbeFjyK45?usp=sharing)  

## Trabajos de Aprendizaje en Contacto con el Docente (ACD)
- ✅ [**APE 1: Resolución de Ejercicios**](https://drive.google.com/file/d/1D93A9cEgeQfb8lLbzO9sqaAnZbXsEB1y/view?usp=sharing)  
## Trabajos de Aprendizaje Practico Experimental (APE)  
- ✅ [**ACD 1: Proposiciones y Tablas de Verdad**](https://docs.google.com/presentation/d/10VQOUdrHfdM3vqs_OVxFbRKs7bCvAE6y/edit?usp=sharing&ouid=107467171818254633929&rtpof=true&sd=true)  
- ✅ [**ACD 2: Leyes de Proposiciones y Reglas de Inferencia**](https://docs.google.com/presentation/d/1tGq99rhMM4vlq9yb5BiJlqFFbqPcsTwl/edit?usp=sharing&ouid=107467171818254633929&rtpof=true&sd=true)     
## Trabajos de Aprendizaje Autonomo (AA)
- ✅ [**AA 1: Lectura y Ejercicios**](https://drive.google.com/file/d/1kuGYZvN85Z9gIRCfdrMqun00SHvuIw_d/view?usp=sharing)  
  


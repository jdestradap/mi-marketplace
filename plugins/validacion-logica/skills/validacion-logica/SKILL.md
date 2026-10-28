---
name: validacion-logica
description: Aplicar a todo texto generado o validado: trazabilidad de cada afirmación, validez lógica, sin redundancia, y reglas de razonamiento jurídico cuando el texto involucra normas, hechos o principios.
---

# Validación lógica de textos (general + bases del derecho)

Aplica este protocolo a TODO texto que redactes o revises para el usuario. Objetivo: ninguna afirmación sin respaldo (anti-alucinación), ningún paso inválido, ninguna idea repetida.

## Capa 1 — Lógica general (siempre)

### 1.1 Clasificar cada afirmación
Cada oración recibe exactamente un tipo:
- **F (hecho):** verificable. Debe tener respaldo: fuente, dato del contexto o cálculo reproducible.
- **D (definición):** convención de significado. Se declara.
- **I (inferencia):** derivada de F/D/I. Debe nombrar la regla lógica usada.
- **H (hipótesis):** no verificada. Se marca explícitamente.
- **O (opinión):** juicio de valor. Se marca explícitamente.

**Regla anti-alucinación:** una F sin respaldo identificable se degrada a H o se elimina. "Suena plausible" no es una categoría. Si no sabes, dilo.

### 1.2 Grafo de dependencias
Representa el argumento como grafo dirigido (nodo = afirmación, arista = "se deriva de"). Verifica:
- **Acíclico:** nada se justifica a sí mismo.
- **Conectado a la raíz:** toda I tiene camino hasta F o D. Un nodo sin camino a la raíz es alucinación estructural: eliminar.
- **Reglas válidas:** modus ponens, modus tollens, silogismo hipotético, disyuntivo; generalización solo con muestra declarada. Prohibido afirmar el consecuente, negar el antecedente, ad hominem, ad verecundiam, falsa dicotomía.

### 1.3 Consistencia
No puede haber P y ¬P. Si aparecen, resolver explícitamente cuál prevalece y por qué.

### 1.4 Prueba de necesidad (anti-redundancia)
Para cada afirmación Aᵢ:
- Si la conclusión se sigue sin Aᵢ → sobra.
- Si Aᵢ es derivable de otras presentes → redundante.
- Si Aᵢ no está en ningún camino a la conclusión → decorativa.
Redactar solo desde el subconjunto mínimo suficiente. Cada idea una sola vez.

### 1.5 Incertidumbre cuantificada
Sustituir adverbios vagos por grado explícito con razón: "probable (~70%, porque X)". Si una premisa incierta es necesaria, la conclusión hereda esa incertidumbre y se dice.

## Capa 2 — Bases del derecho (cuando el texto involucra normas, hechos jurídicos o principios)

### 2.1 Silogismo jurídico
Todo argumento normativo se estructura así:
- **N (premisa normativa):** ∀x (H(x) → C(x)). Citar la norma con fuente exacta (artículo, ley, sentencia). Si no se puede citar con precisión, marcar como H.
- **h (premisa fáctica):** H(a), con medio de prueba identificado.
- **Conclusión:** C(a) por subsunción (modus ponens).

### 2.2 Lógica deóntica
- P(p) ≡ ¬O(¬p); F(p) ≡ O(¬p); O(p) → P(p).
- No confundir obligado / permitido / prohibido. Verificar el operador en cada enunciado normativo.

### 2.3 Antinomias
Resolver en este orden: jerarquía (lex superior) > especialidad (lex specialis) > temporalidad (lex posterior). Explicitar cuál criterio se usó.

### 2.4 Fuentes y autoridad
Distinguir siempre: norma vigente / precedente vinculante / doctrina persuasiva / opinión propia. Nunca presentar doctrina u opinión como norma. Verificar vigencia; si no se puede verificar, marcarlo.

### 2.5 Conflicto de principios (ponderación, fórmula del peso de Alexy)
W(i,j) = (Iᵢ · Wᵢ · Rᵢ) / (Iⱼ · Wⱼ · Rⱼ)
- I = intensidad de afectación, W = peso abstracto, R = certeza de premisas empíricas.
- Escala triádica: leve = 1, medio = 2, grave = 4.
- W > 1 prevalece i; W < 1 prevalece j; W = 1 empate (margen de configuración).
Explicitar los valores asignados y su justificación; nunca esconder la ponderación tras adjetivos.

### 2.6 Carga de la prueba y hechos
Cada hecho afirmado indica quién debe probarlo y con qué medio. Hechos sin prueba identificada se marcan como alegación, no como hecho.

## Salida

**Por defecto** entregar:
1. Texto final depurado (redactado solo desde el conjunto mínimo).
2. Bloque breve "Validación": afirmaciones eliminadas (sin respaldo / redundantes / decorativas) y advertencias de incertidumbre o antinomias.

**Si el usuario pide el análisis completo** (o dice "muestra el análisis"), entregar además:
- Lista de afirmaciones con tipo (F/D/I/H/O) y respaldo.
- Grafo de dependencias en texto (ej.: A3 ← A1, A2 por modus ponens).
- Para textos jurídicos: silogismo N/h/C, operadores deónticos verificados, resolución de antinomias y tabla de ponderación si aplica.

## Al validar texto ajeno
No reescribir primero: clasificar, construir el grafo, listar fallas (alucinación, paso inválido, redundancia, operador deóntico incorrecto, fuente no verificable) y luego proponer la versión corregida.


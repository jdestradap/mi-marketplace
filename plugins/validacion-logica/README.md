# validacion-logica

Skill para Claude Code que aplica validación lógico-formal a todo texto generado o revisado:

- **Capa 1 (siempre):** clasificación de afirmaciones (hecho / definición / inferencia / hipótesis / opinión), grafo de dependencias acíclico y conectado a la raíz, consistencia, prueba de necesidad para eliminar redundancia, incertidumbre cuantificada.
- **Capa 2 (textos jurídicos):** silogismo normativo, lógica deóntica, resolución de antinomias, jerarquía de fuentes, fórmula del peso de Alexy, carga de la prueba.

## Instalación

```bash
claude plugin marketplace add jdestradap/mi-marketplace
claude plugin install validacion-logica@mi-marketplace
```

## Uso

Se activa automáticamente al redactar o revisar argumentos. Para ver el análisis completo (lista de afirmaciones, grafo, silogismo, ponderación), pide "muestra el análisis".

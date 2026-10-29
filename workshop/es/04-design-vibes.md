<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización con el diseño como punto de partida

---

En esta parte usarás los flujos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Este es un enfoque de desarrollo centrado en el diseño: empieza con una visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Introduce este prompt:

> Quiero transformar esta página en una experiencia completa de arcade retro. Planifica una renovación visual integral que incluya: efectos de líneas de barrido CRT en el fondo, un brillo de neón pulsante en el título, una insignia VS animada con cambios de color en el degradado, una capa de brillo y resplandor en las tarjetas de resultados, animaciones de entrada flotante para los campos de texto, texto de carga que cambie entre verde y morado, y efectos de resplandor al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) y usa verde (`#5fed83`) y morado (`#8a2be2`) como colores de acento. Utiliza el tema oscuro y la fuente retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación con todos los efectos visuales. **No lo aceptes de inmediato**: revísalo e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo, «Haz que el pulso de neón sea más lento, de unos 3 segundos»).
- Pregunta por efectos concretos (por ejemplo, «¿Cómo funcionará la capa de brillo de las tarjetas?»).
- Pide cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés conforme con el plan, pide a Copilot que lo implemente.

> Implementa el plan de tema de arcade retro que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a la hoja de estilos. Esto puede incluir:

- `@keyframes` para líneas de barrido, pulsos de neón, efectos de brillo y entradas flotantes.
- Pseudoelementos (`::before`, `::after`) para los efectos de superposición.
- Propiedades personalizadas de CSS para los colores del tema.
- Transiciones y estados al pasar el cursor sobre elementos interactivos.

<!-- track:cli:start -->
Cuando terminen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta los detalles visuales

> **⚠️ ¿No ves los cambios?** Si el nuevo tema o las animaciones no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y actualiza el navegador con **Ctrl+Shift+R**.

Mantén abierta la vista previa en el navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un sutil parpadeo eléctrico al texto del título.

> La insignia VS debería pulsar con más intensidad.

Esto es **desarrollo centrado en el diseño**: iteras sobre el resultado visual en tiempo real. Cada prompt mejora la experiencia hasta que te convenza. No te conformes con algo «suficientemente bueno»: perfecciona el diseño hasta que la página parezca de una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Las instrucciones deben reflejar las decisiones de diseño importantes para que los prompts posteriores mantengan el mismo rumbo.

<!-- track:vscode:start -->
Pide a Copilot Chat:
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:
<!-- track:cli:end -->

> Añade una sección de guía de diseño a `copilot-instructions.md` que describa nuestro tema de arcade retro: colores, fuentes y estilo de animación.

Haz commit de las instrucciones y los cambios de diseño cuando la página te convenza.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para esbozar un **sistema de diseño antes de implementarlo**.
- **Iterar sobre el resultado visual** con prompts de seguimiento.
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener la identidad visual.

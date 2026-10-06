# Ejercicio de Extensión Customer con Validación de Email

## Cómo empezar

Este repositorio contiene **el enunciado y una guía de estilo**, no una extensión instalable: no hay `app.json` ni objetos AL. El resultado del ejercicio es tu propia extensión Customer con validación de email, comparada antes y después de aplicar instrucciones.

Clona el repo y lee esta guía y [VibeCoding_AL_StyleGuide.md](VibeCoding_AL_StyleGuide.md). En otra carpeta, usa **AL: Go!** en VS Code con AL Language; configura tu sandbox en `launch.json`, descarga símbolos y elige versiones e IDs adecuados para ese entorno. GitHub Copilot se utiliza para la generación y comparación; conserva ambos resultados.

Compila y publica **el proyecto que crees**, no esta carpeta. Comprueba email válido/inválido y la acción de detección con clientes de prueba; entrega código y comparación. No hay una versión BC validada por este repositorio. Material histórico de aula, revisado estáticamente el 6 de octubre de 2026; no se ha ejecutado el ejercicio.


## 0. Dinámica del Ejercicio

1. **Primera parte:** Realiza todo el ejercicio sin instrucciones personalizadas, aplicando tus conocimientos y criterios propios.
2. **Segunda parte:** Repite el ejercicio, pero esta vez siguiendo las instrucciones personalizadas de nomenclatura, organización y buenas prácticas proporcionadas por el instructor.
3. Al finalizar, compara ambos resultados y reflexiona sobre las diferencias en calidad, claridad y mantenibilidad.

---


## 1. Objetivo y Metodología con VibeCoding y GitHub Copilot

El objetivo es extender la tabla y páginas de clientes en Business Central para añadir un campo de email con validación, gestión de emails inválidos y organización profesional del código.

### ¿Cómo realizar el ejercicio usando VibeCoding y GitHub Copilot?

1. **Trabaja en modo agente o Ask:** Utiliza GitHub Copilot en modo agente para pedirle que genere el código necesario para cada paso del ejercicio.
2. **Introduce los prompts adecuados:** Formula tus peticiones de forma clara y específica, por ejemplo: "Crea una extensión de tabla para Customer que añada un campo Email con validación de formato".
3. **Ajustes manuales:** Si algún cambio requiere intervención manual, realiza el ajuste en el código y añade un comentario indicando el motivo del cambio, por ejemplo: `// Ajuste manual: corregido el nombre del campo según estándar`.
4. **Solicita un archivo resumen:** Al finalizar, pide a Copilot que genere un archivo (por ejemplo, `ResumenCambios.md`) que contenga todos los cambios realizados, tanto automáticos como manuales, para documentar el proceso.
5. **Revisa y reflexiona:** Compara el resultado obtenido con y sin instrucciones personalizadas, y reflexiona sobre la experiencia y la calidad del código generado.

---

## 2. Estructura del Proyecto

Organiza los archivos en carpetas según el tipo de objeto AL:

- `/TableExtensions` → Extensiones de tablas
- `/PageExtensions` → Extensiones de páginas
- `/Codeunits` → Codeunits (lógica de negocio)

---

## 3. Extensión de la Tabla Customer

- Se crea una extensión de tabla que añade el campo `Email` a la tabla de clientes.
- El campo tiene longitud adecuada, validación de formato (expresión regular), clasificación de datos y caption descriptivo.

---

## 4. Extensión de Páginas

- Se crean extensiones para mostrar el campo `Email` en:
  - La lista de clientes (`Customer List`)
  - La ficha de clientes (`Customer Card`)

---

## 5. Lógica de Gestión de Emails Inválidos

- Se implementa una codeunit que:
  - Recorre todos los clientes y detecta emails inválidos.
  - Permite bloquear automáticamente clientes con email incorrecto.
  - Puede ser llamada desde una acción en la lista de clientes o como suscriptor de eventos.

---

## 6. Automatización y Acciones

- Se añade una acción en la lista de clientes para ejecutar la validación de emails desde la interfaz.
- Se implementa un EventSubscriber que bloquea automáticamente al cliente si su email es inválido al modificarlo.

---

## 7. Buenas Prácticas

- Usa prefijos únicos (ejemplo: `VBC_`) y sufijos según el tipo de objeto (`TableExt`, `PageExt`, `Codeunit`).
- Mantén los archivos organizados en carpetas por tipo.
- Elimina duplicados y mantén la solución limpia.

---

## 8. ¿Cómo probarlo?

1. Abre Business Central y accede a la lista de clientes.
2. Añade o edita un cliente, introduciendo un email inválido.
3. Observa que el sistema bloquea automáticamente al cliente y muestra un mensaje.
4. Usa la acción “Detectar Emails Inválidos” para revisar todos los clientes de forma masiva.

---

## 9. Recomendaciones

- Mantén siempre la estructura y nomenclatura para facilitar el mantenimiento y la colaboración.
- Documenta cada objeto y procedimiento relevante.

---

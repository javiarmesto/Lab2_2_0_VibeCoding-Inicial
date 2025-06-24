# Guía de Estilo AL para VibeCoding

## 1. Nomenclatura de Objetos
- Usa siempre el prefijo `VBC_` para todos los objetos personalizados.
- Utiliza sufijos descriptivos según el tipo de objeto: `TableExt`, `PageExt`, `Codeunit`, etc.
- Ejemplo: `VBC_CustomerEmail.TableExt.al`, `VBC_CustomerListEmail.PageExt.al`, `VBC_CustomerEmailMaintenance.Codeunit.al`

## 2. Organización de Carpetas
- Organiza los archivos en carpetas por tipo de objeto:
  - `/TableExtensions`
  - `/PageExtensions`
  - `/Codeunits`
  - `/Enums`, `/Reports`, etc. según necesidad

## 3. IDs y Rangos
- Usa un rango de IDs reservado para tu solución o partner.
- No reutilices IDs ni nombres de objetos.

## 4. Estructura y Comentarios
- Incluye comentarios claros en procedimientos y bloques de código relevantes.
- Documenta la finalidad de cada objeto y sus métodos principales.

## 5. Buenas Prácticas de Desarrollo
- Valida siempre los datos críticos (ejemplo: emails, identificadores).
- Usa `DataClassification` y `Caption` en todos los campos nuevos.
- Evita duplicidad de objetos y mantén la solución limpia.
- Implementa lógica reutilizable en codeunits.
- Usa suscriptores de eventos para lógica automática y desacoplada.

## 6. Estilo de Código
- Indenta con 4 espacios.
- Usa nombres descriptivos en variables y procedimientos.
- Mantén los nombres y comentarios en español salvo que el proyecto requiera inglés.

## 7. Ejemplo de Estructura de Proyecto
```
/TableExtensions
    VBC_CustomerEmail.TableExt.al
/PageExtensions
    VBC_CustomerEmail.PageExt.al
/Codeunits
    VBC_CustomerEmailMaintenance.Codeunit.al
```

## 8. Revisión y Control de Calidad
- Revisa y elimina archivos y objetos no utilizados.
- Realiza pruebas funcionales tras cada cambio relevante.
- Mantén actualizado el README y la documentación interna.

---

**Esta guía debe ser revisada y adaptada periódicamente según las necesidades del equipo y las mejores prácticas de la comunidad AL.**

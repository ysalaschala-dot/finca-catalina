# OCI-001: Recepción de residuos orgánicos

## 1. Identificación y estado
- **Código:** OCI-001
- **Nombre:** Recepción de residuos orgánicos
- **Proyecto:** Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina
- **Tipo:** Requisito funcional / elemento de configuración
- **Versión:** 1.1
- **Estado:** Especificación propuesta; implementación y pruebas pendientes

## 2. Propósito
Definir los datos, validaciones y flujo mínimos para registrar y consultar la recepción de residuos orgánicos agroindustriales con trazabilidad.

## 3. Alcance
El proceso permitirá registrar una recepción, identificar su procedencia, clasificar el residuo, registrar cantidad y responsable, consultar el historial y conocer su estado.

## 4. Datos y validaciones
| Campo | Origen | Validación |
|---|---|---|
| Código de recepción | Generado por el sistema al guardar (por ejemplo, REC-AAAAMMDD-0001) | Único; no lo escribe el usuario |
| Fecha y hora | Usuario/sistema | Obligatoria; fecha y hora válidas en formato ISO 8601 o formato local validado y normalizado |
| Procedencia | Catálogo de fincas, rutas o puntos de origen | Obligatoria; debe corresponder a un registro permitido |
| Tipo de residuo | Catálogo configurable aprobado por el responsable | Obligatorio; seleccionar un valor existente |
| Cantidad | Usuario | Obligatoria; numérica y mayor que cero |
| Unidad de medida | Catálogo controlado (por ejemplo, kg o t) | Obligatoria; unidad compatible con el registro |
| Responsable | Sesión autenticada | Obligatorio; se toma del usuario autenticado siempre que sea posible |
| Observaciones | Usuario | Opcional; longitud limitada y texto seguro |
| Estado | Sistema | Inicial: Recibida; valores posteriores: En revisión, Aceptada o Rechazada |

Los catálogos de procedencia, tipos de residuo y unidades deben mantenerse de forma centralizada para evitar valores incompatibles. La lista de estados es controlada por el sistema, no texto libre.

## 5. Flujo propuesto
1. El responsable autenticado abre el formulario de recepción.
2. Ingresa fecha/hora, procedencia, tipo de residuo, cantidad y unidad; añade observaciones si hace falta.
3. El sistema valida los campos obligatorios, la fecha, la cantidad positiva y los valores seleccionados de catálogos.
4. Si hay errores, no guarda el registro y muestra mensajes claros junto a los campos correspondientes.
5. Si todo es válido, guarda el registro y genera el código único.
6. El sistema registra el estado inicial Recibida y confirma el resultado.
7. El personal autorizado puede consultar la recepción y cambiar el estado siguiendo las transiciones permitidas.

## 6. Transiciones de estado
- Recibida → En revisión
- En revisión → Aceptada o Rechazada
- Aceptada y Rechazada son estados finales para esta recepción; cualquier reapertura requiere un cambio autorizado y auditado.

Cada cambio de estado debe registrar fecha/hora, usuario responsable y motivo cuando corresponda. No se permite cambiar estados mediante texto libre.

## 7. Criterios de aceptación
- No se guarda una recepción si falta un dato obligatorio.
- La fecha/hora se valida y se almacena en un formato normalizado.
- La cantidad debe ser numérica y mayor que cero.
- El código lo genera el sistema y no se repite.
- Tipo de residuo, procedencia y unidad deben pertenecer a catálogos válidos.
- Se rechazan transiciones de estado no permitidas.
- El registro guardado puede consultarse posteriormente por código.
- Se conserva una trazabilidad básica de quién creó y actualizó el registro.
- Los mensajes de error indican cómo corregir los datos sin exponer información técnica sensible.

## 8. Trazabilidad y control de cambios
Este documento se mantiene en la rama feature/oci-001-recepcion. Los cambios deben tener commits descriptivos, revisión mediante Pull Request hacia develop y comprobaciones antes de integrar en main.

## 9. Verificación pendiente
Esta especificación no demuestra que exista una implementación funcional. Los criterios deben verificarse cuando el sistema esté implementado. Registrar los resultados de las pruebas reales en el informe de pruebas; no marcar pruebas como ejecutadas sin evidencia.

# OCI-001: Recepción de residuos orgánicos

## 1. Identificación del elemento de configuración
- **Código:** OCI-001
- **Nombre:** Recepción de residuos orgánicos
- **Proyecto:** Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina
- **Tipo:** Requisito/documento funcional del sistema
- **Versión inicial:** 1.0
- **Estado:** Propuesta académica

## 2. Propósito
Definir la información mínima necesaria para registrar la recepción de residuos orgánicos agroindustriales y facilitar su seguimiento dentro del sistema propuesto.

## 3. Alcance funcional
El proceso de recepción debe permitir:
1. Registrar una nueva recepción.
2. Identificar la fecha de recepción y la procedencia del residuo.
3. Describir el tipo de residuo recibido y su cantidad con unidad de medida.
4. Registrar a la persona responsable de la recepción.
5. Consultar el registro y su estado de seguimiento.

## 4. Datos propuestos
| Campo | Descripción | Validación propuesta |
|---|---|---|
| Código de recepción | Identificador único del registro | Obligatorio y no repetido |
| Fecha y hora | Momento de la recepción | Obligatorio y con formato válido |
| Procedencia | Lugar o proceso de origen | Obligatorio |
| Tipo de residuo | Clasificación del residuo recibido | Obligatorio |
| Cantidad | Cantidad recibida | Número mayor que cero |
| Unidad de medida | Unidad usada para expresar la cantidad | Obligatorio |
| Responsable | Persona que registra la recepción | Obligatorio |
| Observaciones | Información adicional | Opcional |
| Estado | Situación del registro | Valor controlado por el sistema |

## 5. Flujo propuesto
1. El responsable abre el formulario de recepción.
2. Ingresa los datos requeridos.
3. El sistema valida los campos obligatorios y la cantidad.
4. Si los datos son válidos, registra la recepción y asigna un identificador único.
5. El sistema confirma el registro y permite consultarlo posteriormente.
6. Si hay errores, informa qué datos deben corregirse sin guardar un registro inválido.

## 6. Criterios de aceptación
- No se guarda una recepción si faltan campos obligatorios.
- La cantidad debe ser numérica y mayor que cero.
- Cada recepción tiene un identificador único.
- Los datos registrados pueden consultarse posteriormente.
- El sistema muestra un mensaje comprensible cuando el registro se guarda o cuando hay errores de validación.

## 7. Trazabilidad y control de cambios
Este documento se desarrolla en la rama `feature/oci-001-recepcion`. Cada cambio debe registrarse mediante un commit descriptivo y revisarse antes de integrarse en `develop`. La incorporación a `main` debe realizarse después de la revisión y de las comprobaciones acordadas.

## 8. Verificación pendiente
Los criterios descritos son requisitos propuestos. Deben validarse mediante pruebas cuando exista una implementación funcional; este documento no afirma que las pruebas ya se hayan ejecutado.

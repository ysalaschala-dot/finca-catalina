# Auditoría de gestión de configuración

## Proyecto
Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina.

## Objetivo y alcance
Revisar documentalmente la organización del repositorio, las ramas, la trazabilidad de la OCI-001 y la existencia de artefactos de configuración. Esta lista no sustituye la revisión de código ni las pruebas ejecutadas.

## Ramas
- `main`: versión principal del repositorio.
- `develop`: integración prevista para cambios revisados.
- `feature/oci-001-recepcion`: especificación de la orden de cambio OCI-001.

## OCI-001
**Nombre:** Recepción de residuos orgánicos.  
**Alcance:** definir campos, validaciones, estados, criterios de aceptación y trazabilidad para la recepción.  
**Pull Request:** [PR #1 hacia develop](https://github.com/ysalaschala-dot/finca-catalina/pull/1).  
**Estado:** fusionado en `develop` después de corregir los hallazgos sobre código, fecha, estados y catálogos. Las pruebas funcionales siguen pendientes.

## Lista de verificación documental
- [x] Repositorio público creado.
- [x] README con descripción, estructura y enlaces a los artefactos.
- [x] Ramas `main`, `develop` y `feature/oci-001-recepcion` existentes.
- [x] Carpeta `docs/` organizada con documentos de arquitectura, riesgos y auditoría.
- [x] Especificación OCI-001 registrada en la rama de funcionalidad.
- [x] Pull Request #1 creado hacia `develop`.
- [x] Comentarios de revisión identificados para corrección.
- [x] Catálogo ECS, diagramas UML, prototipo UI/UX, Product Backlog/Sprints y plan de pruebas documentados.
- [x] PR #1 fusionado en `develop` después de corregir la especificación OCI-001.
- [ ] Ejecutar las pruebas del sistema y guardar evidencia verificable.
- [ ] Confirmar que los diagramas corresponden a la solución implementada.
- [ ] Confirmar que el informe PDF final coincide con los artefactos del repositorio.
- [ ] Realizar la revisión final de integridad antes de promover una versión a `main`.

## Hallazgos y acciones
| Hallazgo | Acción | Estado |
|---|---|---|
| La OCI-001 necesitaba precisar el código generado, estados, fecha y catálogos | Se actualizó la especificación v1.1 y se integró por PR | Corregido; pruebas funcionales pendientes |
| El PR requiere revisión de los cambios | Resolver los comentarios y obtener aprobación antes de integrar | Pendiente |
| No hay evidencia registrada de ejecución de pruebas | Ejecutar los casos de prueba y guardar capturas/logs reales | Pendiente |
| El prototipo es demostrativo y no usa base de datos | Indicarlo en README e interfaz | Documentado |

## Resultado de la auditoría
La revisión actual confirma la existencia de los principales artefactos documentales. No confirma que la aplicación esté implementada ni que las pruebas funcionales hayan sido ejecutadas. La auditoría final debe completarse cuando existan evidencias de revisión, integración y pruebas.

## Evidencias
- Repositorio: https://github.com/ysalaschala-dot/finca-catalina
- Pull Request OCI-001: https://github.com/ysalaschala-dot/finca-catalina/pull/1

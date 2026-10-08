# Catálogo de Elementos de Configuración de Software (ECS)

**Proyecto:** Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina  
**Versión:** 1.0  
**Estado:** Inventario documental inicial

| ID | Elemento | Tipo | Ubicación | Estado | Regla de control |
|---|---|---|---|---|---|
| ECS-001 | Informe técnico final | Documento | Archivo PDF/DOCX de entrega | Por validar | Revisar contenido, enlaces y exportación |
| ECS-002 | README | Documentación | README.md | Versionado en Git | Actualizar al cambiar estructura o alcance |
| ECS-003 | Arquitectura lógica | Diseño | docs/arquitectura.md | Propuesta | Contrastar con la solución implementada |
| ECS-004 | Diagramas UML | Diseño | docs/diagramas-uml.md | Propuesta | Revisar junto con los cambios del modelo |
| ECS-005 | Prototipo UI/UX | Interfaz | docs/prototipo-ui-ux.html | Demostrativo | Validar flujo antes de implementar |
| ECS-006 | Product Backlog y Sprints | Planificación | docs/product-backlog-sprints.md | Plan propuesto | Ajustar con el equipo y datos reales |
| ECS-007 | OCI-001 Recepción | Requisito funcional | docs/oci-001-recepcion.md | En revisión por PR | Revisión antes de integrar |
| ECS-008 | Auditoría de configuración | Auditoría | docs/auditoria-configuracion.md | Lista documental | No marcar controles sin evidencia |
| ECS-009 | Riesgos y métricas | Calidad | docs/riesgos-metricas.md | Plan propuesto | Revisar en cada iteración |
| ECS-010 | Plan de pruebas | Verificación | docs/pruebas-y-metricas.md | Ejecución pendiente | Guardar resultados y evidencia real |
| ECS-011 | Repositorio Git | Configuración | https://github.com/ysalaschala-dot/finca-catalina | Activo | Registrar cambios mediante commits y PR |

## Reglas de gestión
1. Cada cambio debe identificar los documentos, diagramas o módulos afectados.
2. Los commits deben describir el cambio realizado.
3. Los cambios funcionales se proponen mediante Pull Request hacia `develop`.
4. Antes de promover una versión a `main`, se revisan documentos, diagramas, pruebas y trazabilidad.
5. Un elemento marcado como “propuesto” no implica que ya esté implementado.

## Historial
| Versión | Cambio |
|---|---|
| 1.0 | Inventario inicial de elementos de configuración |

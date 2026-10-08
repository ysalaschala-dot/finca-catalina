# Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina

## 1. Descripción del proyecto
Proyecto académico de Ingeniería de Software 2 que propone organizar y mejorar el seguimiento de la gestión de residuos orgánicos agroindustriales en la Finca Catalina, contextualizada en la región de Urabá.

## 2. Objetivo general
Proponer un sistema que permita registrar, organizar y consultar información relacionada con la recepción y el seguimiento de residuos orgánicos agroindustriales, desde la recepción hasta su trazabilidad y despacho.

## 3. Documentación del proyecto
Los artefactos se encuentran en la carpeta `docs/`:

- [Arquitectura del sistema](docs/arquitectura.md): capas, componentes y patrones State y Observer.
- [Diagramas UML](docs/diagramas-uml.md): diagramas conceptuales de componentes y clases.
- [Prototipo interactivo UI/UX](docs/prototipo-ui-ux.html): abrir el archivo en un navegador; datos solo de demostración.
- [Product Backlog y Sprints Scrum](docs/product-backlog-sprints.md): historias priorizadas, planificación y definición de terminado.
- [Catálogo de elementos de configuración ECS](docs/catalogo-ecs.md): inventario de artefactos y reglas de control.
- [OCI-001: recepción de residuos](docs/oci-001-recepcion.md): especificación funcional, validaciones y estados.
- [Auditoría de gestión de configuración](docs/auditoria-configuracion.md): ramas, control de cambios y lista de verificación.
- [Riesgos y métricas de calidad](docs/riesgos-metricas.md): matriz inicial, referencia ISO/IEC 25010 y GQM.
- [Plan de pruebas y registro de métricas](docs/pruebas-y-metricas.md): casos propuestos y espacio para resultados reales.
- [Informe del proyecto en PDF](Informe_Sistema_Gestion_Residuos%20yola%20%289%29.pdf): documento que ya estaba en el repositorio.

## 4. Control de versiones
Repositorio público: https://github.com/ysalaschala-dot/finca-catalina

- `main`: versión principal.
- `develop`: integración de cambios revisados.
- `feature/oci-001-recepcion`: trabajo de la especificación OCI-001.
- [Pull Request #1 hacia develop](https://github.com/ysalaschala-dot/finca-catalina/pull/1): integrado en `develop` después de corregir la especificación OCI-001. Las pruebas funcionales siguen pendientes.

### Flujo de trabajo sugerido
1. Crear la rama de funcionalidad desde `develop`.
2. Registrar cambios con commits descriptivos.
3. Abrir un Pull Request y revisar el cambio y sus pruebas.
4. Integrar en `develop` después de resolver observaciones.
5. Promover a `main` después de la verificación de la versión.

## 5. Alcance y calidad
Los diagramas, el prototipo y el backlog son artefactos de diseño/propuesta. El prototipo no se conecta a una base de datos y no debe considerarse un sistema productivo. Los casos de prueba están definidos, pero deben ejecutarse y acompañarse de evidencias antes de informar resultados. No se presentan porcentajes sin mediciones verificables.

## 6. Autora
Yolaniz Salas Chala

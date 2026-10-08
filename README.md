# Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina

## 1. Descripción del proyecto
Proyecto académico de Ingeniería de Software 2 que propone organizar y mejorar el seguimiento de la gestión de residuos orgánicos agroindustriales en la Finca Catalina.

## 2. Objetivo general
Proponer un sistema que permita registrar, organizar y consultar información relacionada con la recepción y el seguimiento de residuos orgánicos agroindustriales.

## 3. Documentación del proyecto
Los documentos se encuentran organizados en la carpeta `docs/`:

- [Arquitectura del sistema](docs/arquitectura.md): componentes principales y patrones de diseño State y Observer.
- [Auditoría de gestión de configuración](docs/auditoria-configuracion.md): estructura del repositorio, ramas, elemento OCI-001 y lista de verificación.
- [Gestión de riesgos y métricas de calidad](docs/riesgos-metricas.md): matriz de riesgos, referencia ISO/IEC 25010 y métricas propuestas con GQM.
- [Informe del proyecto en PDF](Informe_Sistema_Gestion_Residuos%20yola%20%289%29.pdf): documento de informe entregado junto con el repositorio.

## 4. Control de versiones
El repositorio utiliza Git y GitHub para registrar los cambios.

- `main`: versión principal y estable.
- `develop`: integración de cambios antes de incorporarlos a la versión principal.
- `feature/oci-001-recepcion`: trabajo relacionado con el elemento de configuración OCI-001, recepción de residuos orgánicos. [Pull Request #1 hacia develop](https://github.com/ysalaschala-dot/finca-catalina/pull/1) pendiente de revisión.

### Flujo de trabajo sugerido
1. Desarrollar los cambios en la rama de funcionalidad correspondiente.
2. Registrar cambios con commits descriptivos.
3. Integrar la funcionalidad en `develop` después de revisarla.
4. Revisar y probar la integración antes de llevarla a `main`.

## 5. Alcance y calidad
La arquitectura y las métricas documentadas son propuestas académicas. Los resultados de calidad deben calcularse con evidencias y pruebas reales; no se presentan porcentajes sin datos verificables.

## 6. Autora
Yolaniz Salas Chala

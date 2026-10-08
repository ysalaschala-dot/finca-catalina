# Diagramas UML — Finca Catalina

Estos modelos son conceptuales. Deben contrastarse con el alcance aprobado y con la implementación real antes de considerarlos definitivos.

## 1. Diagrama de componentes

```mermaid
flowchart TB
    UI[Interfaz web]
    AUTH[Autenticación y autorización]
    APP[Servicios de aplicación]
    DOMAIN[Dominio: recepción, rutas y lotes]
    TRACE[Trazabilidad]
    REPORT[Reportes e indicadores]
    REPO[Repositorios de datos]
    DB[(Base de datos)]

    UI --> AUTH
    UI --> APP
    APP --> DOMAIN
    APP --> TRACE
    APP --> REPORT
    DOMAIN --> REPO
    TRACE --> REPO
    REPORT --> REPO
    REPO --> DB
```

**Descripción:** la interfaz solicita operaciones a los servicios de aplicación; el dominio contiene las reglas del negocio; los repositorios separan la lógica de negocio del acceso a datos. La autorización debe comprobarse en el servidor.

## 2. Diagrama de clases conceptual

```mermaid
classDiagram
    class Usuario {
      +id: UUID
      +nombre: String
      +correo: String
      +rol: String
      +estado: String
      +autenticar()
      +tienePermiso()
    }
    class Finca {
      +id: UUID
      +nombre: String
      +ubicacion: String
    }
    class Ruta {
      +id: UUID
      +origen: String
      +destino: String
      +fechaProgramada: DateTime
      +estado: String
      +actualizarEstado()
    }
    class Recepcion {
      +codigo: String
      +fechaHora: DateTime
      +procedencia: String
      +tipoResiduo: String
      +cantidad: Decimal
      +unidad: String
      +estado: String
      +validar()
      +cambiarEstado()
    }
    class Lote {
      +id: UUID
      +codigo: String
      +fechaRegistro: DateTime
      +peso: Decimal
      +estado: String
    }
    class RegistroProceso {
      +id: UUID
      +fechaHora: DateTime
      +etapa: String
      +observaciones: String
    }
    class Despacho {
      +id: UUID
      +fecha: DateTime
      +cantidad: Decimal
      +destino: String
    }
    class Reporte {
      +id: UUID
      +tipo: String
      +periodoInicio: Date
      +periodoFin: Date
      +generar()
    }

    Finca "1" --> "0..*" Lote : origina
    Ruta "0..*" --> "0..*" Finca : atiende
    Recepcion "1" --> "0..1" Lote : puede crear
    Lote "1" --> "0..*" RegistroProceso : historial
    Lote "1" --> "0..*" Despacho : se despacha
    Reporte ..> Lote : consulta
    Reporte ..> Ruta : consulta
    Usuario ..> Recepcion : registra
```

## 3. Patrones de diseño propuestos

- **State:** el estado de una recepción o lote cambia mediante transiciones válidas definidas por el dominio. Para recepción: Recibida → En revisión → Aceptada o Rechazada.
- **Observer:** cuando cambia el estado de un lote, componentes como trazabilidad, tablero o notificaciones podrían recibir un evento y actualizarse sin acoplarse directamente a la entidad.

## 4. Decisiones de diseño
- Los identificadores se generan de forma única.
- Las cantidades usan un tipo decimal y una unidad explícita.
- Las fechas se validan y normalizan.
- Los permisos se verifican en el servidor.
- Los diagramas describen una propuesta y no prueban que los módulos ya estén implementados.

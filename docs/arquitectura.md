# Arquitectura del sistema – Finca Catalina

## 1. Objetivo
Definir una arquitectura conceptual para registrar y consultar la gestión de residuos orgánicos agroindustriales, incluyendo recepción, lotes, procesos, rutas, trazabilidad y reportes.

## 2. Estilo arquitectónico seleccionado: arquitectura en capas
Se propone una arquitectura en capas para separar responsabilidades, facilitar mantenimiento y reducir el acoplamiento entre interfaz, reglas de negocio y persistencia.

| Capa | Responsabilidad | Ejemplos de componentes |
|---|---|---|
| Presentación | Mostrar pantallas, formularios, navegación y mensajes accesibles | Inicio de sesión, recepción, listado, trazabilidad, reportes |
| Aplicación | Coordinar casos de uso, permisos y transacciones | Registrar recepción, consultar lote, cambiar estado, generar reporte |
| Dominio | Mantener entidades y reglas de negocio | Recepción, Lote, Ruta, RegistroProceso, Despacho |
| Datos | Persistir, consultar y respaldar información | Repositorios, base de datos, servicios de respaldo |

## 3. Justificación por atributos de calidad
- **Mantenibilidad:** cada capa tiene una responsabilidad clara y puede cambiarse con menor impacto.
- **Seguridad:** la autorización se verifica en la capa de aplicación/servidor; ocultar botones no es una medida suficiente.
- **Integridad:** validaciones de campos, unidades, fechas, identificadores y transiciones se ejecutan antes de persistir datos.
- **Usabilidad:** formularios con etiquetas, mensajes de error comprensibles, contraste y navegación por teclado.
- **Disponibilidad en campo:** debido a la conectividad variable de la región de Urabá, el diseño debe considerar mensajes ante fallos de conexión y una estrategia de sincronización si se requiere modo desconectado. El prototipo actual no implementa sincronización offline.
- **Escalabilidad:** los módulos pueden ampliarse sin concentrar toda la lógica en la interfaz.

## 4. Componentes principales
- **Autenticación y autorización:** identifica al usuario y aplica permisos según rol.
- **Recepción:** registra fecha, procedencia, tipo de residuo, cantidad, unidad, responsable y estado.
- **Gestión de lotes y procesos:** asocia recepciones a lotes y registra las etapas de procesamiento.
- **Rutas y puntos de acopio:** organiza el origen, destino y fecha programada.
- **Trazabilidad:** conserva eventos relacionados con cada lote en orden temporal.
- **Reportes e indicadores:** resume información filtrada por periodo, procedencia, tipo o estado.
- **Persistencia y respaldo:** guarda datos y permite recuperación controlada.

## 5. Patrones de diseño propuestos

### State
Permite controlar el ciclo de vida de una recepción o lote. Ejemplo para recepción: Recibida → En revisión → Aceptada o Rechazada. Las transiciones inválidas deben rechazarse y quedar registradas.

### Observer
Permite que, al cambiar el estado de un lote, componentes suscritos —como trazabilidad, tablero o notificaciones— reciban un evento y actualicen su información sin que la entidad dependa directamente de cada componente.

## 6. Diagramas y trazabilidad
Los diagramas conceptuales de componentes y clases se encuentran en [diagramas-uml.md](diagramas-uml.md). La especificación de recepción se encuentra en [oci-001-recepcion.md](oci-001-recepcion.md).

## 7. Limitaciones
Este documento y el prototipo son artefactos de diseño. No demuestran que exista una aplicación productiva conectada a base de datos. Antes de liberar una implementación, se deben verificar los requisitos, probar los permisos, validar la persistencia y conservar evidencia de pruebas.

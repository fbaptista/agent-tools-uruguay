# Propuesta: herramienta MCP para cotización histórica de monedas (BCU)

**Tipo de issue**: enhancement

## ¿Qué problema resuelve?

Permitir que agentes de IA consulten de forma sencilla los valores históricos de compra y venta de divisas en Uruguay. Actualmente la información está disponible vía los servicios SOAP del Banco Central del Uruguay (BCU), pero requiere conocimiento específico para consumirla.

## ¿Qué datos usaría?

Se consumirían los datos de cotización histórica provistos por el BCU a través de su API SOAP pública. Esta fuente incluye valores diarios de compra y venta para el dólar, euro y otras monedas relevantes.

## ¿Qué beneficio aporta a los agentes de IA?

- Facilita tareas de análisis financiero y contextualización histórica.
- Permite tomar decisiones informadas en flujos que requieran conocer el valor del dólar u otras monedas en fechas pasadas.
- Centraliza y simplifica el acceso a una fuente oficial y confiable.

## ¿Hay alguna fuente confiable disponible?

Sí, el **Banco Central del Uruguay** ofrece un servicio SOAP oficial para consultar "Tipo de Cambio" y otras series financieras. Ejemplo de referencia: <https://www.bcu.gub.uy/Estadisticas-e-Indicadores/Paginas/Servicios-Web.aspx>

## Implementación propuesta

1. Investigar las operaciones SOAP necesarias para obtener la serie histórica de monedas.
2. Crear un wrapper en Python utilizando la librería **fast-mcp** para exponer estas consultas como herramienta MCP.
3. Documentar parámetros (moneda, rango de fechas) y estructura de la respuesta.
4. Incluir ejemplos de uso y pruebas básicas para validar la integración.

---

*Este es el primer issue de la comunidad para abrir la discusión y coordinar esfuerzos en torno a esta herramienta.*

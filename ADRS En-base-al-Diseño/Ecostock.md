# 📘 Registro de Decisiones Arquitectónicas (ADRs)
**Proyecto:** Sistema Web de Gestión de Inventario con Semaforización de Productos  
**Fecha de inicio:** 25/10/2025  
**Autor:** David Cocha  
**Versión:** 1.0  

---

## ADR-001: Identidad y Lema de Marca (Pág. 1) 🏷️
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Establecer el lema **“La inteligencia que tu tienda merece”** y el concepto **“Control Visual con Semaforización de Calidad”** como pilares en la comunicación y desarrollo.

### Contexto
La portada debe definir inmediatamente el valor y la sofisticación del sistema para las tiendas de barrio.

### Alternativas
- Usar un lema más técnico o genérico.

### Consecuencias
+ Genera una conexión emocional y un alto valor percibido.  
+ Orienta todas las funcionalidades hacia la gestión de calidad (Semaforización).  
− El término "inteligente" puede generar altas expectativas tecnológicas.  

---

## ADR-002: Mensaje de Bienvenida y Propósito (Pág. 2) ✨
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Enmarcar el sistema como una **“revolución”** que combina **tecnología, simplicidad visual y control de calidad**.

### Contexto
Definir la propuesta de valor como una solución integral que va más allá de la simple gestión de stock.

### Alternativas
- Enfocarse solo en la reducción de pérdidas.

### Consecuencias
+ Refuerza la identidad como un cambio positivo y completo para el negocio.  
+ Justifica la necesidad de la tecnología.  

---

## ADR-003: Priorización de la Detección de Caducidad (Pág. 3 y 11) 📉
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
El foco principal del sistema será el **control total de fechas** para eliminar la causa del **60% de las pérdidas** por productos caducados no detectados.

### Contexto
El problema principal del cliente es que la mayoría de pérdidas provienen de productos caducados.

### Alternativas
- Priorizar el control de stock mínimo.  
- Priorizar la gestión de pedidos a proveedores.

### Consecuencias
+ Aborda la causa raíz del problema del cliente.  
+ Garantiza el 60% menos de pérdidas.  
+ Permite ofrecer el beneficio de “Cero productos caducados”.  

---

## ADR-004: Diseño para el Mercado Latinoamericano y Simplicidad (Pág. 4) 🌎
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Centrar la visión en ser **el sistema más intuitivo** para tiendas de barrio en Latinoamérica, buscando **democratizar la tecnología inteligente**.

### Contexto
El sistema se dirige a un público específico: tiendas pequeñas en Latinoamérica.

### Alternativas
- Diseñar un sistema genérico para cualquier tipo de comercio.

### Consecuencias
+ Alinea el producto con la meta de reducir pérdidas en un 80% para 2026.  
+ Facilita el uso sin capacitación compleja.  

---

## ADR-005: Valores de Simplicidad y Transparencia (Pág. 5) 🤝
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Adoptar **Simplicidad** y **Transparencia** como valores rectores del diseño de la interfaz y experiencia de usuario.

### Contexto
Los valores determinan cómo se presenta la información y se construye la confianza con el cliente.

### Alternativas
- Priorizar únicamente Eficacia y Compromiso.

### Consecuencias
+ Genera confianza en el usuario final.  
+ Garantiza adopción sin requerir conocimientos técnicos.  

---

## ADR-006: Definición Estricta de la Semaforización (Pág. 6) 🚦
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Codificar la lógica del semáforo con definiciones fijas:  
- **Verde:** Stock saludable  
- **Amarillo:** Stock bajo (7–30 días)  
- **Rojo:** Caducado o sin stock  

### Contexto
El sistema requiere reglas claras para un control visual automático.

### Alternativas
- Permitir que el usuario defina los umbrales de forma flexible.

### Consecuencias
+ Asegura coherencia en las alertas.  
+ Reduce configuraciones complejas.  

---

## ADR-007: Arquitectura con Updates Automáticos (Pág. 7) 💾
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Integrar un sistema de **actualizaciones automáticas** mediante **Node.js y despliegue en la nube**, evitando intervención del usuario.

### Contexto
Los usuarios no deben gestionar actualizaciones manuales.

### Alternativas
- Descargar e instalar actualizaciones manualmente.

### Consecuencias
+ Mejora la seguridad y estabilidad.  
+ Garantiza que todos los clientes tengan la última versión.  

---

## ADR-008: Módulos del Ecosistema (Pág. 8) 🧩
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Diseñar **6 módulos principales**:  
1. Dashboard Central  
2. Gestión de Productos  
3. Sistema de Alertas  
4. Reportes y Analytics  
5. Semaforización  
6. Configuración  

### Contexto
Cada módulo aborda una necesidad de gestión de inventario.

### Alternativas
- Implementar un diseño monolítico sin separación funcional.

### Consecuencias
+ Facilita mantenimiento y escalabilidad.  
+ Mejora la navegación por tareas.  

---

## ADR-009: Flujo de Trabajo Lineal (Pág. 8) ➡️
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Estructurar el flujo del sistema en 5 etapas:  
**Entrada → Proceso → Semáforo → Alertas → Acción**

### Contexto
El usuario necesita una secuencia clara de trabajo.

### Alternativas
- Acceso libre a todos los módulos sin guía.

### Consecuencias
+ Aumenta la eficiencia operativa.  
+ Facilita el aprendizaje de uso.  

---

## ADR-010: Automatización Total y Precisión (Pág. 10 y 16) 🎯
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Automatizar el **100% de los procesos** de revisión y cálculo para lograr **85% de precisión**.

### Contexto
El sistema busca reemplazar tareas manuales y reducir errores.

### Alternativas
- Mantener parte de la revisión manual asistida.

### Consecuencias
+ Elimina el error humano.  
+ Mejora la confiabilidad de reportes.  

---

## ADR-011: Métricas de Éxito (Pág. 11 y 16) 📊
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Cuantificar el éxito con métricas de:  
- Reducción de pérdidas (60%)  
- Mayor precisión (85%)  
- Menos tiempo (40%)  
- Mejor servicio al cliente  

### Contexto
El diseño debe reforzar resultados tangibles para el usuario.

### Alternativas
- Usar solo una métrica principal.

### Consecuencias
+ Refuerza el valor medible del sistema.  
+ Permite justificar el ROI (6 meses).  

---

## ADR-012: Metáfora de Transformación Digital (Pág. 12) 🔄
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Utilizar el contraste **ANTES vs AHORA** para ilustrar el cambio digital.

### Contexto
Visualizar la transición ayuda a convencer al cliente.

### Alternativas
- Describir solo las nuevas características.

### Consecuencias
+ Refuerza la justificación de compra.  
+ Destaca la evolución hacia la digitalización.  

---

## ADR-013: Diseño para Usuario sin Experiencia Técnica (Pág. 13) 👶
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
El sistema debe **funcionar sin conocimientos técnicos** y permitir **configuración en 1 hora**.

### Contexto
Está orientado a tenderos sin formación digital.

### Alternativas
- Requerir alfabetización digital básica.

### Consecuencias
+ Democratiza el uso de la tecnología.  
+ Libera tiempo al usuario.  

---

## ADR-014: Usabilidad Offline (Pág. 13) 📶
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Incorporar **caché y almacenamiento local** para operar sin conexión constante.

### Contexto
Dirigido a tiendas con conectividad inestable.

### Alternativas
- Requerir conexión permanente.

### Consecuencias
+ Garantiza disponibilidad continua.  
+ Mejora la experiencia en zonas rurales.  

---

## ADR-015: Diseño con Impacto Ambiental Positivo (Pág. 14) ♻️
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Destacar el valor de **sostenibilidad**: reducción de desperdicios y ahorro de recursos.

### Contexto
El sistema busca ser responsable con el medio ambiente.

### Alternativas
- No mencionar impacto ambiental.

### Consecuencias
+ Refuerza el compromiso ecológico de la marca.  
+ Convierte la eficiencia en un impacto positivo.  

---

## ADR-016: Roadmap de Despliegue de 4 Fases (Pág. 15) 🗺️
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Implementar 4 fases:  
1. Diagnóstico  
2. Implementación  
3. Optimización  
4. Crecimiento  

### Contexto
Se requiere un plan progresivo para generar confianza.

### Alternativas
- Instalar todo en una sola etapa.

### Consecuencias
+ Gestiona expectativas del cliente.  
+ Asegura adopción gradual.  

---

## ADR-017: Diseño de Salida (Pág. 17) 🖼️
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Concluir con la promesa **“TU NEGOCIO TRANSFORMADO”**, mostrando Dashboard, Móvil e inventario optimizado.

### Contexto
Debe visualizar el resultado del uso del sistema.

### Alternativas
- Terminar con un mensaje genérico.

### Consecuencias
+ Refuerza visualmente el éxito del cliente.  
+ Cierra la narrativa de transformación.  

---

## ADR-018: Llamada a la Acción Final (Pág. 18) 📞
**Estado:** Aprobado  
**Fecha:** 25/10/2025  

### Decisión
Finalizar con una **llamada a la acción** clara:  
> ¡TRANSFORMA TU NEGOCIO HOY!

Incluyendo datos de contacto e iconos.

### Contexto
El cierre debe incitar a la compra o contacto.

### Alternativas
- Un simple “Gracias”.

### Consecuencias
+ Facilita el contacto con el equipo comercial.  
+ Cierra reforzando el lema **“La inteligencia que tu tienda merece”**.  

---

## ✅ Conclusión General
Este conjunto de ADRs garantiza una arquitectura visual, técnica y narrativa **alineada al propósito ecológico, social y tecnológico** del sistema. Cada decisión fue validada para mantener **simplicidad, automatización y sostenibilidad**, pilares clave para el éxito del proyecto.

# 📘 ADRs Técnicos Clave del Sistema de Inventario 

> **Contexto general:**  
> Este documento recopila las Decisiones de Arquitectura de Software (ADRs) puramente técnicas del proyecto, enfocadas en la pila tecnológica, interfaz, hosting, base de datos, offline, alertas y seguridad.

---

## 💻 ADR-TÉC-001: Pila Tecnológica para el Backend

**Estado:** Aprobado  
**Fecha:** 25/10/2025  
**Decisión:** Utilizar **Node.js** como entorno de ejecución y un modelo de datos basado en **JSON**.  

**Contexto:**  
Se necesita un backend robusto y simple que permita desarrollo ágil, eficiente y escalable para manejar inventario, semaforización y alertas.

**Alternativas:**  
- Java/Spring  
- Python/Django  

**Consecuencias:**  
- ✅ **Velocidad y Eficiencia:** Desarrollo rápido y rendimiento alto en I/O.  
- ✅ **Facilidad de Integración:** Compatible con frontend web y datos no relacionales.  
- ❌ **Complejidad Relacional:** Puede requerir lógica adicional para manejar relaciones complejas (ej. productos con múltiples proveedores).

---

## 📱 ADR-TÉC-002: Tipo de Interfaz de Usuario

**Estado:** Aprobado  
**Fecha:** 25/10/2025  
**Decisión:** Implementar una **Web responsive** como interfaz principal.  

**Contexto:**  
El sistema debe funcionar en móviles y ser accesible sin conocimientos técnicos, alineado con la simplicidad del proyecto.

**Alternativas:**  
- Aplicaciones nativas (iOS/Android)  

**Consecuencias:**  
- ✅ **Baja Barrera de Entrada:** No requiere instalación.  
- ✅ **Mantenimiento Unificado:** Un solo código base para todos los dispositivos.  
- ❌ **Rendimiento:** Puede limitar el acceso a funciones nativas o rendimiento gráfico.

---

## ☁️ ADR-TÉC-003: Estrategia de Despliegue / Hosting

**Estado:** Aprobado  
**Fecha:** 25/10/2025  
**Decisión:** Utilizar **Cloud Computing** para desplegar el sistema.  

**Contexto:**  
Es fundamental asegurar respaldo seguro y permitir actualizaciones automáticas.

**Alternativas:**  
- Hosting local  
- VPS básico  

**Consecuencias:**  
- ✅ **Disponibilidad y Seguridad:** Gestión de infraestructura por proveedor.  
- ✅ **Automatización de Updates:** Mantenimiento y actualización sin intervención manual.  
- ❌ **Costo Operativo:** Genera gasto mensual.

---

## 💾 ADR-TÉC-004: Modelo de Base de Datos

**Estado:** Provisional  
**Fecha:** 25/10/2025  
**Decisión:** Utilizar una **base de datos NoSQL** (MongoDB, DynamoDB o Firestore) para inventario y reglas de semaforización.

**Contexto:**  
El formato JSON y la necesidad de estructuras flexibles requieren un sistema no relacional.

**Alternativas:**  
- Base de datos SQL (PostgreSQL)  

**Consecuencias:**  
- ✅ **Flexibilidad:** Fácil adaptación de esquemas y atributos nuevos.  
- ✅ **Escalabilidad Horizontal:** Manejo eficiente de grandes volúmenes de datos.  
- ❌ **Integridad de Datos:** La lógica de integridad y relaciones depende del backend.

---

## 📶 ADR-TÉC-005: Gestión de Datos Offline / Sincronización

**Estado:** Aprobado  
**Fecha:** 25/10/2025  
**Decisión:** Implementar arquitectura **First-Offline** usando **Service Workers** y **IndexedDB**.  

**Contexto:**  
Tiendas de barrio con conectividad limitada requieren operaciones esenciales sin conexión.

**Alternativas:**  
- Solo consulta online  

**Consecuencias:**  
- ✅ **Disponibilidad:** Sistema operativo incluso sin conexión.  
- ✅ **Experiencia rápida:** Carga inmediata de inventario y semáforo.  
- ❌ **Complejidad:** Desarrollo costoso para sincronización y resolución de conflictos.

---

## 🚨 ADR-TÉC-006: Mecanismo de Alertas

**Estado:** Aprobado  
**Fecha:** 25/10/2025  
**Decisión:** Implementar **notificaciones Web Push** mediante **Firebase Cloud Messaging (FCM)** activadas por lógica del servidor.  

**Contexto:**  
Alertas de acción inmediata son clave para la eficacia del sistema.

**Alternativas:**  
- Alertas solo en dashboard  
- Email o SMS  

**Consecuencias:**  
- ✅ **Inmediatez:** Notificaciones en tiempo real.  
- ✅ **Costo eficiente:** Más barato que SMS.  
- ❌ **Dependencia de la nube:** Requiere conexión mínima para recibir alertas.

---

## 🔒 ADR-TÉC-007: Seguridad y Autenticación

**Estado:** Obligatorio  
**Fecha:** 25/10/2025  
**Decisión:** Implementar autenticación **stateless con JWT (JSON Web Tokens)**.  

**Contexto:**  
El sistema maneja datos sensibles de stock y ventas, requiriendo control seguro de acceso.

**Alternativas:**  
- Sesiones con cookies  
- OAuth2  

**Consecuencias:**  
- ✅ **Escalabilidad:** Ideal para entornos Cloud y Web responsive.  
- ✅ **Seguridad:** Tokens expiran automáticamente y contienen información del usuario.  
- ❌ **Almacenamiento del token:** Debe gestionarse seguro en el cliente (localStorage o IndexedDB).

---

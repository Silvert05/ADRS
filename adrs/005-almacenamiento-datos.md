# ADR-005: Almacenamiento de datos para prototipo


## Contexto
Backend real y base de datos no se implementarán en el proyecto académico


## Decisión
Usar JSON local para almacenar productos temporalmente


## Opciones consideradas
1. LocalStorage en frontend → menos flexible para pruebas de API
2. JSON + mock API → más cercano a un backend real y fácil de migrar


## Consecuencias
Datos simulados de forma realista, permite mostrar funcionalidades de semaforización y reportes
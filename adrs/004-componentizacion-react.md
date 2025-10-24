# ADR-004: Componentización en React.js


## Contexto
Se necesitan vistas separadas: tablero de inventario, registro de productos, reportes, administración de alertas


## Decisión
Crear componentes independientes:
- InventoryBoard → tablero con semáforo
- ProductForm → registro de productos
- ProductList → listado de productos
- Reports → reportes básicos


## Opciones consideradas
1. Una sola página monolítica → difícil de mantener y probar
2. Componentes → fácil de escalar y realizar pruebas de UX


## Consecuencias
Prototipo organizado, fácil de mantener y extender
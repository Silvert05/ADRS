# ADR-007: Modularidad de componentes


## Contexto
Facilitar escalabilidad, mantenimiento y pruebas unitarias


## Decisión
Separar componentes por función y responsabilidad:
- InventoryBoard, ProductForm, ProductList, Reports, AlertPanel


## Opciones consideradas
1. Un solo archivo para todo → difícil de probar y mantener
2. Componentes independientes → más escalable


## Consecuencias
Permite agregar futuras funcionalidades sin reescribir el frontend
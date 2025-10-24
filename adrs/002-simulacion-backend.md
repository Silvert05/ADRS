# ADR-002: Simulación del backend


## Contexto
Alcance académico incluye solo el frontend; backend real no será implementado inicialmente.


## Decisión
Usar mock API con Node.js y JSON local para simular la base de datos


## Opciones consideradas
1. Backend real con Node.js + MySQL → fuera de alcance
2. Mock API → cumple con el prototipo funcional


## Consecuencias
Permite pruebas de interfaz, semaforización y reportes sin dependencias externas
# ADR-008: Preparación para backend real


## Contexto
En futuras fases se integrará Node.js + MySQL


## Decisión
Diseñar frontend para consumir API REST, aunque actualmente use mock API


## Opciones consideradas
1. Conectar directamente al JSON → limitado
2. Preparar fetch/axios para API REST → fácil migración futura


## Consecuencias
Transición a backend real será sencilla
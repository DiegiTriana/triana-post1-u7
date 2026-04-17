# U7 Post-Contenido 1 - API de Tareas con Arquitectura en Capas

## Objetivo
Implementar una API REST con capas estrictas: presentacion, aplicacion, dominio e infraestructura.

## Paquetes
- `controller`: capa presentacion.
- `service`: capa aplicacion.
- `domain`: entidad y excepcion de negocio.
- `repository`: capa infraestructura.

## Ejecutar
```bash
mvn clean spring-boot:run
```

## Endpoints
- `GET /api/tareas`
- `GET /api/tareas/{id}`
- `POST /api/tareas`
- `PATCH /api/tareas/{id}/estado?estado=COMPLETADA`
- `DELETE /api/tareas/{id}`

## Verificacion
- Consola H2: `http://localhost:8080/h2-console`

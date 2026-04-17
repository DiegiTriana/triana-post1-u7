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

## Evidencias de Verificacion (2026-04-17 16:26:56)

| Checkpoint | Estado | Evidencia |
|---|---|---|
| Compila sin errores (mvn compile) | PASS | mvn -q -DskipTests compile |
| Aplicacion inicia en puerto de prueba | PASS | http://localhost:18503 |
| GET /api/tareas inicial retorna 200 | PASS | status=200 |
| POST valido retorna 201 | PASS | status=201, id=1 |
| POST sin titulo retorna 400 | PASS | status=400 |
| GET inexistente retorna 404 | PASS | status=404 |
| PATCH estado actualiza correctamente | PASS | status=200 |
| DELETE retorna 204 | PASS | status=204 |



# Reglas de Versionado

Cada push **debe** llevar su tag. No se pushea sin tag.

## Flujo de cada push

1. Obtener el último tag (ej: `v1.0.0`).
2. Verificar que `VERSION` coincida con ese tag (sin `v`).
3. Incrementar: `patch + 0.0.1` (ej: `1.0.0` → `1.0.1`).
4. Actualizar el archivo `VERSION` con la nueva versión.
5. Commit con mensaje conventional: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`.
6. Tag: `git tag -a vX.Y.Z -m "descripcion"`.
7. Push con tag: `git push origin main --tags`.

## Reglas

- **Tag = VERSION.** Si tag es `v1.0.5`, `VERSION` es `1.0.5`.
- **Cada push lleva su tag.** No hay excepciones.
- **No saltar versiones.** El ciclo patch va de 0 a 9. De `v1.0.9` → `v1.1.0`.
- **No retroceder.** Una vez publicado un tag, no se reemplaza.
- **Conventional commits.** Mensajes: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`.
- **No eliminar tags publicados.**

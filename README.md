# Calculadora Edad

Action compuesta que calcula la edad a partir del año de nacimiento. Resta ese año al año actual y devuelve el resultado.

## Entradas

| Nombre | Obligatorio | Descripción |
| --- | --- | --- |
| `anio_nacimiento` | sí | Año de nacimiento |

## Salidas

| Nombre | Descripción |
| --- | --- |
| `edad` | Edad calculada (año actual − año de nacimiento) |

## Uso

```yaml
- name: Calcular edad
  id: calcular
  uses: ./
  with:
    anio_nacimiento: "1995"

- name: Mostrar resultado
  run: echo "Edad calculada ${{ steps.calcular.outputs.edad }}"
```

Con año de nacimiento `1995` y año actual `2026`, la salida `edad` es `31`.

---
titulo: Análisis de ventas verano 2026
autor: Noa Tóth-Égetö
fecha: 2026-10-19
---

# <Título de la práctica>

**Bloque X · Sesión X.X.X** · <fecha>

## Objetivo

<Qué pregunta de negocio respondemos. Una o dos frases.>

## Datos

| Tabla / archivo | Filas | Descripción |
|---|--:|---|
| `ventas.csv` | 20.000 | Una fila por pedido, 2023–2025 |

## Metodología

1. <Paso 1: limpieza…>
2. <Paso 2: transformación…>
3. <Paso 3: análisis…>

## Resultados

- <Hallazgo principal, con su cifra.>
- <Segundo hallazgo.>

## Cómo reproducirlo

```bash
python limpieza.py
```

## Limitaciones y próximos pasos

- <Qué no cubre el análisis y qué haríamos con más tiempo o datos.>

## Ejemplo de diccionario de datos

| Columna | Tipo | Descripción | Ejemplo |
|---|---|---|---|
| `pedido_id` | Texto | Identificador único del pedido | `P000123` |
| `fecha` | Fecha | Fecha de creación del pedido | `2024-06-15` |
| `importe` | Decimal | Importe total en euros, IVA incluido | `125.40` |
| `region` | Texto | Región de entrega. Valores: Norte, Sur, Este, Oeste | `Norte` |

## ejemplo de diagrama mermaid

```mermaid
flowchart LR
    A[CSV de ventas] --> B[Limpieza con pandas]
    B --> C[(PostgreSQL)]
    C --> D[Dashboard Power BI]
```
# Performance Guidelines (ABAP)

## Overview

Este documento describe buenas prácticas para optimizar el rendimiento en desarrollos ABAP, enfocadas en eficiencia, escalabilidad y reducción de consumo de recursos.

---

## Objectives

* Reducir tiempos de ejecución
* Minimizar consumo de base de datos
* Optimizar uso de memoria
* Mejorar escalabilidad

---

## Principles

* Procesar en base de datos, no en ABAP
* Minimizar accesos a DB
* Evitar loops innecesarios
* Usar estructuras eficientes

---

## Database Access

### Evitar

```abap
SELECT * FROM mara INTO TABLE lt_mara.
```

### Recomendado

```abap
SELECT matnr ersda
  FROM mara
  INTO TABLE lt_mara.
```

✔ Leer solo los campos necesarios

---

## SELECT dentro de LOOP (ANTI-PATTERN)

### Incorrecto

```abap
LOOP AT lt_vbak INTO ls_vbak.
  SELECT * FROM vbap INTO TABLE lt_vbap
    WHERE vbeln = ls_vbak-vbeln.
ENDLOOP.
```

### Correcto

```abap
SELECT * FROM vbap
  INTO TABLE lt_vbap
  FOR ALL ENTRIES IN lt_vbak
  WHERE vbeln = lt_vbak-vbeln.
```

---

## FOR ALL ENTRIES

### Validación obligatoria

```abap
IF lt_vbak IS NOT INITIAL.
  SELECT * FROM vbap
    INTO TABLE lt_vbap
    FOR ALL ENTRIES IN lt_vbak
    WHERE vbeln = lt_vbak-vbeln.
ENDIF.
```

✔ Evita lecturas completas innecesarias

---

## Internal Tables

### Uso correcto de tipos

* STANDARD TABLE → uso general
* SORTED TABLE → búsquedas ordenadas
* HASHED TABLE → accesos rápidos (clave)

---

### READ eficiente

```abap
READ TABLE lt_mara INTO ls_mara
  WITH KEY matnr = lv_matnr
  BINARY SEARCH.
```

Requiere tabla ordenada

---

## LOOP optimizado

### Evitar

```abap
LOOP AT lt_data INTO ls_data.
```

### Mejor

```abap
LOOP AT lt_data INTO DATA(ls_data).
```

Menos variables globales

---

## Memory Usage

* Liberar tablas grandes cuando no se usan
* Evitar duplicación innecesaria de datos
* Usar referencias cuando sea posible

---

## Parallel Processing (cuando aplica)

* Dividir procesamiento en paquetes
* Usar RFC paralelos
* Evitar bloqueos innecesarios

---

## Index Usage

* Asegurar uso de índices en SELECT
* Evitar condiciones no indexadas
* Analizar planes de ejecución

---

## Tools

* ST05 (SQL Trace)
* SE30 / SAT (Runtime Analysis)
* SQL Monitor

---

## Anti-Patterns

* SELECT * innecesarios
* SELECT dentro de LOOP
* FOR ALL ENTRIES sin validación
* Tablas internas sin orden para búsquedas
* Procesamiento excesivo en ABAP

---

## Best Practices

* Diseñar pensando en volumen de datos
* Optimizar accesos a base de datos
* Usar estructuras adecuadas
* Medir antes de optimizar

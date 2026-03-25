# Error Handling (ABAP)

## Overview

Este documento describe las buenas prácticas para el manejo de errores en desarrollos ABAP, enfocadas en robustez, trazabilidad y mantenibilidad.

---

## Objectives

- Manejo consistente de errores  
- Facilitar debugging  
- Evitar fallos silenciosos  
- Mejorar experiencia del usuario  

---

## Principles

- No ignorar errores (`sy-subrc`)
- Centralizar manejo de errores
- Mensajes claros y trazables
- Separar errores técnicos de funcionales

---

## Basic Handling

### Validación de `sy-subrc`

```abap
SELECT * FROM mara INTO TABLE lt_mara.

IF sy-subrc <> 0.
  MESSAGE 'No data found' TYPE 'E'.
ENDIF.

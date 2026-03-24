# Naming Conventions (ABAP)

## Overview

Estas convenciones buscan mejorar la legibilidad, mantenibilidad y estandarización del código ABAP.

---

## General Rules

- Nombres claros y descriptivos
- Evitar abreviaturas innecesarias
- Consistencia en todo el desarrollo

---

## Objects
| Object Type               | Naming Convention                    | Example                  |
|---------------------------|--------------------------------------|--------------------------|
| Programa o Reporte        | `Z<Modulo><SubModulo>_<desc>`        | ZMMPUR_MOV_STOCK         |
| Modulpool                 | `Z<Modulo><SubModulo>_MP_<desc>`     | ZFIAP_MP_PRINT_INVOICE   |
| Grupo de Función          | `Z<Modulo><SubModulo>_GF_<desc>`     | ZSDLE_GF_KUNNX           |
| Function Module           | `Z<Modulo><SubModulo>_F_<desc>`      | ZSDLE_F_CHECK_PARTNER    |
| Formulario Sapscript      | `Z<Modulo><SubModulo>_SS_<desc>`     | ZHRPY_SS_SUELDO_AR       |
| Formulario Smartform      | `Z<Modulo><SubModulo>_SF_<desc>`     | ZHRPY_SF_SUELDO_UY       |
| Formulario AdobeForm      | `Z<Modulo><SubModulo>_AF_<desc>`     | ZHRPY_AF_SUELDO_MX       |
| Estilo Smartform          | `Z<Modulo><SubModulo>_STY_<desc>`    | ZHRPY_STY_SUELDO_UY      |
| WebDynpro                 | `Z<Modulo><SubModulo>_WD_<desc>`     | ZQMIM_WD_INSPECCION      |
| Clase de Objetos ABAP     | `Z<Modulo><SubModulo>_CL_<desc>`     | ZMMPUR_CL_CONTROL        |
| IDOC: Mensaje Lógico      | `Z<Modulo><SubModulo>_IMSG_<desc>`   | ZFIAR_IMSG_DELIVERY      |
| IDOC: Nombre del Segmento | `Z<Modulo><SubModulo>_ISG_<desc>`    | ZFIAR_ISG_DEL_HEADER     |
| IDOC: Tipo Base           | `Z<Modulo><SubModulo>_ITB_<desc>`    | ZFIAR_ITB_DELIVERY       |
| Transacciones             | `Z<Modulo><SubModulo>_<desc>`        | ZSDLE_Check_Int          |
| Ampliaciones              | `Z<Modulo><SubModulo>_ENH_<desc>`    | ZSDLE_ENH_KUNNX          |
| Implementaciones          | `Z<Modulo><SubModulo>_IMP_<desc>`    | ZSDLE_IMP_KUNNX          |
| Clase de Mensaje          | `Z<Modulo>_<desc>`                   | ZSD_AFIP                 |
| Proyectos(CMOD)           | `Z<Modulo>_<sec>`                    | ZHR_001                  |
| Productos de BTE          | `Z<Modulo>_<sec>`                    | ZFI_001                  |

`<Modulo>`: Modulo SAP

`<SubModulo>`: SubModulo SAP

`<desc>`: Descripcion

`<Sec>`: Secuencial de 3 digitos


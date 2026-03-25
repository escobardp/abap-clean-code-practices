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

---
## Objects: Dictionary
| Object Type       | Naming Convention                | Example         |
|-------------------|----------------------------------|-----------------|
| Tablas            | `Z<Modulo><SubModulo>_<desc>`    | ZMMPUR_CHECK    |
| Vistas            | `Z<Modulo><SubModulo>_V_<desc>`  | ZMMPUR_V_CHECK  |
| Estructuras       | `Z<Modulo><SubModulo>_E_<desc>`  | ZMMPUR_E_CHECK  |
| Tipo Tabla        | `Z<Modulo><SubModulo>_TT_<desc>` | ZMMPUR_TT_CHECK |
| Campo             | `<desc>`                         | CHECK_TIME      |
| Elemento de dato  | `ZE_<desc>`                      | ZE_CHECK        | 
| Dominio           | `ZD_<desc>`                      | ZD_CHECK        |
| Ayuda de Búsqueda | `Z<Modulo><SubModulo>_TT_<desc>` | ZMMPUR_SH_CHECK |
| Objeto de Bloqueo | `EZ_<desc>`                      | EZ_CHECK        |

---
## Objects: Programming

| Object Type                                     | Naming Convention | Example       |
|-------------------------------------------------|-------------------|---------------|
| Parámetros de pantalla de selección             | PA_XXXXXX         | PA_BUKRS      |
| Select Option                                   | SO_XXXXXXX        | SO_BELNR      |
| Checkbox                                        | CH_XXXXXXXX       | CH_ONLINE     |
| Radio Button                                    | RB_XXXXXX         | RB_LOCAL      |
| Constante Global tipo tabla                     | C_T_XXXXXXX       | C_T_BUKRS     |
| Constante Global estructura                     | C_W_XXXXXXX       | C_W_T001      |
| Constante Global variable                       | C_V_XXXXXXX       | C_V_BLART     |
| Constante Local tipo tabla                      | CL_T_XXXXXXX      | CL_T_LFA1     |
| Constante Local estructura                      | CL_W_XXXXXXX      | CL_W_KNA1     |
| Constante Local variable                        | CL_V_XXXXXXX      | CL_V_KUNNR    |
| Tipo Global tabla                               | TYT_XXXXXXX       | TYT_BSEG      |
| Tipo Global Rango                               | TYT_R_XXXXXXX     | TYT_R_BUKRS   |
| Tipo Global estructura                          | TY_XXXXXXX        | TY_BSEG       |
| Tipo Global variable                            | TY_XXXXXXXXX      | TY_COMPANY    |
| Tipo Local tabla                                | TYTL_XXXXXXXX     | TYT_BSIS      |
| Tipo Local Rango                                | TYTL_R_XXXXXXX    | TYTL_R_LIFNR  |
| Tipo Local estructura                           | TYL_XXXXXXX       | TYL_BSEG      |
| Tipo Local variable                             | TYL_XXXXXXX       | TYL_VENDOR    |
| Field Symbols Global tabla                      | <FS_T_XXXXXX>     | <FS_T_BSET>   |
| Field Symbols Global estructura                 | <FS_W_XXXXXX>     | <FS_W_MARA>   |
| Field Symbols Global variables                  | <FS_V_XXXXXX>     | <FS_V_AUART>  |
| Field Symbols Local Tabla                       | <FSL_T_XXXXXX>    | <FSL_T_BSAK>  |
| Field Symbols Local estructura                  | <FSL_W_XXXXXX>    | <FSL_W_MARD>  |
| Field Symbols Local variables                   | <FSL_V_XXXXXX>    | <FSL_V_BLART> |
| Rangos Globales                                 | R_XXXXXXX         | R_BUKRS       |
| Rangos Locales                                  | RL_XXXXXX         | RL_STCDT      |
| Global Tabla interna                            | IT_XXXXX          | IT_FILE       |
| Global Work Area                                | WA_XXXXX          | WA_T001W      |
| Global Variables                                | V_XXXXXXXX        | V_STCD1       |
| Local Tabla interna                             | ITL_XXXXX         | ITL_WERKS     |
| Local Work Area                                 | WAL_XXXXX         | WAL_T001L     |
| Local Variables                                 | VL_XXXXXXXX       | VL_NAME1      |
| Objetos Globales                                | O_XXXXXX          | O_DATA        |
| Objetos Locales                                 | OL_XXXXXXX        | OL_FILE       |
| Clases Locales(No SE24)                         | LCL_XXXXXXXX      | LCL_FILE      |
| Clase Parámetro Importing Tablas                | IM_T_XXXXX        | IM_T_LFA1     |
| Clase Parámetro Importing Work Area             | IM_W_XXXXX        | IM_W_KNA1     |
| Clase Parámetro Importing Variables             | IM_V_XXXXX        | IM_V_KUNNR    |
| Clase Parámetro Exporting Tablas                | EX_T_XXXXX        | E_T_BSIK      |
| Clase Parámetro Exporting Work Area             | EX_W_XXXXX        | E_W_BSEG      |
| Clase Parámetro Exporting Variables             | EX_V_XXXXX        | E_V_BUKRS     |
| Clase Parámetro Chaging Tablas                  | CH_T_XXXXX        | CH_T_MARD     |
| Clase Parámetro Chaging Work Area               | CH_W_XXXXX        | CH_W_PA0001   |
| Clase Parámetro Chaging Variables               | CH_V_XXXXX        | CH_V_PERNR    |
| Clase Parámetro Returning Tablas                | RE_T_XXXXX        | RE_T_MAKT     |
| Clase Parámetro Returning Work Area             | RE_W_XXXXX        | RE_W_MSEG     |
| Clase Parámetro Returning Variables             | RE_V_XXXXX        | RE_V_LGORT    |
| Clase Datos Globales Tablas                     | CC_T_XXXXX        | CC_T_CUSTOMER |
| Clase Datos Globales Work Area                  | CC_W_XXXXX        | CC_W_VENDOR   |
| Clase Datos Globales Variables                  | CC_V_XXXXX        | CC_V_SPART    |
| Clase Atributos Tablas                          | TM_XXXXX          | TM_A901       |
| Clase Atributos Variables                       | VM_XXXXX          | VM_TEXT       |
| Clase Atributos Constantes                      | CM_XXXXX          | CM_LANGU      |
| Clase Atributos Objeto                          | OM_XXXXX          | OM_MAIN       |
| Clase Atributos Work Area                       | WAM_XXXXX         | WAM_DATOS     |
| Clase Atributos Rangos                          | RM_XXXXX          | RM_BUDAT      |
| Parámetro de Funcion Importing Tablas           | IM_T_XXXXX        | IM_T_BSID     |
| Parámetro de Funcion Importing Work Area        | IM_W_XXXXX        | IM_W_BSIK     |
| Parámetro de Funcion Importing Variables        | IM_V_XXXXX        | IM_V_GJAHR    |
| Parámetro de Funcion Exporting Tablas           | EX_T_XXXXX        | E_T_BSAD      |
| Parámetro de Funcion Exporting Work Area        | EX_W_XXXXX        | E_W_BSAK      |
| Parámetro de Funcion Exporting Variables        | EX_V_XXXXX        | E_V_BUZEI     |
| Parámetro de Funcion Changing Tablas            | CH_T_XXXXX        | CH_T_MESSAGE  |
| Parámetro de Funcion Changing Work Area         | CH_W_XXXXX        | CH_W_STATUS   |
| Parámetro de Funcion Changing Variables         | CH_V_XXXXX        | CH_V_SUBRC    |
| Rutinas (Form)                                  | F_XXXXXXXX        | F_GET_BKPF    |
| Rutinas (Form) Parámetro de entrada tabla       | PI_T_XXXXX        | PI_T_LIKP     |
| Rutinas (Form) Parámetro de entrada rango       | PI_R_XXXXX        | PI_R_SPART    |
| Rutinas (Form) Parámetro de entrada estructura  | PI_W_XXXXX        | PI_W_LIPS     |
| Rutinas (Form) Parámetro de entrada variable    | PI_V_XXXXX        | PI_V_XBLNR    |
| Rutinas (Form) Parámetro de salida tabla        | PO_T_XXXXX        | PO_T_KNVV     |
| Rutinas (Form) Parámetro de salida rango        | PO_R_XXXXX        | PO_R_WAERS    |
| Rutinas (Form) Parámetro de salida estructura   | PO_W_XXXXX        | PO_W_HEADER   |
| Rutinas (Form) Parámetro de salida variable     | PO_V_XXXXX        | PO_V_MONAT    |

---
## Objects: Screen

| Object Type             | Naming Convention          | Example         |
|-------------------------|----------------------------|-----------------|
| Pantalla / Screen       | 9XXXX                      | 9010            |
| Campo de texto          | TXT_XXXX                   | TXT_BUKRS       |
| Campo entrada           | INP_XXXX                   | INP_BELNR       |
| Campo de salida         | OUT_XXX                    | OUT_GJAHR       |
| Campo de entrada/salida | IO_XXX                     | IO_BUDAT        |
| Botón                   | BTN_xxxxx                  | BTN_ACEPTAR     |
| Radio Button            | RB_XXX                     | RB_LOCAL        |
| Checkbox                | CH_xxxx                    | CH_UPDATE       |

---
## Objects: Web Dynpro

| Object Type              | Naming Convention | Example       |
|--------------------------|-------------------|---------------|
| Application              | ZMM_AAA           | ZMM_CONSUMOS  |    
| Component                | WDC_AAA           | WDC_CHK       |
| Configuration Controller | WCC_AAA           | WCC_MAIN      |
| Assistant class          | CL_XXXX_ASS       | CL_MAIN_ASS   |
| Button                   | BTN_XXX           | BTN_ACEPTAR   |   
| Caption                  | CP_XXX            | CP_ACEPTAR    |
| Checkbox                 | CB_XXX            | CB_LOCAL      | 
| Container                | CT_XXX            | CT_HEADER     |
| Dropdown                 | DD_XXX            | DD_BUKRS      |
| Event handler            | ON_XXXXX          | ON_EVENT_01   |  
| FileDownLoad             | FD_XXXX           | FD_HEADER     |
| FileUpload               | FU_XXXX           | FU_HEADER     |
| Group                    | GR_XXXX           | GR_HEADER     |
| HorizontalGutter         | HG_XXXX           | HG_CHECK      |
| Image                    | IMG_XXXX          | IMG_LOGO_1    | 
| Inbound plug             | FROM_XXXX         | FROM_VIEW_1   | 
| Inputfield               | INP_XXXX          | INP_BUKRS     |
| ItemListBox              | ILB_XXXX          | ILB_LIFNR     |
| Label                    | LBL_XXX           | LBL_BUKRS     |
| MessageArea              | MSA_XXXX          | MSA_BLOCK_1   | 
| Outbound plug            | TO_XXXXX          | TO_VIEW_2     |
| PageHeader               | PH_XXXX           | PH_VIEW_1     |
| RadioButton              | RB_XXXX           | RB_LIFNR      |
| Supply function          | SUPPLY_XXXX       | SUPPLY_CHECK  |
| Tab                      | T_XXXX            | T_MAIN        |
| Table                    | TBL_XXXX          | TBL_VENDOR    |
| TableCellEditor          | TBLCE_XXX         | TBLCE_VENDOR  | 
| TableColumn              | TBLC_XXXX         | TBLC_VENDOR   |
| TableColumnHeader        | TBLCH_XXXX        | TBLCH_VENDOR  |
| Tableheader              | TBLH_XXXX         | TBLH_VENDOR   |
| TabStrip                 | TS_XXXX           | TS_VENDOR     |
| TextEdit                 | TXTE_XXXX         | TXTE_VENDOR   | 
| TextView                 | TXTV_XXXX         | TXTV_VENDOR   |
| Toolbar                  | TB_XXXX           | TB_UPDATE_1   |
| TransparentContainer     | TC_XXXX           | TC_VIEW_1     |
| Tree                     | TR_XXXX           | TR_VIEW_1     |
| TreeItemType             | TIT_XXXX          | TIT_MAIN      |
| TreeNodeType             | TNT_XXXX          | TNT_MAIN_1    | 
| TriStateCheckBox         | TSCB_XXXX         | TSCB_MAIN_1   |
| View                     | V_CCCC            | V_MAIN        |
| ViewContainerElement     | VC_CCCC           | VC_MAIN_1     |
| Window                   | W_XXXX            | W_MAIN        |

## Convenciones base
- `<Modulo>`: Módulo SAP
- `<SubModulo>`: Submódulo SAP
- `<desc>`: Descripción funcional
- `<Sec>`: Secuencial de 3 dígitos



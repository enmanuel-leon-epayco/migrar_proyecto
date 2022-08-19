## Actualizar recaudo_configuracion_detalle con el siguiente valor para apuntar al servicio de produccion.

- Cambiar el id requerido en la condicional del Query con el respectivo en el ambiente de produccion

```sql
UPDATE epayco_db.recaudo_configuracion_detalle
SET valor='{
    "consulta": {
        "url_consulta": "https:\\/\\/wom.epayco.com\\/api\\/v1\\/wom\\/Consultar",
        "method": "POST",
        "basic_auth": false,
        "user_basic_auth": "",
        "pass_basic_auth": "",
        "jwt_auth": false,
        "url_jwt_auth": "",
        "user_jwt_aut": "",
        "pass_jwt_auth": "",
        "jwt_bearer_field": "",
        "mutual_tls": false,
        "crt_mutual_tls": "",
        "private_key_mutual_tls": "",
        "jwt_login_url_method": "",
        "campo_respuesta": "data",
        "bool_campo_respuesta": true,
        "tipo_campo_respuesta": "object",
        "http_code": 200,
        "result": "{\\n  \\"success\\": true,\\n  \\"title_response\\": \\"Consulta exitosa\\",\\n  \\"text_response\\": \\"Consulta exitosa\\",\\n  \\"last_action\\": \\"Consulta exitosa\\",\\n  \\"data\\": [\\n    {\\n      \\"billID\\": \\"212815294\\",\\n      \\"folioID\\": \\"1016325\\",\\n      \\"billingCycleID\\": \\"7064\\",\\n      \\"billingCycleName\\": \\"7064\\",\\n      \\"issueDate\\": \\"2022-03-25\\",\\n      \\"cycleBeginDate\\": \\"2022-02-25\\",\\n      \\"cycleEndDate\\": \\"2022-03-25\\",\\n      \\"openAmount\\": \\"22000\\",\\n      \\"invoiceAmount\\": \\"22000\\",\\n      \\"dueDate\\": \\"2022-03-30\\",\\n      \\"pdfLink\\": null,\\n      \\"documentType\\": \\"CYCLE-INV\\",\\n      \\"accountCode\\": \\"531384810001\\",\\n      \\"serviceNumber\\": \\"3026111867\\"\\n    },\\n    {\\n      \\"billID\\": \\"211775197\\",\\n      \\"folioID\\": \\"1010757\\",\\n      \\"billingCycleID\\": \\"7062\\",\\n      \\"billingCycleName\\": \\"7062\\",\\n      \\"issueDate\\": \\"2022-01-25\\",\\n      \\"cycleBeginDate\\": \\"2021-12-25\\",\\n      \\"cycleEndDate\\": \\"2022-01-25\\",\\n      \\"openAmount\\": \\"187499\\",\\n      \\"invoiceAmount\\": \\"187499\\",\\n      \\"dueDate\\": \\"2022-04-02\\",\\n      \\"pdfLink\\": null,\\n      \\"documentType\\": \\"CYCLE-INV\\",\\n      \\"accountCode\\": \\"531384810001\\",\\n      \\"serviceNumber\\": \\"3026111867\\"\\n    },\\n    {\\n      \\"billID\\": \\"29286001\\",\\n      \\"folioID\\": \\"2404\\",\\n      \\"billingCycleID\\": \\"6069\\",\\n      \\"billingCycleName\\": \\"6069\\",\\n      \\"issueDate\\": \\"2021-08-25\\",\\n      \\"cycleBeginDate\\": \\"2021-07-25\\",\\n      \\"cycleEndDate\\": \\"2021-08-25\\",\\n      \\"openAmount\\": \\"5849999\\",\\n      \\"invoiceAmount\\": \\"5849999\\",\\n      \\"dueDate\\": \\"2021-12-25\\",\\n      \\"pdfLink\\": null,\\n      \\"documentType\\": \\"CYCLE-INV\\",\\n      \\"accountCode\\": \\"531384810001\\",\\n      \\"serviceNumber\\": \\"3026111867\\"\\n    }\\n  ]\\n}"
    },
    "consultar": [
        {
            "idForm": "consulta0",
            "formValid": true,
            "order": 0,
            "tituloCampo": "serviceNumber",
            "textoAyuda": "serviceNumber",
            "tipoCampo": "",
            "campoDb": "",
            "configCampo": "text",
            "configCampos": [],
            "options": [],
            "haveOptions": false,
            "obligatorio": true,
            "nombreParametro": "serviceNumber",
            "tipoParametro": "string"
        }
    ],
    "opcionesRecaudo": {
        "modificarValorPagar": {
            "activo": false,
            "opcion": ">"
        },
        "multiplesValoresPago": {
            "activo": false,
            "opcion": 2
        },
        "agruparFacturas": {
            "activo": true
        },
        "ultraFacturas": {
            "activo": false,
            "opcion": 15
        },
        "decimal": {
            "value": "none"
        },
        "moneda": {
            "value": "COP"
        },
        "mostrarFacturasLimite": {
            "activo": false,
            "valor": 1,
            "opcion": null
        },
        "conceptoPago": {
            "activo": false,
            "options": []
        },
        "conceptoPagoNewOption": {
            "name": "",
            "value": ""
        },
        "generarCodigoPago": {
            "activo": false,
            "index": 0
        }
    },
    "visualizacion": [
        {
            "idForm": "respuesta0",
            "option": 0,
            "nombreParametro": "billID",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra1",
            "campoDb": "extras",
            "textoAyuda": "billID",
            "formValid": true,
            "nombreCampo": "billID"
        },
        {
            "idForm": "respuesta1",
            "option": 1,
            "nombreParametro": "folioID",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "facturaId",
            "campoDb": "factura_id",
            "textoAyuda": "folioID",
            "formValid": true,
            "nombreCampo": "folioID"
        },
        {
            "idForm": "respuesta2",
            "option": 2,
            "nombreParametro": "billingCycleID",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra2",
            "campoDb": "extras",
            "textoAyuda": "billingCycleID",
            "formValid": true,
            "nombreCampo": "billingCycleID"
        },
        {
            "idForm": "respuesta3",
            "option": 3,
            "nombreParametro": "billingCycleName",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra3",
            "campoDb": "extras",
            "textoAyuda": "billingCycleName",
            "formValid": true,
            "nombreCampo": "billingCycleName"
        },
        {
            "idForm": "respuesta4",
            "option": 4,
            "nombreParametro": "issueDate",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra4",
            "campoDb": "extras",
            "textoAyuda": "issueDate",
            "formValid": true,
            "nombreCampo": "issueDate"
        },
        {
            "idForm": "respuesta5",
            "option": 5,
            "nombreParametro": "cycleBeginDate",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra5",
            "campoDb": "extras",
            "textoAyuda": "cycleBeginDate",
            "formValid": true,
            "nombreCampo": "cycleBeginDate"
        },
        {
            "idForm": "respuesta6",
            "option": 6,
            "nombreParametro": "cycleEndDate",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra6",
            "campoDb": "extras",
            "textoAyuda": "cycleEndDate",
            "formValid": true,
            "nombreCampo": "cycleEndDate"
        },
        {
            "idForm": "respuesta7",
            "option": 7,
            "nombreParametro": "openAmount",
            "visible": true,
            "configCampo": "number",
            "tipoCampo": "total",
            "campoDb": "total",
            "textoAyuda": "openAmount",
            "formValid": true,
            "nombreCampo": "openAmount"
        },
        {
            "idForm": "respuesta8",
            "option": 8,
            "nombreParametro": "invoiceAmount",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra7",
            "campoDb": "extras",
            "textoAyuda": "invoiceAmount",
            "formValid": true,
            "nombreCampo": "invoiceAmount"
        },
        {
            "idForm": "respuesta9",
            "option": 9,
            "nombreParametro": "dueDate",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra8",
            "campoDb": "extras",
            "textoAyuda": "dueDate",
            "formValid": true,
            "nombreCampo": "dueDate"
        },
        {
            "idForm": "respuesta10",
            "option": 10,
            "nombreParametro": "pdfLink",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra9",
            "campoDb": "extras",
            "textoAyuda": "pdfLink",
            "formValid": true,
            "nombreCampo": "pdfLink"
        },
        {
            "idForm": "respuesta11",
            "option": 11,
            "nombreParametro": "documentType",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra10",
            "campoDb": "extras",
            "textoAyuda": "documentType",
            "formValid": true,
            "nombreCampo": "documentType"
        },
        {
            "idForm": "respuesta12",
            "option": 12,
            "nombreParametro": "accountCode",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra11",
            "campoDb": "extras",
            "textoAyuda": "accountCode",
            "formValid": true,
            "nombreCampo": "accountCode"
        },
        {
            "idForm": "respuesta13",
            "option": 13,
            "nombreParametro": "serviceNumber",
            "visible": true,
            "configCampo": "texto",
            "tipoCampo": "extra12",
            "campoDb": "extras",
            "textoAyuda": "serviceNumber",
            "formValid": true,
            "nombreCampo": "serviceNumber"
        }
    ],
    "confirmacion": {
        "url_confirmacion": "https:\\/\\/wom.epayco.com\\/api\\/v1\\/wom\\/Confirmar",
        "method": "POST",
        "basic_auth": false,
        "user_basic_auth": "",
        "pass_basic_auth": "",
        "jwt_auth": false,
        "url_jwt_auth": "",
        "user_jwt_aut": "",
        "pass_jwt_auth": "",
        "jwt_bearer_field": "",
        "mutual_tls": false,
        "crt_mutual_tls": "",
        "private_key_mutual_tls": "",
        "jwt_login_url_method": "",
        "tipo_servicio": "servicio",
        "inputs": [
            {
                "campo": "billID",
                "variable": "",
                "id": 0,
                "valido": false
            },
            {
                "campo": "folioID",
                "variable": "",
                "id": 1,
                "valido": false
            },
            {
                "campo": "billingCycleID",
                "variable": "",
                "id": 2,
                "valido": false
            },
            {
                "campo": "billingCycleName",
                "variable": "",
                "id": 3,
                "valido": false
            },
            {
                "campo": "issueDate",
                "variable": "",
                "id": 4,
                "valido": false
            },
            {
                "campo": "cycleBeginDate",
                "variable": "",
                "id": 5,
                "valido": false
            },
            {
                "campo": "cycleEndDate",
                "variable": "",
                "id": 6,
                "valido": false
            },
            {
                "campo": "openAmount",
                "variable": "",
                "id": 7,
                "valido": false
            },
            {
                "campo": "invoiceAmount",
                "variable": "",
                "id": 8,
                "valido": false
            },
            {
                "campo": "dueDate",
                "variable": "",
                "id": 9,
                "valido": false
            },
            {
                "campo": "pdfLink",
                "variable": "",
                "id": 10,
                "valido": false
            },
            {
                "campo": "documentType",
                "variable": "",
                "id": 11,
                "valido": false
            },
            {
                "campo": "accountCode",
                "variable": "",
                "id": 12,
                "valido": false
            },
            {
                "campo": "serviceNumber",
                "variable": "",
                "id": 13,
                "valido": false
            }
        ],
        "respuestas": {
            "aceptadas": true,
            "pendientes": false,
            "rechazadas": false
        },
        "reintentosConfirmacion": "3",
        "reintentosRecurrencia": 60,
        "reintentosHoraLimite": "23:59"
    },
    "errores": []
}'
WHERE id='$id';

```

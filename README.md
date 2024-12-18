# Módulo Validador de TAXID de Ecuador para WHMCS 8.11.2
Módulo para WHMCS 8.11.2 que permite validar el TAXID de Ecuador (Cédula o RUC) en los campos de registro y checkout. Compatible com los temas SIX, TwentyOne y Lagom.

# Instrucciones de Instalación:
- Descomprime el archivo y sube las carpetas a la ruta de instalación de tu WHMCS. Si utilizas cPanel, súbelas al directorio public_html.
- El archivo comprimido ya contiene las rutas correctas: /modules/addons/.
- Ingresa a Configuración > Módulos Extra en WHMCS.
- Activa el módulo "Validación de TaxID de Ecuador" y asigna los permisos de rol necesarios.
- Dirígete al menú "Módulos" y selecciona "Validación de TaxID de Ecuador" para configurarlo.
- Habilita la validación desde el panel del módulo.
- Accede a Configuración > Configuración de Impuestos en WHMCS y habilita el soporte para impuestos.

# ¿Cómo funciona?
El módulo utiliza el campo TAX ID, que se habilita automáticamente al activar el soporte para impuestos de WHMCS, por lo que no requiere la creación de campos personalizados adicionales.

Cuando el país seleccionado en el registro o en el checkout es Ecuador, la validación se activa en el campo TAX ID y realiza las siguientes comprobaciones:

- Validación de cédula de identidad ecuatoriana.
- Validación de RUC de empresa privada ecuatoriana.
- Validación de RUC de empresa pública ecuatoriana.

Si el valor ingresado no cumple con alguna de estas validaciones, se mostrará un mensaje de error correspondiente.

# Áreas de Aplicación

El módulo funciona tanto en el formulario de registro como en el checkout de WHMCS.cPara evitar bloqueos en clientes ya registrados que no hayan ingresado su TAX ID previamente, la validación no se ejecuta si el usuario ha iniciado sesión. Sin embargo, se mostrará una advertencia al administrador en el backend para que el TAX ID sea ingresado manualmente. Si el país seleccionado no es Ecuador, la validación no se ejecutará.

# Compatibilidad
- WHMCS 8.11.2 y temas SIX, TwentyOne y Lagom
- WHMCS 8.X
- PHP 8.1 y 8.2

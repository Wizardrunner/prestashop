# 🛒 Configurar la tienda

## ⚙️ Configuración de Parámetros Avanzados

Explorar el menú de parámetros avanzados es como adentrarse en el motor de tu tienda en línea. Aquí encontrarás ajustes técnicos esenciales que permiten que todo funcione sin problemas. Desde revisar información de configuración hasta realizar copias de seguridad de la base de datos y configurar correos electrónicos, esta sección es crucial para la gestión eficaz de tu sitio, especialmente para tu webmaster.

### Índice de Contenidos:
* ℹ️ [**Información**](#informacion)
* 🚀 [**Rendimiento**](#rendimiento)
* 🛠️ [**Administración**](#administracion)
* ✉️ [**Correo electrónico**](#correo)
* 📥 [**Importación**](#importacion)
* 👥 [**Equipo**](#equipo)
* 💾 [**Base de datos**](#basededatos)
* 📝 [**Registros**](#registros)
* 🌐 [**Servicio web**](#webservice)
* 🏢 [**Multitienda**](#multitienda)
* ✨ [**Características Especiales**](#caracteristicas)
* 🔒 [**Seguridad**](#seguridad)


## ℹ️ Información

Esta página proporciona un recordatorio útil sobre la configuración de tu tienda PrestaShop, incluyendo detalles como la versión de PrestaShop, la información del servidor, la versión de PHP y la versión de MySQL. Esta información es muy valiosa cuando necesitas reportar un problema a los desarrolladores de PrestaShop o cuando estás trabajando con tu webmaster o proveedor de alojamiento.

### Lista de Archivos Modificados

En esta sección, tras la instalación inicial de PrestaShop, verás el mensaje "No se ha detectado ningún cambio en sus archivos". Sin embargo, después de instalar algunos módulos, agregar temas, hacer cambios avanzados en clases o eliminar archivos, esta lista mostrará las diferencias entre tu instalación actual y la original. Esto es útil para tener claridad sobre los cambios realizados en tu instalación, lo cual es importante si deseas actualizar tu tienda manualmente o mover archivos a un nuevo servidor.

Incluso en una instalación limpia, es posible que se muestren archivos faltantes, como `.gitattributes`, `.gitignore`, `CONTRIBUTING.md`, `CONTRIBUTORS.md` o `README.md`. Estos son archivos específicos de Git que PrestaShop no utiliza, por lo que no debes preocuparte por ellos.

## 🚀 Rendimiento

Esta página reúne varias herramientas y consejos que pueden ayudarte a mejorar el rendimiento de tu tienda desde el punto de vista del servidor. Aunque un servidor rápido puede no aumentar directamente tus ventas, sin duda mejora la capacidad de atender más clientes simultáneamente, lo que puede generar más ventas a largo plazo.

### 🧑‍💻 Smarty

Smarty es el lenguaje de plantillas utilizado por los temas de PrestaShop. Puedes aprender más sobre él en [Smarty.net](http://www.smarty.net/).

#### Opciones de Caché:

* **Caché de plantilla:** PrestaShop almacena en caché las páginas HTML para mejorar el rendimiento en el front-end.
* **No recompilar archivos de plantilla:** Las páginas HTML se compilan y se almacenan en caché, mostrando siempre el mismo contenido, incluso si el tema cambia.
* **Recompilar plantillas si los archivos se han actualizado:** PrestaShop detecta cuando un archivo de tema ha sido modificado.
* **Forzar la compilación:** Habilita esta opción solo si estás editando el tema y necesitas ver los cambios cada vez que recargas la página.
* **Caché:** Desactiva todas las cachés de archivos, no solo las de las plantillas, si estás depurando un tema o módulo. Mantén esta opción activada de lo contrario.

Puedes limpiar la caché con el botón "Limpiar caché" en la parte superior de la página.

### 🌐 Optimización Multi-frontal

Si tienes varios servidores, esta opción te ayuda a sincronizar la caché entre ellos.

### 🗄️ Tipo de Caché

Por defecto, Smarty usa un sistema de caché basado en archivos. Sin embargo, puedes elegir MySQL como sistema de almacenamiento para la caché de salida de Smarty.

### 🛠️ Modo de Depuración

Cuando el modo de depuración está activado, puedes reducir el impacto de ciertas funciones en PrestaShop para identificar mejor el origen de errores:

* **Desactivar módulos que no son de PrestaShop:** Permite determinar si un problema proviene de un módulo propio de PrestaShop o de un módulo de terceros.
* **Desactivar todas las sobrecargas:** Desactiva las sobrecargas de código para identificar el origen de los problemas.
* **Modo de depuración:** Activa esta opción para mostrar mensajes de error técnicos, útil para los desarrolladores.

### ⚙️ Características Opcionales

Si no usas algunas características de PrestaShop, puedes desactivarlas para mejorar el rendimiento. Sin embargo, si tu catálogo incluye productos con estas características, no podrás desactivarlas sin eliminar datos primero.

Características que puedes desactivar:

* **Combinaciones:** Permiten crear variaciones de un producto (tamaño, color, etc.).
* **Características:** Detalles específicos del producto, como peso, material, etc.
* **Grupos de clientes:** Permiten segmentar clientes con privilegios y restricciones especiales (descuentos, módulos).

### 🔧 Combinar, Comprimir y Almacenar en Caché (CCC)

Las herramientas CCC ayudan a reducir la carga del servidor y optimizar el tiempo de carga del tema:

* **Caché inteligente para CSS:** Los archivos CSS pueden combinarse y comprimirse para mejorar la carga.
* **Caché inteligente para JavaScript:** Los archivos JavaScript también pueden combinarse, pero asegúrate de probar todo antes de activarlo.
* **Optimización de Apache:** Mejora el rendimiento de Apache para trabajar de forma más eficiente con CCC.

### 📦 Servidores de Medios

Puedes redirigir parte del tráfico (como imágenes y videos) a otros servidores, por ejemplo, a través de una CDN (Red de Entrega de Contenido). Aquí se explica cómo hacerlo:

1. Regístrate en un host especializado en CDN (Akamai, Amazon AWS CloudFront, CloudFlare, entre otros).
2. Copia tus archivos de medios al servidor de ese host.
3. Asegúrate de que las carpetas `/img`, `/themes` y `/modules` estén sincronizadas con tu servidor CDN.

Agrega la URL proporcionada por tu host CDN en el campo "Servidor de medios #1" de la configuración.

### 💾 Caché

La caché almacena versiones estáticas de tu sitio para reducir la carga del servidor y mejorar el tiempo de carga.

Tipos de caché disponibles:

* **Memcached:** Sistema de caché distribuido, ideal para múltiples servidores.
* **APC:** Alternative PHP Cache, útil para un solo servidor.
* **Xcache:** Sistema de caché específico para el servidor Lighttpd, no funciona con Apache.

## ⚙️ Administración

La página de "Administración" contiene opciones generales y configuraciones sobre cómo funciona PrestaShop. Tiene tres secciones.

### **🛠️ General**

Esta sección es para la configuración más general:

* **Comprobar automáticamente si hay actualizaciones de módulos:** Puedes pedirle a PrestaShop que revise regularmente si hay nuevas versiones de tus módulos disponibles en el sitio web de Addons. Si hay actualizaciones, la página "Módulos" mostrará un botón de "Actualizar" junto al de "Desinstalar".
* **Comprobar la dirección IP de la cookie:** Esta es una medida de seguridad adicional que permite a PrestaShop verificar que el usuario proviene de la dirección IP almacenada en la cookie de su navegador.
* **Duración de la cookie de la tienda:** Por defecto, la duración de una cookie de PrestaShop es de 480 horas (20 días). Puedes reducirla si consideras que la seguridad lo requiere.
* **Duración de la cookie del panel de administración:** De forma predeterminada, la duración de la cookie es de 480 horas (20 días). Puedes reducirla según lo que exija la seguridad.

### **📤 Cuota de carga**

Esta sección te ayuda a definir el tamaño autorizado de los archivos cargados desde tu propio equipo, no desde tus clientes. Existen tres opciones, una general y dos más específicas:

* **Tamaño máximo para archivos adjuntos:** El valor predeterminado se toma de la configuración del servidor, pero puedes reducirlo si es necesario.
* **Tamaño máximo para un producto descargable:** Si vendes productos virtuales (servicios, reservas, productos descargables), esta configuración puede limitar el tamaño de los archivos que puedes cargar.
* **Tamaño máximo para la imagen de un producto:** Puedes limitar el tamaño de las imágenes que tú o tu equipo pueden cargar. Esto ayuda a reducir el uso de espacio en el servidor y ancho de banda. Se recomienda no cargar imágenes mayores a 600x600 px, aproximadamente 200 kB cuando están comprimidas.

### **🔔 Notificaciones**

Las notificaciones se muestran en la parte superior de cualquier página de administración al cargarla, junto al nombre de la tienda. Te indican la cantidad de nuevos elementos desde la última vez que hiciste clic en ellas.

Al hacer clic en el icono de la campana, se abre una pequeña tabla con los distintos tipos de notificaciones.

Puedes elegir no recibir notificaciones para algunos tipos de contenido:

* **Mostrar notificaciones de nuevos pedidos:** Muestra los números, cantidades y nombres de los clientes para los pedidos recientes. Puedes abrir cualquier pedido individual o acceder a la página "Pedidos" para ver la lista completa.
* **Mostrar notificaciones de nuevos clientes:** Muestra los nombres de los clientes que se registraron desde la última vez. Puedes abrir cualquier cliente individual o acceder a la página "Clientes" para la lista completa.
* **Mostrar notificaciones de nuevos mensajes:** Muestra el correo electrónico de las personas que te enviaron un mensaje a través del formulario de contacto. Puedes abrir cualquier mensaje o acceder a la página "Atención al Cliente" para ver la lista completa.

## 📧 Correo electrónico

Tu tienda envía muchos mensajes a lo largo de los pasos de registro y realización de pedidos. Aquí podrás configurar cómo se enviarán esos mensajes y consultar los mensajes enviados.

### **✉️ Correo electrónico enviados**

En esta sección, verás un listado de todos los correos electrónicos enviados desde tu tienda, incluyendo el destinatario, la plantilla utilizada, el idioma del mensaje, el asunto del correo y la hora de envío.

### **🔧 Configuración del correo electrónico**

Aquí podrás decidir cómo se envían y reciben los correos electrónicos. El formulario tiene tres secciones principales:

* **Enviar correo a.** Esta es una configuración del front-end. Al final del proceso de pago, los clientes pueden dejar un mensaje para tu equipo. Puedes seleccionar a quién se enviará este mensaje desde una lista desplegable. Si deseas agregar más direcciones, ve a **Parámetros de la tienda > Contactos**.
* **Parámetros del correo electrónico:** Configura cómo se envían técnicamente los correos electrónicos. Hay tres opciones disponibles; consulta más abajo para más detalles.
* **Formato del correo electrónico:** Establece cómo se verán visualmente los correos electrónicos. Puedes elegir entre tres opciones. Más información más abajo.
* **Registrar correos electrónicos.** Si desactivas esta opción, ya no se hará un seguimiento de los correos electrónicos enviados, como se muestra en la sección anterior.

### **🛠️ Configuración técnica**

Configura PrestaShop para enviar correos electrónicos a tus clientes. Es recomendable que consultes con tu proveedor de alojamiento web para determinar qué configuraciones utilizar. Las opciones son:

* **Nunca enviar correos electrónicos.** Mantén esta opción solo para pruebas. No debe usarse una vez que la tienda esté en producción.
* **Usar la función mail() de PHP.** Esta es la opción recomendada por defecto. Si no funciona, puedes utilizar la opción SMTP que se describe a continuación.
* **Configurar mis propios parámetros SMTP.** En este caso, aparecerán más campos para completar. Los detalles para estos campos te los proporcionará tu proveedor de alojamiento web, como el servidor SMTP, usuario y contraseña.

Los detalles para configurar el SMTP pueden ser proporcionados por:

* Tu administrador de sistemas,
* Tu proveedor de alojamiento,
* Tu ISP (Proveedor de servicios de Internet),
* Tu proveedor de correo electrónico.

Por ejemplo, si usas Gmail, la configuración podría ser la siguiente:

* **Servidor SMTP:** smtp.gmail.com
* **Usuario:** my.user.name@gmail.com
* **Contraseña:** RT22UE87
* **Encriptación:** SSL
* **Puerto:** 465

### **👀 Configuración visual**

Existen dos formatos disponibles para los correos electrónicos:

* **HTML:** Ideal para una visualización más atractiva, aunque no siempre funciona en todas las plataformas.
* **Texto:** Más simple visualmente, pero es compatible con todos los dispositivos.

Puedes elegir entre usar solo uno de los dos formatos o ambos, siendo recomendable usar ambos para garantizar la mayor compatibilidad.

### **🛡️ Usar firmas DKIM para los correos electrónicos**

Las firmas DKIM son firmas digitales invisibles que se insertan en los encabezados de los correos electrónicos, permitiendo verificar su autenticidad y evitando el phishing. Esto también reduce la posibilidad de que tus correos sean marcados como spam.

Puedes habilitar la firma DKIM desde **Parámetros Avanzados > Correo electrónico**. Al activarla, aparecerá un formulario con los campos para el dominio DKIM, selector DKIM y clave privada DKIM. Completa estos campos y guarda la configuración.

### **📨 Prueba tu configuración de correo electrónico**

Una vez que hayas configurado los correos electrónicos, ingresa tu propia dirección de correo electrónico en esta sección y haz clic en "Enviar un correo de prueba". Luego, revisa tu bandeja de entrada para verificar que el correo se haya recibido correctamente, en el formato seleccionado. Si no lo recibes, revisa y ajusta la configuración según sea necesario.

## 🛠 Importación

La página de importación facilita la carga masiva de productos en tu catálogo o el traspaso de datos desde otra plataforma de comercio electrónico. Es útil tanto para grandes catálogos como para transferencias de datos previamente exportados.

Históricamente, las importaciones en PrestaShop se realizaban con archivos .CSV. A partir de la versión 1.7, también se aceptan otros formatos como .xls, .xlsx, .xlst, .ods y .ots.

CSV, "Comma-separated values" (valores separados por comas), es un formato de texto plano muy utilizado para el almacenamiento, importación y exportación de datos de manera accesible y no propietaria. Muchas herramientas de gestión de datos admiten CSV en diversas versiones. Puedes conocer más sobre el formato CSV en [Wikipedia](https://es.wikipedia.org/wiki/Valores_separados_por_comas).

### 🔄 El proceso de importación

La importación requiere cierta preparación y comienza con un formulario que contiene las configuraciones principales:

* **¿Qué deseas importar?** Selecciona en el menú desplegable el tipo de entidad que deseas cargar en tu tienda. Los "Campos disponibles" a la derecha se actualizarán según la entidad elegida, para mostrar los datos requeridos en el archivo.
    * Datos importables: Categorías, Productos, Combinaciones, Clientes, Direcciones, Marcas, Proveedores, Alias, Órdenes de suministro y Detalles de órdenes de suministro (estos dos últimos solo si está activa la gestión avanzada de stock), y Contactos de la tienda.
* **Seleccionar archivo para importar:** Es posible importar varios archivos a la vez, siempre que contengan el mismo tipo de datos. Puedes subir archivos desde tu equipo o seleccionar archivos disponibles en tu FTP o historial.
* **Descargar archivos CSV de ejemplo:** Descarga ejemplos para cada tipo de datos en esta sección y compáralos con tus propios archivos para garantizar que están en el formato adecuado. Estos archivos se encuentran en /docs/csv_import en la instalación de PrestaShop.
* **Idioma del archivo:** Cada importación se realiza para un solo idioma a la vez. Si tienes datos en varios idiomas, divídelos en archivos separados.
* **Separador de campos:** Indica el delimitador de campos utilizado en el archivo (coma, tabulación, punto y coma, etc.).
* **Separador de valores múltiples:** Cuando un campo puede tener múltiples valores, deben estar separados por el delimitador específico que indiques aquí.
* **Eliminar todo \_\_\_ antes de importar:** Esta opción eliminará las entradas preexistentes del tipo de datos que estás importando, permitiéndote comenzar de cero.
* **Usar referencia de producto como clave:** Solo para productos. Puedes optar por usar la referencia del producto como ID, en lugar de la clave generada por PrestaShop. En este caso, asegúrate de que todos los productos tengan referencia en el archivo.
* **Saltar regeneración de miniaturas:** Solo para categorías y productos. Permite que PrestaShop no regenere miniaturas vinculadas desde el archivo CSV.
* **Forzar todos los números de ID:** Decide si quieres conservar los IDs originales o permitir que el importador los incremente automáticamente.
* **Enviar correo de notificación:** Activa esta opción para recibir un correo una vez completada la importación en caso de que el archivo sea grande.

Cada vez que cambies la entidad a importar, "Campos disponibles" mostrará los campos de datos necesarios para esa entidad. Aunque la herramienta de importación ayuda a mapear tus campos, organizar los datos en el orden y formato requeridos facilitará el proceso de importación.

Algunos campos tienen un icono de información ("i") que puedes consultar para obtener detalles útiles, especialmente para las configuraciones multitienda o de gestión avanzada de stock.

### 📄 Formato de los datos

El archivo debe ser de texto y con extensión .csv. Se recomienda utilizar un punto y coma (";") como delimitador de campos. Si los textos de tu archivo (como las descripciones) contienen punto y coma, elimínalos o selecciona otro delimitador en "Separador de campos".

Se pueden crear archivos CSV con cualquier editor de texto, aunque usar una hoja de cálculo facilita el trabajo visual y de organización. Opciones populares incluyen Microsoft Excel (comercial) y OpenOffice.org Calc (gratuito).

### 📂 Ejemplo de archivo de importación

Aquí se muestra un archivo de ejemplo para la importación de productos:

"Enabled";"Name";"Categories";"Price";"Tax rule ID";"Buying price";"On sale";"Reference";"Weight";"Quantity";"Short desc.";"Long desc.";"Images URL"
1;"Test";"1,2,3";130;1;75;0;"PROD-TEST";"0.500";10;"Descripción breve";"Descripción larga";"https://www.ejemplo.com/images/product1.gif"


**Notas:**
- La columna de precios usará la moneda predeterminada de tu tienda.
- Las categorías deben ser IDs existentes, separadas por comas.
- La URL de imagen debe ser un enlace absoluto.
- La codificación debe ser UTF-8 o ISO-8859-1.
- Fechas en formato ISO 8601: `2013-06-21 15:07:27`.

### 🚀 Subida del archivo

Carga tus archivos CSV mediante:

1. **Navegador:** Selecciona el archivo en "Subir" y confirma. Repite para cada archivo necesario.
2. **Cliente FTP:** Sube archivos a /admin-dev/import en tu instalación de PrestaShop, luego recarga la página de importación.

Selecciona el archivo y define el tipo de datos en "¿Qué deseas importar?". A continuación, ajusta el idioma, los delimitadores y selecciona si deseas borrar los productos antes de importar. Presiona "Siguiente paso" para continuar.

### 🗺 Herramienta de mapeo de datos

Al hacer clic en "Siguiente paso", la página muestra la herramienta de mapeo para ajustar tus columnas al formato de PrestaShop. Asegúrate de alinear correctamente las columnas usando los selectores de encabezados para que los datos se importen sin errores.

Si usaste la primera fila para nombres de columnas, ingresa "1" en "Filas a omitir" para evitar que se importen. Al finalizar el mapeo, haz clic en "Importar" para iniciar la importación y ver el progreso.

### 🔧 Configuraciones de Mapeo

El mapeo puede guardarse y reutilizarse en futuras importaciones. En la parte superior de la herramienta, podrás:

- **Guardar:** Ingresa un nombre y selecciona "Guardar".
- **Cargar:** Elige una configuración guardada y selecciona "Cargar".
- **Eliminar:** Selecciona y elimina configuraciones de mapeo innecesarias.

### 📊 Importación de Características con Excel

Excel no permite definir delimitadores personalizados, así que ten cuidado con los campos "irregulares" como las Características en Productos. Usa el formato `nombrecaracterística:valor:posición:valorpersonalizado`, separado por comas para múltiples características.

Ejemplo: `Nombre:Ingredientes:1:0,Nombre:Origen::1`

* **nombrecaracterística:** Nombre exacto de la característica.
* **valor:** Valor específico de la característica.
* **posición:** Ubicación relativa en la lista.
* **valorpersonalizado:** 1 si es un valor personalizado, 0 si es un valor estándar.

## 👥 Equipo

Ya sea que estés gestionando tu tienda en solitario o tengas un negocio en expansión con empleados, en algún momento tendrás que permitir que otros accedan a tu tienda para realizar diversas tareas. Podrías necesitar ayuda para gestionar pedidos, soporte técnico, trabajo de traducción, etc.

Cuando otorgues acceso a alguien, asegúrate de crear una cuenta específica para esa persona (¡nunca compartas tus credenciales!) y asigna permisos adecuados para sus tareas. Las opciones de configuración del equipo te permitirán hacer esto de manera segura.

Este capítulo contiene las siguientes secciones:

* **Empleados**
* **Perfiles**
* **Permisos**

### 👷 Empleados

La página de administración "Empleados" lista todas las cuentas de usuario con acceso al back office de la tienda. Inicialmente, encontrarás la cuenta creada durante la instalación, configurada automáticamente como SuperAdmin, que tiene acceso total a todas las funciones de PrestaShop.

Para gestionar adecuadamente, crea una cuenta de empleado única para cada persona que colabore en tu tienda. Evita cuentas de uso compartido, ya que esto impide identificar quién hizo qué. Cada empleado debe tener su cuenta personal para garantizar una gestión responsable de tu tienda.

#### ➕ Agregar un nuevo empleado

Haz clic en "Agregar nuevo empleado" para abrir el formulario de creación de cuenta. Los campos del formulario incluyen:

* **Nombre y Apellido**: Estos datos no son visibles para los clientes, pero te ayudarán a identificar quién realiza cambios.
* **Correo electrónico**: Dirección que también sirve como identificador de inicio de sesión. Si está habilitado, este correo recibirá notificaciones de clientes y de PrestaShop.
* **Contraseña**: Asegúrate de que no sea fácil de adivinar. La seguridad de la cuenta es esencial.
* **Suscribirse al boletín**: Permite recibir noticias y consejos de comercio electrónico de PrestaShop.
* **Página predeterminada**: Define la página inicial para el usuario al iniciar sesión, como la página de Estadísticas para un SuperAdmin o Pedidos para vendedores.
* **Idioma**: Elige el idioma de preferencia para el usuario, útil en equipos multilingües. Puedes agregar idiomas en "Internacional" > "Traducciones".
* **Activo**: Activa o desactiva temporalmente una cuenta según sea necesario.
* **Perfil de permisos**: Selecciona un perfil para asignar los derechos de acceso adecuados. Esto controla a qué secciones del back office puede acceder el empleado. Consulta los perfiles existentes en "Perfiles" y elige uno adecuado.
* **Avatar**: La imagen de perfil se vincula a la cuenta del foro de PrestaShop. Personalízala registrándote en [http://www.prestashop.com/forums/](http://www.prestashop.com/forums/).

#### ⚙️ Opciones de empleados

En la parte inferior de la página "Empleados" encontrarás dos opciones adicionales:

* **Regeneración de contraseña**: Define la frecuencia permitida para cambios de contraseña.
* **Memorizar idioma de formularios**: Al activar esta opción, los empleados pueden mantener su idioma preferido para los formularios del panel de administración.

### 🔑 Perfiles

PrestaShop permite asignar derechos y permisos específicos a cada perfil de empleado para controlar el acceso. Por ejemplo, un administrador tiene acceso completo, mientras que un empleado puede tener acceso solo a la gestión de pedidos.

#### Perfiles predeterminados

PrestaShop ofrece 4 perfiles predefinidos:

* **SuperAdmin**: Acceso total sin restricciones.
* **Logístico**: Acceso a pedidos, envíos, gestión de stock y parte del catálogo.
* **Traductor**: Permiso para traducir contenido, con acceso a productos, categorías y la página de "Traducciones".
* **Vendedor**: Acceso a clientes, módulos y estadísticas, además de las secciones disponibles para Traductor.

Para revisar los permisos de cada perfil, consulta la página "Permisos". 

> **Nota:** El perfil SuperAdmin no puede eliminarse, solo renombrarse, y siempre debe existir al menos una cuenta SuperAdmin.

#### ➕ Agregar un nuevo perfil

Puedes crear perfiles personalizados según las necesidades. Para agregar uno:

1. Haz clic en "Agregar nuevo perfil" e introduce un nombre único.
2. Una vez guardado, ve a la página "Permisos" para asignar derechos al nuevo perfil.

### 🔒 Permisos

Los permisos son la clave para gestionar el acceso en tu tienda. Cada perfil tiene un conjunto de permisos que puedes ajustar en la página de administración "Permisos".

#### Configuración de Permisos

La página "Permisos" está organizada en pestañas:

* **Pestañas de perfiles**: A la izquierda, cada perfil tiene una pestaña.
* **Opciones de permisos**: A la derecha, los permisos de cada perfil se dividen en dos secciones.

Para cada perfil (excepto SuperAdmin), podrás ver dos tablas:

* **Permisos de menú**: Configura lo que el perfil puede ver o hacer con los menús, como ocultar o restringir funciones de edición.
* **Permisos de módulos**: Puedes permitir o restringir el acceso a la configuración de módulos clave.

##### Opciones de permisos

* **Ver**: Permite ver la información.
* **Agregar**: Permite agregar nueva información.
* **Editar**: Permite modificar la información.
* **Eliminar**: Permite eliminar información.
* **Todo**: Habilita todas las opciones anteriores para el criterio.

Los módulos tienen tres permisos específicos:

* **Ver**: Permite ver la configuración.
* **Configurar**: Permite modificar la configuración del módulo.
* **Desinstalar**: Permite desinstalar el módulo.

> **Importante:** Los permisos del perfil SuperAdmin no pueden modificarse; este perfil siempre tiene todos los derechos.

#### 📋 Configurar permisos para un nuevo perfil

Para crear un perfil como "Preparador de pedidos":

1. Crea el perfil en "Perfiles".
2. Ve a "Permisos" y ajusta los derechos según el nivel de acceso deseado.

> **Consejo:** Puedes asignar permisos en bloque, por columna o fila, para agilizar el proceso. PrestaShop guarda automáticamente los cambios realizados en permisos, evitando así la pérdida de configuraciones.

Una vez configurado el perfil, asigna el nuevo perfil a los empleados necesarios desde la página de administración de "Empleados".

## 🗃️ Base de datos

El menú de la base de datos contiene las herramientas necesarias para gestionar tu base de datos, incluyendo el Gestor SQL y la opción de Respaldo de Base de Datos. Estas herramientas son especialmente útiles para usuarios avanzados que necesiten realizar tareas complejas.

Este capítulo está compuesto por las siguientes secciones:

*   Gestor SQL
*   Respaldo de Base de Datos

### 🖥️ Gestor SQL

El Gestor SQL es una herramienta avanzada que debería ser utilizada por usuarios con conocimientos técnicos en SQL. Su potencia radica en la capacidad de ejecutar consultas SQL directamente sobre la base de datos de PrestaShop, permitiendo personalizar y extraer datos de manera más precisa que con la interfaz estándar de PrestaShop.

Con esta herramienta, puedes realizar consultas complejas, como obtener un listado actualizado de los clientes suscritos a tu boletín o exportar productos en formato CSV o HTML. Es ideal para quienes necesiten acceder a los datos de forma cruda y detallada.

Es importante recordar que, por motivos de seguridad, ciertas acciones están restringidas, como actualizaciones de datos (UPDATE), eliminaciones (DELETE), o la creación de nuevas tablas (CREATE TABLE). De esta manera, solo se permite leer los datos con consultas SELECT.

Las contraseñas y claves seguras están ocultas por razones de seguridad.

#### ➕ Crear una nueva consulta

Para crear una nueva consulta SQL, haz clic en "Añadir nueva consulta SQL". El formulario que aparece te pide dos datos principales:

*   **Nombre de la consulta SQL:** Aquí puedes poner un nombre descriptivo para tu consulta.
*   **Consulta SQL:** Introduce la consulta SQL que deseas ejecutar. Puedes incluir comandos complejos como JOINs.

La sección "Lista de tablas MySQL" te permitirá explorar fácilmente las tablas disponibles en la base de datos. Selecciona una tabla y PrestaShop te mostrará sus atributos, que puedes agregar a tu consulta con el botón "Añadir atributo a la consulta SQL".

Una vez guardada la consulta, regresarás a la página principal con la lista de consultas guardadas.

#### ▶️ Ejecutar una consulta

Cada consulta guardada se presenta en una tabla con cuatro íconos a la derecha:

*   **Exportar:** Ejecuta la consulta y la descarga en formato CSV.
*   **Ver:** Muestra los resultados de la consulta en una tabla HTML dentro de la interfaz de PrestaShop.
*   **Editar:** Permite modificar la consulta para mejorarla o refinarla.
*   **Eliminar:** Elimina una consulta que ya no sea útil o no funcione correctamente.

#### ⚙️ Ajustes

Actualmente, solo hay una opción de configuración disponible:

*   **Selecciona la codificación de archivo predeterminada:** Configura la codificación para los archivos CSV descargados. Se recomienda UTF-8, pero puedes elegir ISO-8859-1 si lo prefieres.

#### 📝 Algunos ejemplos de consultas

A continuación, se presentan ejemplos de consultas SQL para que puedas utilizarlas o adaptarlas:

*   **Listado de todos los correos electrónicos de los clientes:**  
    `SELECT email FROM ps_customer`
*   **Listado de los correos electrónicos de los clientes suscritos al boletín:**  
    `SELECT email FROM ps_customer WHERE newsletter = 1`
*   **Listado de productos activos con descripción en francés (id_lang = 4):**  
    `SELECT p.id_product, pl.name, pl.link_rewrite, pl.description FROM ps_product p LEFT JOIN ps_product_lang pl ON (p.id_product = pl.id_product) WHERE p.active = 1 AND pl.id_lang = 4`
*   **Listado de pedidos, con detalles sobre transportista, moneda, pago, total y fecha:**  
    `SELECT o.id_order AS id, CONCAT(LEFT(c.firstname, 1), '. ', c.lastname) AS Customer, ca.name AS Carrier, cu.name AS Currency, o.payment, CONCAT(o.total_paid_real, ' ', cu.sign) AS Total, o.date_add AS Date FROM ps_orders o LEFT JOIN ps_customer c ON (o.id_customer = c.id_customer) LEFT JOIN ps_carrier ca ON (o.id_carrier = ca.id_carrier) LEFT JOIN ps_currency cu ON (o.id_currency = cu.id_currency)`

### 💾 Respaldo de Base de Datos

El respaldo de la base de datos implica guardar una copia de la información contenida en tu base de datos en archivos que se almacenan en un lugar seguro. Esto es crucial para restaurar tu tienda en caso de fallos.

Es fundamental hacer respaldos regulares de la base de datos, ya que contiene la mayoría de la información vital de tu tienda, como productos, categorías y clientes. Sin embargo, las imágenes y archivos del tema se almacenan en el servidor y no se incluyen en el respaldo.

Es recomendable realizar respaldos semanalmente como mínimo.

Para respaldar tu base de datos, puedes utilizar herramientas como phpMyAdmin o la opción integrada en PrestaShop: la página de "Respaldo de BD".

La página de Respaldo de Base de Datos contiene dos grandes secciones informativas:

*   **Descargo de responsabilidad:** Un recordatorio sobre la importancia de realizar respaldos, con un botón al final que debes presionar para iniciar el respaldo. Tras completar el respaldo, podrás descargar el archivo desde la nueva "Sección de descarga".
*   **Cómo restaurar:** Te proporciona instrucciones detalladas sobre cómo restaurar la base de datos en caso de fallos. Asegúrate de guardar esta información en un lugar seguro, ya que podría ser necesario en situaciones de emergencia.

#### 🔄 Cómo restaurar un respaldo de base de datos en 10 sencillos pasos

1.  Configura "Habilitar tienda" en "No" en la página de "Mantenimiento" en el menú "Preferencias".
2.  Descarga el respaldo desde la lista o desde tu servidor FTP (en la carpeta "admin/backups").
3.  Verifica la integridad del archivo de respaldo: busca errores y asegúrate de que todos los archivos estén completos.
4.  Solicita acceso a "phpMyAdmin" desde tu proveedor de hosting.
5.  Conéctate a "phpMyAdmin" y selecciona tu base de datos actual.
6.  Elimina todas las tablas de la base de datos actual, a menos que hayas habilitado la opción "Eliminar tablas existentes".
7.  En "phpMyAdmin", selecciona la pestaña "Importar".
8.  Haz clic en "Examinar" y selecciona el archivo de respaldo.
9.  Asegúrate de que el tamaño del archivo no exceda el límite permitido (por ejemplo, 16MB).
10.  Haz clic en "Continuar" y espera a que se complete el proceso de importación.

#### 🗂️ Acciones disponibles en la lista de respaldos

La lista de respaldos muestra todos los respaldos realizados, con información sobre la fecha de creación, edad, nombre del archivo y tamaño.

*   **Ver:** Permite descargar el archivo de respaldo.
*   **Eliminar:** Elimina el archivo de respaldo. Ten cuidado, ya que esta acción no se puede deshacer.

Después de realizar un respaldo, descarga el archivo generado y guárdalo en un lugar seguro. También puedes encontrar los respaldos en tu servidor, dentro de la carpeta /backup, bajo la carpeta /admin.

El respaldo de la base de datos se guarda en formato SQL con extensión .sql, y se comprime utilizando el algoritmo BZip2, lo que da como resultado un archivo con extensión .sql.bz2.

#### ⚙️ Opciones de Respaldo

En la parte inferior de la página, hay dos opciones de configuración:

*   **Ignorar tablas de estadísticas:** PrestaShop almacena estadísticas en algunas tablas que pueden hacer que el archivo de respaldo sea muy grande. Si tienes poco espacio en disco, puedes desmarcar esta opción para excluirlas.
*   **Eliminar tablas existentes durante la importación:** Si se habilita, esta opción eliminará todas las tablas antes de importar los datos del respaldo, lo que puede evitar duplicados. Está habilitada por defecto.

## 📜 Registros (logs)

Los errores pueden ocurrir en cualquier momento. A menudo, PrestaShop los maneja sin que te des cuenta, pero puede ser útil revisarlos para corregir problemas comunes y mejorar la estabilidad de tu tienda.

La página **Registros** muestra todas las acciones realizadas en tu tienda, permitiéndote ver los errores PHP que podrían afectarla. Estos errores se presentan en una tabla central con cuatro niveles de gravedad:

* **1:** Solo informativo. Son avisos durante la ejecución del código que indican algo que podría señalar un problema, pero también podría ser parte del funcionamiento normal del script.
* **2:** Advertencia. Errores no fatales que no interrumpen la ejecución del script.
* **3:** Error. Indica un error que puede afectar la funcionalidad, pero no detiene el script.
* **4:** Problema mayor (¡fallo!). Errores fatales que interrumpen la ejecución del script, como problemas de memoria.

Estos niveles se basan en las categorías oficiales del manual de PHP. [Más información en el manual de PHP](http://www.php.net/manual/en/errorfunc.constants.php).

### 📧 Registros por correo electrónico

Los niveles de error también se utilizan para la función de **Registros por correo electrónico**. PrestaShop introduce un valor adicional, el **5**, que significa que el administrador no desea recibir ninguna notificación, ni de errores menores ni mayores.

Esta herramienta te permite configurar notificaciones por correo electrónico cuando se produce un error. Los correos electrónicos se enviarán a la dirección del propietario de la tienda, y puedes elegir el nivel de importancia para recibir estos correos:

* **"1":** Para recibir notificaciones de todos los errores, incluso los menores.
* **"3":** Solo para recibir notificaciones sobre errores y problemas mayores.
* **"4":** Para recibir solo notificaciones de problemas mayores.
* **"5":** El valor predeterminado, que significa que no recibirás notificaciones de ningún tipo.

## 🌐 Servicio Web

En esta página, puedes habilitar el servicio web de tu tienda para permitir que herramientas de terceros accedan a tus datos. Esto facilita el uso de aplicaciones que pueden mejorar la experiencia de tus clientes o ayudarte en la gestión de la tienda (como aplicaciones móviles).

Un **servicio web** es un método de comunicación entre dos dispositivos electrónicos a través de una red. Utiliza un conjunto de métodos, formatos y derechos de acceso para que el contenido del servicio web pueda ser utilizado por otras herramientas autorizadas y expandir el contenido original. [Más información en Wikipedia](https://es.wikipedia.org/wiki/Servicio_web).

La página muestra una lista de las claves de servicio web existentes en tu tienda, si es que ya hay alguna. **Una clave de servicio web** es un acceso único que se otorga a un desarrollador para vincular una herramienta a tu tienda. Comparte estas claves con precaución, ya que no siempre querrás que todas las herramientas tengan acceso a tus datos.

No todas las aplicaciones pueden acceder a tu tienda a través del servicio web de PrestaShop: tú decides qué aplicaciones pueden acceder y qué permisos tienen. Cada aplicación tiene una clave única con derechos de acceso específicos.

### ➕ Agregar una nueva clave

Al hacer clic en el botón **"Agregar nueva clave de servicio web"**, serás redirigido a un formulario donde podrás crear una clave de servicio web:

* **Clave:** Una clave única. Puedes crear una personalizada o usar una generada, por ejemplo, haciendo clic en el botón "¡Generar!" o utilizando un generador de claves en línea. Las claves generadas son más seguras porque son más difíciles de adivinar.
* **Descripción de la clave:** Un recordatorio de quién es esa clave y qué tipo de acceso otorga.
* **Estado:** Puedes desactivar una clave en cualquier momento. Esto permite otorgar acceso temporalmente a través de una clave específica.
* **Permisos:** No es necesario compartir todos tus datos con cada clave. Puedes elegir entre una variedad de permisos, ya sea por sección o por tipo de acceso. Tal vez quieras que algunas aplicaciones solo puedan ver ciertos elementos, mientras que otras (como las que gestionan la tienda remotamente) puedan editar y eliminar casi todo. Elige con cuidado.

Haz clic en **"Guardar"** cuando tu clave esté lista.

### ⚙️ Configuración

Por razones de seguridad, asegúrate de que el servidor de tu tienda sea compatible con conexiones seguras SSL.

La configuración del servicio web es sencilla:

* **Habilitar el servicio web de PrestaShop:** Si prefieres no permitir el acceso a tu tienda a través de herramientas y aplicaciones externas, simplemente mantenlo deshabilitado.
* **Habilitar el modo CGI para PHP:** El modo CGI es una configuración especial para el servidor Apache que le dice que use PHP como un script CGI en lugar de un módulo de Apache. Aunque el modo CGI es más seguro, se han encontrado vulnerabilidades de seguridad (como una en mayo de 2012). Consulta con tu proveedor de hosting para recibir más orientación.

### 🌍 Habilitar el servicio web de PrestaShop

Al habilitar el servicio web de PrestaShop, el estado y la URL del servicio web de tu tienda se mostrarán en la parte superior de la página en **Parámetros avanzados > servicio web > Estado del servicio web**. Esta información es útil para solucionar problemas comunes.

### 🔄 Realizar actualizaciones parciales

Puedes realizar actualizaciones parciales en los endpoints del servicio web utilizando el método **PATCH**. Esto permite que las integraciones actualicen solo una parte de un recurso, en lugar de actualizar todos los campos a la vez.

## 🛍️ Multitienda

Esta página solo está disponible cuando habilitas la función **multitienda**.

Convertir tu instalación de PrestaShop de una tienda única a una **multitienda** es muy sencillo:

1. Ve al menú **"Parámetros de la tienda"** y selecciona la página **"General"**.
2. Busca la opción **"Habilitar multitienda"** y selecciona **"Sí"**.
3. Guarda los cambios.

El menú **"Parámetros avanzados"** ahora incluirá la página **"Multitienda"**, que se detalla en el capítulo "[Gestionando múltiples tiendas](#)" de esta guía.

## ⚙️ Características Experimentales

Habilitar una característica experimental te permite probar una nueva función en desarrollo antes de su lanzamiento oficial.

Las **características experimentales** (también conocidas como "banderas de características") están dirigidas a usuarios experimentados y aventureros, que desean probar una función que aún no es lo suficientemente estable para su uso general. Aunque puede sonar emocionante, debes ser consciente de los riesgos de tales experimentos:

* Las características experimentales todavía están en desarrollo. Habilitarlas podría tener consecuencias imprevistas y causar la pérdida de datos.
* En cualquier caso, **nunca experimentes en un entorno de producción**.

### Habilitar la página experimental de productos

La página experimental de productos está disponible en PrestaShop 1.7.8. Esta página mejora el rendimiento e incluye nuevas características como un nuevo sistema de gestión de combinaciones. Está en progreso y algunas funciones aún no están disponibles.

Para hacer visible la página experimental de productos en tu back office, habilita la característica en **"Parámetros avanzados"** > **"Características experimentales"** y guarda.

Luego, ve a **"Catálogo"** > **"Productos"**. Deberías notar algunos cambios, específicamente un nuevo botón: **"Nuevo producto en página experimental"**. Haz clic en él para abrir la página experimental de productos.

También puedes editar un producto existente en la página experimental, seleccionando esta opción en el menú desplegable en la columna de **Acciones** del listado de productos.

### Nuevas características experimentales (PrestaShop 8.1)

PrestaShop 8.1 presenta una nueva página de productos reestructurada.

Para usar esta nueva página de productos, debes habilitarla en la página de **"Noticias y características experimentales"** de PrestaShop 8.1.

## 🔒 Seguridad

### Protección de tokens en el back office

La protección de tokens ayuda a asegurar el acceso a tu back office utilizando tokens.

### Configurar la política de contraseñas y el indicador de fuerza de la contraseña

El menú de **política de contraseñas** te permite configurar la política de contraseñas de tu tienda, eligiendo entre 5 niveles crecientes de complejidad. Esto te permitirá decidir qué tan estricta quieres ser con las contraseñas de los usuarios.

Las contraseñas se califican de 0 (Extremadamente adivinables) a 4 (Muy difíciles de adivinar) según su puntaje de seguridad. La longitud mínima y máxima de las contraseñas puede ser configurada manualmente.

Al crear una cuenta, los usuarios del **front office** reciben indicaciones en tiempo real sobre la fortaleza de la contraseña elegida, de acuerdo con la política de contraseñas del back office. Una indicación codificada por colores, así como un tooltip, les ayudará a entender si su contraseña es lo suficientemente fuerte.

**Nota:** Los temas deben ser actualizados para soportar esta función. Ver: Tu tema actual.

#### Tabla de colores de indicación

| Color   | Longitud de la Contraseña      | Fuerza de la Contraseña    |
|---------|-------------------------------|----------------------------|
| 🟥      | No es lo suficientemente larga | No es lo suficientemente fuerte |
| 🟧      | No es lo suficientemente larga | Fuerte                     |
| 🟩      | Buena                         | Fuerte                     |

**Ejemplos:**

- Un ejemplo de una contraseña **débil** (🟥,🟧)
- Un ejemplo de una contraseña **fuerte** (🟩)

### Gestionar las sesiones de empleados y clientes

Estas pestañas te permiten gestionar las sesiones de empleados y clientes. Para eliminar una sesión y desconectar al usuario, haz clic en el botón de eliminar en la columna de **Acciones**.

Para acceder al back office, el empleado o cliente deberá iniciar sesión nuevamente usando su correo electrónico y contraseña.

#### Pestaña de Sesiones de Empleados

La pestaña de **sesiones de empleados** te permite gestionar las sesiones de los empleados.

#### Pestaña de Sesiones de Clientes

La pestaña de **sesiones de clientes** te permite gestionar las sesiones de los clientes.

#### Eliminar sesiones obsoletas

El botón **"Eliminar"** te permite eliminar manualmente las sesiones obsoletas para reducir el desorden en la base de datos.

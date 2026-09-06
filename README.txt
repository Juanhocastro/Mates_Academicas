============================================================
 MATEMÁTICAS ACADÉMICAS 4º ESO
 C.E.I.P.S. Santo Domingo (Algete)
 Sitio web de apuntes y ejercicios — Instrucciones de subida
============================================================

Este paquete contiene un sitio web estático (HTML, CSS, imágenes y PDF)
listo para copiarse directamente dentro de la carpeta "public_html" de
tu alojamiento en EducaMadrid. No requiere instalación, base de datos
ni ningún programa especial en el servidor.

------------------------------------------------------------
1. CONTENIDO DEL ZIP
------------------------------------------------------------
index.html              -> Portada + menú principal (página de inicio)
bloque-a.html … f.html  -> Páginas de cada bloque temático
ampliacion.html         -> Página de Ampliación (Derivadas)
indice.html             -> Índice completo de PDF descargables
programacion.html       -> Programación curricular y fuentes oficiales
css/                    -> Hojas de estilo del sitio
js/                     -> Script del menú en móvil
assets/img/             -> Logotipo y fotografías
assets/pdf/             -> Los 22 PDF (11 apuntes + 11 boletines de ejercicios)

Todas las rutas del sitio son relativas, así que puedes subir la
carpeta completa a la raíz de tu alojamiento sin modificar nada.

------------------------------------------------------------
2. QUÉ NECESITAS ANTES DE EMPEZAR
------------------------------------------------------------
- Un cliente FTP. Recomendado: FileZilla (gratuito) → https://filezilla-project.org/
- Los datos de conexión FTP de tu alojamiento en EducaMadrid:
    · Servidor (Host):   lo facilita EducaMadrid al activar tu web de centro
                          (normalmente algo como ftp.educa.madrid.org
                          o una IP concreta que te asignan)
    · Usuario:            tu usuario de centro/gestor web de EducaMadrid
    · Contraseña:         tu contraseña de EducaMadrid
    · Puerto:             21 (FTP estándar) — si EducaMadrid indica SFTP,
                          usa el puerto 22 y selecciona "SFTP" en FileZilla

Si no conoces estos datos, pídelos en la sección de "Gestión web" o
"Alojamiento web" del panel de tu centro en EducaMadrid, o contacta
con el coordinador TIC del centro.

------------------------------------------------------------
3. PASOS PARA SUBIR EL SITIO CON FILEZILLA
------------------------------------------------------------
1. Descomprime este archivo ZIP en tu ordenador. Debes obtener una
   carpeta con index.html, css/, js/ y assets/ dentro.

2. Abre FileZilla.

3. En la barra superior, introduce:
     Servidor:    (el host FTP de EducaMadrid)
     Nombre de usuario: (tu usuario)
     Contraseña:  (tu contraseña)
     Puerto:      21 (o 22 si es SFTP)
   Pulsa "Conexión rápida".

4. En el panel de la IZQUIERDA (tu ordenador), navega hasta la carpeta
   donde descomprimiste el sitio.

5. En el panel de la DERECHA (servidor remoto), entra en la carpeta
   "public_html" (o "www", según cómo la llame tu alojamiento).

   IMPORTANTE: el archivo index.html debe quedar directamente dentro
   de "public_html", NO dentro de una subcarpeta. Es decir, la
   estructura en el servidor debe quedar así:

     public_html/
       ├── index.html
       ├── bloque-a.html
       ├── ...
       ├── css/
       ├── js/
       └── assets/

6. Selecciona TODOS los archivos y carpetas del panel izquierdo
   (index.html, bloque-*.html, ampliacion.html, indice.html,
   programacion.html, css, js, assets) y arrástralos al panel derecho,
   dentro de "public_html".

7. Espera a que termine la transferencia (son unos 10 MB en total,
   principalmente por los PDF y las fotografías). FileZilla mostrará
   una barra de progreso y la cola de archivos pendientes.

8. Cuando termine, comprueba que no hay ningún archivo en rojo o con
   error en la cola de transferencia (parte inferior de FileZilla).

------------------------------------------------------------
4. COMPROBAR QUE FUNCIONA
------------------------------------------------------------
1. Abre un navegador y entra en la dirección web de tu centro en
   EducaMadrid (la misma que usarías para ver la web del centro).

2. Debe cargar la portada "Matemáticas Académicas · 4º ESO" con el
   logotipo y el menú de 6 bloques + Ampliación.

3. Pincha en un bloque (por ejemplo, "Ir a Medida") y comprueba que
   los botones "Apuntes" y "Ejercicios" descargan el PDF correcto.

4. Repite la comprobación desde el móvil, ya que el sitio se adapta
   automáticamente a pantallas pequeñas.

------------------------------------------------------------
5. TODOS LOS TEMAS YA ESTÁN ACTIVOS
------------------------------------------------------------
Los 16 temas del curso y la Ampliación (Cálculo diferencial) tienen
ya sus botones de descarga de Apuntes y Ejercicios activos, tanto en
cada página de bloque como en el Índice completo de recursos PDF.

Si en el futuro necesitas SUSTITUIR el contenido de un PDF (por
ejemplo, cuando tengas la versión definitiva de un tema que hoy es
un documento provisional):
1. Genera el nuevo PDF con el MISMO nombre de archivo que el actual
   (revisa el nombre exacto en la carpeta "assets/pdf/").
2. Sube ese archivo por FTP a la carpeta "assets/pdf/" del servidor,
   sobrescribiendo el PDF antiguo. No hace falta tocar ningún HTML,
   ya que los enlaces apuntan siempre al mismo nombre de archivo.

Si en cambio quieres añadir un tema completamente nuevo que no
existía antes, guarda esta petición y podemos regenerar el sitio
completo con la nueva estructura ya integrada.

------------------------------------------------------------
6. SOPORTE
------------------------------------------------------------
Este sitio es completamente estático: no necesita PHP, bases de datos
ni ningún backend. Cualquier alojamiento web básico (incluido el de
EducaMadrid) es compatible sin configuración adicional.

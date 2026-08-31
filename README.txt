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
5. CÓMO ACTIVAR LOS TEMAS 12-16 Y LA AMPLIACIÓN EN EL FUTURO
------------------------------------------------------------
Ahora mismo los Temas 12-16 y la Ampliación (Derivadas) aparecen
marcados como "Próximamente" porque sus PDF todavía no existen.

Cuando tengas listos los apuntes y ejercicios de un tema nuevo:
1. Añade los dos PDF correspondientes (Apuntes y Ejercicios) dentro
   de la carpeta "assets/pdf/", siguiendo el mismo patrón de nombre
   que los ya existentes (por ejemplo T12_Apuntes_Nombre.pdf y
   T12_Ejercicios_Nombre.pdf).
2. En el archivo HTML del bloque correspondiente (por ejemplo
   bloque-e.html para el Tema 12), sustituye el bloque
   "⏳ Próximamente" del tema por los dos botones de descarga,
   copiando el mismo formato que usan los temas ya activos del mismo
   archivo (busca la etiqueta <div class="btn-row"> de un tema ya
   disponible y cópiala, cambiando el nombre de los archivos PDF).
3. Haz lo mismo en indice.html, en la fila correspondiente a ese
   tema, sustituyendo la etiqueta "Próximamente" por los dos enlaces
   de descarga.
4. Vuelve a subir esos archivos HTML modificados por FTP, sobrescribiendo
   los que ya están en el servidor (basta con volver a arrastrar el
   archivo concreto que has editado).

Si prefieres no editar el HTML a mano, guarda esta petición y podemos
generar de nuevo el sitio completo con los temas nuevos ya activados.

------------------------------------------------------------
6. SOPORTE
------------------------------------------------------------
Este sitio es completamente estático: no necesita PHP, bases de datos
ni ningún backend. Cualquier alojamiento web básico (incluido el de
EducaMadrid) es compatible sin configuración adicional.

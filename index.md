# Política de privacidad — Agenda

**Última actualización: 13 de agosto de 2026**

Esta política describe cómo la aplicación **Agenda** (en adelante, "la app")
trata la información del usuario. La app es desarrollada por Ivan Santiago
Torres Rincon (en adelante, "el desarrollador").

Contacto: **ivantr158@gmail.com**

## 1. Resumen

**Agenda guarda tus datos en tu dispositivo.** Todos tus datos —tareas,
contactos, subtareas, gastos, ingresos, ajustes y PIN— se almacenan en el
dispositivo. La app **no tiene servidores**: no envía tu información al
desarrollador ni a terceros, no recolecta datos, no utiliza servicios de
análisis ni publicidad, y no requiere cuenta ni registro.

La app **no se conecta a internet** para enviar ni recibir tus datos. Hay dos
excepciones acotadas, ambas bajo tu control y explicadas en detalle más
abajo:

- **Sincronización entre tus equipos (sección 5).** Si la activás, tus datos
  viajan cifrados por tu red local (Wi-Fi) entre los dispositivos que vos
  emparejaste. Nunca salen de esa red ni pasan por internet.
- **Dictado por voz (sección 4).** Lo transcribe el motor de reconocimiento
  de voz de Android, que según tu dispositivo y configuración puede procesar
  el audio en servidores de Google.

## 2. Datos que la app maneja en tu dispositivo

Los siguientes datos se guardan localmente en la base de datos del dispositivo
y sólo lo abandonan si vos los exportás manualmente o si activás la
sincronización con tus otros equipos (sección 5):

- Tareas, descripciones, fechas, horas, prioridades y categorías.
- Contactos de la app (nombre, teléfono, email, notas). Podés crearlos a mano
  o **importarlos de la libreta del sistema**, si le das el permiso
  correspondiente. Los contactos importados quedan copiados en la base local
  de la app.
- Subtareas asociadas a tus tareas.
- Gastos, ingresos, gastos fijos y variables, deudas y metas de ahorro que
  registres en la sección de Finanzas, incluidas las fotos de comprobantes que
  adjuntes (se copian al almacenamiento privado de la app) y los datos del QR
  de facturas AFIP/ARCA que escanees (fecha, importe, CUIT y número de
  comprobante).
- Listas de compras y de deseos, incluidas las imágenes que elijas para cada
  producto. Las imágenes se copian al almacenamiento privado de la app.
- Hábitos y su historial de cumplimiento.
- Ingreso mensual y meta de ahorro que vos configures.
- Estadísticas internas de uso (categorías y horarios típicos) usadas
  exclusivamente en el dispositivo para sugerencias.
- PIN de acceso (almacenado como hash PBKDF2-HMAC-SHA256 con salt aleatorio
  en el almacenamiento seguro del sistema, nunca en texto plano).

## 3. Datos que la app NO recolecta

- No identificadores publicitarios.
- No ubicación.
- No información del dispositivo más allá de lo necesario para funcionar.
- No analítica.
- No crash reporting automático en la nube.
- No publicidad ni SDK de terceros que recolecten información.
- No cuentas de usuario, correos ni contraseñas en servidores.

### Software de terceros

La app está construida con bibliotecas de código abierto. Ninguna de ellas
envía datos al desarrollador ni a terceros. Podés ver el listado completo y
sus licencias en **Ajustes > Acerca de > Licencias de código abierto**.

## 4. Permisos y por qué se solicitan

| Permiso | Uso |
|---|---|
| `RECORD_AUDIO` | Dictar tareas por voz. La app **no graba ni almacena audio**: lo entrega en vivo al reconocedor de voz de Android y sólo recibe el texto. Ese reconocedor es un componente del sistema operativo y, según tu dispositivo y tu configuración de Android, puede procesar el audio en servidores de Google bajo la política de privacidad de Google. La app no controla ese tratamiento. Si no querés que ocurra, no uses el dictado por voz. |
| `CAMERA` | Tres usos, siempre iniciados por vos: escanear el código QR que vincula dos de tus equipos, leer el QR de una factura AFIP/ARCA para cargar un gasto, y sacarle una foto a un comprobante o a un producto de tu lista de deseos. Del escaneo de QR **no se guarda ninguna imagen**: sólo se lee el código. Las fotos que sacás a propósito se guardan en el almacenamiento privado de la app (ver sección 2). La cámara sólo se activa mientras estás en esas pantallas. |
| `READ_CONTACTS` | Opcional. Importar contactos de la libreta del teléfono a la app, sólo cuando vos elegís hacerlo. Los contactos importados quedan en la base local; no se envían a ningún servidor. |
| `INTERNET` / `ACCESS_NETWORK_STATE` / `ACCESS_WIFI_STATE` / `CHANGE_WIFI_MULTICAST_STATE` | Sincronizar con tus otros equipos dentro de tu red local (ver sección 5). La app no los usa para comunicarse con internet. |
| `USE_BIOMETRIC` / `USE_FINGERPRINT` | Opcional. Permite desbloquear la app con huella o rostro si activás esa opción. |
| `POST_NOTIFICATIONS` | Mostrar recordatorios de tareas. |
| `USE_EXACT_ALARM` / `SCHEDULE_EXACT_ALARM` | Programar recordatorios de tareas en la hora exacta indicada. |
| `USE_FULL_SCREEN_INTENT` | Mostrar el aviso a pantalla completa cuando llega un recordatorio con el teléfono bloqueado. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Opcional. Pedirte que excluyas la app del ahorro de batería, porque en algunos teléfonos esa optimización cancela los recordatorios programados. |
| `RECEIVE_BOOT_COMPLETED` | Reprogramar los recordatorios pendientes después de reiniciar el dispositivo. |
| `VIBRATE` / `WAKE_LOCK` | Hacer vibrar el dispositivo y mantener la pantalla encendida brevemente al recibir un recordatorio. |

Podés revocar estos permisos en cualquier momento desde los ajustes del
sistema operativo. Si revocás un permiso necesario, la funcionalidad
asociada (por ejemplo, los recordatorios) dejará de funcionar.

## 5. Conexiones de red y sincronización entre equipos

**La app no se comunica con servidores del desarrollador ni de terceros.** No
existe backend, no hay cuentas ni registro, y la app no descarga contenido de
internet ni envía tu información a ningún destino remoto.

La única funcionalidad de red es la **sincronización entre tus propios
equipos**, que está **apagada por defecto**:

- Sólo funciona dentro de tu red local (Wi-Fi). Los datos no atraviesan
  internet en ningún momento.
- Sólo se comunica con dispositivos que vos emparejaste explícitamente
  escaneando un código QR. Ese emparejamiento crea una clave secreta
  compartida entre tus equipos.
- Cada mensaje viaja **cifrado y autenticado con AES-256-GCM** usando una
  clave derivada de ese secreto compartido. Alguien conectado a tu misma red
  Wi-Fi que capture el tráfico ve un bloque ilegible, y un dispositivo ajeno
  a tu grupo no puede inyectar ni alterar datos.
- La clave se genera en tu propio dispositivo y sólo se transmite en el
  código QR que escaneás vos. El desarrollador no la conoce ni tiene forma
  de obtenerla, y por lo tanto no puede descifrar tu información aunque
  interceptara el tráfico.
- Podés desactivarla cuando quieras y desvincular tus equipos desde
  **Ajustes > Sincronizar equipos**.

Si nunca activás la sincronización, la app no realiza ninguna conexión de
red y podés verificarlo bloqueando su acceso a la red desde los ajustes del
sistema.

## 6. Copia de seguridad y exportación de datos

La app permite exportar tus datos en formato JSON desde **Ajustes > Copia de
seguridad > Exportar**. Este archivo contiene todos tus datos sin cifrar.
**Vos sos responsable** de elegir dónde guardarlo (almacenamiento local,
pendrive, gestor de contraseñas, servicio en la nube de tu elección, etc.).
La app no envía este archivo automáticamente a ningún destino.

La importación se realiza desde el mismo apartado y solo procesa archivos
que vos selecciones manualmente.

## 7. Eliminación de datos

Como todos los datos están en tu dispositivo, podés eliminarlos en cualquier
momento:

- **Borrar el contenido**: usá las opciones de borrado dentro de la app
  (eliminar tareas, contactos, gastos, etc.).
- **Borrar todo**: desinstalá la app o usá "Borrar datos" desde los ajustes
  del sistema operativo. Esto elimina la base de datos completa, los
  ajustes y el PIN.

No hay servidores donde solicitar la eliminación porque no se almacena
nada fuera de tu dispositivo.

## 8. Registro local de errores (opcional)

La app guarda un archivo local (`agenda-crashlog.txt`) con errores técnicos
para fines de diagnóstico. Este archivo se mantiene únicamente en el
dispositivo. Vos podés revisarlo, compartirlo manualmente con el
desarrollador (si lo solicita para resolver un problema) o borrarlo
desde **Ajustes > Diagnóstico**. La app **nunca lo envía automáticamente**.

## 9. Menores de edad

La app no está dirigida específicamente a menores de 13 años. Como no
recolecta datos ni los envía al desarrollador, su uso por menores no implica
recolección ni tratamiento de información personal por parte del
desarrollador.

## 10. Cambios en esta política

Si esta política se modifica, la nueva versión se publicará en la misma
URL donde leíste esta y la fecha de "Última actualización" se modificará
en consecuencia. Los cambios sustanciales se reflejarán en una nota de la
versión de la app.

## 11. Contacto

Para preguntas, reclamos o solicitudes relacionadas con esta política o con
la app:

**Email:** ivantr158@gmail.com
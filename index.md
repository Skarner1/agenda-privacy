Política de privacidad — Agenda
Última actualización: 29 de abril de 2026

Esta política describe cómo la aplicación Agenda (en adelante, "la app") trata la información del usuario. La app es desarrollada por Ivan C (en adelante, "el desarrollador").

Contacto: ivantr158@gmail.com

1. Resumen
Agenda es una aplicación 100% local. Todos tus datos —tareas, contactos, subtareas, gastos, ingresos, ajustes y PIN— se almacenan exclusivamente en tu dispositivo. La app no se conecta a internet, no recolecta datos, no los envía a ningún servidor, no los comparte con terceros y no utiliza servicios de análisis ni publicidad.

2. Datos que la app maneja en tu dispositivo
Los siguientes datos se guardan localmente en la base de datos del dispositivo y nunca abandonan el mismo a menos que vos los exportes manualmente:

Tareas, descripciones, fechas, horas, prioridades y categorías.
Contactos creados manualmente dentro de la app (nombre, teléfono, email, notas). La app no accede a la libreta de contactos del sistema.
Subtareas asociadas a tus tareas.
Gastos e ingresos extra que registres en la sección de Finanzas.
Ingreso mensual y meta de ahorro que vos configures.
Estadísticas internas de uso (categorías y horarios típicos) usadas exclusivamente en el dispositivo para sugerencias.
PIN de acceso (almacenado como hash PBKDF2-HMAC-SHA256 con salt aleatorio en el almacenamiento seguro del sistema, nunca en texto plano).
3. Datos que la app NO recolecta
No identificadores publicitarios.
No ubicación.
No información del dispositivo más allá de lo necesario para funcionar.
No analítica.
No crash reporting automático en la nube.
4. Permisos y por qué se solicitan
Permiso	Uso
RECORD_AUDIO	Dictar tareas por voz. El audio se procesa localmente por el reconocedor de voz del sistema operativo. No se graba ni se transmite.
USE_BIOMETRIC / USE_FINGERPRINT	Opcional. Permite desbloquear la app con huella o rostro si activás esa opción.
POST_NOTIFICATIONS	Mostrar recordatorios de tareas.
USE_EXACT_ALARM / SCHEDULE_EXACT_ALARM	Programar recordatorios de tareas en la hora exacta indicada.
RECEIVE_BOOT_COMPLETED	Reprogramar los recordatorios pendientes después de reiniciar el dispositivo.
VIBRATE / WAKE_LOCK	Hacer vibrar el dispositivo y mantener la pantalla encendida brevemente al recibir un recordatorio.
Podés revocar estos permisos en cualquier momento desde los ajustes del sistema operativo. Si revocás un permiso necesario, la funcionalidad asociada (por ejemplo, los recordatorios) dejará de funcionar.

5. Conexiones de red
La app no realiza solicitudes de red. No se conecta a internet en ningún momento. Podés verificar esto bloqueando el acceso a internet de la app desde los ajustes del sistema sin que ninguna funcionalidad se vea afectada.

6. Copia de seguridad y exportación de datos
La app permite exportar tus datos en formato JSON desde Ajustes > Copia de seguridad > Exportar. Este archivo contiene todos tus datos sin cifrar. Vos sos responsable de elegir dónde guardarlo (almacenamiento local, pendrive, gestor de contraseñas, servicio en la nube de tu elección, etc.). La app no envía este archivo automáticamente a ningún destino.

La importación se realiza desde el mismo apartado y solo procesa archivos que vos selecciones manualmente.

7. Eliminación de datos
Como todos los datos están en tu dispositivo, podés eliminarlos en cualquier momento:

Borrar el contenido: usá las opciones de borrado dentro de la app (eliminar tareas, contactos, gastos, etc.).
Borrar todo: desinstalá la app o usá "Borrar datos" desde los ajustes del sistema operativo. Esto elimina la base de datos completa, los ajustes y el PIN.
No hay servidores donde solicitar la eliminación porque no se almacena nada fuera de tu dispositivo.

8. Registro local de errores (opcional)
La app guarda un archivo local (agenda-crashlog.txt) con errores técnicos para fines de diagnóstico. Este archivo se mantiene únicamente en el dispositivo. Vos podés revisarlo, compartirlo manualmente con el desarrollador (si lo solicita para resolver un problema) o borrarlo desde Ajustes > Diagnóstico. La app nunca lo envía automáticamente.

9. Menores de edad
La app no está dirigida específicamente a menores de 13 años, pero al ser 100% local y sin recolección de datos, su uso por menores no implica recolección ni tratamiento de información personal por parte del desarrollador.

10. Cambios en esta política
Si esta política se modifica, la nueva versión se publicará en la misma URL donde leíste esta y la fecha de "Última actualización" se modificará en consecuencia. Los cambios sustanciales se reflejarán en una nota de la versión de la app.

11. Contacto
Para preguntas, reclamos o solicitudes relacionadas con esta política o con la app:

Email: ivantr158@gmail.com

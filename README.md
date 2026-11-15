# Gym Tracker — primera versión

Miniapp web responsive para registrar entrenamiento de fuerza y seguimiento del Aquiles. Los datos se guardan en Supabase por usuario (RLS).

## Puesta en marcha
1. Crear un proyecto en https://supabase.com y abrir **SQL Editor**. Ejecutar el contenido de `schema.sql`.
2. En **Authentication > Providers > Email**, habilitar el acceso por correo (OTP / magic link). En **Authentication > URL Configuration**, agregar la URL definitiva de la app como Site URL y Redirect URL permitida.
3. Copiar `config.example.js` como `config.js` y completar URL de proyecto y **clave pública anon/publishable** de Supabase. **Nunca** usar service_role/secret key en el navegador.
4. Subir `index.html`, `config.js` y `manifest.webmanifest` a un repositorio GitHub privado o a una carpeta de proyecto en Vercel. Deploy como sitio estático (sin build). Alternativamente usar Netlify u otro hosting HTTPS.
5. Abrir la URL publicada en iPhone. Ingresar email y abrir el enlace recibido. En Safari, Compartir > Añadir a pantalla de inicio.

## Funciones
- Rutinas A/B y opcional C precargadas, con sets, carga, reps y checks.
- Registro de dolor del Aquiles, esfuerzo, rigidez del día siguiente y notas.
- Guardar/editar sesiones, historial y resumen de cargas y dolor.
- Datos aislados por cuenta con políticas RLS.

## Limitaciones de la versión 1
- Necesita configurar Supabase y desplegarse: no hay backend activo incluido en este ZIP.
- No funciona sin conexión a internet; no hay sincronización offline.
- Rutinas predefinidas en código, no editables desde la interfaz.
- No incorpora calendario ni notificaciones ni evaluación clínica automatizada.
- La rigidez de la mañana siguiente puede actualizarse editando la sesión.
- Si se modifica el programa, los entrenamientos anteriores conservan sus datos guardados.

## Precaución
El programa es orientativo y no reemplaza indicaciones del kinesiólogo o traumatólogo. Evitar aumentos bruscos de carga si persisten síntomas del tendón.

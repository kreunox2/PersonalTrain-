# Programa de banda

Web personal para seguir un programa de entrenamiento de fútbol enfocado en
la posición de lateral: rutina semanal, marcado de ejercicios completados,
racha de días, estadísticas con gráfico, fecha estimada de fin del programa
según tu ritmo real, y un botón para justificar los días que no puedas
entrenar.

Es un sitio 100% estático (HTML, CSS y JavaScript sin frameworks ni
backend). Todo el progreso se guarda en el `localStorage` del navegador —
no hay servidor ni base de datos.

## Estructura del proyecto

```
index.html      Estructura de la web (vistas: Hoy, Semana, Estadísticas, Ajustes)
styles.css      Estilos visuales
app.js          Rutina de entrenamiento, lógica de guardado y cálculos
LICENSE         Licencia MIT del código
TERMS.md        Términos de uso
PRIVACY.md      Política de privacidad
```

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub (puede ser público o privado, pero
   GitHub Pages gratuito requiere que sea público salvo que tengas un plan
   de pago).
2. Sube estos archivos a la raíz del repositorio (o a una carpeta `docs/`,
   como prefieras).
3. Ve a **Settings → Pages** en el repositorio.
4. En "Source", elige la rama (normalmente `main`) y la carpeta (`/root` o
   `/docs`).
5. Guarda. GitHub te dará una URL del tipo
   `https://tu-usuario.github.io/tu-repositorio/`.
6. Espera 1-2 minutos y abre la URL: tu web ya está en línea.

## Personalizar la rutina

Toda la rutina está definida en `app.js`, en la constante `ROUTINE`. Cada
día de la semana (0 = domingo, 1 = lunes... 6 = sábado) tiene un título y
una lista de ejercicios con `id`, `name` y `meta` (series/repeticiones o
duración). Puedes editar, añadir o quitar ejercicios libremente; solo asegúrate
de que cada `id` sea único.

## Cómo se calcula la fecha estimada de fin

En Ajustes defines la **fecha de inicio** y la **duración del programa en
semanas**. La app calcula tu adherencia real (sesiones completadas ÷ días
transcurridos) y proyecta cuánto tardarías en terminar el programa completo
si mantienes ese ritmo. Si entrenas siempre según lo previsto, la fecha
estimada coincide con la fecha ideal del programa.

## Exportar / importar progreso

En Ajustes puedes descargar un archivo `.json` con todo tu progreso (copia
de seguridad) y volver a importarlo más adelante o en otro dispositivo,
ya que el `localStorage` no se sincroniza automáticamente entre navegadores
o dispositivos.

## Aviso legal

Revisa `TERMS.md` y `PRIVACY.md`. En resumen: esta herramienta es orientativa,
no sustituye a un profesional de la salud o del deporte, y no recopila ni
envía ningún dato a servidores externos.

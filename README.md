# Lengua Quiz · 2º ESO

Concurso en directo tipo Kahoot para clase (Temas I y II de Lengua), con estética de película antigua.

**Web:** https://emanuel-hosu.github.io/quiz-lengua/

## Cómo se usa en clase

1. **Profesor:** abre la web en el ordenador del proyector → *Soy profesor* → elige tema, nº de preguntas y segundos → *Crear partida*.
2. Aparecen un **PIN** y un **código QR**.
3. **Alumnos:** desde el móvil o iPad escanean el QR (o entran en la web → *Soy alumno*), escriben el PIN y su apodo.
4. Cuando estén todos, el profe pulsa **¡Empezar!**. La pregunta sale en el proyector y en cada dispositivo; los alumnos responden en su pantalla.
5. Tras cada pregunta: respuesta correcta, cuántos acertaron y clasificación. Al final, podio y botón **Descargar resultados** (CSV para Excel con aciertos por alumno y pregunta).

Extras: tocar un nombre en la sala de espera lo expulsa; si el navegador del profe se recarga, la partida se puede reanudar; *Practicar solo* funciona sin profesor.

## Técnica

- Un único `index.html` estático (GitHub Pages).
- Tiempo real con Supabase Realtime (proyecto `quiz-lengua`): solo se envían mensajes, no se guarda ningún dato de los alumnos.
- `.github/workflows/keepalive.yml` hace una consulta cada 3 días para que el proyecto gratuito de Supabase no se pause.

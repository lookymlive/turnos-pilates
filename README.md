# Sistema de Turnos Pilates Reformer

## Descripción

Este sistema permite gestionar turnos de clases de Pilates Reformer, mostrando y editando horarios por día en formato horizontal y horarios en formato vertical en turnos de 1 hora (mañana y tarde  de 08 a 09, 09 a 10, 10 a 11, 11 a 12, 14 a 15, tarde y noche de 17 a 18, 18 a 19 y 19 a 20, 20 a 21) para 6 camas.

## Prompt guía para Product Manager, Dev, UI/UX y IA

> "Quiero un sistema de turnos para Pilates Reformer con los siguientes requisitos:
>
> - Turnos de 1 hora, de 08 a 09, 09 a 10, 10 a 11, 11 a 12, 14 a 15, tarde y noche de 17 a 18, 18 a 19 y 19 a 20, 20 a 21.
> - Visualización clara por día hotizontal y por bloque horario vertical (mañana y tarde y tarde y noche).
> - Edición y guardado de turnos en la misma interfaz.
> - Estadísticas de ocupación y alumnos únicos.
> - Persistencia de datos para que los turnos no se pierdan al recargar la página o pasar los días.
> - Interfaz moderna, accesible y fácil de usar para cualquier usuario."

## Persistencia de datos

Actualmente, los datos se almacenan en memoria (en el navegador). Para que los datos persistan al pasar los días o al recargar la página, puedes:

1. **LocalStorage**: Guardar y cargar los datos en el almacenamiento local del navegador (`localStorage`).
2. **Backend/API**: Implementar una API o backend (por ejemplo, con Node.js, Firebase, Supabase, etc.) para guardar y recuperar los datos de turnos.
3. **Exportar/Importar**: Usar los botones de exportar/importar para guardar y restaurar los datos manualmente.

### Ejemplo de persistencia con LocalStorage

Agrega estas líneas en el script de `index.html`:

```js
// Al guardar cambios:
localStorage.setItem('pilatesSchedule', JSON.stringify(scheduleData));

// Al cargar la página:
const saved = localStorage.getItem('pilatesSchedule');
if (saved) scheduleData = JSON.parse(saved);
```

Esto hará que los turnos se mantengan aunque cierres o recargues la página.

---

**Sugerencia:**

- El Product Manager puede usar el prompt guía para definir requisitos claros.
- El Dev puede seguir los pasos y el ejemplo de persistencia.
- El UI/UX puede mejorar la experiencia visual y de interacción.
- La IA puede usar el prompt para entender el contexto y automatizar tareas o sugerir mejoras.

---

¿Dudas o sugerencias? ¡Edita este README o consulta a tu equipo!

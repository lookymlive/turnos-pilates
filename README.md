# Sistema de Turnos Pilates Reformer

## 🌟 Descripción General

Este proyecto es una aplicación web frontend para la gestión de turnos de clases de Pilates Reformer. Permite a los administradores o profesores visualizar, crear, editar y organizar los horarios de clases para múltiples camas, días y franjas horarias. La aplicación está diseñada para ser intuitiva y facilitar la administración diaria de un estudio de Pilates.

## ✨ Funcionalidades Actuales

- **Visualización de Horarios:**
  - Selección de día (Lunes a Viernes).
  - Selección de franja horaria combinada:
    - Mañana y Tarde (08:00-12:00 y 14:00-15:00).
    - Tarde y Noche (16:00-21:00).
  - Tabla de horarios clara con 6 camas disponibles por hora.
- **Gestión de Alumnos:**
  - Añadir y editar nombres de alumnos en cada turno.
  - Marcar asistencia de alumnos.
  - Añadir notas específicas para cada alumno en su turno.
- **Gestión de Profesores:**
  - Asignar y editar el nombre del profesor/a para cada bloque horario.
- **Modo Edición:**
  - Interfaz para modificar nombres de alumnos y profesores.
  - Guardar y cancelar cambios.
- **Persistencia de Datos:**
  - Los datos del horario (alumnos, profesores, asistencia, notas) y la preferencia de tema se guardan en `localStorage` del navegador.
  - Importación y exportación de datos en formato JSON.
- **Tema Visual:**
  - Alternar entre tema claro y oscuro.
- **Utilidades:**
  - Limpiar el horario del turno actual.
  - Copiar el horario del turno actual (para pegarlo en otro día/turno, funcionalidad a mejorar).
  - Imprimir el horario visible.
  - Estadísticas básicas: alumnos únicos, turnos ocupados, porcentaje de ocupación del turno visible.

## 🚀 Cómo Empezar

Simplemente abre el archivo `index.html` en tu navegador web preferido.

## 💡 Propuestas de Evolución del Producto (Perspectivas)

A continuación, se presentan ideas para futuras mejoras desde diferentes roles profesionales, inspiradas en proyectos similares y mejores prácticas:

### 🧑‍💼 Product Manager (PM)

*Objetivo: Maximizar el valor para el usuario y el estudio, identificando necesidades y oportunidades.*

- **Investigación de Usuarios:** Realizar encuestas o entrevistas a dueños de estudios y profesores para entender a fondo sus necesidades y puntos débiles con la gestión actual.
- **Roadmap Estratégico:** Definir un plan de funcionalidades a corto, mediano y largo plazo (ej. Módulo de pagos, portal de alumnos, app móvil).
- **Métricas Clave (KPIs):** Establecer métricas para medir el éxito: tasa de adopción, frecuencia de uso, satisfacción del usuario (ej. a través de un simple feedback), reducción de tiempo en gestión.
- **Integraciones:**
  - **Calendarios Externos:** Sincronización con Google Calendar, Outlook Calendar para profesores y/o alumnos.
  - **Pasarelas de Pago:** Para reserva y pago online de clases.
- **Gestión de Clientes (CRM Lite):** Ficha de alumno más completa (historial de clases, pagos, notas generales).
- **Listas de Espera:** Funcionalidad para que los alumnos se anoten si un turno está lleno y reciban notificaciones si se libera un lugar.
- **Notificaciones Automáticas:** Recordatorios de clase (email/SMS), confirmaciones de reserva, avisos de cancelación.
- **Roles de Usuario:** Diferenciar entre Administrador (acceso total), Profesor (gestión de sus clases y alumnos), Alumno (ver/reservar sus clases).

### 💻 Developer (Dev)

*Objetivo: Construir una solución robusta, escalable, mantenible y con buen rendimiento.*

- **Refactorización del Código JS:**
  - Modularizar el código: Separar la lógica de la interfaz (UI), la gestión de datos (estado) y las utilidades en diferentes archivos/módulos.
  - Considerar patrones de diseño (ej. Módulo, Observador) para una mejor organización.
- **Framework/Librería Frontend:** Para funcionalidades más complejas y escalabilidad, evaluar la migración a un framework como React, Vite o Nextjs. Esto facilitaría la gestión del estado, el enrutamiento y la componentización.
- **Backend y Base de Datos:**
  - Para persistencia robusta, multiusuario y funcionalidades avanzadas, desarrollar un backend (Node.js/supabase).
  - Utilizar una base de datos (PostgreSQL, MongoDB, Firebase Firestore).
- **Pruebas (Testing):** Implementar pruebas unitarias (Jest, Vitest) para funciones críticas y pruebas E2E (Cypress, Playwright) para flujos de usuario.
- **Build Tools:** Integrar herramientas como Vite, Webpack o Parcel para optimización de assets, transpilación de JS moderno y hot-reloading durante el desarrollo.
- **Gestión de Estado Avanzada:** Si se adopta un framework, utilizar sus herramientas de gestión de estado (Pinia para Vue, Redux/Zustand para React).
- **API Design (si se crea backend):** Diseñar una API RESTful o GraphQL clara y bien documentada.
- **Seguridad:** Implementar medidas de seguridad si se manejan datos sensibles (autenticación, autorización, protección contra XSS, CSRF).

### 🎨 UI/UX Designer

*Objetivo: Crear una experiencia de usuario intuitiva, eficiente, accesible y visualmente agradable.*

- **Investigación de Usuario (UX):** Observar cómo los usuarios actuales interactúan con la herramienta. Crear personas y user journeys.
- **Flujos de Usuario Optimizados:** Rediseñar flujos críticos (ej. reserva de un alumno, reprogramación) para que sean más rápidos y sencillos.
- **Diseño de Interfaz (UI):**
  - **Sistema de Diseño Ligero:** Definir una paleta de colores cohesiva, tipografía legible, espaciado consistente e iconografía clara.
  - **Componentes Reutilizables:** Diseñar componentes de UI estándar (botones, modales, inputs) para consistencia.
  - **Dashboard Mejorado:** Para el administrador, una vista general más visual con gráficos de ocupación, ingresos (si aplica), etc.
- **Accesibilidad (A11y):** Asegurar el cumplimiento de las pautas WCAG (contraste adecuado, navegación por teclado, etiquetas ARIA, texto alternativo para imágenes).
- **Responsividad Avanzada:** Optimizar la visualización y la interacción en una gama más amplia de dispositivos móviles y tablets.
- **Feedback Visual y Microinteracciones:** Añadir animaciones sutiles y feedback claro para las acciones del usuario (ej. al guardar, al cargar).
- **Personalización Visual:** Permitir al estudio (si fuera un producto SaaS) personalizar colores básicos o subir un logo.

### 🤖 Inteligencia Artificial (IA) / Machine Learning (ML)

*Objetivo: Integrar capacidades inteligentes para optimizar operaciones y mejorar la experiencia.*

- **Predicción de Demanda:** Analizar datos históricos de asistencia para predecir qué horarios y días tendrán mayor demanda, ayudando a optimizar la oferta de clases.
- **Sistema de Recomendación:**
  - Para alumnos: Sugerir clases o horarios basados en su historial o preferencias.
  - Para administradores: Sugerir profesores para cubrir turnos basados en su disponibilidad o especialidad.
- **Optimización de Horarios:** Algoritmo que sugiera la asignación óptima de profesores a clases para maximizar la ocupación o minimizar conflictos.
- **Detección de Anomalías:** Identificar patrones inusuales (ej. un alumno que falta mucho, un horario con baja ocupación persistente).
- **Chatbot de Asistencia:** Un chatbot básico para responder preguntas frecuentes de alumnos sobre horarios, precios, etc.

---

## 📝 TODO - Próximos Pasos

Este es un plan de trabajo sugerido, priorizando mejoras incrementales:

### Fase 1: Mejoras Fundamentales y UX

- **[Dev]** Refactorizar JavaScript:
  - [ ] Separar `scheduleData` y su lógica de manipulación en un módulo/objeto dedicado.
  - [ ] Separar las funciones de renderizado de la tabla (`createTable` y relacionadas) en un módulo de UI.
  - [ ] Centralizar la gestión del estado (día actual, turno actual, modo edición).
- **[UI/UX]** Mejorar la función "Copiar Turno":
  - [ ] Permitir seleccionar un día/turno destino para "Pegar" el horario copiado.
  - [ ] Feedback visual claro durante el proceso de copiado y pegado.
- **[UI/UX]** Revisión de Accesibilidad:
  - [ ] Verificar contrastes de color (especialmente en modo oscuro).
  - [ ] Asegurar navegación completa por teclado.
  - [ ] Añadir atributos ARIA donde sea necesario.
- **[Dev]** Mejorar la gestión de errores y feedback al usuario (ej. en importación JSON).
- **[PM]** Recopilar feedback inicial de usuarios sobre las funcionalidades actuales y las propuestas.

### Fase 2: Funcionalidades Clave Adicionales

- **[PM/Dev]** Diseño e implementación de "Lista de Espera" para turnos completos.
  - [ ] Lógica para añadir/quitar alumnos de la lista.
  - [ ] Notificación (manual por ahora) si se libera un cupo.
- **[UI/UX/Dev]** Mejorar la visualización de estadísticas:
  - [ ] Estadísticas globales (semanales/mensuales) además de las del turno actual.
  - [ ] Gráficos simples para ocupación.
- **[Dev]** Explorar un sistema de "plantillas de horarios" para crear rápidamente semanas típicas.

### Fase 3: Escalabilidad y Profesionalización

- **[Dev]** Evaluación y posible migración a un framework frontend (ej. Vue.js o Svelte) si la complejidad sigue aumentando.
- **[Dev/PM]** Planificación de un backend y base de datos si se requieren funcionalidades como:
  - [ ] Cuentas de usuario (admin, profesor, alumno).
  - [ ] Reservas online por alumnos.
  - [ ] Pagos.
- **[Dev]** Implementar un sistema de build (ej. Vite).
- **[Dev]** Iniciar la escritura de pruebas unitarias para la lógica de negocio.

### Continuo

- **[Todos]** Documentar decisiones de diseño y código.
- **[Todos]** Mantener el `.gitignore` actualizado.
- **[Todos]** Realizar pruebas regulares en diferentes navegadores y dispositivos.

---

*Este README es un documento vivo. ¡Siéntete libre de actualizarlo a medida que el proyecto evoluciona!*

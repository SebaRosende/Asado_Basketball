
# 🏀 Asado Basketball | Financial & Sports Management

> Transparencia total para el Pre-Maxi de Racing. Una plataforma diseñada para centralizar la economía del equipo (compras, aportes y saldos) con el soporte deportivo como valor agregado.
LINK: https://asadobasketball.club/
-----

📖 Visión del Proyecto
Asado Basketball resuelve el problema logístico de los equipos amateurs: la gestión de gastos. Mientras que otras apps se enfocan solo en el juego, esta herramienta prioriza la transparencia financiera de los "asados" y cuotas del equipo, utilizando el fixture y los resultados como el contexto deportivo donde ocurren estos gastos.

🌟 Funcionalidades Core (Finanzas)
Gestión de Gastos Centralizada: Registro detallado de compras (asado, bebida, alquiler de cancha).

Control de Aportes: Seguimiento en tiempo real de quién pagó y quién debe.

Cálculo de Saldos: Algoritmo automático para el balance de la "caja chica" del equipo.

Transparencia Total: Historial de movimientos auditable por cualquier miembro logueado.

🎨 Funcionalidades Secundarias (Decoración)
Fixture Dinámico: Fechas, sedes y horarios de los partidos de Racing.

Tanteador Live: Actualización de resultados para mantener el engagement del grupo.

### 🌟 Key Features (Funcionalidades Clave)

  * **Sistema de Roles Dinámico:** Implementación de RBAC (Role-Based Access Control) para proteger acciones críticas.
  * **Fixture Inteligente:** Visualización optimizada de encuentros con detalles de localía, sedes y horarios.
  * **Interfaz Industrial-Sport:** Diseño UI/UX personalizado con el ADN de Racing, optimizado para uso "en cancha" (Mobile-First).
  * **Seguridad de Grado Cloud:** Reglas de seguridad en Firestore y restricciones de API Keys en Google Cloud.

-----

## 🛠️ Stack Tecnológico Detallado

### Frontend & Core

  * **Framework:** Next.js 14 con App Router para una navegación instantánea.
  * **UI/UX:** Tailwind CSS con componentes personalizados para una estética limpia y deportiva.
  * **Tipografía:** Fuentes sans-serif de alto impacto para legibilidad en ambientes dinámicos.

### Backend & Cloud (Serverless)

  * **Authentication:** Google Identity Platform integrado con Firebase.
  * **Database:** Cloud Firestore (NoSQL) para baja latencia y sincronización offline.
  * **Security:** Firebase Security Rules para validación de escrituras por rol de usuario.
  * **Deployment:** Pipeline de despliegue automático mediante Firebase Hosting.

-----

## 🏗️ Arquitectura de la Solución

### Estructura de Carpetas

```text
/src
 ├── app/               # App Router: Páginas, Layouts y Error Handlers
 ├── components/        # UI Atoms & Molecules (Modals, Buttons, Cards)
 ├── context/           # AuthContext para manejo de sesión global
 ├── firebase/          # Configuración de SDK y servicios (Auth, Firestore)
 ├── hooks/             # Custom hooks para lógica de negocio reutilizable
 └── types/             # Definiciones de TypeScript (Interfaces de Jugadores, Partidos)
/public
 └── images/            # Activos visuales (Logo Racing, Favicons)
```

### Flujo de Datos (Data Flow)

1.  **Auth:** El usuario se loguea vía Google -\> Firebase emite un `idToken`.
2.  **Context:** React atrapa el estado del usuario y lo distribuye a los componentes.
3.  **Firestore:** Los componentes escuchan cambios en tiempo real en la colección `/matches`.
4.  **UI:** Si el usuario tiene el campo `role: 'admin'`, se habilitan los inputs de edición de puntos.

-----
-----

## ✍️ Sobre el Autor

**Sebastian**

  * **Formación:** Desarrollador de Aplicaciones (UNICEN - Olavarría).
  * **Experiencia:** Analista de Infraestructura en Loma Negra CIASA.
  * **Pasión:** Integración de IA y soluciones escalables para el deporte local.

-----

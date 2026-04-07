
# 🏀 Asado Basketball | Sistema de Gestión Deportiva

> La planilla digital del Pre-Maxi. Una aplicación web de alto rendimiento diseñada para centralizar fixtures, resultados y estadísticas en tiempo real.
-----

## 📖 Descripción del Proyecto

**Asado Basketball** no es solo una planilla de resultados; es una plataforma centralizada para la categoría **Pre-Maxi de Racing de Olavarría**. El objetivo es eliminar la fragmentación de la información (mensajes de WhatsApp, fotos de planillas de papel) y ofrecer una experiencia de usuario fluida, rápida y segura para jugadores y administradores.

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

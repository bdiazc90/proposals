# Bruno Díaz Dev - Cotización

> Fecha: 2025-06-01. Validez:  2025-06-30.
>
> **Aplicación Fullstack Web**

### "Gestión de ordenes de trabajo e inventarios para Bombas de Agua"

- ✅ App web profesional para técnicos y supervisores
- ✅ Gestión completa de órdenes con estados automáticos
- ✅ Checklists digitales para instalación y mantenimiento
- ✅ Acceso móvil optimizado para trabajo en campo
- ✅ Sistema de usuarios con permisos por rol

---

## Fase 1: MVP - Resumen Técnico y Funcional

Sistema de gestión de órdenes de trabajo y gestión de equipos; con autenticación de 2 tipos de usuarios y dashboard básico.

### Stack Tecnológico
- NextJS 15.3 + TypeScript
- Supabase (auth + database)
- Shadcn/ui + Tailwind v4
- Deploy: Vercel + Supabase

### RoadMap: 3 Sprints

#### Sprint 1: Base Funcional (16h)
- Setup NextJS + Supabase
- Autenticación con Google (OAuth2)
- Lista básica de órdenes asignadas
- Layout responsive (celular y laptop)

#### Sprint 2: Gestión de Órdenes (20h)
- CRUD completo de órdenes
- Estados: pending → in_progress → completed
- Búsqueda por texto
- Modal de detalles/edición

#### Sprint 3: Gestión de Equipos (16h)
- CRUD completo de equipos
- Búsqueda por texto
- Modal de detalles/edición

## Resumen de funcionalidades Clave

### **Acceso y Seguridad**
#### Inicio de Sesión Simple
- Acceso únicamente con cuenta de Google
- Los usuarios deben ser agregados por un admin
- Acceso instantáneo desde cualquier dispositivo

#### Roles de Usuario
- **Técnicos**: Ven solo sus órdenes asignadas, pueden completar trabajo
- **Administradores**: Ven todo, crean órdenes, asignan técnicos

### **Gestión de Órdenes de Trabajo**
#### Para Administradores
- **Crear Nuevas Órdenes:**
    - Datos del cliente y ubicación
    - Tipo de bomba a instalar/mantener
    - Asignar técnico específico
    - Programar fecha de trabajo
- **Supervisar Progreso:**
    - Ver todas las órdenes en curso
    - Estados en tiempo real de cada trabajo
    - Buscar órdenes por cliente o ubicación
    - Reasignar trabajos si es necesario

#### Para Técnicos
- **Ver Trabajos Asignados:**
    - Lista personalizada solo con sus órdenes
    - Información completa: cliente, dirección, tipo de bomba
    - Fecha programada

- **Actualizar Estado del Trabajo:**
    - Marcar "En proceso" al llegar al sitio
    - Marcar "Completado" al terminar
    - Agregar notas sobre el trabajo realizado

### **Gestión de Equipos e Inventario**

#### Para Administradores
- **Registrar Equipos Instalados:**
    - Crear ficha de bomba tras instalación
    - Especificar modelo, serie y características
    - Vincular equipo con cliente y ubicación

- **Control de Inventario:**
    - Lista completa de equipos instalados
    - Ver estado actual de cada bomba
    - Programar mantenimientos (creando una orden)

#### Para Técnicos
- **Ver Equipos Asignados:**
    - Lista de bombas bajo su responsabilidad
    - Información técnica completa de cada equipo
    - Historial de trabajos realizados por equipo

## Presupuesto y Pago

#### Equipo técnico
- 1 Desarrollador Fullstack Senior * 52 horas

#### Precio
- PEN 3120 (Soles)

#### Plazo
- 21 días a partir de inicio del desarrollo

#### Modalidad de Pago
- 50% para iniciar el proyecto
- 50% en la entregable final

#### Entrega Final
- Código fuente completo en un repositorio privado
- Acceso a las cuentas de Vercel para monitorear el servicio
- Aplicación desplegada publicamente

## Límites y Responsabilidades del Proyecto

### Inclusiones del Desarrollo
- Desarrollo de la aplicación según especificaciones (Fase 1)
- Hosting gratuito en Vercel (frontend) y Supabase (backend)
- Dominio temporal (.vercel.app) para pruebas y lanzamiento
- 15 días de soporte post-entrega para bugs y ajustes menores

### Exclusiones y Costos del Cliente
- **Dominio personalizado**: Cliente debe adquirir y configurar
- **Hosting premium**: Si requiere mayor capacidad o funciones avanzadas
- **Integraciones externas**: APIs de terceros, servicios de pago, SMS
- **Capacitación**: Entrenamiento presencial o personalizado de usuarios
- **Mantenimiento**: Actualizaciones y nuevas funcionalidades post-entrega

### Responsabilidades del Cliente
- Proveer contenido, logos e información específica del negocio
- Revisar y aprobar entregables en máximo 48 horas
- Designar persona de contacto para feedback y decisiones
- Acceso a cuenta Google Workspace si se requiere integración

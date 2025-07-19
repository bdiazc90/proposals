# Reto Técnico: Mini Sistema de Subastas

**Tiempo límite:** 40 minutos  
**Objetivo:** Crear una API REST básica para un sistema de subastas usando Django

## Historias de Usuario

### Historia #1: Crear Subasta
**Como** usuario registrado  
**Quiero** crear una nueva subasta con título, descripción, precio inicial y fecha de cierre  
**Para que** otros usuarios puedan pujar por mi producto  

**Criterios de Aceptación:**
- Puedo especificar título, descripción, precio inicial y fecha de fin
- La subasta se crea con estado "activa" automáticamente
- El precio inicial debe ser mayor a 0

### Historia #2: Realizar Oferta
**Como** usuario registrado  
**Quiero** hacer una oferta en una subasta activa  
**Para que** pueda intentar ganar el producto que me interesa  

**Criterios de Aceptación:**
- Solo puedo ofertar en subastas que no han vencido
- Mi oferta debe ser mayor al precio actual (inicial o última oferta válida)
- No puedo ofertar en mis propias subastas
- Cada oferta queda registrada con timestamp y mi usuario
- Recibo confirmación de oferta exitosa o mensaje de error claro

### Historia #3: Consultar Estado de Subasta
**Como** usuario registrado  
**Quiero** ver el listado de subastas activas y el historial de ofertas  
**Para que** pueda decidir en cuáles participar y monitorear mi actividad  

**Criterios de Aceptación:**
- Puedo ver todas las subastas que no han vencido
- Para cada subasta veo: título, precio actual, tiempo restante
- Puedo ver el historial completo de ofertas de una subasta específica
- Las ofertas se muestran ordenadas por fecha (más reciente primero)
- Puedo identificar cuál es la oferta ganadora actual

---

## Requisitos Funcionales

### Modelos Requeridos
- **User**: Usuario del sistema (usar User de Django)
- **Auction**: Subasta con título, descripción, precio inicial, fecha fin
    - `title` (CharField, max_length=200)
    - `description` (TextField)
    - `starting_price` (DecimalField, max_digits=10, decimal_places=2)
    - `end_date` (DateTimeField)
    - `creator` (ForeignKey a User)
    - `created_at` (DateTimeField, auto_now_add=True)
- **Bid**: Oferta/puja con monto y timestamp
    - `auction` (ForeignKey a Auction)
    - `bidder` (ForeignKey a User)
    - `amount` (DecimalField, max_digits=10, decimal_places=2)
    - `created_at` (DateTimeField, auto_now_add=True)

### APIs Requeridas
1. **POST /auctions/** - Crear nueva subasta
2. **GET /auctions/** - Listar subastas activas
3. **POST /auctions/{id}/bid/** - Hacer oferta en subasta
4. **GET /auctions/{id}/bids/** - Ver ofertas de una subasta

### Validaciones de Negocio
- Nueva oferta debe ser mayor al precio actual (inicial o última oferta)
- No se puede ofertar en subastas vencidas
- Usuario no puede ofertar en su propia subasta

---

## Bonus

Utiliza una herramienta de vibe coding para crear una aplicación front-end con Next.js que consuma tu API REST y permita realizar los 3 flujos especificados en las historias de usuario.



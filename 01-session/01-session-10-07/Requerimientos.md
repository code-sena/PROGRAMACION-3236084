# Evidencia GA1-220501092-AA1-EV03: Taller de Historias de Usuario
## Proyecto: Sistema de Carrito de Compras E-commerce

### Simulación de Reunión de Planeación de Sprint

**Fecha:** 10 de Julio, 2025  
**Sprint:** Sprint 2 - Funcionalidades del Carrito de Compras  
**Duración del Sprint:** 2 semanas  

---

## Roles Participantes

### 🔧 Scrum Master: María Rodríguez
- **Responsabilidades:** Dirigir la reunión, controlar tiempos, facilitar la estimación con Planning Poker
- **Participación:** Modera las discusiones y asegura que todas las historias queden bien definidas

### 📋 Product Owner: Carlos Mendoza
- **Responsabilidades:** Presentar épicas, definir prioridades, aclarar requisitos de negocio
- **Participación:** Explica el valor de negocio de cada funcionalidad del carrito

### 👨‍💻 Equipo de Desarrollo:
- **Ana Gómez** (Frontend Developer)
- **Luis Torres** (Backend Developer) 
- **Diana Silva** (QA Tester)

---

## Historia Épica: Gestión del Carrito de Compras

### Descripción de la Épica:
Como cliente del e-commerce, quiero poder gestionar los productos en mi carrito de compras de manera intuitiva y segura, para realizar mis compras de forma eficiente.

---

## Descomposición en Historias de Usuario

| ID | Historia de Usuario | Esfuerzo | Prioridad | Criterios de Aceptación |
|----|--------------------|----------|-----------|-------------------------|
| **HU04** | Como cliente, quiero agregar productos al carrito desde la página de producto, para poder comprar los artículos que me interesan. | **5 pts** | Alta | • El botón "Agregar al carrito" debe estar visible en la página del producto<br>• Debe mostrar confirmación visual cuando se agrega el producto<br>• El contador del carrito debe actualizarse automáticamente<br>• Debe funcionar tanto para productos simples como con variantes (talla, color)<br>• Validar stock disponible antes de agregar |
| **HU05** | Como cliente, quiero ver el resumen de mi carrito con productos, cantidades y precios, para revisar mi pedido antes de pagar. | **3 pts** | Alta | • Mostrar imagen, nombre, precio unitario y cantidad de cada producto<br>• Calcular y mostrar subtotal por producto<br>• Mostrar total general del carrito<br>• Incluir costos de envío si aplica<br>• Mostrar descuentos o cupones aplicados<br>• Tiempo de carga menor a 2 segundos |
| **HU06** | Como cliente, quiero modificar las cantidades de productos en mi carrito, para ajustar mi pedido según mis necesidades. | **8 pts** | Alta | • Permitir aumentar/disminuir cantidad con botones + y -<br>• Permitir edición directa del campo cantidad<br>• Validar que la cantidad no exceda el stock disponible<br>• Actualizar precios automáticamente al cambiar cantidades<br>• Mostrar mensaje de error si cantidad es inválida<br>• Opción de eliminar producto si cantidad = 0 |
| **HU07** | Como cliente, quiero eliminar productos de mi carrito, para quitar artículos que ya no deseo comprar. | **2 pts** | Media | • Botón "Eliminar" visible en cada producto del carrito<br>• Mostrar confirmación antes de eliminar<br>• Actualizar totales automáticamente tras eliminación<br>• Mostrar mensaje "Carrito vacío" si no hay productos<br>• Permitir deshacer eliminación en los siguientes 10 segundos |
| **HU08** | Como cliente, quiero guardar mi carrito para continuar la compra más tarde, para no perder mi selección si cierro la aplicación. | **13 pts** | Media | • Guardar carrito automáticamente para usuarios registrados<br>• Persistir carrito por 30 días mínimo<br>• Sincronizar carrito entre dispositivos para el mismo usuario<br>• Validar disponibilidad de productos al recuperar carrito<br>• Notificar si algún producto ya no está disponible<br>• Funcionar sin conexión temporal (localStorage) |
| **HU09** | Como cliente, quiero aplicar cupones de descuento en mi carrito, para obtener beneficios y ahorrar dinero. | **5 pts** | Baja | • Campo para ingresar código de cupón<br>• Validar código en tiempo real<br>• Mostrar descuento aplicado claramente<br>• Permitir solo un cupón por pedido<br>• Mostrar mensaje de error si cupón es inválido o expirado<br>• Calcular descuento sobre subtotal sin incluir envío |

---

## Proceso de Estimación - Planning Poker

### Metodología Utilizada:
Se utilizó la secuencia de Fibonacci modificada: 1, 2, 3, 5, 8, 13, 21

### Proceso de Estimación por Historia:

#### HU04 - Agregar productos al carrito (5 pts)
- **Ana (Frontend):** 5 pts - "Requiere manejo de estado, validaciones de UI y diferentes variantes de producto"
- **Luis (Backend):** 3 pts - "API endpoints simples, pero validación de stock es compleja"
- **Diana (QA):** 8 pts - "Muchos casos de prueba: variantes, stock, diferentes productos"
- **Consenso:** 5 pts (promedio después de discusión)

#### HU05 - Ver resumen del carrito (3 pts)
- **Ana (Frontend):** 3 pts - "Mainly display logic, calculations straightforward"
- **Luis (Backend):** 2 pts - "Simple data retrieval"
- **Diana (QA):** 3 pts - "Testing calculations and display"
- **Consenso:** 3 pts

#### HU06 - Modificar cantidades (8 pts)
- **Ana (Frontend):** 8 pts - "Complex UI interactions, real-time validations"
- **Luis (Backend):** 5 pts - "Stock validation, concurrent updates handling"
- **Diana (QA):** 13 pts - "Many edge cases, boundary testing"
- **Consenso:** 8 pts (después de aclarar alcance)

#### HU07 - Eliminar productos (2 pts)
- **Ana (Frontend):** 2 pts - "Simple delete with confirmation"
- **Luis (Backend):** 1 pt - "Straightforward deletion"
- **Diana (QA):** 3 pts - "Few test cases"
- **Consenso:** 2 pts

#### HU08 - Guardar carrito (13 pts)
- **Ana (Frontend):** 8 pts - "Sync between devices, offline handling"
- **Luis (Backend):** 13 pts - "Complex persistence, user sessions, data sync"
- **Diana (QA):** 13 pts - "Cross-device testing, offline scenarios"
- **Consenso:** 13 pts

#### HU09 - Aplicar cupones (5 pts)
- **Ana (Frontend):** 3 pts - "Form validation, discount display"
- **Luis (Backend):** 8 pts - "Complex business rules, validation logic"
- **Diana (QA):** 5 pts - "Various coupon scenarios"
- **Consenso:** 5 pts

---

## Resumen del Sprint

### Velocity del Equipo: 25-30 story points por sprint
### Total de Story Points: 36 pts

**Decisión del Product Owner:** 
Priorizar las historias HU04, HU05, HU06, y HU07 (18 pts) para este sprint, dejando HU08 y HU09 para el siguiente sprint debido a su complejidad.

---

## Documentación del Proceso

### Decisiones Tomadas:
1. **Alcance del Sprint:** Se decidió enfocarse en funcionalidades core del carrito
2. **Criterios de Aceptación:** Se definieron con participación del PO para asegurar valor de negocio
3. **Estimación:** Se utilizó Planning Poker para obtener estimaciones consensuadas
4. **Priorización:** Se priorizó según impacto en experiencia del usuario

### Riesgos Identificados:
- Complejidad de la sincronización entre dispositivos (HU08)
- Validación de stock en tiempo real para HU04 y HU06
- Integración con sistema de cupones de terceros (HU09)

### Próximos Pasos:
1. Definir tareas técnicas para cada historia
2. Establecer criterios de Definition of Done
3. Planificar daily standups
4. Configurar ambiente de testing

---

**Facilitado por:** María Rodríguez (Scrum Master)  
**Documentado el:** 10 de Julio, 2025
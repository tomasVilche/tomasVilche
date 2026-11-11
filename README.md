<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,100:DC2626&height=160&section=header&text=CRM%20para%20Concesionarias&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=35" width="100%" />

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL_16-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Electron-47848F?style=for-the-badge&logo=electron&logoColor=white" />
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white" />
</p>

<p align="center"><img src="media/mi-dia.jpg" width="100%" alt="Pantalla Mi día" /></p>

CRM de escritorio para concesionarias de autos 0 km y usados. Varias PC trabajan sobre una misma base central, con usuarios individuales y permisos verificados en el servidor.

> 🔒 **Repositorio vitrina.** El código fuente es privado. Las capturas usan datos inventados.

## 🚗 Qué hace

- **Mi día**: tareas vencidas, citas, cuotas por cobrar y reservas por vencer, apenas se entra.
- Gestión de **clientes, oportunidades, inventario, agenda y financiación**.
- Circuito completo: lead → propuesta → reserva → contrato → cobro / permuta → gestoría → entrega → postventa.
- **Reserva de unidades segura** aunque dos personas lo intenten a la vez.
- Planes de cuotas en ARS y USD, permutas, consignaciones y tasaciones.
- Importación de clientes desde planillas con detección de duplicados y exportación a Excel.
- Tema claro y oscuro.

## 📸 Capturas

<p align="center">
  <img src="media/inventario.jpg" width="49%" alt="Inventario" />
  <img src="media/inventario-oscuro.jpg" width="49%" alt="Inventario en tema oscuro" />
</p>
<p align="center">
  <img src="media/clientes.jpg" width="49%" alt="Clientes" />
  <img src="media/oportunidades.jpg" width="49%" alt="Oportunidades" />
</p>
<p align="center"><img src="media/financiacion.jpg" width="100%" alt="Financiación" /></p>

## 🔐 Seguridad

- Login con **2FA (TOTP)** y contraseñas con **Argon2**.
- Permisos por rol, denegados por defecto y verificados en cada solicitud.
- Sesiones con cookies `HttpOnly`, protección CSRF y cierre por inactividad.
- Las reglas críticas viven en la base de datos: movimientos inmutables y auditoría de solo agregado.

## 🧱 Arquitectura

| Capa | Tecnología |
|---|---|
| Base de datos | PostgreSQL 16 con migraciones versionadas y tests de invariantes |
| Servidor | Node.js + Fastify 5, validación con Zod |
| Escritorio | Electron, instalable en Windows |
| Calidad | Pruebas de accesibilidad con axe-core y Playwright, contraste AA verificado |

---
<p align="center">© 2026 Tomás Vilche · Todos los derechos reservados</p>

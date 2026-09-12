# AulaTrack — Sistema académico

AulaTrack es una aplicación web académica para gestionar actividades, fechas de entrega y estados de progreso. Este repositorio contiene la continuidad del proyecto desarrollada para la **Actividad 5: programación del lado del servidor**.

## Funcionalidades

La aplicación incluye autenticación mediante OAuth, persistencia de usuarios y actividades en MySQL/TiDB, validación de entradas con Zod, procedimientos tRPC protegidos y operaciones CRUD con aislamiento por propietario. La interfaz muestra estados de carga, error y vacío, además de una consola visual de evidencias para las operaciones del servidor.

## Arquitectura

El cliente está implementado con React y Vite. El servidor utiliza Express y tRPC; la persistencia se gestiona mediante Drizzle ORM. El esquema se encuentra en `drizzle/schema.ts` y la migración inicial en `drizzle/0000_low_living_lightning.sql`. Los helpers de base de datos están en `server/db.ts`, mientras que los procedimientos están en `server/routers.ts`.

## Instalación y ejecución

Requisitos: Node.js 22 o compatible, pnpm y una base de datos MySQL/TiDB configurada mediante las variables de entorno del proyecto.

```bash
pnpm install
pnpm check
pnpm test
pnpm build
pnpm dev
```

No se incluyen secretos, archivos `.env`, `node_modules`, `dist` ni logs del entorno local. En el entorno, las variables requeridas se inyectan mediante la configuración del proyecto.

## Evidencias

La documentación completa de la Actividad 5 está en `Actividad5_AulaTrack.md`. El manifiesto de entrega está en `ENTREGA_ACTIVIDAD5.txt`. Las pruebas de autorización, validación y ciclo CRUD están en `server/aulaTrack.test.ts`; las pruebas automatizadas ejecutadas en la entrega aprobaron cinco casos.

La carpeta también conserva `Evidencias_Actividad4.md` como antecedente de la continuidad del proyecto desde la programación del lado del cliente.

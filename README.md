# technoshop-app

Aplicación de la tienda online de TechnoShop SRL (laboratorio). Contiene el código
de la API y los archivos para empaquetarla y ejecutarla en contenedores Docker.

## Estructura (prevista)

- `app/` – Código de la aplicación de e-commerce (API en Python con FastAPI).
- `Dockerfile` – Archivo para la construcción de una imagen personalizada de la aplicación.
- `docker-compose.yml` – Archivo de configuración para definir y correr la aplicación
  junto con los servicios que necesita (PostgreSQL, Redis) en múltiples contenedores.

## Entornos

- Staging: APP01 (on-prem, red de servidores).
- Producción: WEB01 (nube simulada).

## Reglas del repo

- No se suben secretos (contraseñas, tokens, claves). Se usan variables de entorno.
- Todo cambio entra por Pull Request; no se hacen cambios directos en `main`.
- La infraestructura se gestiona en el repo `technoshop-infra`.

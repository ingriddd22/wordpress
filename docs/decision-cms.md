# Decisión de Imagen y Versión de WordPress

## 1. Requisitos oficiales de WordPress
- **PHP:** Versión recomendada PHP 7.4 o superior (recomendado PHP 8.2+).
- **Base de Datos:** MySQL 8.0+ o MariaDB 10.5+.
- **HTTPS:** Recomendado para entornos de producción.

## 2. Elección de la imagen de Docker
- **Imagen seleccionada:** `wordpress:7.1-php8.3-fpm`
- **Diferencia entre variante Apache y FPM:**
  - `apache`: Incluye el servidor web y PHP en un mismo contenedor.
  - `fpm`: Incluye únicamente el servicio de procesamiento PHP (FastCGI), requiriendo un servidor web externo. Ofrece mejor rendimiento y modularidad.
- **Significado de php8.3:** Garantiza el uso de la rama 8.3 de PHP.
- **Razón para evitar 'latest':** Se evita `latest` para asegurar la reproducibilidad del entorno y prevenir fallos imprevistos por actualizaciones automáticas.

## 3. Verificación de requisitos
- Versión de PHP confirmada: PHP 8.3.x.
- Módulos confirmados en el contenedor: `mysqli`, `gd`, `zip`, `intl` e `imagick`.

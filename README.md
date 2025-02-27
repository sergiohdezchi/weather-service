# Weather App

Este proyecto consta de dos aplicaciones:
- **weather-service**: Backend en Ruby on Rails con PostgreSQL y Redis.
- **weather-webapp**: Frontend en React con Vite y TypeScript.

## Requisitos
Asegúrate de tener instalados los siguientes requisitos antes de continuar:
- Ruby 3.4.1
- Bundler
- PostgreSQL
- Redis
---

## Variables de Entorno
Crea un archivo `.env` en la raíz del proyecto con las siguientes variables:

```ini
# Backend (weather-service)
DATABASE_HOST=
DATABASE_USERNAME=
DATABASE_PASSWORD=
DATABASE_NAME=weather_service
OPENWEATHER_API_KEY=
FORECAST_CNT=
REDIS_URL=redis://localhost:6379/0

```

---

## Instalación y ejecución del backend (`weather-service`)

1. **Clonar el repositorio**
   ```sh
   git clone https://github.com/sergiohdezchi/weather-service.git
   cd weather-service
   ```

2. **Instalar las dependencias**
   ```sh
   bundle install
   ```

3. **Configurar la base de datos**
   ```sh
   rails db:create db:migrate db:seed
   ```

4. **Ejecutar Redis (si no está en ejecución)**
   ```sh
   redis-server
   ```

5. **Iniciar el servidor**
   ```sh
   rails server
   ```

El backend estará disponible en `http://localhost:3000`

---

## Notas adicionales
- Asegúrate de que PostgreSQL y Redis estén en ejecución antes de iniciar `weather-service`.

Si tienes problemas, revisa los logs de cada servicio o ejecuta los comandos con más verbosidad (`bundle exec rails server --debug`).

## Notas sobre IA
Durante la elaboración de este proyecto, se utilizaron herramientas de inteligencia artificial para optimizar el proceso de desarrollo:

- GitHub Copilot fue de gran utilidad para la generación de código, sugerencias de sintaxis y autocompletado en diversas secciones del proyecto.
- ChatGPT fue empleado principalmente para resolver problemas de configuración, depuración de errores y obtención de explicaciones técnicas en distintos contextos del desarrollo.

El uso de estas herramientas permitió acelerar el desarrollo y mejorar la eficiencia en la escritura de código y configuración del entorno. Sin embargo, todas las decisiones finales fueron revisadas y validadas manualmente para garantizar la calidad y coherencia del código.

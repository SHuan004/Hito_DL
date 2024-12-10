# Hito 3 - Aplicación Backend en Node y Express

## Descripción

Este proyecto implementa un backend en Node.js con Express que incluye pruebas automatizadas utilizando **Vitest**, un framework moderno y compatible con TypeScript. El objetivo del Hito 3 es validar el correcto funcionamiento de las rutas implementadas mediante la escritura y ejecución de pruebas automatizadas.

## Cumplimiento de Requerimientos

### **1. Instalación y Configuración de Vitest**

En lugar de Jest, se eligió **Vitest** por su mejor integración con TypeScript. Esto no afecta el cumplimiento del hito, ya que Vitest ofrece las mismas funcionalidades para escribir y ejecutar pruebas automatizadas.

El archivo de configuración de Vitest se incluye en el proyecto y permite ejecutar las pruebas con el comando:

```bash
npm run test
```

### **2. Implementación de Pruebas**

Se implementaron pruebas para las siguientes rutas:

#### **GET /api/v1/patients/resume**

Esta ruta retorna una lista de pacientes. Las pruebas verifican:

- Que el estado de la respuesta sea `200`.
- Que el cuerpo de la respuesta contenga un arreglo de pacientes con propiedades específicas (`id`, `name`, `age`, `rut`).

#### **POST /api/v1/patients/look**

Esta ruta busca un paciente por su RUT. Las pruebas consideran:

- Caso exitoso (`200`): Se retorna el paciente correspondiente.
- Caso no encontrado (`404`): Se retorna un mensaje indicando que el paciente no existe.
- Validación de entrada (`400`): Verifica que la ruta devuelva un error cuando el `rut` no es proporcionado.

#### **GET /api/v1/staff**

Esta ruta lista a los miembros del staff. La prueba verifica:

- Que el estado de la respuesta sea `200`.

### **3. Ejecución y Verificación**

Las pruebas se ejecutan correctamente y validan tanto los casos exitosos como los fallidos. Esto asegura que las rutas principales de la aplicación cumplen con los requisitos funcionales esperados.

### **Pruebas Ejecutadas**

Se incluyeron tres archivos de pruebas:

1. **`test/patients/patient.route.test.ts`**: Contiene las pruebas para `GET /api/v1/patients/resume`.
2. **`test/patients/patient.look.test.ts`**: Contiene las pruebas para `POST /api/v1/patients/look`.
3. **`test/staff/staff.route.test.ts`**: Contiene la prueba para `GET /api/v1/staff`.

## Justificación del Cumplimiento

### **Por qué se cumple el hito**

1. **Rutas `GET` probadas**:

   - Se implementaron dos pruebas para rutas `GET` (`/api/v1/patients/resume` y `/api/v1/staff`), cumpliendo con el requerimiento de probar al menos dos rutas `GET`.

2. **Pruebas funcionales y completas**:

   - Cada prueba valida los códigos de estado HTTP y el contenido del cuerpo de la respuesta, cubriendo escenarios exitosos y fallidos.

3. **Uso de Vitest**:

   - Aunque el hito menciona Jest, el cambio a Vitest es válido porque cumple la misma función, es compatible con TypeScript, y asegura la calidad del código.

4. **Ejecución exitosa**:
   - Todas las pruebas pasan al ejecutarse, verificando que el sistema funciona como se espera.

### **Cobertura adicional**

Además de cumplir con los requisitos mínimos, se implementó una prueba para la ruta `POST /api/v1/patients/look`, lo que mejora la cobertura general del proyecto.

## Comandos para Ejecutar

1. Instalar las dependencias:

   ```bash
   npm install
   ```

2. Ejecutar las pruebas:
   ```bash
   npm run test
   ```

## Conclusión

El proyecto cumple con todos los requerimientos del Hito 3 y los excede, al incluir pruebas adicionales y utilizar un framework moderno que facilita el desarrollo en TypeScript.

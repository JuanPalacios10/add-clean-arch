## Attribute-Driven Design (ADD) y Clean Architecture

### 1. ¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?

ADD es un enfoque de diseño arquitectónico que prioriza cómo las necesidades de calidad de un sistema (como rendimiento o seguridad) impulsan su estructura. Su propósito es crear una arquitectura que satisfaga directamente los atributos de calidad críticos para asegurar que el diseño sea adecuado desde el inicio.

### 2. ¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?

ADD define la estructura de alto nivel impulsada por la calidad (qué arquitectura se necesita), mientras que Clean Architecture proporciona una guía de bajo nivel y un patrón para organizar los componentes internos de esa estructura (cómo implementarla).

### 3. ¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?

1. Elegir el elemento del sistema a diseñar o refinar.
2. Identificar los atributos de calidad y las restricciones.
3. Seleccionar las tácticas arquitectónicas que satisfacen esos atributos.
4. Definir las interfaces y la estructura.
5. Revisar y documentar el diseño.
6. Repetir para otros elementos.

### 4. ¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?

Se identifican mediante escenarios de calidad (ej. "tiempo de respuesta de 3 segundos"), entrevistas con stakeholders y análisis de requisitos. Son importantes porque son los motores de las decisiones arquitectónicas, asegurando que el sistema sea viable y usable en el entorno real.

### 5. ¿Por qué Clean Architecture complementa ADD en la implementación de una solución?

Clean Architecture complementa ADD porque, después de que ADD define la necesidad de un atributo como "alta mantenibilidad", Clean Architecture proporciona el mecanismo de implementación (reglas de dependencia y capas aisladas) que garantiza esa calidad al separar la lógica de negocio de los detalles técnicos volátiles.

### 6. ¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?

- **Regla de Dependencia:** Las dependencias de código siempre deben apuntar hacia el interior (las capas externas dependen de las internas, no al revés).
- **Aislamiento de Volatilidad:** Las capas deben aislar los aspectos que cambian con frecuencia (BD, UI, frameworks) para proteger el núcleo.
- **Separación de Intereses:** Cada capa debe tener una responsabilidad única y bien definida (Entidades, Casos de Uso, etc.).

### 7. ¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?

ADD obliga a traducir las necesidades de negocio (ej. crecimiento rápido) en atributos de calidad específicos (ej. Escalabilidad) y luego seleccionar las tácticas arquitectónicas adecuadas para satisfacerlos. Esto alinea la arquitectura directamente con los objetivos estratégicos del negocio.

### 8. ¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?

- **Claridad de Límites:** ADD define los límites del microservicio según el contexto de calidad, y Clean Architecture define su estructura interna.
- **Mantenibilidad Consistente:** Cada microservicio es internamente limpio y fácil de mantener (gracias a Clean Architecture), cumpliendo un atributo de calidad clave.
- **Coherencia Global:** Asegura que cada servicio cumpla no solo su función, sino también los estándares de calidad (ej. latencia) requeridos por el sistema general.

### 9. ¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?

Se asegura mediante:

- **Evaluación Formal:** Usando metodologías como ATAM (Architecture Tradeoff Analysis Method) para revisar el diseño contra los escenarios de calidad antes de codificar.
- **Pruebas Específicas:** Creando pruebas de carga o seguridad automatizadas para validar los atributos de calidad críticos en el código.
- **Prototipos:** Implementando una porción representativa de la arquitectura para demostrar que las tácticas elegidas funcionan.

### 10. ¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?

- **ATAM:** Metodología formal para evaluar y revisar la arquitectura.
- **Herramientas de Pruebas de Carga:** (JMeter, Gatling) para validar rendimiento y escalabilidad.
- **Análisis Estático de Código:** Para verificar el cumplimiento de las reglas de dependencia de Clean Architecture.
- **Diagramas de Vistas Arquitectónicas (C4):** Para documentar claramente y validar visualmente que la estructura soporta los atributos.

# Tarea: Mi prompt avanzado

## Tarea elegida

Desarrollo de una aplicacón web

## Version 1: prompt basico
```text
Crear una aplicación web que permita buscar habitaciones y tambien permira publicar a los dueños habitaciones disponibles.
```

## Version 2

```text
Eres Desarrollador senior de Java y arquitecto de software Crear una aplicación web que cuente con tres tipos de accesos. El primero para usuarios que permita buscar habitaciones a través de diferentes filtros. Por ultimo, Acceso a los dueños habitaciones para que publiquen sus habitaciones disponibles. 
```

## Version 3: prompt final

```text
<rol>

Actúa como un equipo de cuatro perfiles que trabajan juntos:

1.Desarrollador senior de Java (Java 17, Spring Boot).
2. Project Manager
3. Arquitecto de software (UML, patrones, modelo de datos).

</rol>

<contexto>

Estoy desarrollando una aplicación para alquiler de habitaciones en Perú, principalmente Lima.
Registro/login: el usuario debe ingresar DNI, edad, fecha de nacimiento, correo electrónico y lugar de origen. Valida que la edad sea coherente con la fecha de nacimiento.

</contexto>

<stack_tecnologico>

Define el stack técnologico priorizando la seguridad, incluye Java para el backEnd.

</stack_tecnologico>

<funcionalidades>

Dos roles: USUARIO, PROPIETARIO

USUARIO (busca habitaciones):
Ve un mapa e ingresa la zona donde desea buscar.
Las habitaciones disponibles aparecen como pequeños iconos de casa verde.
Filtros: precio, cercanía, seguridad de la zona, garantia, contrato,baño propio o compartido, servicios incluidos, si se puede cocinar y otros que consideres relevantes.
Ve los comentarios y referencias de la casa y del vecindario, y puede escribir los suyos.

Agenda visitas y chatea con el propietario dentro de la aplicación.
PROPIETARIO (publica habitaciones):
Sube mínimo 4 y máximo 10 fotos por habitación. Es obligatorio incluir al menos una foto del cuarto y una del baño.
Indica: baño propio o compartido, agua, luz, internet y otros servicios (incluidos o no), si se puede cocinar y otros detalles.
Gestiona la programación de visitas y el chat con los usuarios.
</funcionalidades>

<tarea>

Trabaja en las siguientes fases. Entrega UNA fase por respuesta concreta y espera mi mensaje "continuar" antes de pasar a la siguiente.

Fase 1: Requisitos y arquitectura.
Lista de requisitos funcionales y no funcionales, supuestos, riesgos en una tabla.
Fase 2: Diagramas UML.
Entrega en formato imagen entendible y explicativo donde detalles el tipo de relación entre objetos (asociación, agregación, composición, herencia, dependencia) y por qué elegiste cada una.
Fase 3: Código base.
Estructura de carpetas del proyecto y un archivo separado por cada clase (entidades, repositorios, servicios, controladores y la clase Main). I
Fase 4: Interfaz y mapa.
Código de las vistas y paso a paso para ejecutar el proyecto muestrame tambien el link verlo en el navegador.
Fase 5: APIs.
Integra el mapa (ver sección <apis>).
Fase 6: Seguridad y calidad.
Ver sección <seguridad>.
Fase 7: Documento de consideraciones.
Ver sección <consideraciones>.
</tarea>

<razonamiento>

Antes de generar el contenido de cada fase, razona paso a paso y muéstrame un resumen breve de:
(a) qué requisitos de esta fase vas a cubrir,
(b) qué supuestos haces,
(c) qué decisiones de diseño tomas y por qué.
Después entrega el resultado.
</razonamiento>

<apis>

Busca APIs gratuitas (sin tarjeta de crédito) para:
Mapa interactivo

2. Nivel de seguridad de la zona en Lima.
Para cada API indica: nombre, tipo, enlace oficial para verificarla, límites de uso gratuito, términos de uso y cómo configurarla en el proyecto paso a paso.
Si no existe una API gratuita confiable de seguridad para Lima, dilo claramente y propón una alternativa (por ejemplo, un puntaje calculado con los comentarios de los usuarios y datos abiertos verificables). No inventes APIs ni enlaces.
</apis>

<seguridad>
Como no puedes ejecutar pruebas de hacking real, haz una revisión de seguridad del código:

Revisa contra OWASP Top 10: inyección SQL, XSS, CSRF, control de acceso roto, autenticación débil, carga insegura de archivos (fotos) y exposición de datos personales.
Aplica protección de datos personales según la Ley 29733 de Perú.
Entrega pruebas unitarias y de integración con JUnit para las reglas críticas (edad mínima, 4 a 10 fotos, permisos por rol).
Entrega una lista de pruebas de seguridad manuales que yo pueda ejecutar (por ejemplo, con OWASP ZAP, que es gratuito).
Indica qué vulnerabilidades quedan pendientes y su prioridad.
</seguridad>

<autocritica>

Al final de cada fase, antes de entregar:
Revisa tu respuesta contra la lista de requisitos de este prompt y marca cada uno como cumplido, parcial o faltante.
2. Señala errores, ambigüedades o riesgos que encuentres en tu propia entrega.
3. Corrige lo que falte y muestra solo un resumen de las correcciones.
</autocritica> 
```

## Tecnicas usadas en el prompt final

| Técnicas usadas| Detalle|
|--------|:-----------------|
|Zero-shot|Si|
|Chain of Thought|Si|
|Rol prompting|	Si|
|Descomposición|Si|
|Prompt estructurado|Si|
|Autocrítica|Si|

## Evaluacion del resultado

| Qué revisar | Cumple (Sí / No) 
|--------|:-----------------:
| ¿Ejecuto las 7 fases?|Si |
| ¿Ejecuto la API de forma correcta?|No |
| ¿Presento errores y se autocorrigio?|Si |
| ¿Se recomienda crear un software desde cero solo con IA?|No |


## Por que elegí estas tecnicas

Para esta actividad elegí una combinación de técnicas aplicadas para garantizar que las especificaciones iniciales tanto técnicas como de negocio sean más precisas durante el desarrollo de la aplicación. No obstante, aunque este enfoque estructurado funciona como una potente prueba de concepto inicial, considero que no reemplaza por completo el ciclo de vida de un software real en producción, pero si reduce su iteración.
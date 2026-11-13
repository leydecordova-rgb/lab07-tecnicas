# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | Si | En tabla| Si|
| One-shot |Si|Como el ejemplo pero enumerado|Si|
| Few-shot |Si|Como el ejemplo |Si|


## Ejercicio 3: Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo |318.6|No |Si |
| Paso a paso |S/ 318.60 |Si |Si |


## Ejercicio 4: Role prompting

| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol |Sencillo|Si |Principiante|
| B. Rol docente |Sencillo |Si |Estudiante |
| C. Rol senior |Tecnica|Si |Desarrollador|


## Ejercicio 5: Descomposicion

1. Voy a crear un sistema de inventario para una tienda pequena en Java. Lista los 5 requisitos principales del sistema.
2. Con esos requisitos, disena las clases necesarias. Para cada clase indica sus atributos con su tipo de dato.
3. Escribe el codigo Java de la clase Producto con sus atributos, un constructor y los metodos get y set.
4. Revisa el codigo de la clase Producto y propone 3 mejoras concretas.

## Ejercicio 6: Prompt estructurado y autocritica

| Qué revisar | Cumple (Sí / No) 
|--------|:-----------------:
| ¿Tiene las 4 columnas pedidas?|Si |
| ¿Incluye el bloqueo después de 3 intentos? |Si   |
| ¿Incluye casos con campos vacíos?|Si |
| ¿Indica qué casos agregó en la autocrítica?|Si  |
| ¿Hay algún caso repetido o que no tenga sentido?|No |

```text
PROMT ESTRUCTURADO:

<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea
despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada,
resultado esperado.</formato>

AUTOCRÍTICA:

Al revisar la tabla anterior, el CP-05 mezclaba el correo sin @ con la contraseña vacía en un solo caso (lo cual es una mala práctica en QA porque un fallo oculta al otro), y faltaba por completo el caso de contraseña con espacios.

Para aislar cada condición de borde correctamente, desglosé el antiguo CP-05 y agregué los casos límite individuales:

Agregados / Desglosados:

CP-05 (Ajustado): Exclusivo para ambos campos vacíos.

CP-06 (Nuevo): Exclusivo para correo sin @ (con contraseña válida para aislar la validación de formato).

CP-07 (Nuevo): Exclusivo para contraseña con espacios en blanco (al inicio y al final, para verificar que el sistema no haga un trim automático indebido o rompa la autenticación).

CP-08 (Renumerado): El caso anterior de correo no registrado pasa a ser el CP-08.

```

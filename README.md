# Ejercicio-7

Ejercicio 7: Pregunta en Java (Metodología Waterfall)
1. Requisitos (Requirements)
El programa tiene que mostrar una pregunta por consola con cuatro opciones (a, b, c, d) sobre qué lenguaje de programación estamos usando. Luego lee lo que escribe el usuario por teclado y le dice si ha acertado, si ha fallado (indicando cuál era la correcta) o si ha puesto una letra que no vale.

2. Diseño (Design)
Para no complicar el código, se ha planteado usar un Scanner para leer la respuesta, guardarla en un String y comprobar qué letra es usando un bloque if / else if / else. Así evitamos meter bucles innecesarios y cualquier cosa que no sea a, b, c o d cae directo al final como no válida.

3. Implementación (Implementation)
Este es el código final en Java (ej7.java):

Java
void main() {
    Scanner sc = new Scanner(System.in);

    System.out.println("Que lenguaje estmos usando?"); //a, b, c, d
    System.out.println("a. python");
    System.out.println("b. HTML");
    System.out.println("c. Java");
    System.out.println("d. C++");

    String respuesta = sc.nextLine();

    if (respuesta.equals("c")) {
        System.out.println("Respuesta correcta!");
    } else if (respuesta.equals("a") || respuesta.equals("b") || respuesta.equals("d")) {
        System.out.println("Respuesta incorrecta, la respuesta correcta es la C.");
    } else {
        System.out.println("Respuesta no valida.");
    }
}
4. Verificación (Verification)
Se han hecho varias pruebas ejecutando el programa desde la consola para ver que todo responde bien:

Si meto c, sale "Respuesta correcta!".

Si meto a, b o d, avisa de que es incorrecta y dice que la buena es la C.

Si meto otra letra distinta (como f o o), salta el else y muestra "Respuesta no valida.".

5. Mantenimiento (Maintenance)
Si más adelante hubiera que ampliar el ejercicio, se podría hacer que acepte tanto mayúsculas como minúsculas (por ejemplo con .equalsIgnoreCase()) o meter varias preguntas seguidas usando arrays.

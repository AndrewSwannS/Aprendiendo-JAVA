# Aprendiendo-JAVA
En ese repositorio, practico y y aprendo JAVA
Calculadora 

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package calculadora;

import java.util.Scanner;

/**
 *
 * @author super
 */
public class Calculadora {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here

        String user = "cami";
        String pass = "12345";

        Scanner scanner = new Scanner(System.in);

        // LOGIN
        while (true) {
            System.out.println("Inserte su nombre de usuario:");
            String inputUsuario = scanner.nextLine();

            System.out.println("Ingrese su contraseña:");
            String inputContrasena = scanner.nextLine();

            if (inputUsuario.equals(user) && inputContrasena.equals(pass)) {
                System.out.println("Inicio de sesión exitoso\n");
                break;
            } else {
                System.out.println("Usuario o contraseña incorrectos\n");
            }
        }

        int opcion;

        do {
            double num1, num2, total;

            System.out.println("""
            Seleccione la operación:
            1. Suma
            2. Resta
            3. Multiplicación
            4. División
            5. Potencia
            6. Raíz 
            7. Seno
            8. Coseno
            9. Tangente
            10. Salir
            """);

            opcion = scanner.nextInt();

            switch (opcion) {

                case 1:
                    System.out.print("Ingrese el primer número: ");
                    num1 = scanner.nextDouble();
                    System.out.print("Ingrese el segundo número: ");
                    num2 = scanner.nextDouble();
                    total = num1 + num2;
                    System.out.println("Resultado: " + total);
                    break;

                case 2:
                    System.out.print("Ingrese el primer número: ");
                    num1 = scanner.nextDouble();
                    System.out.print("Ingrese el segundo número: ");
                    num2 = scanner.nextDouble();
                    total = num1 - num2;
                    System.out.println("Resultado: " + total);
                    break;

                case 3:
                    System.out.print("Ingrese el primer número: ");
                    num1 = scanner.nextDouble();
                    System.out.print("Ingrese el segundo número: ");
                    num2 = scanner.nextDouble();
                    total = num1 * num2;
                    System.out.println("Resultado: " + total);
                    break;

                case 4:
                    System.out.print("Ingrese el primer número: ");
                    num1 = scanner.nextDouble();
                    System.out.print("Ingrese el segundo número: ");
                    num2 = scanner.nextDouble();
                    if (num2 != 0) {
                        total = num1 / num2;
                        System.out.println("Resultado: " + total);
                    } else {
                        System.out.println("No se puede dividir entre cero");
                    }
                    break;

                case 5:
                    System.out.print("Base: ");
                    num1 = scanner.nextDouble();
                    System.out.print("Exponente: ");
                    num2 = scanner.nextDouble();
                    System.out.println("Resultado: " + Math.pow(num1, num2));
                    break;

                case 6:
                    System.out.print("Ingrese el número: ");
                    num1 = scanner.nextDouble();

                    System.out.print("Ingrese el índice de la raíz: ");
                    num2 = scanner.nextDouble();

                    total = Math.pow(num1, 1.0 / num2);
                    System.out.println("Resultado: " + total);
                    break;
                 
                case 7:
                    System.out.print("Ángulo en grados: ");
                    num1 = scanner.nextDouble();
                    System.out.println("Seno: " + Math.sin(Math.toRadians(num1)));
                    break;

                case 8:
                    System.out.print("Ángulo en grados: ");
                    num1 = scanner.nextDouble();
                    System.out.println("Coseno: " + Math.cos(Math.toRadians(num1)));
                    break;

                case 9:
                    System.out.print("Ángulo en grados: ");
                    num1 = scanner.nextDouble();
                    System.out.println("Tangente: " + Math.tan(Math.toRadians(num1)));
                    break;

                case 10:
                    System.out.println("Saliendo del programa...");
                    break;

                default:
                    System.out.println("Opción inválida");
            }

        } while (opcion != 10);
    }
}

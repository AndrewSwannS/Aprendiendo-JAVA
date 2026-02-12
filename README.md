# Aprendiendo-JAVA
En ese repositorio, practico y y aprendo JAVA
Calculadora 


package calculadora.con.ciclos;

import java.util.Scanner;

public class CalculadoraConCiclos {

    public static void main(String[] args) {
        
        String texto1 = "Inserte el primer número: ";
        String texto2 = "Inserte el segundo número: ";
        String operacion = "Inserte el operador matemático (+,-,/,*,p,r,t,s,c): ";

        
        int num1;
        int num2 = 0;
        char signo;
        char continuar;
        
        Scanner escanner = new Scanner(System.in);
        
        do {            
            System.out.println(texto1);
            num1 = escanner.nextInt();
            
            System.out.println(operacion);
            signo = escanner.next().charAt(0);
            
            if (signo != 'r' && signo != 'R' &&
    signo != 't' && signo != 'T' &&
    signo != 's' && signo != 'S' &&
    signo != 'c' && signo != 'C') {
    
    System.out.println(texto2);
    num2 = escanner.nextInt();
}

            
            switch (signo) {
                
                case '+':
                    System.out.println("El resultado es: " + (num1 + num2));
                    break;
                    
                case '-':
                    System.out.println("El resultado es: " + (num1 - num2));
                    break;
                    
                case '*':
                    System.out.println("El resultado es: " + (num1 * num2));
                    break;
                    
                case '/':
                    if (num2 != 0) {
                        System.out.println("El resultado es: " + ((double) num1 / num2));
                    } else {
                        System.out.println("No se puede dividir entre 0");
                    }
                    break;
                
                case 'p':
                case 'P':
                    System.out.println("Resultado: " + Math.pow(num1, num2));
                    break;

                case 'r':
                case 'R':
                    System.out.println("La raíz cuadrada es: " + Math.sqrt(num1));
                    break;
                
                case 't':
                case 'T':
                    System.out.println("Resultado: " + Math.tan(Math.toRadians(num1)));
                    break;
                    
                case 's':
                case 'S':
                    System.out.println("Resultado: " + Math.sin(Math.toRadians(num1)));
                    break;
                    case 'c':
                    case 'C':
                        System.out.println("Resultado: " + Math.cos(Math.toRadians(num1)));
                    break;

                default:
                    System.out.println("Operación incorrecta");
            }
            
            System.out.println("¿Desea continuar? (s/n)");
            continuar = escanner.next().charAt(0);
            
        } while (continuar == 's' || continuar == 'S');
        
        escanner.close();
    }
}


# actividad-2
Código 
Clase Promedio

package actividad2;

import java.util.Scanner;
public class Promedio {
Scanner leer=new Scanner(System.in); //Se crean las variables y array a usar 
double [] calificaciones = new double [5];
double R,Suma;
String name;


public void inicializar (){ //Se coloca el nombre y se va llenando el arreglo con las notas
System.out.println("Ingrese nombre: ");
name=leer.next();
for(int i=0; i<5;i++){
System.out.println("Ingrese la calificacion "+(i+1)+":");
   calificaciones[i] = leer.nextInt();
   Suma += calificaciones [i]; 

}

}

public void Calcular(){ //Calcula el promedio de las notas
R=Suma/5;
}

public void imprimir(){ //Imprime los valores de acuerdo a la condición
System.out.println("El promedio es "+ R);
if (R<=50) {
System.out.println ("Nota = F");
}
else if (R<=60) {
System.out.println ("Nota = E");
}
else if (R<=70) {
System.out.println ("Nota = D");
}
else if (R<=80) {
System.out.println ("Nota = C");
}
else if (R<=90) {
System.out.println ("Nota = B");
}
else if (R<=100) {
System.out.println ("Nota = A");
}
System.out.println("Alumno:" + name);
}
    
}






Clase Principal

package actividad2;


public class Principal {
    public static void main(String[] args) {
        Promedio objeto1= new Promedio(); //Se instancia el objeto del tipo Promedio
//Se llaman a los métodos
objeto1.inicializar();
objeto1.Calcular();
objeto1.imprimir();
    }
    

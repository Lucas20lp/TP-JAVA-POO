# TP-JAVA-POO
TP Pulido Lucas 

(PUNTO 1)

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {


        int notas[] = new int[5];
        Scanner teclado = new Scanner (System.in);

        for (int i=0; i<notas.length; i++){
            System.out.println("Ingrese la nota en el indide " + i + ":");
            notas[i] = teclado.nextInt();
        }

        for (int i=0; i<notas.length; i++) {
            System.out.println("La nota es " + notas[i]);
            System.out.println("-----------------------");
        }
        int suma = 0;
        int notaMax = notas[0];

        for (int i = 0; i < notas.length; i++) {
            suma += notas[i];

                if (notas[i] > notaMax) {
                    notaMax = notas[i];
                }
        }
        double promedio = (double) suma / notas.length;

        System.out.println("La nota mas alta es: " + notaMax);
        System.out.println("El promedio es: " + promedio);

    }
}






(PUNTO 2)




import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        int notas[] = new int[3];
        Scanner teclado = new Scanner(System.in);

        for (int i = 0; i < notas.length; i++) {
            System.out.print("Ingrese la nota en el índice " + i + ": ");
            notas[i] = teclado.nextInt();
        }

        System.out.println("\nResultados:");
        for (int i = 0; i < notas.length; i++) {
            if (notas[i] >= 6) {
                System.out.println("Nota en el índice " + i + " (" + notas[i] + "): Aprobado");
            } else {
                System.out.println("Nota en el índice " + i + " (" + notas[i] + "): Desaprobado");
            }
        }
    }
}







(PUNTO 3)

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese la cantidad de productos: ");
        int n = scanner.nextInt();

        int[] cantidad = new int[n];
        double[] costos = new double[n];

        for (int i = 0; i < n; i++) {
            System.out.println("Cantidad del producto " + (i + 1) + ": ");
            cantidad[i] = scanner.nextInt();

            System.out.println("Costo unitario del producto " + (i + 1) + ":");
            costos[i] = scanner.nextDouble();
        }

        double precioTotal = 0;

        System.out.println("\nProductos con precio individual total mayor a 1000");

        for (int i = 0; i < n; i++) {

            double totalProductos = cantidad[i] * costos[i];
            precioTotal += totalProductos;

            if (totalProductos > 1000) {
                System.out.println("Producto " + (i + 1) + ":" + totalProductos);
            }
        }
        System.out.println("\nPrecio total de todos los productos: $" + precioTotal);

    }
}



(PUNTO 4)


import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);

        
        //Lo hice a 3 camiones, por que se hace eterno en la onsola poner los datos :)
        
        String[] patentes = new String[3];
        String[] choferes = new String[3];
        String[] tiposCarga = new String[3];
        String[] horasEgreso = new String[3];
        int cantidadTe = 0;


        for (int i = 0; i < 3; i++) {
            System.out.println("Camión " + (i + 1));

            System.out.print("Ingrese la patente: ");
            patentes[i] = teclado.nextLine();

            System.out.print("Ingrese el nombre y apellido del chofer: ");
            choferes[i] = teclado.nextLine();

            System.out.print("Ingrese el tipo de carga (madera, yerba o te): ");
            tiposCarga[i] = teclado.nextLine();

            if (tiposCarga[i].equalsIgnoreCase("te")) {
                cantidadTe++;
            }

            System.out.print("Ingrese la hora de egreso: ");
            horasEgreso[i] = teclado.nextLine();

            System.out.println();
        }


        System.out.println("---- Datos de los camiones ----");
        for (int i = 0; i < 3; i++) {
            System.out.println("Camión " + (i + 1));
            System.out.println("Patente: " + patentes[i]);
            System.out.println("Chofer: " + choferes[i]);
            System.out.println("Tipo de carga: " + tiposCarga[i]);
            System.out.println("Hora de egreso: " + horasEgreso[i]);
            System.out.println("-----------------------------");
        }


        System.out.println("Cantidad de camiones que cargaron té: " + cantidadTe);
    }
}



(PUNTO 5)


import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);


        int[] dnis = new int[5];
        int[] tipoServicio = new int[5];
        double[] montoPagar = new double[5];


        for (int i = 0; i < 5; i++) {
            System.out.println("Cliente " + (i + 1));


            System.out.print("Ingrese el DNI del cliente: ");
            dnis[i] = teclado.nextInt();


            System.out.print("Ingrese el tipo de servicio (1: 30 megas, 2: 50 megas, 3: 100 megas): ");
            tipoServicio[i] = teclado.nextInt();


            if (tipoServicio[i] == 1) {
                montoPagar[i] = 750;
            } else if (tipoServicio[i] == 2) {
                montoPagar[i] = 1100;
            } else if (tipoServicio[i] == 3) {
                montoPagar[i] = 1500 - (1500 * 0.05);
            } else {
                System.out.println("Tipo de servicio inválido. Se colocará monto 0.");
                montoPagar[i] = 0;
            }

            System.out.println();
        }


        System.out.println("---- Facturas de Clientes ----");
        for (int i = 0; i < 5; i++) {
            System.out.println("Cliente " + (i + 1));
            System.out.println("DNI: " + dnis[i]);
            System.out.println("Tipo de servicio: " + tipoServicio[i]);
            System.out.println("Monto a pagar: $" + montoPagar[i]);
            System.out.println("------------------------------");
        }
    }
}




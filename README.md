# Projetos
//Projetos//

import java.util.Scanner; 
public class SubRotinas { 
 static int opcao = 3; 
 static int[] a = new int[5]; 
 static int[] b = new int[5]; 
 static int[] c = new int[5]; 
 static int i; 
 static Scanner ler = new Scanner(System.in); 
 public static void menu() { 
 while (opcao != 0) { 
 System.out.println("--------- MENU -------");  System.out.println("| 1-Ler vetor de A |");  System.out.println("| 2-Ler vetor de B |");  System.out.println("| 3-Imprimir vetores |");  System.out.println("| 0-Encerrar programa|");  System.out.println("--------- **** -------");  System.out.print("Digite a opcao desejada: \n>>"); 
 opcao = ler.nextInt(); 
 while (opcao < 0 || opcao > 3) { 
 System.out.println("Essa opcao nao existente!");  System.out.println("Digite novamente!");  opcao = ler.nextInt(); 
 } 
 if (opcao == 1) { 
 ler_vetor(a); 
 operacoes_matematica(); 
 } else if (opcao == 2) { 
 ler_vetor(b); 
 operacoes_matematica(); 
 } else if (opcao == 3) { 
 System.out.print("Vetor A: "); 
 for (i = 0; i < a.length; i++) { 
 System.out.print(a[i] + " ");  } 
 System.out.println(); 
 System.out.print("Vetor B: "); 
 for (i = 0; i < a.length; i++) { 
 System.out.print(b[i] + " ");  } 
 System.out.println(); 
 System.out.print("Vetor C: "); 
 for (i = 0; i < a.length; i++) { 
 System.out.print(c[i] + " ");  } 
 System.out.println(); 
 } 
 }
 } 
 public static void ler_vetor(int[] aux) { 
 for (i = 0; i < aux.length; i++) { 
 System.out.println("Digite o " + (i + 1) + " valor do vetor");  aux[i] = ler.nextInt(); 
 } 
 } 
 public static void operacoes_matematica() { 
 for (i = 0; i < c.length; i++) { 
 if (a[i] % 2 == 0) { 
 c[i] = a[i] + b[i]; 
 } else { 
 c[i] = (int) Math.pow(a[i], b[i]); 
 } 
 } 
 } 
 public static void main(String[] args) throws Exception {  menu(); 
 } 
}

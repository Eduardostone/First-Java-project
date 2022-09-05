# First-Java-project
import java.util.Scanner;

public class Classeaula2_1 {

	public static void main(String[] args) {
		
				Scanner entCaractere = new Scanner(System.in);
				Scanner entNumeros = new Scanner(System.in);
				char operacao = ' ';
				int[] numeros = new int [1000];
				int i = 0 ;int somatorio = 0;int contapares = 0;
				double media = 0;
				
				do {
					System.out.printf("Menu de opções.\n"
							+ "D - para digitar novos numeros.\n"
							+ "Z - para apresentar o somatório dos números (Todos).\n"
							+ "V - para visualizar todos os números digitados.\n"
							+ "P- para a quantidade de numeros digitados. \n"
							+ "M - para a média simples de números digitados. \n"
							+ "Q - para a quantidade de pares.\n"
							+ "S - sair");
					operacao = entCaractere.nextLine().charAt(0);
					
					switch(operacao){
						case 'D':
							System.out.println("Digite o número desejado: \n");
							numeros[i] = entNumeros.nextInt();
							i++;
							break;
						case 'Z':
							for (int j = 0; j < i;j++) {
								somatorio = somatorio + numeros[j];
					
							}
							System.out.printf("O somatório dos números é: %d\n", somatorio);
							break;
						case 'V':
							for (int j = 0; j < i;j++) {
								System.out.printf("%d\n",numeros [j]);
							}
							break;
						case 'P': 
							System.out.printf("Foram digitados %d números. \n",i );
							break;
						case 'M':
							for (int j = 0; j < i;j++) {
								somatorio = somatorio + numeros[j];
							}
							media= somatorio / i;
							System.out.printf("A média é: %.2f.\n",media);
							break;
						case'Q': 
							for (int j = 0; j < i;j++) {
								if (numeros[j]%2 ==0)
									contapares = contapares +1;
							}
							System.out.printf ("Quantidade de números pares: %d.\n", contapares);
							break;
						case 'S':
							break;
							default:
								System.out.printf ("Opção inválida\n");
								
				}

			}while(operacao != 'S');
				System.out.println ("Fim da operação\n");
			}

# Atividade Lógica de Programação Java
---------
##### *Ramirez Marques*
---
##### *Parte 1: Condicional While*



**01 - Leia uma quantidade indeterminada de duplas de valores inteiros X e Y.
Escreva para cada X e Y uma mensagem que indique se estes valores foram
digitados em ordem crescente ou decrescente. O programa deve finalizar quando
forem digitados dois valores iguais.**

```package exercisios;
import java.util.Scanner;
public class While_1 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite 2 Numeros Inteiros: ");
		int x = sc.nextInt();
		int y = sc.nextInt();
		while (x != y) {
			if (x < y) {
				System.out.println("Cresente!");
			} else {
				System.out.println("Decresente!");
			}
			System.out.println("Digite 2 Numeros Inteiros: ");
			x = sc.nextInt();
			y = sc.nextInt();
		}
		System.out.println("Valores Iguais!!");
		sc.close();
	}
}
```
**02 - Faça um programa para ler um número indeterminado de dados, contendo cada
um, a idade de um indivíduo. O último dado, que não entrará nos cálculos, contém
um valor de idade negativa. Calcular e imprimir a idade média deste grupo de
indivíduos. Se for entrado um valor negativo na primeira vez, mostrar a mensagem
"IMPOSSIVEL CALCULAR".**

```package exercisios;
import java.util.Scanner;
public class While_2 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite as Idades: ");
		int idade = sc.nextInt();
		int soma = 0;
		int qtd = 0 ;
		while (idade >= 0) {
			
			soma += idade ;
			qtd ++;
			idade = sc.nextInt();
			
		}
			if (qtd > 0) {
				double media = soma/ qtd;
				System.out.printf("Média = %.2f", media);	
		} 		else {
					System.out.println("Idade Inválida");		
		}	
		sc.close();
	}
}
```
**03 - Escreva um programa que repita a leitura de uma senha até que ela seja válida.
Para cada leitura densenha incorreta informada, escrever a mensagem "Senha
Inválida! Tente novamente:". Quando a senha for informada corretamente deve ser
impressa a mensagem "Acesso Permitido" e o algoritmo encerrado. Considere que
a senha correta é o valor 2002.**
```package exercisios;
import java.util.Scanner;
public class While_3 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Informe a Senha de Quatro Digitos: ");
		int senha = sc.nextInt();
		while (senha != 2002) {
			System.out.println("Senha Inválida!");
			System.out.println("Digite sua Senha Novamente: ");
			senha = sc.nextInt();
		}
		System.out.println("Acesso Permitido!");	
		sc.close();
	}
}
```
**04 - Escreva um programa para ler as coordenadas (X,Y) de uma quantidade
indeterminada de pontos no sistema cartesiano. Para cada ponto escrever o
quadrante a que ele pertence (Q1, Q2, Q3 ou Q4). O algoritmo será encerrado
quando pelo menos uma de duas coordenadas for NULA (nesta situação sem
escrever mensagem alguma).**
```package exercisios;
import java.util.Scanner;
public class While_4 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Informe 2 Cordenadas de um Plano Cartesiano: ");
		int x = sc.nextInt();
		int y = sc.nextInt();
		while (x != 0 && y != 0) {
			if (x > 0 && y > 0) {
				System.out.println("Quadrante 1!");
			} else if (x < 0 && y > 0) {
				System.out.println("Quadrante 2!");
			} else if (x < 0 && y < 0) {
				System.out.println("Quadrante 3!");
			} else {
				System.out.println("Quadrante 4!");
			}
			System.out.println("Informe 2 Cordenadas de um Plano Cartesiano: ");
			x = sc.nextInt();
			y = sc.nextInt();
		}
		sc.close();
	}
}
```
**05 - Faça um programa que leia as notas referentes às duas avaliações de um
aluno. Calcule e imprima a média semestral. Faça com que o algoritmo só aceite
notas válidas (uma nota válida deve pertencer ao intervalo [0,10]). Cada nota deve
ser validada separadamente.**
```package exercisios;
import java.util.Scanner;
public class While_5 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Informe a Primeira Nota: ");
		double n1 = sc.nextDouble();
		while (n1 < 0 || n1 > 10) {
			System.out.println("Valor da N1 Inválido! Digite Novamente: ");
			n1 = sc.nextDouble();
		}
		System.out.println("Informe a Segunda Nota: ");
		double n2 = sc.nextDouble();
		while (n2 < 0 || n2 > 10) {
			System.out.println("Valor da N2 Inválido! Digite Novamente: ");
			n2 = sc.nextDouble();
		}
		double media = (n1+n2)/2;
		System.out.printf("Média do Aluno: %.2f",media);
		sc.close();
	}
}
```
**06 - Um posto de combustíveis deseja determinar qual de seus produtos tem a
preferência de seus clientes. Escreva um algoritmo para ler o tipo de combustível
abastecido (codificado da seguinte forma: 1. Álcool 2. Gasolina 3. Diesel 4. Fim).
Caso o usuário informe um código inválido (fora da faixa de 1 a 4) deve ser solicitado
um novo código (até que seja válido). O programa será encerrado quando o código
informado for o número 4, devendo então mostrar a mensagem "MUITO
OBRIGADO", bem como as quantidades de cada combustível.**
```ackage exercisios;
import java.util.Scanner;
public class While_6 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int alcool = 0;
		int gasolina = 0;
		int diesel = 0;
		System.out.println("Informe o Código do combustível: ");
		int cod = sc.nextInt();
		while (cod < 1 || cod > 4) {
			System.out.println("Código Inválido! Favor Digíte Novamente: ");
			cod = sc.nextInt();
		
		while (cod >=1 && cod <= 3) {
			if (cod == 4) {
				System.out.println("Muito Obrigado!");
			}
			else if (cod == 2) {
				gasolina ++;
			}
			else if (cod == 1){
				diesel ++;
			}
			else
				alcool ++;
		
			System.out.println("Informe o Código do combustível: ");
			cod = sc.nextInt();	
		}}
		System.out.println("Muito Obrigado!");
		System.out.println("Alcool: "+ alcool);
		System.out.println("Gasolina: "+ gasolina);
		System.out.println("Diesel: "+ diesel);
		sc.close();
	}
}
```
**07 - O programa deve ler um valor inteiro X indefinidas vezes. (O programa irá parar
quando o valor de X for igual a 0). Para cada X lido, imprima a soma dos 5 pares
consecutivos a partir de X, inclusive o X, se for par. Se o valor de entrada for 4, por
exemplo, a saída deve ser 40, que é o resultado da operação: 4+6+8+10+12,
enquanto que se o valor de entrada for 11, por exemplo, a saída deve ser 80, que é
a soma de 12+14+16+18+20.**
```package exercisios;
import java.util.Scanner;
public class While_7 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite um numero inteiro: ");
		int x = sc.nextInt();
		int soma = 0;
		while (x != 0) {
			if (x % 2 == 0) {
				soma = x * 5 + 20;
			} else {
				soma = (x + 1) * 5 + 20;
			}
			System.out.println("Soma = " + soma);
			System.out.println("Digite um numero inteiro: ");
			x = sc.nextInt();
		}
		sc.close();
	}
}
```

# Final da Lista!!!



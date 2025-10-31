import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        double[] notas = new double[8];
        
        System.out.println("=== SISTEMA DE NOTAS ANUAIS ===");
        
        // Entrada das 8 notas
        for (int i = 0; i < 8; i++) {
            System.out.print("Digite a nota " + (i + 1) + ": ");
            notas[i] = entrada.nextDouble();
        }
        
        // Cálculo das médias bimestrais
        double bimestre1 = notas[0];
        double bimestre2 = notas[1];
        double bimestre3 = notas[2];
        double bimestre4 = notas[3];
        double bimestre5 = notas[4];
        double bimestre6 = notas[5];
        double bimestre7 = notas[6];
        double bimestre8 = notas[7];
        
        // Cálculo das médias semestrais
        double semestre1 = (bimestre1 + bimestre2 + bimestre3 + bimestre4) / 4;
        double semestre2 = (bimestre5 + bimestre6 + bimestre7 + bimestre8) / 4;
        
        // Cálculo da média final
        double mediaFinal = (semestre1 + semestre2) / 2;
        
        // Exibição dos resultados
        System.out.println("\n=== RESULTADOS ===");
        System.out.println("Práticas");
        System.out.printf("1º Bimestre: %.1f%n", bimestre1);
        System.out.printf("2º Bimestre: %.1f%n", bimestre2);
        System.out.printf("3º Bimestre: %.1f%n", bimestre3);
        System.out.printf("4º Bimestre: %.1f%n", bimestre4);
        System.out.printf("1º Semestre: %.1f%n", semestre1);
        System.out.println("----------------------");
        System.out.printf("5º Bimestre: %.1f%n", bimestre5);
        System.out.printf("6º Bimestre: %.1f%n", bimestre6);
        System.out.printf("7º Bimestre: %.1f%n", bimestre7);
        System.out.printf("8º Bimestre: %.1f%n", bimestre8);
        System.out.printf("2º Semestre: %.1f%n", semestre2);
        System.out.println("----------------------");
        System.out.printf("Média Final: %.1f%n", mediaFinal);
        
        entrada.close();
    }
}

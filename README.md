📘 RESUMO COMPLETO DE JAVA PARA PROVA

🔹 1. Sintaxe Básica do Java
public class Main {
    public static void main(String[] args) {
        System.out.println("Olá, mundo!");
    }
}

Pontos importantes:
Todo código fica dentro de uma classe
main é o ponto de entrada
System.out.println() imprime na tela

🔹 2. Tipos de Dados
int idade = 20;
double salario = 1500.50;
char letra = 'A';
boolean ativo = true;
String nome = "Mateus";


🔹 3. Estruturas de Controle
IF
if (idade >= 18) {
    System.out.println("Maior de idade");
} else {
    System.out.println("Menor de idade");
}

FOR
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}

WHILE
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}


🔹 4. Classes e Objetos
Criando uma classe
public class Pessoa {
    String nome;
    int idade;

    void falar() {
        System.out.println("Olá!");
    }
}

Criando objeto
Pessoa p1 = new Pessoa();
p1.nome = "João";
p1.idade = 20;
p1.falar();

Construtor
public class Pessoa {
    String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }
}


🔹 5. Encapsulamento (GET e SET)
public class Pessoa {
    private String nome;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }
}


🔹 6. Strings (MUITO COBRADO)
String nome = "Mateus";

nome.length();          // tamanho
nome.toUpperCase();     // MAIÚSCULO
nome.toLowerCase();     // minúsculo
nome.charAt(0);         // pega letra
nome.contains("te");   // verifica
nome.equals("Mateus"); // comparação correta

⚠️ Nunca use == para comparar String!

🔹 7. ArrayList (ESSENCIAL)
Import
import java.util.ArrayList;

Criando
ArrayList<String> lista = new ArrayList<>();

Principais métodos
lista.add("A");        // adiciona
lista.add("B");

lista.get(0);          // acessa

lista.set(0, "X");    // altera

lista.remove(1);       // remove por índice
lista.remove("X");    // remove por valor

lista.size();          // tamanho

lista.contains("A");  // verifica

lista.clear();         // limpa tudo

Percorrendo ArrayList
for (int i = 0; i < lista.size(); i++) {
    System.out.println(lista.get(i));
}

OU
for (String item : lista) {
    System.out.println(item);
}


🔹 8. ArrayList com Objetos
ArrayList<Pessoa> pessoas = new ArrayList<>();

pessoas.add(new Pessoa("João"));

for (Pessoa p : pessoas) {
    System.out.println(p.getNome());
}


🔹 9. Exemplo COMPLETO (CRUD simples)
import java.util.ArrayList;

class Pessoa {
    String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }
}

public class Main {
    public static void main(String[] args) {
        ArrayList<Pessoa> lista = new ArrayList<>();

        // CREATE
        lista.add(new Pessoa("João"));
        lista.add(new Pessoa("Maria"));

        // READ
        for (Pessoa p : lista) {
            System.out.println(p.nome);
        }

        // UPDATE
        lista.get(0).nome = "Carlos";

        // DELETE
        lista.remove(1);
    }
}


🔹 10. Scanner (Entrada de Dados)
Import
import java.util.Scanner;

Usando Scanner
Scanner sc = new Scanner(System.in);

System.out.print("Digite seu nome: ");
String nome = sc.nextLine();

System.out.print("Digite sua idade: ");
int idade = sc.nextInt();

Cuidados importantes
nextLine() → lê texto
nextInt() → lê número
⚠️ Problema comum: depois de nextInt(), use um nextLine() extra
int idade = sc.nextInt();
sc.nextLine(); // limpar buffer
String nome = sc.nextLine();

Fechar Scanner
sc.close();


🔥 DICAS DE PROVA
Sempre use .equals() para String
Saiba TODOS os métodos do ArrayList
Entenda diferença entre classe e objeto
Treine criação de objetos dentro de listas
Cuidado com NullPointerException
Lembre do new para criar objetos

🔹 11. Vetores (Arrays)
Um vetor é uma estrutura fixa (tamanho definido).
📌 Declaração
int[] numeros = new int[5];
📌 Inicialização direta
int[] numeros = {10, 20, 30, 40, 50};
📌 Acessar e alterar
System.out.println(numeros[0]); // 10

numeros[1] = 99;
📌 Percorrer vetor
for (int i = 0; i < numeros.length; i++) {
   System.out.println(numeros[i]);
}
OU (for-each)
for (int n : numeros) {
   System.out.println(n);
}
⚠️ Pontos importantes
Índice começa em 0
Última posição = length - 1
Estoura erro: ArrayIndexOutOfBoundsException

🔹 12. Matrizes (Arrays 2D)
Uma matriz é um vetor de vetores.
📌 Declaração
int[][] matriz = new int[3][3];
📌 Inicialização
int[][] matriz = {
   {1, 2, 3},
   {4, 5, 6},
   {7, 8, 9}
};
📌 Acessar
System.out.println(matriz[0][1]); // 2
📌 Percorrer matriz
for (int i = 0; i < matriz.length; i++) {
   for (int j = 0; j < matriz[i].length; j++) {
       System.out.println(matriz[i][j]);
   }
}

🔹 13. Fórmulas Matemáticas (Math)
A classe Math é muito cobrada em prova.
📌 Principais métodos
Math.sqrt(25);      // raiz quadrada → 5.0
Math.pow(2, 3);     // potência → 8.0
Math.abs(-10);      // valor absoluto → 10
Math.max(10, 20);   // maior → 20
Math.min(10, 20);   // menor → 10
Math.round(4.6);    // arredonda → 5
Math.ceil(4.2);     // arredonda pra cima → 5.0
Math.floor(4.9);    // arredonda pra baixo → 4.0
Math.random();      // número aleatório (0 a 1)
📌 Número aleatório em intervalo
int num = (int)(Math.random() * 10); // 0 a 9
Ou:
int num = (int)(Math.random() * (max - min + 1)) + min;

🔹 14. Exemplos que caem MUITO em prova
📌 Somar elementos de um vetor
int[] nums = {1, 2, 3, 4};
int soma = 0;

for (int n : nums) {
   soma += n;
}

System.out.println(soma);

📌 Maior valor do vetor
int maior = nums[0];

for (int n : nums) {
   if (n > maior) {
       maior = n;
   }
}

📌 Média
double media = (double) soma / nums.length;

📌 Diagonal principal da matriz
for (int i = 0; i < matriz.length; i++) {
   System.out.println(matriz[i][i]);
}

📌 Soma de matriz
int soma = 0;

for (int i = 0; i < matriz.length; i++) {
   for (int j = 0; j < matriz[i].length; j++) {
       soma += matriz[i][j];
   }
}

🔹 HashMap (Java)
É uma estrutura que armazena pares de chave e valor:
👉 tipo um dicionário
 👉 exemplo: "nome" → "Mateus"

🔹 Importação
import java.util.HashMap;

🔹 Criando um HashMap
HashMap<String, String> mapa = new HashMap<>();
👉 String, String = (chave, valor)

🔹 Adicionando elementos (put)
mapa.put("nome", "Mateus");
mapa.put("cidade", "BH");

🔹 Acessando valor (get)
System.out.println(mapa.get("nome")); // Mateus

🔹 Remover elemento
mapa.remove("cidade");

🔹 Verificar se existe chave
mapa.containsKey("nome"); // true

🔹 Verificar valor
mapa.containsValue("Mateus"); // true

🔹 Tamanho
mapa.size();

🔹 Percorrer HashMap
📌 Usando chave
for (String chave : mapa.keySet()) {
   System.out.println(chave + " = " + mapa.get(chave));
}

📌 Usando valores
for (String valor : mapa.values()) {
   System.out.println(valor);
}

🔹 Exemplo completo
import java.util.HashMap;

public class Main {
   public static void main(String[] args) {

       HashMap<String, Integer> alunos = new HashMap<>();

       alunos.put("João", 8);
       alunos.put("Maria", 9);
       alunos.put("Pedro", 7);

       // acessar
       System.out.println(alunos.get("Maria"));

       // percorrer
       for (String nome : alunos.keySet()) {
           System.out.println(nome + " - " + alunos.get(nome));
       }
   }
}




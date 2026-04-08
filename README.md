# RevisaoPm

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



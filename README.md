🚀 Resumo Completo de Java (POO + Sintaxe)

«📚 Guia rápido e direto para provas e estudos de Java»

---

🧠 Estrutura Básica

public class Main {
    public static void main(String[] args) {
        System.out.println("Olá mundo");
    }
}

---

🔢 Tipos de Variáveis

int idade = 18;
double altura = 1.75;
char letra = 'A';
boolean ativo = true;
String nome = "Lucas";

Tipo| Exemplo
int| 10
double| 1.75
String| "Texto"
boolean| true/false

---

🔁 Condições

If / Else

if (idade >= 18) {
    System.out.println("Maior de idade");
} else {
    System.out.println("Menor de idade");
}

Switch

switch (op) {
    case 1:
        System.out.println("Opção 1");
        break;
    case 2:
        System.out.println("Opção 2");
        break;
}

---

🔄 Laços de Repetição

For

for (int i = 0; i < 5; i++) {
    System.out.println(i);
}

While

int i = 0;
while (i < 5) {
    i++;
}

For-each

for (String nome : lista) {
    System.out.println(nome);
}

---

📦 Arrays

int[] numeros = {1, 2, 3};
System.out.println(numeros[0]);

---

📚 ArrayList ⭐

import java.util.ArrayList;

ArrayList<String> nomes = new ArrayList<>();

nomes.add("Lucas");
nomes.add("Ana");

System.out.println(nomes.get(0));

nomes.remove("Ana");

Método| Função
add()| Adicionar
get()| Buscar
remove()| Remover

---

🧱 Classes (POO)

public class Pessoa {
    String nome;
    int idade;
}

---

🏗️ Construtor

public class Pessoa {
    String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }
}

---

🔒 Encapsulamento ⭐

private String nome;

public String getNome() {
    return nome;
}

public void setNome(String nome) {
    this.nome = nome;
}

---

🔗 Associação entre Classes

class Carro {
    Motorista motorista;
}

---

🧩 Métodos

public void falar() {
    System.out.println("Oi");
}

public int somar(int a, int b) {
    return a + b;
}

---

🧮 Operadores

Tipo| Operadores
Matemáticos| + - * /
Comparação| == != > <
Lógicos| &&

---

📥 Entrada de Dados

import java.util.Scanner;

Scanner sc = new Scanner(System.in);

int idade = sc.nextInt();
String nome = sc.nextLine();

---

🧾 toString()

public String toString() {
    return nome + " - " + idade;
}

---

🧠 Regras de Ouro (PROVA)

✔ Use "private" nos atributos
✔ Use "ArrayList" ao invés de vetor
✔ Separe classes corretamente
✔ Use "this" no construtor
✔ Evite lógica na "main"

---

⚡ Resumo Final

Conceito| Uso
Classe| "class"
Objeto| "new"
Lista| "ArrayList"
Decisão| "if / switch"
Loop| "for / while"
Método| Função
Encapsulamento| get/set

---

🏁 Dica Final

«💡 Se fizer isso aqui bem feito, você já garante a maior parte da prova!»

---

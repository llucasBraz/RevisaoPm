🚀 Guia Completo de Java (Sintaxe + POO + ArrayList)

«📚 Feito para provas — simples, direto e com MUITOS exemplos»

---

🧠 1. Estrutura Básica

public class Main {
    public static void main(String[] args) {
        System.out.println("Olá mundo!");
    }
}

---

🔢 2. Variáveis (Tipos)

int idade = 20;
double altura = 1.80;
String nome = "Lucas";
boolean ativo = true;
char letra = 'A';

---

🔁 3. Condições

if (idade >= 18) {
    System.out.println("Maior de idade");
} else {
    System.out.println("Menor");
}

switch (idade) {
    case 18:
        System.out.println("Tem 18");
        break;
    default:
        System.out.println("Outra idade");
}

---

🔄 4. Repetição

for (int i = 0; i < 3; i++) {
    System.out.println(i);
}

int i = 0;
while (i < 3) {
    i++;
}

---

📦 5. Arrays

int[] numeros = {1, 2, 3};

System.out.println(numeros[0]);

---

📚 6. ArrayList (MUUUITO IMPORTANTE)

Criando

import java.util.ArrayList;

ArrayList<String> nomes = new ArrayList<>();

Adicionando

nomes.add("Lucas");
nomes.add("Ana");

Acessando

System.out.println(nomes.get(0));

Removendo

nomes.remove("Ana");

Tamanho

System.out.println(nomes.size());

Loop

for (String n : nomes) {
    System.out.println(n);
}

---

🔥 Exemplos Práticos com ArrayList

Lista de números

ArrayList<Integer> numeros = new ArrayList<>();

numeros.add(10);
numeros.add(20);

for (int n : numeros) {
    System.out.println(n);
}

---

Buscar valor

if (nomes.contains("Lucas")) {
    System.out.println("Achou!");
}

---

Remover por índice

nomes.remove(0);

---

Limpar lista

nomes.clear();

---

🧱 7. Classes (POO)

public class Pessoa {
    String nome;
    int idade;
}

---

🏗️ 8. Construtor

public class Pessoa {
    String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }
}

---

🔒 9. Encapsulamento

private String nome;

public String getNome() {
    return nome;
}

public void setNome(String nome) {
    this.nome = nome;
}

---

🔗 10. Classe com ArrayList dentro (CAI MUITO NA PROVA)

import java.util.ArrayList;

public class Turma {
    private ArrayList<String> alunos = new ArrayList<>();

    public void adicionarAluno(String nome) {
        alunos.add(nome);
    }

    public void listar() {
        for (String a : alunos) {
            System.out.println(a);
        }
    }
}

---

🔥 11. Classe com Objetos dentro (IMPORTANTE)

import java.util.ArrayList;

public class Escola {
    private ArrayList<Pessoa> pessoas = new ArrayList<>();

    public void adicionarPessoa(Pessoa p) {
        pessoas.add(p);
    }
}

---

🧩 12. Métodos (VÁRIOS EXEMPLOS)

Método simples

public void falar() {
    System.out.println("Oi");
}

Método com retorno

public int somar(int a, int b) {
    return a + b;
}

Método com condição

public boolean maiorIdade(int idade) {
    return idade >= 18;
}

---

🔥 Métodos com ArrayList

Somar valores

public int somarLista(ArrayList<Integer> lista) {
    int total = 0;
    for (int n : lista) {
        total += n;
    }
    return total;
}

---

Buscar elemento

public boolean existe(ArrayList<String> lista, String nome) {
    return lista.contains(nome);
}

---

Contar elementos

public int contar(ArrayList<String> lista) {
    return lista.size();
}

---

🔗 13. Associação entre Classes

class Carro {
    Motorista motorista;
}

---

🔥 Exemplo completo (CAI MUITO)

public class Aluno {
    String nome;

    public Aluno(String nome) {
        this.nome = nome;
    }
}

import java.util.ArrayList;

public class Curso {
    ArrayList<Aluno> alunos = new ArrayList<>();

    public void adicionar(Aluno a) {
        alunos.add(a);
    }

    public void listar() {
        for (Aluno a : alunos) {
            System.out.println(a.nome);
        }
    }
}

---

📥 14. Scanner

import java.util.Scanner;

Scanner sc = new Scanner(System.in);

int idade = sc.nextInt();
String nome = sc.nextLine();

---

🧾 15. toString()

public String toString() {
    return nome;
}

---

🧮 16. Operadores

+ - * /
== != > <
&& ||

---

🧠 17. DICAS QUE GARANTEM PONTO

✔ Sempre usar "private"
✔ Sempre usar "ArrayList"
✔ Criar métodos para tudo
✔ Evitar lógica na "main"
✔ Usar objetos (new) corretamente

---

⚡ RESUMÃO FINAL

- Classe → "class"
- Objeto → "new"
- Lista → "ArrayList"
- Método → função
- Loop → "for"
- Decisão → "if"

---

🏁 Dica final

«💡 Se você souber:

- Criar classe
- Usar ArrayList
- Fazer métodos

👉 Você já passa na prova!»

--- 

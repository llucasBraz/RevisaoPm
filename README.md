Java
public class Motorista {
    private String nome;
    private String cpf;
    private String cnh;
    private String telefone;
    private Veiculo veiculo;

    public Motorista(String nome, String cpf, String cnh, String telefone) {
        this.nome = nome;
        this.cpf = cpf;
        this.cnh = cnh;
        this.telefone = telefone;
    }

    public void setVeiculo(Veiculo veiculo) {
        this.veiculo = veiculo;
    }

    public String getNome() {
        return nome;
    }

    public Veiculo getVeiculo() {
        return veiculo;
    }
}
🚙 Veiculo.java
Java
import java.util.ArrayList;

public class Veiculo {
    private String placa;
    private String modelo;
    private int ano;
    private double capacidade;
    private String tipo;

    private Motorista motorista;
    private ArrayList<Entrega> entregas;

    public Veiculo(String placa, String modelo, int ano, double capacidade, String tipo) {
        this.placa = placa;
        this.modelo = modelo;
        this.ano = ano;
        this.capacidade = capacidade;
        this.tipo = tipo;
        this.entregas = new ArrayList<>();
    }

    public void setMotorista(Motorista motorista) {
        this.motorista = motorista;
    }

    public Motorista getMotorista() {
        return motorista;
    }

    public void adicionarEntrega(Entrega e) {
        entregas.add(e);
    }

    public ArrayList<Entrega> getEntregas() {
        return entregas;
    }

    public String getPlaca() {
        return placa;
    }
}
📦 Entrega.java
Java
public class Entrega {
    private int codigo;
    private String destinatario;
    private String endereco;
    private String data;
    private String status;
    private double peso;

    private Veiculo veiculo;
    private Rota rota;

    public Entrega(int codigo, String destinatario, String endereco,
                   String data, String status, double peso, Rota rota) {
        this.codigo = codigo;
        this.destinatario = destinatario;
        this.endereco = endereco;
        this.data = data;
        this.status = status;
        this.peso = peso;
        this.rota = rota;
    }

    public String getStatus() {
        return status;
    }

    public void setVeiculo(Veiculo veiculo) {
        this.veiculo = veiculo;
    }

    public String toString() {
        return "Entrega " + codigo + " | Cliente: " + destinatario + " | Status: " + status;
    }
}
🗺️ Rota.java
Java
public class Rota {
    private String origem;
    private String destino;
    private double distancia;
    private double tempo;

    public Rota(String origem, String destino, double distancia, double tempo) {
        this.origem = origem;
        this.destino = destino;
        this.distancia = distancia;
        this.tempo = tempo;
    }
}
⚙️ Sistema.java
Java
import java.util.ArrayList;

public class Sistema {

    public ArrayList<Veiculo> veiculos = new ArrayList<>();
    private ArrayList<Motorista> motoristas = new ArrayList<>();
    private ArrayList<Entrega> entregas = new ArrayList<>();

    public void adicionarVeiculo(Veiculo v) {
        veiculos.add(v);
    }

    public void adicionarMotorista(Motorista m) {
        motoristas.add(m);
    }

    public void adicionarEntrega(Entrega e) {
        entregas.add(e);
    }

    public void associar(Motorista m, Veiculo v) {
        m.setVeiculo(v);
        v.setMotorista(m);
    }

    public void atribuirEntrega(Entrega e, Veiculo v) {
        v.adicionarEntrega(e);
        e.setVeiculo(v);
    }

    // 🔥 RELATÓRIO FINAL
    public void gerarRelatorio() {

        int pendentes = 0;
        int finalizadas = 0;

        System.out.println("\n===== RELATÓRIO FINAL =====");

        for (Veiculo v : veiculos) {

            System.out.println("\nVeículo: " + v.getPlaca());

            if (v.getMotorista() != null) {
                System.out.println("Motorista: " + v.getMotorista().getNome());
            }

            for (Entrega e : v.getEntregas()) {
                System.out.println(e);

                if (e.getStatus().equals("pendente")) {
                    pendentes++;
                } else if (e.getStatus().equals("finalizada")) {
                    finalizadas++;
                }
            }
        }

        System.out.println("\nTotal pendentes: " + pendentes);
        System.out.println("Total finalizadas: " + finalizadas);
    }
}
🚀 Main.java
Java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        Sistema sistema = new Sistema();

        // 🚗 VEÍCULOS + MOTORISTAS
        System.out.print("Quantos veículos? ");
        int qtdVeiculos = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < qtdVeiculos; i++) {

            System.out.println("\nVeículo " + (i + 1));

            System.out.print("Placa: ");
            String placa = sc.nextLine();

            System.out.print("Modelo: ");
            String modelo = sc.nextLine();

            Veiculo v = new Veiculo(placa, modelo, 2020, 1000, "Carga");

            System.out.print("Nome do motorista: ");
            String nome = sc.nextLine();

            Motorista m = new Motorista(nome, "000", "B", "999");

            sistema.adicionarVeiculo(v);
            sistema.adicionarMotorista(m);
            sistema.associar(m, v);
        }

        // 📦 ENTREGAS
        System.out.print("\nQuantas entregas? ");
        int qtdEntregas = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < qtdEntregas; i++) {

            System.out.println("\nEntrega " + (i + 1));

            System.out.print("Destinatário: ");
            String dest = sc.nextLine();

            System.out.print("Status (pendente/finalizada): ");
            String status = sc.nextLine();

            Rota r = new Rota("A", "B", 10, 1);

            Entrega e = new Entrega(i + 1, dest, "Rua X", "Hoje", status, 10, r);

            sistema.adicionarEntrega(e);

            // 🔥 associa sempre ao primeiro veículo (simples pra prova)
            sistema.atribuirEntrega(e, sistema.veiculos.get(0));
        }

        // 📊 RELATÓRIO FINAL
        sistema.gerarRelatorio();

        sc.close();
    }
}

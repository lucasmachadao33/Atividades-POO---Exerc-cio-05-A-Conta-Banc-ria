5-
public class ContaBancaria {

    // Atributos
    String titular;
    String numeroConta;
    double saldo;

    // Método para depositar
    void depositar(double valor) {

        if (valor > 0) {
            saldo += valor;
            System.out.println("Depósito de R$ " + valor + " realizado.");
        } else {
            System.out.println("Valor inválido para depósito.");
        }
    }

    // Método para sacar
    void sacar(double valor) {

        if (valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque de R$ " + valor + " realizado.");
        } else {
            System.out.println("Saldo insuficiente.");
        }
    }

    // Método para exibir extrato
    void exibirExtrato() {

        System.out.println("===== Extrato =====");
        System.out.println("Titular: " + titular);
        System.out.println("Conta: " + numeroConta);
        System.out.println("Saldo: R$ " + saldo);
        System.out.println("===================");
    }

    // Método principal
    public static void main(String[] args) {

        ContaBancaria conta = new ContaBancaria();

        conta.titular = "Carlos Souza";
        conta.numeroConta = "0042-7";
        conta.saldo = 0;

        conta.depositar(1500.00);
        conta.depositar(250.00);
        conta.sacar(300.00);

        conta.exibirExtrato();
    }
}

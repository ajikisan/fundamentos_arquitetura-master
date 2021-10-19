Aluna: Mirian Ajiki Molicawa
Instrutor: Jefferson Stachelski
Linguagem Java

# Exercício 1

Escrever um pequeno sistema de qualquer tópico (exemplo biblioteca).
Esse sistema deve ter pelo menos três serviços, por exemplo:

- Serviço que gerencia usuários
  Declaração de variáveis

String[][] livro = new String[2][3];
String usuario;

        System.out.print("Por gentileza digite o nome do bibliotecario: ");
        usuario = new Scanner(System.in).nextLine();
        boolean resp = true;
        int soma = 0;

- Serviço que gerencia os livros e suas locações

for (int i = 0; i < 3; i++) {
for (int j = 0; j < 4; j++) {
if (j == 0 && resp) {
System.out.print("Digite o título do livro: ");
livro[i][j] = new Scanner(System.in).nextLine();
}
if (j == 1 && resp) {
System.out.print("Digite o nome do autor do livro: ");
livro[i][j] = new Scanner(System.in).nextLine();
}
if (j == 2 && resp) {
System.out.print("Digite o assunto/tema do livro: ");
livro[i][j] = new Scanner(System.in).nextLine();
}

            if (i < 3 && resp) {
                soma = soma + 1;
                System.out.println("Foi realizado " + (i + 1) + " cadastro(s) de livro(s), deseja continuar? s/n");
                if (new Scanner(System.in).nextLine().equalsIgnoreCase("n")) {
                    resp = false;
                }
            } else {
                if (i == 3 && resp) {
                    System.out.print("Prezado bibliotecário, três são o número máximo de livros cadastrados para empréstimo.");
                    resp = false;
                }
            }

- Serviço que gera relatórios

System.out.println("");
System.out.print("Foram cadastrado(s) " + soma + " livro(s) pelo bibliotecário: " + bibliotecario + ".");

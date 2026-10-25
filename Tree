public class Tree {
    Node raiz;

    public void inserir(int valor) {
        raiz = inserirNo(raiz, valor);
    }

    private Node inserirNo(Node atual, int valor) {
        if (atual == null) {
            return new Node(valor);
        }

        if (valor < atual.valor) {
            atual.esquerda = inserirNo(atual.esquerda, valor);
        } else if (valor > atual.valor) {
            atual.direita = inserirNo(atual.direita, valor);
        }

        return atual;
    }

    public int contarFolhas() {
        return contar(raiz);
    }

    private int contar(Node atual) {
        if (atual == null) {
            return 0;
        }

        if (atual.esquerda == null && atual.direita == null) {
            return 1;
        }

        return contar(atual.esquerda) + contar(atual.direita);
    }
}

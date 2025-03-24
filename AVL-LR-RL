class Node {
    int val;
    int ht;
    Node left, right;

    Node(int val) {
        this.val = val;
        this.ht = 1; 
    }
}

class AVL {
    int getHeight(Node node) {
        return (node == null) ? 0 : node.ht;
    }
    int getBalance(Node node) {
        return (node == null) ? 0 : getHeight(node.left) - getHeight(node.right);
    }
    Node rightRotate(Node y) {
        Node x = y.left;
        Node T2 = x.right;
        x.right = y;
        y.left = T2;
        y.ht = Math.max(getHeight(y.left), getHeight(y.right)) + 1;
        x.ht = Math.max(getHeight(x.left), getHeight(x.right)) + 1;
        return x;
    }
    Node leftRotate(Node y) {
        Node x = y.right;
        Node T2 = x.left;
        x.left = y;
        y.right = T2;
        y.ht = Math.max(getHeight(y.left), getHeight(y.right)) + 1;
        x.ht = Math.max(getHeight(x.left), getHeight(x.right)) + 1;
        return x;
    }

    Node leftRightRotate(Node y) {
        y.left = leftRotate(y.left); 
        return rightRotate(y); 
    }

    Node rightLeftRotate(Node y) {
        y.right = rightRotate(y.right); 
        return leftRotate(y); 
    }

    Node insert(Node node, int val) {
        if (node == null)
            return new Node(val);
        if (val < node.val)
            node.left = insert(node.left, val);
        else if (val > node.val)
            node.right = insert(node.right, val);
        else
            return node; 

        node.ht = Math.max(getHeight(node.left), getHeight(node.right)) + 1;

        int balance = getBalance(node);

        if (balance > 1 && val < node.left.val)
            return rightRotate(node);

        if (balance < -1 && val > node.right.val)
            return leftRotate(node);

        if (balance > 1 && val > node.left.val)
            return leftRightRotate(node);

        if (balance < -1 && val < node.right.val)
            return rightLeftRotate(node);

        return node;
    }

    void inorder(Node root) {
        if (root != null) {
            inorder(root.left);
            System.out.print(root.val + " ");
            inorder(root.right);
        }
    }

    void preorder(Node root) {
        if (root != null) {
            System.out.print(root.val + " ");
            preorder(root.left);
            preorder(root.right);
        }
    }

    
    void postorder(Node root) {
        if (root != null) {
            postorder(root.left);
            postorder(root.right);
            System.out.print(root.val + " ");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        AVL tree = new AVL();
        Node root = null;

        int[] values = {20, 30, 25, 47, 67, 90, 33, 89};
        for (int val : values) {
            root = tree.insert(root, val);
        }

        System.out.println("Inorder Traversal:");
        tree.inorder(root);
        System.out.println("\nPreorder Traversal:");
        tree.preorder(root);
        System.out.println("\nPostorder Traversal:");
        tree.postorder(root);
    }
}

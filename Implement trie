class Trie {
    Trie[] child = new Trie[26];
    boolean end;

    public void insert(String word) {
        Trie cur = this;
        for (char c : word.toCharArray()) {
            int i = c - 'a';
            if (cur.child[i] == null)
                cur.child[i] = new Trie();
            cur = cur.child[i];
        }
        cur.end = true;
    }

    public boolean search(String word) {
        Trie cur = this;
        for (char c : word.toCharArray()) {
            int i = c - 'a';
            if (cur.child[i] == null)
                return false;
            cur = cur.child[i];
        }
        return cur.end;
    }

    public boolean startsWith(String prefix) {
        Trie cur = this;
        for (char c : prefix.toCharArray()) {
            int i = c - 'a';
            if (cur.child[i] == null)
                return false;
            cur = cur.child[i];
        }
        return true;
    }

    public static void main(String[] args) {
        Trie t = new Trie();

        t.insert("apple");

        System.out.println(t.search("apple"));
        System.out.println(t.search("app"));
        System.out.println(t.startsWith("app"));

        t.insert("app");
        System.out.println(t.search("app"));
    }
}

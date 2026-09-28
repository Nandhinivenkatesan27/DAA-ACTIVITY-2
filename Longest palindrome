class LongestPalindrome {
    public static void main(String[] args) {
        String s = "babad";
        String ans = "";

        for (int i = 0; i < s.length(); i++) {
            for (int j = i; j < s.length(); j++) {
                String sub = s.substring(i, j + 1);
                String rev = new StringBuilder(sub).reverse().toString();

                if (sub.equals(rev) && sub.length() > ans.length())
                    ans = sub;
            }
        }

        System.out.println(ans);
    }
}

class MinimumWindow {
    public static void main(String[] args) {
        String s = "ADOBECODEBANC";
        String t = "ABC";

        int[] count = new int[128];

        for (char c : t.toCharArray())
            count[c]++;

        int left = 0, required = t.length();
        int start = 0, min = Integer.MAX_VALUE;

        for (int right = 0; right < s.length(); right++) {
            if (count[s.charAt(right)] > 0)
                required--;

            count[s.charAt(right)]--;

            while (required == 0) {
                if (right - left + 1 < min) {
                    min = right - left + 1;
                    start = left;
                }

                count[s.charAt(left)]++;

                if (count[s.charAt(left)] > 0)
                    required++;

                left++;
            }
        }

        System.out.println(min == Integer.MAX_VALUE ? "" :
                s.substring(start, start + min));
    }
}

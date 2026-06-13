

public class Main{ 

    public static int strCount(String str, char target) {
        if (str == null) return 0;  // Защита от null
        
        int count = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == target) {
                count++;
            }
        }

        return count;
    }
    `
    public static void main(String[] args) {
        int result1 = strCount("Hello", 'o');
        System.out.println("str_count(\"Hello\", 'o') = " + result1);

        int result2 = strCount("Hello", 'l');
        System.out.println("str_count(\"Hello\", 'l') = " + result2);

        int result3 = strCount("", 'z');
        System.out.println("str_count(\"\", 'z') = " + result3);

        System.out.println("\n--- Дополнительные тесты ---");
        int result4 = strCount("Programming", 'g');
        System.out.println("str_count(\"Programming\", 'g') = " + result4);

        int result5 = strCount("Java", 'a');
        System.out.println("str_count(\"Java\", 'a') = " + result5);

        int result6 = strCount("Test", 'x');
        System.out.println("str_count(\"Test\", 'x') = " + result6);
    }
}

/**
 * Программа для подсчета количества вхождений символа в строку
 * Вариант 4
 */
public class Main {

    /**
     * Метод подсчета количества вхождений символа в строку
     * @param str - строка для поиска
     * @param target - символ для поиска
     * @return количество вхождений символа в строку
     */
    public static int strCount(String str, char target) {
        if (str == null) return 0;  // Защита от null
        
        int count = 0;
        
        // Проходим по всей строке
        for (int i = 0; i < str.length(); i++) {
            // Если текущий символ совпадает с искомым
            if (str.charAt(i) == target) {
                count++;
            }
        }
        
        return count;
    }

    public static void main(String[] args) {
        // Тест 1: str_count("Hello", 'o') должно вернуть 1
        int result1 = strCount("Hello", 'o');
        System.out.println("str_count(\"Hello\", 'o') = " + result1);
        // Ожидаем: 1
        
        // Тест 2: str_count("Hello", 'l') должно вернуть 2
        int result2 = strCount("Hello", 'l');
        System.out.println("str_count(\"Hello\", 'l') = " + result2);
        // Ожидаем: 2
        
        // Тест 3: str_count("", 'z') должно вернуть 0
        int result3 = strCount("", 'z');
        System.out.println("str_count(\"\", 'z') = " + result3);
        // Ожидаем: 0
        
        // Дополнительные тесты
        System.out.println("\n--- Дополнительные тесты ---");
        
        int result4 = strCount("Programming", 'g');
        System.out.println("str_count(\"Programming\", 'g') = " + result4);
        // Ожидаем: 2
        
        int result5 = strCount("Java", 'a');
        System.out.println("str_count(\"Java\", 'a') = " + result5);
        // Ожидаем: 2
        
        int result6 = strCount("Test", 'x');
        System.out.println("str_count(\"Test\", 'x') = " + result6);
        // Ожидаем: 0
    }
}

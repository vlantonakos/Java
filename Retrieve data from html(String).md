```
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Main {
	public static void main(String[] args) {
        String html = "<html>\n" +
                "\n" +
                " <body>\n" +
                "\n" +
                "<p>Coders favourite music genre:</p>\n" +
                "\n" +
                "<ol>\n" +
                "\n" +
                "<li>House</li>\n" +
                "\n" +
                "<li>Ballad</li>\n" +
                "\n" +
                "<li>Dance</li>\n" +
                "\n" +
                "</ol>\n" +
                "\n" +
                "<p>Coders favourite beverage:</p>\n" +
                "\n" +
                "<ol>\n" +
                "\n" +
                " <li>Coffee</li>\n" +
                "\n" +
                "  <li>Tea</li>\n" +
                "\n" +
                "      	 	   <li>Coke</li>\n" +
                "\n" +
                "</ol>\n" +
                "\n" +
                "<p>Coders favourite phrase:</p>\n" +
                "\n" +
                "<ol>\n" +
                "\n" +
                "<li>Pfff</li>\n" +
                "\n" +
                "<li>Damn</li>\n" +
                "\n" +
                "<li>It works</li>\n" +
                "\n" +
                "</ol>\n" +
                "\n" +
                "\n" +
                "\n" +
                " </body>\n" +
                "\n" +
                "</html>";

        Pattern pattern = Pattern.compile("<p>Coders favourite beverage:</p>\\s*<ol>\\s*(.*?)\\s*</ol>", Pattern.DOTALL);
        Matcher matcher = pattern.matcher(html);

        if (matcher.find()) {
            String beverageListHtml = matcher.group(1);
            Pattern itemPattern = Pattern.compile("<li>(.*?)</li>");
            Matcher itemMatcher = itemPattern.matcher(beverageListHtml);

            while (itemMatcher.find()) {
                String beverage = itemMatcher.group(1);
                System.out.println(beverage);
            }
        }
    }
}
```
OUTPUT:
Coffee
Tea
Coke

    

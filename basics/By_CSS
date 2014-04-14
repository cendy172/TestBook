#Locating elements by CSS

##Java
```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class Trial {

    public static void main(String[] args) {
        WebDriver driver = new FirefoxDriver();
        String search_box_locator = ".gbqfif";

        driver.get("http://www.google.com");
        WebElement searchBoxElem = driver.findElement(By.cssSelector(search_box_locator));
        searchBoxElem.sendKeys("Hello");

        driver.quit();
    }
}
```

##Python
```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

if __name__=='__main__':

	webdriver_obj=webdriver.Firefox()
	search_box_locator=".gbqfif";

	webdriver_obj.get("http://www.google.com")
	searchBoxElem=webdriver_obj.find_element_by_css_selector(search_box_locator)
	searchBoxElem.send_keys("Hello")
	webdriver_obj.close()
```

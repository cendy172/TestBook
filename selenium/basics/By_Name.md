#Locating elements by Name

##Java
```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class SeleniumTrialRun {

     public static void main(String[] args) {
        WebDriver driver = new FirefoxDriver();
        String search_box_name = "q";

        driver.get("http://www.google.com");
        WebElement searchBoxElem = driver.findElement(By.name(search_box_name));
        searchBoxElem.sendKeys("Hello");

        driver.quit();
    }
}
```

##Python
```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

if __name__=='__main__':

	webdriver_obj=webdriver.Firefox()
	search_box_name="q";

	webdriver_obj.get("http://www.google.com")
	searchBoxElem=webdriver_obj.find_element_by_name(search_box_name)
	searchBoxElem.send_keys("Hello")
	webdriver_obj.close()
```

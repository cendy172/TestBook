#Locating elements by ID

##Java
```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class SeleniumTrialRun {

    public static void main(String[] args) {
        WebDriver driver = new FirefoxDriver();
        String search_box_id = "gbqfq";

        driver.get("http://www.google.com");
        WebElement searchBoxElem = driver.findElement(By.id(search_box_id));
        searchBoxElem.sendKeys("Hello");

        driver.quit();
    }
}
```

##Python
```python
  
from selenium import webdriver
  
webdriver_obj=webdriver.Firefox()
search_box_id="gbqfq";

webdriver_obj.get("http://www.google.com")
searchBoxElem=webdriver_obj.find_element_by_id(search_box_id)
searchBoxElem.send_keys("Hello")
	
webdriver_obj.close()
```

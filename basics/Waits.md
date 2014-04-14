#Driver Waits

Driver waits define the phenomenon, where a certain amount of time is passed, before the next step is executed.

There are two different knid if waits in Selenium
- Explicit Wait
- Implicit Wait

##Explicit Wait
###Java
```java
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

WebDriverWait wait = new WebDriverWait(driver,10);
wait.until(ExpectedConditions.presenceOfElementLocated(By.cssSelector(element_locator)));
```
###Python
```python
from selenium.webdriver.support import expected_conditions as EC

wait = WebDriverWait(driver, 10)
element = wait.until(EC.element_to_be_clickable((By.CSS,'element_locator')))
```

##Implicit Wait
###Java
```java
driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
```
###Python
```python
driver.implicitly_wait(10) # seconds
```

#Upload Files

```java
String fileName="/data/files_to_upload_text.txt";
File file = new File ( ResourceManager.class.getResource(fileName).toURI() );
String absoluteFilePath = file.getAbsolutePath();
fileUploadButton.sendKeys(absoluteFilePath);
```
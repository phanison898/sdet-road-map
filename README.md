### Software Development Engineer in Test

### Tech Stack

#### 1. Web Application Automation

- Development approach

  1. TDD : Test Driven Development
  1. DDD : Data Driven Development
  1. BDD : Behavior Driven Development
  1. Hybrid Development

- Automation Design pattern

  1. POM : Page Object Model
  1. PFM : Page Factory Model

- Programming Languages
  1. Java
  2. Python
- Automation Tools / Libraries

  1. Selenium
  1. Cucumber

- Test Frameworks

  1. TestNG (for Java)
  2. JUnit (for Java)
  3. Pytest (for Python)

- Build Tools

  1. Maven (for Java)
  1. PIP (for Python)

- Extras
  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files
  1. Pandas (for Python) : for reading / writing excel or csv files

#### 2. Mobile Application Automation

- Development approach

  1. TDD : Test Driven Development
  1. DDD : Data Driven Development
  1. BDD : Behavior Driven Development
  1. Hybrid Development

- Automation Design pattern

  1. POM : Page Object Model
  1. PFM : Page Factory Model

- Programming Languages
  1. Java
- Automation Tools / Libraries

  1. Appium
  1. Selenium
  1. Cucumber

- Devices

  1. Android - Real / Emulator devices
  1. iOS - Real / Simulator devices

- Test Frameworks

  1. TestNG (for Java)
  2. JUnit (for Java)

- Build Tools

  1. Maven (for Java)

- Extras
  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files

#### API Automation

- Development approach

  1. TDD : Test Driven Development
  1. BDD : Behavior Driven Development

- Programming Languages

  1. Java

- Automation Tools / Libraries

  1. Rest Assured
  1. Cucumber

- Test Frameworks

  1. TestNG (for Java)
  2. JUnit (for Java)

- Build Tools

  1. Maven

- Extras
  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files

#### Database Automation

- Tools / Libraries

  1. Java
  1. JDBC

- Databases

  1. MySQL
  1. Oracle SQL Developer
  1. Microsoft SQL Server

---

#### Database Automation

##### Key point and concepts

- Class.forName(driver)

  1. MySQL : "com.mysql.jdbc.Driver"
  1. Oracle : "oracle.jdbc.driver.OracleDriver"
  1. MS : "com.microsoft.sqlserver.jdbc.SQLServerDriver"

- Connection string

  1. MySQL : "jdbc:mysql://IP_ADDESS:PORT/DB_NAME" # commonly used port : 3306
  1. Oracle : "jdbc:oracle:thin:@IP_ADDESS:PORT:xe" # commonly used port : 1521
  1. MySQL : "jdbc:sqlserver://IP_ADDESS:PORT;databaseName=DB_NAME;user=USERNAME;password=PASSWORD;
     "

- Example Code

```java

import java.sql.*

public class JDBC {

    String url = "jdbc:mysql://localhost:3306/mydatabase";
    String user = "username";
    String password = "password";

    // JDBC variables for managing connection and query execution
    Connection connection = null;
    Statement statement = null;
    ResultSet resultSet = null;

    public static void main(String[] args) {

        // add the driver to class path
        Class.forName("database.driver.classpath");

        // Establishing connection to the database
        connection = DriverManager.getConnection(url, user, password);

        // Creating a statement object
        statement = connection.createStatement();

        // Executing a SQL query
        String query = "SELECT * FROM mytable";
        resultSet = statement.executeQuery(query);

        while (resultSet.next()) {
           // do your implementation
        }
    }
}


```

#### Appium's Capabilities

- Android Capabilities
  ```json
  {
    "platformName": "Android",
    "appium:platformVersion": "14.0",
    "appium:deviceName": "name of the device which displayed when we run 'adb devices' command",
    "appium:automationName": "UiAutomator2",
    "appium:app": "path to app",
    "appium:packageName": "", #required when app is not mentioned
    "appium:activityName": "" #required when app is not mentioned
  }
  ```
- iOS Capabilities
  ```json
  {
    "platformName": "iOS",
    "appium:platformVersion": "14.5",
    "appium:deviceName": "simulator name", # only required when dealing with simulators
    "appium:udid": "real device id", # only required when dealing with real devices
    "appium:automationName": "XCUITest",
    "appium:app": "path to app", #full path to the app to be tested, it can also be a URL. Extensions are “.ipa” for real devices and “.app” for Simulators.
    "appium:packageName": "", #required when app is not mentioned
    "appium:activityName": "", #required when app is not mentioned
    "appium:bundleId": "com.yourcompany.yourapp",
    "appium:autoGrantPermissions" : true,
    "appium:androidInstallTimeout" : 60,
    "appium:autoAcceptAlerts" : true
  }
  ```
- Find the Android App's package name and activity name from the output.

```bash
adb shell dumpsys activity activities | grep mFocusedActivity

Here's a breakdown of what this command does:

    1. **adb shell**: Executes the following command on the connected Android device.
    2. **dumpsys activity activities**: Prints information about all running activities.
    3. **grep mFocusedActivity**: Filters the output to only show lines containing mFocusedActivity.
    4. use **findstr** in case if you are using Window Operating System
```

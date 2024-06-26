### Software Development Engineer in Test

<details>
<summary>1. Web Application Automation</summary>

- **Development approach**

  1. TDD : Test Driven Development
  1. DDD : Data Driven Development
  1. BDD : Behavior Driven Development
  1. Hybrid Development

- **Automation Design pattern**

  1. POM : Page Object Model
  1. PFM : Page Factory Model

- **Programming Languages**
  1. Java
  2. Python
- **Automation Tools / Libraries**

  1. Selenium
  1. Cucumber

- **Test Frameworks**

  1. TestNG (for Java)
  2. JUnit (for Java)
  3. Pytest (for Python)

- **Build Tools**

  1. Maven (for Java)
  1. PIP (for Python)

- **Extras**
  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files
  1. Pandas (for Python) : for reading / writing excel or csv files

</details>

<details>
<summary>2. Mobile Application Automation</summary>

- **Development approach**

  1. TDD : Test Driven Development
  1. DDD : Data Driven Development
  1. BDD : Behavior Driven Development
  1. Hybrid Development

- **Automation Design pattern**

  1. POM : Page Object Model
  1. PFM : Page Factory Model

- **Programming Languages**
  1. Java
- **Automation Tools / Libraries**

  1. Appium
  1. Selenium
  1. Cucumber

- **Devices**

  1. Android - Real / Emulator devices
  1. iOS - Real / Simulator devices

- **Test Frameworks**

  1. TestNG (for Java)
  2. JUnit (for Java)

- **Build Tools**

  1. Maven (for Java)

- **Extras**

  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files

- **Appium - Android Architecture**
<p align="center">
    <img src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*0jcsqDOGkceEjYoRJxctnQ.jpeg" />
</p>

- **Android Capabilities**
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
- **Appium - iOS Architecture**
<p align="center">
    <img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*9AHKmwXiFi2vvwBzC5pxpw.jpeg" />
</p>

- **iOS Capabilities**
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
    "appium:autoAcceptAlerts" : true,
    "appium:xcodeOrgId" : "", # real device | dev team will give
    "appium:updateWDABundleId" : "", # real device | dev team will give
    "appium:xcodeSigningId" : "iPhone developer" # real device
  }
  ```
- **Find the Android App's package name and activity name from the output**

```bash
adb shell dumpsys activity activities | grep mFocusedActivity

Here's a breakdown of what this command does:

    1. **adb shell**: Executes the following command on the connected Android device.
    2. **dumpsys activity activities**: Prints information about all running activities.
    3. **grep mFocusedActivity**: Filters the output to only show lines containing mFocusedActivity.
    4. use **findstr** in case if you are using Window Operating System
```

---

</details>

<details>
<summary>3. API Automation</summary>

- **Development approach**

  1. TDD : Test Driven Development
  1. BDD : Behavior Driven Development

- **Programming Languages**

  1. Java

- **Automation Tools / Libraries**

  1. Rest Assured
  1. Cucumber

- **Test Frameworks**

  1. TestNG (for Java)
  2. JUnit (for Java)

- **Build Tools**

  1. Maven

- **Extras**
  1. Extent Reports Library : for generating test reports
  1. Apache POI (for Java) : for reading / writing excel or csv files

---

</details>

<details>
<summary>4. Database Automation</summary>

- **Tools / Libraries**

  1. Java
  1. JDBC

- **Databases**

  1. MySQL
  1. Oracle SQL Developer
  1. Microsoft SQL Server

- **Connection strings and Class paths**
  | Database | Class.forName() | Connection String | Port |
  | :------------------- | :------------------------------------------- | :---------------------------------- | :--: |
  | MySQL | com.mysql.jdbc.Driver | jdbc:mysql://IP_ADDESS:PORT/DB_NAME | 3306 |
  | Oracle SQL Developer | oracle.jdbc.driver.OracleDriver | jdbc:oracle:thin:@IP_ADDESS:PORT:xe | 1521 |
  | Microsoft SQL Server | com.microsoft.sqlserver.jdbc.SQLServerDriver | jdbc:sqlserver://IP_ADDESS:PORT | 0000 |

`Note` : The full connection string for MS SQL Server = `jdbc:sqlserver://IP_ADDESS:PORT;databaseName=DB_NAME;user=USERNAME;password=PASSWORD`

- **Example Java Code**

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

</details>

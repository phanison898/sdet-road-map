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
    "appium:deviceName": "simulator name",
    "appium:udid": "real device id", # required if dealing with real devices
    "appium:automationName": "XCUiTest",
    "appium:app": "path to app",
    "appium:packageName": "", #required when app is not mentioned
    "appium:activityName": "", #required when app is not mentioned
    "appium:bundleId": "com.yourcompany.yourapp"
  }
  ```

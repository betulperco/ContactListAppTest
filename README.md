# ContactListAppTest

Automated Test Documentation: Contact List Application

This project contains automated tests for the Contact List application using JUnit and Selenium WebDriver. The tests cover the following functionalities:

User Registration and Login
Adding a New Contact
Logging Out
The tests are implemented in Java and use JUnit 4 for testing and Selenium WebDriver for browser automation. The tests are executed using ChromeDriver.

Prerequisites

Before running the tests, make sure you have the following installed:

Java (JDK 8 or higher)
Install the latest version of Java
Maven (for dependency management)
Google Chrome (latest version)
IntelliJ IDEA (or any Java IDE)

Setting Up the Project

Clone the repository or download the project to your local machine.
Open the project in IntelliJ IDEA or your preferred IDE.
Make sure Maven dependencies are properly resolved (check if pom.xml contains the necessary dependencies like JUnit and Selenium).
Install the required dependencies with Maven:
bash
Copy
mvn install
Running the Tests

Ensure you have Google Chrome installed on your machine.
The test suite uses ChromeDriver via the WebDriverManager to manage the browser driver automatically.
The setUp() method will set up the WebDriver and navigate to the Contact List web application.
To run the tests:

Via IntelliJ:
Right-click on the ContactListSmokeTest class in the project tree.
Select Run 'ContactListSmokeTest'.
Via Command Line:
Open the terminal in the project directory.
Run the following command to execute the tests:
bash
Copy
mvn test
Test Cases

1. User Registration and Login (testUserRegistrationAndLogin)
This test automates the process of:

Signing up a new user with first name, last name, email, and password.
Verifying redirection to the contact list page after successful registration.
Logging in with the registered user and verifying redirection to the contact list page.
2. Create New Contact (testCreateNewContact)
This test automates the process of:

Adding a new contact with first name, last name, email, and phone number.
Verifying the new contact appears in the contact list.
3. Logout Functionality (testLogoutFunctionality)
This test automates the process of:

Logging out from the application.
Verifying redirection to the login page.
Dependencies

Your project should include the following dependencies in the pom.xml file:

xml
Copy
<dependencies>
    <!-- Selenium WebDriver -->
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>3.141.59</version>
    </dependency>

    <!-- JUnit for testing -->
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.2</version>
        <scope>test</scope>
    </dependency>

    <!-- WebDriver Manager (for automatic driver management) -->
    <dependency>
        <groupId>io.github.bonigarcia</groupId>
        <artifactId>webdrivermanager</artifactId>
        <version>4.4.3</version>
    </dependency>
</dependencies>

Troubleshooting

"WebDriver was not initialized" error: Ensure that the setUp() method correctly initializes the WebDriver instance.
ChromeDriver issues: If you encounter issues with the ChromeDriver, ensure it’s correctly set up and the version matches your installed Chrome version.
Test failures: Check the browser logs and the specific error message to debug the failure.

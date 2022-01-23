# Task

### UI Automation test - Selenium WebDriver
It is a sample project for practising test automation. It will help you to save your time in extracting locators.
 
#### What do you have?
- web application with url http://automationpractice.com/index.php;
- 3 test cases, are described in TESTCASES.md 
- 3 automated tests.
 
#### What is expected?
Use your experience and design a solution for these test cases.
 
Tips:
- Clone project to your git [git help](https://herewecode.io/blog/create-repository-github/)
- Use page object model [example 1](https://www.toolsqa.com/selenium-webdriver/page-object-model/)  [example2](https://www.guru99.com/page-object-model-pom-page-factory-in-selenium-ultimate-guide.html)
- Use Webdriver Manager
- Logging [example1](https://www.baeldung.com/java-logging-intro) [example2 using lombok](http://www.javabyexamples.com/lombok-log4j-slf4j-and-other-log-annotations)
- Readable report - [Allure 1](https://www.swtestacademy.com/allure-report-testng/) [Allure 2](https://blog.knoldus.com/test-automation-report-with-allure-and-testng/)
- Failure evidences [Check Allure attachment and TestNg Listner](https://www.seleniumeasy.com/selenium-tutorials/allure-report-example-with-annotations)
- generating random values for insignificant test data, for example, for new user [Facker lib](https://www.baeldung.com/java-faker)
- Configurable for env/browsers/urls - [Use Properties](https://mkyong.com/java/java-properties-file-examples/)
- Support for parallel execution - [TestNg parallel](https://www.toolsqa.com/testng/testng-parallel-execution/)
- Reading test data from file, for example, the name of dress, size and color in the checkout test.[OpenCSV](https://mkyong.com/java/how-to-read-and-parse-csv-file-in-java/)



# Test Cases

## Sign in
#### Preconditions
* Generated customer with all customer data
#### Test steps
* Open [Home page](http://automationpractice.com/index.php)
* Click *Sign in* button
* Fill *Email address* to create an account
* Click *Create an account* 
* Fill all fields with correct data 
* Click *Register* button
#### Assertions
* My account page(?controller=my-account) is opened
* Proper username is shown in the header
* Log out action is available



## Log in
#### Preconditions
* Existing customer
#### Test steps
* Open [Home page](http://automationpractice.com/index.php)
* Click *Sign in* button (in the header)
* Fill *Email address* in _Already registered_ block
* Fill *Password* in _Already registered_ block
* Click *Sign in* 
#### Assertions
* My account page(?controller=my-account) is opened
* Proper username is shown in the header
* Log out action is available

## Checkout
#### Preconditions
* Existing customer
* Order details
#### Test steps
* Log in as existing customer
* Click *Women* button in the header
* Click the product with name "Faded Short Sleeve T-shirts"
* Click *Add to card*
* Click *Proceed to checkout*
* Click *Proceed to checkout*
* Click *Proceed to checkout*
* Click by *Terms of service* to agree
* Click *Proceed to checkout*
* Click by payment method *Pay by bank wire*
* Click *I confirm my order*
#### Assertions
* Order confirmation page(?controller=order-confirmation) is opened
* The order is complete.
* Current page is the last step of ordering 

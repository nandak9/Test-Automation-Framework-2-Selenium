# Selenium Test Automation

### Key Design Elements: 
1. Architecture Layers include Tests, Framework, Selenium Page Objects and Browser.
2. Page Object Pattern - clear seperation of pages versus test cases and represtative of the application.
3. All page classes contructors are called via a Single Generic type of page.
	* See: [SeleniumDemoFramework/Pages/Page.cs](https://github.com/eddif/SeleniumTestAutomationFramework/blob/master/SeleniumDemoFramework/Pages/Pages.cs)
	* Allows webdriver to only be instatiated once versus the overhead of passing the driver from page to page. 
4. Test cases do not include hard coded data, variables or the need to perform instatiation of any object type.
	* See: [SeleniumDemoTests\SmokeTests.cs](https://github.com/eddif/SeleniumTestAutomationFramework/blob/master/SeleniumDemoTests/SmokeTests.cs)
	* See: [SeleniumDemoTests\Features\TopNavigationTests.cs](https://github.com/eddif/SeleniumTestAutomationFramework/blob/master/SeleniumDemoTests/Features/TopNavigationTests.cs)
	* This creates a type of Internal DSL where test cases are written and read as a user might perfrom them. 	
	* Making test cases easy to write, simple to create, and maintainable.
5. Test cases never manage the state.
6. Extension Methods 
	* See: [SeleniumDemoFramework/Extensions/](https://github.com/eddif/SeleniumTestAutomationFramework/tree/master/SeleniumDemoFramework/Extensions)
7. Data Generators
	* See: [SeleniumDemoFramework/Generators/](https://github.com/eddif/SeleniumTestAutomationFramework/tree/master/SeleniumDemoFramework/Generators)
8. KeyWord driven data via Excel
	* See: [SeleniumDemoFramework/TestData/](https://github.com/eddif/SeleniumTestAutomationFramework/tree/master/SeleniumDemoFramework/TestData)
9. Base Class which can be extended to handle Initializations before Test Suites are executed.
	* Ideal for tracing Events such as realtime reporting of test case failure with wiating for full test run completion.

 
# To Use:

### Required: 

* Firefox installed

### Steps to execute:

* Note: All selenium dependencies are included in the solution.
* Extract Zip to local drive
* Open: \packages\nunit_runnable\bin\nunit.exe
* Click File > Open project and open \SeleniumDemoTests\bin\Debug\SeleniumDemoTests.dll
* Select tests to run
* Click Run


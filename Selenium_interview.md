====================================================================================================

**Q. Tell me about your roles and responsibilities in your project? Have you created framework from scratch? Explain architecture**



**=>**  	Based on your resume, for an Automation Engineer interview, I would answer this in a way that highlights your framework development, Python automation, Selenium/Playwright, PUMBA/SIMBA, API automation, and embedded/connected-services experience.

**Interview Answer**

“In my current role as a Software Automation & Development Engineer at Forvia Faurecia, my responsibilities are a combination of automation development, software integration testing, and framework development.

I work mainly on embedded and connected systems, where I perform SIT, sanity, regression, integration, and system-level testing. I have worked on projects such as McLaren, ESS+, and Technobricks, and my automation responsibilities include setting up the test environment, executing test cases, validating results, and generating logs and reports.

From the automation perspective, I have worked extensively with Python, Selenium, Playwright, TestNG, POM, REST Assured, and BDD. I have also worked with internal simulation frameworks such as PUMBA and SIMBA, where I automated the build, execution, and management of test cases.

Yes, I have developed automation frameworks and modules from scratch. One example is the Connected Services automation framework. I was involved in designing the framework structure, setting up the test environment, implementing reusable automation components, executing test scenarios, and validating the results. I also worked on automating certificate creation and testing, which helped make the process more reliable and scalable.


At a high level, I follow a layered architecture. The test layer contains the actual test cases and business scenarios. Below that, I have reusable automation or page/component layers, which contain common operations and application interactions. Then I have a utility layer for things such as configuration, logging, JSON handling, file operations, and common reusable functions. For API or system communication, I keep separate modules for API calls, socket communication, or hardware interaction.

I also focus heavily on logging and debugging. For one of my automation solutions, I developed an advanced logging mechanism that captured synchronized serial and video logs during test execution, which required multithreading and I/O handling.

I have also developed REST API automation for defect creation, including authentication, JSON processing, and error handling, and Selenium-based automation for workflows on the Leshan server.

Overall, my responsibility is not just writing test scripts. I focus on building reusable, maintainable, scalable automation frameworks, integrating them with the test environment, analyzing failures, and improving execution efficiency.”\*\*

**Explain your framework architecture.**



**=>**                     TEST CASES

&#x20;                       │

&#x20;                       ▼

&#x20;             Test / Scenario Layer

&#x20;          ┌─────────────────────────┐

&#x20;          │ SIT / Regression / Sanity│

&#x20;          │ Functional Test Cases   │

&#x20;          └────────────┬────────────┘

&#x20;                       │

&#x20;                       ▼

&#x20;             Automation Layer

&#x20;          ┌─────────────────────────┐

&#x20;          │ Selenium / Playwright   │

&#x20;          │ Python Automation       │

&#x20;          │ PUMBA / SIMBA            │

&#x20;          └────────────┬────────────┘

&#x20;                       │

&#x20;                       ▼

&#x20;             Reusable Components

&#x20;          ┌─────────────────────────┐

&#x20;          │ Page/Component Objects   │

&#x20;          │ API Modules              │

&#x20;          │ Socket Communication     │

&#x20;          │ ECU/Flashing Modules     │

&#x20;          └────────────┬────────────┘

&#x20;                       │

&#x20;                       ▼

&#x20;                Utility Layer

&#x20;          ┌─────────────────────────┐

&#x20;          │ Config / JSON / Files   │

&#x20;          │ Logging / Reporting     │

&#x20;          │ Common Utilities        │

&#x20;          │ Error Handling          │

&#x20;          └────────────┬────────────┘

&#x20;                       │

&#x20;                       ▼

&#x20;               Execution / CI

&#x20;          ┌─────────────────────────┐

&#x20;          │ Maven / Gradle / Git    │

&#x20;          │ Jenkins / CI Pipeline   │

&#x20;          └─────────────────────────┘

**====================================================================================================**

**Q. Which design pattern you have used in framework ?**

**=>** 

For your resume, the best and safest answer is Page Object Model (POM), especially because your skills explicitly mention Selenium WebDriver, TestNG, and POM Framework.
Interview Answer

“The main design pattern I have used in my automation framework is the Page Object Model, or POM.

The main purpose of POM is to separate the test logic from the application UI interaction logic. I create a separate class for each page or component, where I keep the locators and methods related to that page.

For example, for a Login page, I would have a LoginPage class containing the username, password, and login button locators, along with methods such as enterUsername(), enterPassword(), and clickLogin().



Then my test class only focuses on the business flow, such as login with valid credentials, instead of directly interacting with locators.



This makes the framework reusable, maintainable, and easier to update. For example, if the login button locator changes, I only need to update it in the LoginPage class rather than modifying multiple test cases.



Along with POM, I have also used reusable utility components and a layered framework structure for configuration, logging, API handling, test execution, and reporting.”\*\*



If they ask: “Why did you choose POM?”



**Give these 5 points:**



**Maintainability** – UI changes are handled in one place.

**Reusability** – Page methods can be reused across multiple tests.

**Separation of concerns** – Test logic and UI interaction are separated.

**Readability** – Tests look more like business scenarios.

**Scalability** – Easier to add new pages and test cases.

**Very likely follow-up**



**Interviewer:** “Apart from POM, which other design patterns have you used?”



For your profile, I would answer carefully:



“POM is the primary design pattern I have directly used in my Selenium automation. In addition, I have applied framework-level concepts such as reusable utility classes, separation of concerns, and common driver/configuration management. I would not claim a specific GoF pattern unless I have actually implemented it in the project.”



That last sentence is important—don't name Singleton, Factory, Strategy, etc. just because they are common interview answers. If the interviewer asks specifically about Singleton or Factory, I can prepare the answer based on your actual framework experience.



**==================================================================================================**

**Explain how do you pick which test cases to automate ?**

**=>** 

&#x09; For an Automation Engineer interview, I’d answer this with a practical approach rather than just saying “I automate repetitive test cases.”



**Interview Answer**



**“I don't automate every test case. I first analyze the test suite based on business value, execution frequency, stability, and automation feasibility.**



I generally prioritize test cases that are frequently executed, especially regression and sanity test cases, because automation gives us a good return on investment.



I also prioritize critical business functionality and high-risk areas. For example, if a failure in a particular feature can block the entire release, I would consider that feature a high priority for automation.



Another factor is whether the test case is stable and deterministic. If the functionality is still changing frequently, automating it immediately may create a lot of maintenance effort.



I also look at data complexity, environment dependencies, and technical feasibility. If a test requires a lot of manual judgment or visual interpretation, it may not be a good candidate for automation.



**So my general priority is:**



**High business impact + frequently executed + repetitive + stable + automation-feasible = good candidate for automation.**



In my current project, I have focused on automating regression, integration, and system-level scenarios, including SWC test cases, ECU flashing/performance testing, Connected Services workflows, and API/UI validation. This helped reduce manual effort and improve test coverage and execution efficiency.”\*\*



A simple way to explain your selection criteria

**Test case	 		Automate?	Reason**

**--------------------------------------------------------------**

Smoke/Sanity tests	✅ High priority	Run frequently

Regression tests	✅ High priority	Repeated every release

Critical business flows	✅ High priority	High impact

Data-driven tests	✅			Many combinations

API validation		✅			Fast and repeatable

Performance tests	✅			Difficult manually at scale

One-time test		❌ Usually		Low ROI

Frequently changing UI	⚠️ Later		High maintenance

Exploratory testing	❌			Requires human judgment

Usability testing	❌ Usually		Human observation required

Strong follow-up answer



**If the interviewer asks “How do you decide whether automation is worth it?”, say:**



“I consider the ROI. I compare the initial automation development and maintenance effort against how many times the test will execute and how much manual effort it will save. For example, if a regression test takes 10 minutes manually and runs 50 times across releases, automating it provides significant long-term benefit. But if a test takes two minutes and runs only once, automation may not be justified.”



That ROI-based answer is particularly strong for an Automation Engineer because it shows you're thinking beyond simply writing scripts.



**===================================================================================================**

**Q. Suppose you have 200 test case and 49 test failed , how would you collect the data of only failed test cases in testNg. Best way ?**

==> 

Yes. In a TestNG interview, the best approach is to use an ITestResult listener, specifically ITestListener, because it captures each test's result at runtime. You can collect the failed test method name, class, exception, parameters, etc.



**Interview Answer**



“If I have 200 TestNG test cases and 49 are failed, I would use the TestNG ITestListener interface, particularly the onTestFailure() method.



Whenever a test case fails, TestNG automatically invokes onTestFailure(ITestResult result). I can use the ITestResult object to collect details such as the test method name, class name, parameters, exception, and execution status.



I would store these failed test details in a collection, such as a List, and after execution I can use that list to generate a failed-test report or trigger a retry/rerun of only those failed tests.



So, rather than checking all 200 test cases after execution, the listener captures the 49 failures automatically during execution.”\*\*



**Simple implementation:**



public class TestListener implements ITestListener {



&#x20;   List<String> failedTests = new ArrayList<>();



&#x20;   @Override

&#x20;   public void onTestFailure(ITestResult result) {



&#x20;       String testName = result.getMethod().getMethodName();

&#x20;       String className = result.getTestClass().getName();



&#x20;       failedTests.add(className + "." + testName);



&#x20;       System.out.println("Failed Test: " + testName);

&#x20;       System.out.println("Exception: " + result.getThrowable());

&#x20;   }



&#x20;   @Override

&#x20;   public void onFinish(ITestContext context) {



&#x20;       System.out.println("Total Failed Tests: " + failedTests.size());



&#x20;       for (String test : failedTests) {

&#x20;           System.out.println(test);

&#x20;       }

&#x20;   }

}

**Register it with:**



@Listeners(TestListener.class)

public class LoginTest {

&#x20;   

&#x20;   @Test

&#x20;   public void validLogin() {

&#x20;       // test

&#x20;   }

}

**If interviewer asks: “What exactly can you collect from ITestResult?”**



**You can say:**



“From ITestResult, I can collect the test method name, test class, parameters, start and end time, status, throwable/exception, and test context. I can also use this information for screenshots, logs, reporting, and retry mechanisms.”



**⭐ Best-practice answer**



If they ask “What is the best way?”, don't say you would manually parse the TestNG report.



**Say:**



“The best way is an ITestListener. onTestFailure() gives me the failed test immediately, so I can capture the required information during execution. For reporting, I can then integrate that data with Extent Reports or another reporting mechanism. If the requirement is to rerun only failures, I can also use TestNG's retry mechanism or generate a failed-test suite after execution.”



This is a strong answer because it demonstrates TestNG knowledge + framework design thinking, rather than simply extracting data from an HTML report.



====================================================================================================

**====================================================================================================**



**Can you explain a critical automation scenario you have handled?**



**==>**	 Absolutely. For your profile, I would use your ECU flashing / Connected Services automation experience because it is genuinely critical and demonstrates more than simple UI automation. Your resume specifically mentions Python-based ECU flashing/performance automation and end-to-end Connected Services automation.



**Interview Answer**



“One critical automation scenario I handled was automating the ECU flashing and validation process for our ESS+ and Crony platforms.



This was a critical scenario because the ECU had to be flashed with the correct software, and after flashing we needed to make sure that the ECU was communicating properly and that the required functionality was working as expected.



Initially, some of these activities involved manual steps, so execution was time-consuming and there was also a possibility of human error. I worked on a Python-based automation solution to automate the flashing process and the subsequent validation.



My automation handled the required setup, triggered the flashing process, monitored the execution, and then performed the required validation checks. I also added proper logging and error handling, so whenever the process failed, we could identify at which stage the failure occurred.



One challenge was that this was not just a simple test-script execution. It involved interaction between the automation software, the ECU, and the test environment. So I had to make the automation robust against communication failures and unexpected responses.



I also worked on advanced logging where we captured synchronized serial and video logs during automation execution, which helped significantly during debugging and failure analysis.



The outcome was that we reduced the manual effort involved in flashing and validation and improved the repeatability and efficiency of the testing process. This was also one of the areas where I received a Spot Award for Excellence in Automation Development.”



**If interviewer asks: “What was the biggest challenge?”**



“The biggest challenge was handling the communication between the automation script, ECU, and test environment. A failure was not always a functional failure—it could also be caused by communication, timing, or environment issues. So I focused on proper synchronization, timeout handling, exception handling, and detailed logs. This made it easier to distinguish between an actual product defect and an automation or environment issue.”



**If they ask: “How did you make the automation reliable?”**



**Say:**



“I focused on synchronization rather than using fixed waits wherever possible, added timeout and exception handling, validated the response at each critical step, and captured detailed logs. For failures, I made sure enough diagnostic information was available to reproduce and analyze the issue.”



Key point: Don't present this as just “I wrote a Python script.” Present it as a critical end-to-end automation problem involving hardware/software interaction, synchronization, validation, logging, and failure analysis. That will sound much stronger for an Automation Engineer interview.

**=====================================================================================================**

**=====================================================================================================**



**Q. Apart from try-catch, how do you manage exceptions?**

**==>**  If this is asked in an Automation Engineer interview, I would answer like this:



“**Apart from try-catch, I manage exceptions at different levels of the automation framework.**



**First**, I use throws when the calling method should be responsible for handling the exception. For example, for file or configuration operations, I can propagate the exception to a higher layer instead of handling it at every method.



**Second**, I use custom exceptions for framework-specific failures. For example, if a required configuration is missing or an ECU communication step fails, I can create a meaningful custom exception instead of throwing a generic exception.



**Third**, I use TestNG listeners such as ITestListener to handle test-level failures centrally. When a test fails, I can capture the exception from ITestResult, take a screenshot, collect logs, and mark the test appropriately.



I also use finally blocks for cleanup activities such as closing resources or resetting the test environment, because cleanup should happen whether the test passes or fails.



In addition, I use logging and proper assertions. Assertions help identify functional failures, while logging helps us understand the actual cause of the failure.



So, my approach is not to put try-catch everywhere. I handle exceptions at the appropriate framework layer, propagate them when necessary, log sufficient diagnostic information, perform cleanup, and allow the test framework to report the failure properly.”\*\*



**Quick examples**



**1. throws — propagate exception**



public void readConfig() throws IOException {

&#x20;   // read configuration

}



**2. Custom exception**



class ECUCommunicationException extends Exception {

&#x20;   public ECUCommunicationException(String message) {

&#x20;       super(message);

&#x20;   }

}



**3. TestNG Listener**



@Override

public void onTestFailure(ITestResult result) {

&#x20;   System.out.println(result.getThrowable());

&#x20;   // capture screenshot

&#x20;   // collect logs

}



**4. finally — cleanup**



try {

&#x20;   executeTest();

} finally {

&#x20;   closeConnection();

&#x20;   cleanupEnvironment();

}

⭐ **Strong one-line answer**



**If the interviewer wants a short answer:**



“Apart from try-catch, I use exception propagation with throws, custom exceptions, TestNG listeners for centralized test-level failure handling, assertions for validation, logging for diagnostics, and finally blocks for resource cleanup. I choose the mechanism based on where the exception should be handled rather than catching every exception locally.”

**====================================================================================================**

**===================================================================================================**

**Q. Can you explain a defect with High Priority and Low Severity?**



**==> Yes. In an interview, I would explain it like this:**



“High Priority and Low Severity means the defect has a relatively small technical or functional impact, but it needs to be fixed quickly because it is important from a business or release perspective.”



**For** **example**: Suppose an e-commerce website has a spelling mistake in the company name on the home page, just before a major product launch or marketing campaign.



The defect does not affect any functionality—the user can still log in, search for products, add products to the cart, and make payments. So the severity is Low.



However, the company name is highly visible to customers and the release is scheduled for an important business event. Therefore, the business may want it fixed immediately. So the priority is High.



Therefore: Low Severity + High Priority.



**Easy way to remember**

**Severity = How badly does the defect affect the system?**

**Priority = How quickly does the business want it fixed?**



**Another strong example**



Company logo is incorrect on the login page before a major public release.



**Functionality works → Low Severity**

Highly visible and affects company branding → High Priority



**Interview follow-up: “Can you give a real project example?”**



You can say:



“One example I have seen is a defect in a highly visible UI element where the actual functionality was working correctly, but the displayed information was incorrect. Technically the impact was low, so I considered it low severity, but because it was customer-facing and needed to be corrected before release, the priority was high.”



Don't confuse this with a blocker. A defect can be high priority without being high severity when the business urgency is high but the technical impact is small.



**=====================================================================================================**

**=====================================================================================================**

**Q. How do you handle merge conflicts during code commit?**

**==>**	When I encounter a merge conflict, I first make sure I have the latest changes from the remote repository.



**I usually follow these steps:**



**1.** \*\*Pull the latest code\*\* from the remote branch and check which files have conflicts.

**2**. \*\*Open the conflicted files\*\* and identify the conflict markers such as `<<<<<<<`, `=======`, and `>>>>>>>`.

**3.** I compare both versions and understand what changes were made by my branch and by the other developer.

**4.** I \*\*resolve the conflict manually\*\*, keeping the correct changes from both sides wherever required. I don't blindly choose "ours" or "theirs" because that could remove someone else's changes.

**5.** After resolving the conflict, I remove the conflict markers and \*\*run the relevant test cases\*\* to make sure the code is still working.

**6.** Then I stage the resolved files using `git add`, commit the resolution, and push the changes to the remote repository.

**7.** Finally, I verify the pull request or branch to make sure there are no remaining conflicts and the tests are passing.



For example, if there is a conflict in a Page Object or test class, I first understand why both changes were made, merge the required logic, and then execute the affected automation tests before pushing the code.



So, my approach is \*\*understand the conflict → resolve carefully → test → commit → push\*\*, rather than simply overriding one person's changes.

**If they ask you for the Git commands**



**You can say:**



git checkout my-branch

git pull origin my-branch



**# If merging another branch**

git merge develop



**# Resolve conflicts in the files**



git status

git add .

git commit -m "Resolve merge conflicts"

git push origin my-branch



**Strong interview point:**



“After resolving a conflict, I always run the impacted automation tests because a successful Git merge doesn't necessarily mean the functionality is correct.”



That last sentence is particularly good for an Automation Engineer because it connects Git conflict resolution with your testing responsibility.



**====================================================================================================**  

**====================================================================================================**





**==>**   Absolutely. For your interview, explain the framework as a real project architecture, not just by listing tools. Your resume supports Python, Selenium, Playwright, PUMBA/SIMBA, REST API automation, logging, socket communication, ECU flashing, and end-to-end automation.



How to explain it in the interview



“In my project, I followed a layered and modular automation framework architecture. The main objective was to make the framework reusable, maintainable, scalable, and easy to debug.



At a high level, my framework consists of the following components:



1\. Test/Business Layer



This is where we keep the actual test scenarios and test cases. The test cases describe what functionality needs to be validated, while the implementation details are kept in the lower layers.



For example, a test case could be:



Verify Connected Service certificate creation



The test should only contain the business flow and assertions rather than low-level implementation details.



2\. Automation/Execution Layer



This layer contains the automation logic. Depending on the application, I have worked with Python automation, Selenium, Playwright, and PUMBA/SIMBA-based automation.



For web automation, Selenium or Playwright interacts with the application. For embedded testing, the automation layer communicates with the simulation environment or target system.



3\. Page Object / Component Layer



For Selenium-based applications, I use the Page Object Model. Each page or major component has its own class containing locators and reusable actions.



For example:



LoginPage



enterUsername()

enterPassword()

clickLogin()



This keeps locators and UI interaction separate from the test cases.



4\. API Layer



I maintain separate modules for API operations. I have worked on REST API automation, including authentication, JSON request/response handling, validation, and error handling.



For example, instead of directly calling an API from every test case, I create a reusable API method such as:



createDefect()



and the test case simply calls that method and validates the response.



5\. Communication / Integration Layer



Because my project involves embedded and connected systems, this layer is particularly important. I have worked on client-server socket communication, including handshake and protocol validation.



This layer abstracts the communication mechanism from the test cases.



6\. Utility Layer



This contains common reusable utilities such as:



Configuration handling

JSON/file handling

Common Python utilities

Wait/retry mechanisms

Data handling

Error handling

Log utilities



The purpose is to avoid duplicate code across test cases.



7\. Configuration Layer



Environment-specific information is kept separately instead of hardcoding it inside test cases.



For example:



environment = SIT



server\_url = ...



timeout = ...



ECU configuration = ...



This allows us to run the same automation against different environments with minimal changes.



8\. Logging and Reporting



Logging is a very important component in my framework because we work with embedded systems. I developed an advanced logging mechanism that captures synchronized serial and video logs during automation execution. This involved multithreading and I/O handling.



So when a test fails, we can correlate the automation failure with the system/serial logs and video evidence.



9\. Test Data Layer



Test data is separated from the automation logic wherever possible. This allows us to execute the same test with different input combinations without modifying the test implementation.



10\. Build and Execution Layer



The framework provides a standard way to build and execute the tests. In my projects, I have worked with tools such as Maven, Gradle, Git/GitHub and the relevant test frameworks.



11\. CI/CD Integration



The framework can be integrated with Jenkins so that automation can be triggered automatically after a build or based on a schedule. The pipeline can prepare the environment, execute the required test suite, collect logs/results, and publish the report.



12\. Defect Automation



One of the reusable modules I developed was REST API automation for defect creation. It handled authentication, JSON processing and error management. I also developed UI automation for automatically creating defects in the defect-tracking system.



So overall, the architecture separates test logic, automation logic, application interaction, utilities, configuration, reporting, and execution. This makes the framework easier to maintain and allows us to reuse the same components across multiple projects and test suites.”\*\*



Architecture you can draw on a whiteboard:

&#x20;                        TEST CASES

&#x20;                            │

&#x20;                            ▼

&#x20;                ┌─────────────────────┐

&#x20;                │   Test / Business          │

&#x20;                │       Layer                │

&#x20;                └─────────┬────**-**──────┘

&#x20;                             │

&#x20;            ┌───────────**-**┼──────────────┐

&#x20;            ▼               ▼              ▼

&#x20;      Web Automation   API Automation   Embedded

&#x20;      Selenium /       REST Assured     Automation

&#x20;      Playwright                        PUMBA/SIMBA

&#x20;            │                │              │

&#x20;            └────────────**|─**─────────────┘

&#x20;                             ▼

&#x20;                ┌─────────────────────┐

&#x20;                │ Reusable Components        │

&#x20;                │ Page Objects        	  │

&#x20;                │ API Modules         	  │

&#x20;                │ Socket Modules      	  │

&#x20;                │ ECU Modules         	  │

&#x20;                └──────────┬──────────┘

&#x20;                           │

&#x20;                           ▼

&#x20;                ┌─────────────────────┐

&#x20;                │   Utility Layer     	  │

&#x20;                │ Config / JSON       	  │

&#x20;                │ File / Data         	  │

&#x20;                │ Retry / Error              │

&#x20;                │ Common Functions           │

&#x20;                └──────────┬──────────┘

&#x20;                               |

&#x20;            ┌─────────────┼──────────────┐

&#x20;            ▼                ▼              ▼

&#x20;         Logging           Reporting      Test Data

&#x20;            │                 │              │

&#x20;            └─────────────┼──────────────┘

&#x20;                              ▼

&#x20;                ┌─────────────────────┐

&#x20;                │ Execution / CI-CD   	  │

&#x20;                │ Git → Jenkins       	  │

&#x20;                │ Build → Test          	  │

&#x20;                │ Report → Artifacts  	  │

&#x20;                └─────────────────────┘



**⭐ Very important follow-up question**



**“Why did you design the framework this way?”**



**A strong answer is:**



**“**The main reason was separation of concerns. Test cases should contain business scenarios, while implementation details such as locators, API calls, socket communication, configuration and logging should remain in their respective layers. This reduces code duplication and makes maintenance easier. If a locator or API endpoint changes, I only need to update the corresponding component instead of modifying multiple test cases. It also makes the framework scalable because new test cases can reuse existing components.”



**And if they ask “Did you build this entire framework from scratch?”, don't simply say yes. Say:**



“Yes, I have developed framework components from scratch and have also contributed to existing project frameworks. In the Connected Services project, I was involved in designing and developing the automation framework and end-to-end certificate creation and testing process. My ownership included the automation modules, environment setup, execution flow, validation and logging.”

**=====================================================================================================**

**=====================================================================================================**



**Q. How do you run your test cases in parallel in Cucumber selenium testng ?**



**==>** Yes. In a Cucumber + Selenium + TestNG framework, I would explain parallel execution like this in an interview:



**Interview answer**



“I run Cucumber scenarios in parallel using TestNG. The main idea is that each Cucumber scenario is treated as an independent test and TestNG controls the number of parallel threads.



I use a Cucumber TestNG runner and configure the TestNG suite with parallel="tests" or parallel="methods" depending on how I want the scenarios to execute.



For example, if I have 20 Cucumber scenarios and configure 4 threads, TestNG can execute up to 4 scenarios concurrently instead of executing all 20 sequentially.



The most important part is that the WebDriver must be thread-safe. I don't use one static WebDriver instance across all threads. Instead, I create a separate WebDriver instance for each thread, commonly using ThreadLocal<WebDriver>.



**So the architecture is:**



**TestNG → Cucumber scenarios → Step Definitions → Page Objects → ThreadLocal WebDriver**



Each thread gets its own browser instance. This prevents one scenario from interfering with another.”\*\*



**Example configuration**



**For a TestNG-based Cucumber project, I would typically have:**



<suite name="Parallel Suite" parallel="tests" thread-count="4">



&#x20;   <test name="Cucumber Tests">

&#x20;       <classes>

&#x20;           <class name="runner.TestRunner"/>

&#x20;       </classes>

&#x20;   </test>



</suite>



**And the runner:**



@CucumberOptions(

&#x20;   features = "src/test/resources/features",

&#x20;   glue = "stepdefinitions",

&#x20;   plugin = {

&#x20;       "pretty",

&#x20;       "html:target/cucumber-report.html"

&#x20;   }

)

public class TestRunner extends AbstractTestNGCucumberTests {

}



**For more control over parallel scenarios, I can override the DataProvider:**



@Override

@DataProvider(parallel = true)

public Object\[]\[] scenarios() {

&#x20;   return super.scenarios();

}



This tells TestNG to execute the Cucumber scenarios supplied by the DataProvider in parallel.



**Thread-safe WebDriver**



**This is the most important interview point:**



public class DriverManager {



&#x20;   private static ThreadLocal<WebDriver> driver = new ThreadLocal<>();



&#x20;   public static void setDriver(WebDriver webDriver) {

&#x20;       driver.set(webDriver);

&#x20;   }



&#x20;   public static WebDriver getDriver() {

&#x20;       return driver.get();

&#x20;   }



&#x20;   public static void unload() {

&#x20;       driver.get().quit();

&#x20;       driver.remove();

&#x20;   }

}



**Then in the hooks:**



@Before

public void setUp() {

&#x20;   WebDriver driver = new ChromeDriver();

&#x20;   DriverManager.setDriver(driver);

}



@After

public void tearDown() {

&#x20;   DriverManager.unload();

}



So conceptually:

&#x20;                **TestNG**

&#x20;                  **│**

&#x20;         **┌────────┼────────┐**

&#x20;         **│        │        │**

&#x20;      **Thread-1 Thread-2 Thread-3 Thread-4**

&#x20;         **│        │        │**

&#x20;       **Chrome   Chrome   Chrome   Chrome**

&#x20;         **│        │        │**

&#x20;      **Scenario Scenario Scenario Scenario**

&#x20;         **│        │        │**

&#x20;      **Steps → Page Objects → WebDriver**



**If interviewer asks: “Why ThreadLocal?”**



**Say:**



“Because WebDriver is not thread-safe. If multiple parallel scenarios use the same driver instance, one scenario can navigate or modify the browser state of another scenario. ThreadLocal gives each execution thread its own WebDriver instance, so the scenarios remain isolated.”



**If they ask: “How do you decide the thread count?”**



“I don't simply increase the thread count to the maximum. I consider machine CPU, RAM, browser resource consumption, application/server capacity, and the number of tests. For example, I might start with 4 threads, monitor execution stability and resource utilization, and then tune it based on the environment.”



**Strong follow-up point**



Also mention that test data must be isolated. Even with separate browsers, parallel tests can still interfere if they use the same user/account, database record, file, or environment data.



**Best one-line answer to remember:**



**“**In Cucumber with TestNG, I enable parallel execution through TestNG/DataProvider, and I use ThreadLocal WebDriver so every parallel scenario gets an independent browser session.”





**====================================================================================================**

**====================================================================================================**

**Q. Explain the contents of the Runner File in Cucumber?**



**==>** For a Cucumber + Java automation framework, you can explain the Runner file like this in an interview.



**What is a Cucumber Runner File?**



“The Cucumber Runner class is the entry point for executing Cucumber feature files. It connects the feature files with the step definitions and configures how Cucumber should execute and report the tests.”



**A typical Runner looks like:**



@RunWith(Cucumber.class)

@CucumberOptions(

&#x20;   features = "src/test/resources/features",

&#x20;   glue = "stepdefinitions",

&#x20;   tags = "@Regression",

&#x20;   monochrome = true,

&#x20;   publish = false,

&#x20;   plugin = {

&#x20;       "pretty",

&#x20;       "html:target/cucumber-report.html",

&#x20;       "json:target/cucumber.json"

&#x20;   }

)

public class TestRunner {

}

**Explain each component**

**1. @RunWith(Cucumber.class)**

**@RunWith(Cucumber.class)**



This tells JUnit that this test class should be executed using the Cucumber test runner rather than the normal JUnit runner.



Interview point: It acts as the bridge between JUnit and Cucumber.



**2. features**

features = "src/test/resources/features"



This tells Cucumber where the .feature files are located.



For example:



src/test/resources/features/

&#x20;   Login.feature

&#x20;   Payment.feature

&#x20;   Search.feature



You can also specify a particular feature:



features = "src/test/resources/features/Login.feature"

**3. glue**

glue = "stepdefinitions"



glue tells Cucumber where it can find:



Step Definition classes

Hooks such as @Before and @After



For example:



src/test/java/

&#x20;   stepdefinitions/

&#x20;       LoginSteps.java

&#x20;       PaymentSteps.java

&#x20;   hooks/

&#x20;       Hooks.java



If your feature contains:



Given I enter valid username



Cucumber searches the glue package for the corresponding step definition.



**4. tags**

tags = "@Regression"



Tags allow us to control which scenarios should execute.



For example:



@Smoke

Scenario: Verify login



@Regression

Scenario: Verify payment



Then:



tags = "@Smoke"



runs only Smoke scenarios.



**You can also use expressions:**



tags = "@Smoke and @Login"



or:



tags = "@Smoke or @Regression"



This is particularly useful when you have a large regression suite.



5\. plugin

plugin = {

&#x20;   "pretty",

&#x20;   "html:target/cucumber-report.html",

&#x20;   "json:target/cucumber.json"

}



**Plugins control output and reporting.**



**Common examples:**



**pretty**



Provides readable console output.



html:target/cucumber-report.html



**Generates an HTML report.**



json:target/cucumber.json



Generates JSON results that can be consumed by reporting tools.



**6. monochrome**

monochrome = true



It makes the console output more readable by removing unnecessary formatting characters.



**7. publish**

publish = false



Controls whether Cucumber publishes execution results to Cucumber's online reporting service.



Overall execution flow



Explain the Runner flow like this:



Runner Class

&#x20;    │

&#x20;    ▼

Cucumber

&#x20;    │

&#x20;    ▼

Feature File

&#x20;    │

&#x20;    ▼

Read Gherkin Scenario

&#x20;    │

&#x20;    ▼

Find Step Definition

&#x20;    │

&#x20;    ▼

Execute Automation Code

&#x20;    │

&#x20;    ▼

Hooks / Setup / Cleanup

&#x20;    │

&#x20;    ▼

Assertions

&#x20;    │

&#x20;    ▼

**Generate Report**

**⭐ Strong interview answer**



If the interviewer asks “Explain your Runner file”, give this concise answer:



“Our Cucumber Runner file is the execution entry point. We use @RunWith(Cucumber.class) to integrate Cucumber with JUnit. Inside @CucumberOptions, we configure the feature path, glue package, tags, plugins and execution-related options. The features parameter tells Cucumber where the feature files are, while glue tells it where the step definitions and hooks are located. We use tags to execute specific suites such as Smoke or Regression. Plugins are used for console output and generating HTML or JSON reports. So essentially, the Runner controls which scenarios execute, where Cucumber finds their implementation, and how the execution results are reported.”



One common follow-up question



Interviewer: “What happens if the glue path is incorrect?”



Answer:



“Cucumber will not be able to find the corresponding step definitions or hooks. The scenario will generally be reported as undefined, because Cucumber can find the Gherkin step in the feature file but cannot locate its implementation.”



**===========================================================================================**

**============================================================================================**

**Q.  What is a Singleton Design Pattern?**



**==>**  	A Singleton Design Pattern is a creational design pattern that ensures only one object/instance of a class is created throughout the application, and provides a common way to access that instance.



In automation frameworks, Singleton is commonly used for things like WebDriver, configuration managers, logging, or database connections, where we may want controlled access to a single shared instance.



**How do we implement Singleton in Java?**



**There are 3 important parts:**



**Private constructor** – prevents other classes from creating objects using new.

**Static instance** – stores the single object.

**Static method** – provides access to that object.

public class Singleton {



&#x20;   private static Singleton instance;



&#x20;   // Private constructor

&#x20;   private Singleton() {

&#x20;   }



&#x20;   // Get the single instance

&#x20;   public static Singleton getInstance() {



&#x20;       if (instance == null) {

&#x20;           instance = new Singleton();

&#x20;       }



&#x20;       return instance;

&#x20;   }

}



Usage:



Singleton obj1 = Singleton.getInstance();

Singleton obj2 = Singleton.getInstance();



System.out.println(obj1 == obj2);



Output:



true



**Both references point to the same object.**



**How to explain it in an Automation Engineer interview**



“Singleton is a creational design pattern that restricts a class to having only one instance and provides a global access point to that instance. In an automation framework, it can be useful for components such as configuration or driver management when we intentionally want a single shared instance. We implement it using a private constructor, a static instance variable, and a static getInstance() method.”



**Interview follow-up: Why use Singleton?**



**You can say:**



“It prevents unnecessary creation of multiple objects, provides controlled access to a shared resource, and can help manage resources such as configuration or database connections.”



**⚠️ Important Selenium point**



If the interviewer asks “Would you always make WebDriver Singleton?”, don't say yes.



A Singleton WebDriver means multiple tests/threads may end up sharing the same browser instance, which can create problems with parallel execution and test isolation.



For a modern parallel automation framework, ThreadLocal WebDriver is often more appropriate:



Thread 1 → Driver 1

Thread 2 → Driver 2

Thread 3 → Driver 3



while each thread still gets controlled access to its own driver.



Next likely question: “What is the difference between Singleton and Factory Design Pattern?”



**===========================================================================================**

**===========================================================================================**



**Q. What are the advantages and disadvantages of the Page Object Model?**



**==>** 	Page Object Model (POM) is a design pattern used in UI automation where each application page or major UI component is represented by a separate class. The class contains the locators and methods/actions for that page, while the test class contains the actual test scenario.



For example:



LoginPage.java

&#x20;├── username

&#x20;├── password

&#x20;├── loginButton

&#x20;├── enterUsername()

&#x20;├── enterPassword()

&#x20;└── clickLogin()



LoginTest.java

&#x20;└── verifyLogin()

**Advantages**



**1. Maintainability**



If a locator changes, we generally update it in one Page Object instead of changing it across multiple test cases.



“For example, if the Login button locator changes, I update it in LoginPage, and all tests using that page can continue to work.”



**2. Reusability**



Common actions can be reused across multiple test cases.



loginPage.login("user", "password");



Instead of writing the same locator and interaction repeatedly.



**3. Separation of concerns**



**POM separates:**



Test logic → what we want to test

Page logic → how we interact with the UI



This makes test cases cleaner.



**4. Reduced code duplication**



Common UI operations are implemented once and reused.



**5. Easier debugging**



If a particular page interaction fails, we can directly investigate the corresponding Page Object.



**6. Scalability**



As the automation suite grows, organizing pages/components into separate classes makes the framework easier to manage.



**Disadvantages**



**1. Initial development effort**



Creating Page Object classes for every page/component requires additional time, especially for a large application.



**2. More classes to maintain**



A large application can result in many Page Object classes, which can become difficult to organize if the architecture isn't designed properly.



**3. UI changes can still require maintenance**



POM centralizes locators, but it doesn't eliminate maintenance. If the UI structure changes significantly, the corresponding Page Objects still need to be updated.



**4. Not ideal to put everything into one Page class**



A very large page can have hundreds of locators and methods. This can make the class difficult to maintain.



A better approach is to divide it into reusable components where appropriate—for example:



HomePage

&#x20;├── HeaderComponent

&#x20;├── NavigationComponent

&#x20;├── SearchComponent

&#x20;└── FooterComponent

**⭐ Best interview answer**



“The major advantage of POM is maintainability and reusability. It separates test logic from UI implementation, reduces code duplication, and centralizes locators. So if a locator changes, we usually update it in the Page Object instead of modifying multiple test cases.



The disadvantages are that it requires initial development effort and can lead to a large number of classes or very large Page Objects in a complex application. To overcome that, we can use reusable component objects and maintain a proper layered framework architecture.”



**Likely follow-up**



**Interviewer**: “What is the difference between POM and PageFactory?”



Remember this distinction:



**POM** → design pattern/architecture for organizing page-specific automation code.

PageFactory → Selenium's mechanism traditionally used to initialize @FindBy web elements.



So POM and PageFactory are not the same thing.



**============================================================================================**

**============================================================================================**

**Q. How do you decide the priorities of your Test Cases?**



**==>** For an Automation Engineer interview, I would answer this by explaining that test-case priority is based mainly on business impact, risk, and frequency of use.



**Interview Answer**



“I prioritize test cases based on business criticality, risk, frequency of usage, and the impact of failure.



**First**, I identify the critical business functionalities. Features such as login, payment, data creation, or core services generally get higher priority because their failure can directly impact the customer or business.



**Second**, I consider the risk and impact of the feature. If a feature has a high probability of failure or its failure can affect other modules, I give it higher priority.



**Third**, I consider how frequently the functionality is used. Frequently used and customer-facing features are generally prioritized over rarely used features.



**Based on this,** I normally categorize test cases into P0/P1/P2 or High/Medium/Low priority.



**P0/High**: Critical functionality or smoke tests that must pass before we proceed—for example, application startup, login, core service availability, or a critical end-to-end workflow.



**P1/Medium**: Important functional and integration scenarios that should be covered in the main regression suite.



**P2/Low:** Less frequently used, low-risk, cosmetic, or edge-case scenarios that can be executed later depending on the available time.



**In my project**, especially for SIT and regression testing, I also consider dependencies between modules. If one component is a prerequisite for several other features, I test that component first.



So overall, my priority is business impact → risk → critical functionality → dependencies → frequency of usage.”\*\*



**Example**



Suppose you have these 5 test cases:



Test Case	Priority	Why

Application starts successfully	P0	Basic system availability

User login	P0/P1	Critical and frequently used

Core business workflow	P0/P1	High business impact

API error handling	P1	Important integration coverage

UI color/font validation	P2	Low functional impact





**If the interviewer asks:**



**“What if you have only 2 hours to test?”**



Say:



“I would perform risk-based testing. I would first execute the smoke and critical business scenarios, then high-risk integration/API scenarios, followed by important regression cases. I would communicate the remaining unexecuted cases and the associated risk to the team rather than simply saying testing is complete.”



This answer demonstrates that you understand risk-based testing, rather than prioritizing test cases just because they are easy or automated.



**==========================================================================================**

**==========================================================================================**



**Q. Explain the Maven Lifecycle**



**==>** For an Automation Engineer interview, explain it as:



“Maven Lifecycle is a predefined sequence of phases that Maven follows to build, test, package, and deploy a Java project. Each lifecycle consists of multiple phases, and when we execute a particular phase, all the preceding phases are also executed.”



**Maven has three built-in lifecycles:**



**Clean Lifecycle**

**Default/Build Lifecycle**

**Site Lifecycle**

**1. Clean Lifecycle**



Used to clean the project and remove previously generated build files.



**Important phases:**



pre-clean

&#x20;   ↓

clean

&#x20;   ↓

post-clean



**The most commonly used command is:**



mvn clean



**It removes the target directory.**



For example:



target/

&#x20;├── compiled classes

&#x20;├── test reports

&#x20;└── generated artifacts



will be removed.



**2. Default / Build Lifecycle**



This is the most important lifecycle for automation projects.



Important phases are:



validate

&#x20;  ↓

compile

&#x20;  ↓

test

&#x20;  ↓

package

&#x20;  ↓

verify

&#x20;  ↓

install

&#x20;  ↓

deploy

validate



**Checks whether the project is correctly structured and the required information is available.**



mvn validate

compile



**Compiles the main Java source code.**



mvn compile



The compiled .class files are generally generated under:



**target/classes**



test



Compiles and executes the unit tests using the configured test framework.



mvn test



For an automation project, this is commonly where we execute our test cases depending on the Maven/test-runner configuration.



**For example:**



mvn test -Dcucumber.filter.tags="@Regression"

**package**



Packages the compiled code into an artifact such as a JAR or WAR.



mvn package



**It also runs the earlier phases, so conceptually:**



validate → compile → test → package



**verify**



Runs checks to verify that the package is valid and satisfies quality criteria.



mvn verify



**install**



Installs the generated artifact into the developer's local Maven repository.



mvn install



**Usually the local repository is:**



\~/.m2/repository



**deploy**



Publishes the artifact to a remote Maven repository.



mvn deploy



This is typically relevant when sharing build artifacts across teams or CI/CD environments.



**3. Site Lifecycle**



The Site lifecycle is used for generating project documentation and reports.



Main phases include:



pre-site

&#x20;  ↓

site

&#x20;  ↓

post-site

&#x20;  ↓

site-deploy



For example:



mvn site



can generate project documentation/reports.



⭐ Important interview concept



**“What happens when you run mvn test?”**



Say:



“Maven doesn't execute only the test phase. It executes all phases that come before test in the default lifecycle. So it performs validation, compiles the source code, and then executes the test phase.”



**Conceptually:**



mvn test



validate

&#x20;  ↓

compile

&#x20;  ↓

test



Similarly:



mvn package



will execute:



validate

&#x20;→ compile

&#x20;→ test

&#x20;→ package



And:



mvn install



will execute the required preceding phases through:



validate

&#x20;→ compile

&#x20;→ test

&#x20;→ package

&#x20;→ verify

&#x20;→ install

⭐ Strong 30-second interview answer



“Maven provides three main lifecycles: Clean, Default, and Site. The Default lifecycle is the most important for our automation project. Its major phases are validate, compile, test, package, verify, install, and deploy. When we execute a particular phase, Maven also executes all preceding phases. For example, mvn test validates and compiles the project before executing tests, while mvn clean test first removes the previous target directory and then builds and executes the tests. In automation, we commonly use Maven to manage dependencies through pom.xml and to execute our test suites in a consistent way.”



**============================================================================================**

**============================================================================================**



**Q. How do you run the failed test cases?**



**==>** For an Automation Engineer interview, answer this by explaining both the framework-level retry mechanism and how you rerun only failed tests manually.



Interview Answer



“When test cases fail, first I analyze the failure rather than immediately rerunning them. I check the logs, screenshots, error messages, and whether the failure is due to an application defect, environment issue, or automation issue.



If the failure is a genuine application defect, I don't simply rerun it repeatedly. I log the defect and track it. If it is a transient failure, such as an environment issue, network issue, or timing problem, I can rerun the failed test.



In Cucumber, I can identify the failed scenarios from the execution report and rerun them using tags or a generated failed-scenarios file.



In a Maven-based framework, we can also execute a specific test class or suite again rather than running the entire regression suite.



We can additionally implement a retry mechanism at the framework level. For example, if a test fails because of a temporary issue, the framework can retry it a limited number of times. I prefer keeping the retry count limited so that genuine defects aren't hidden.



After rerunning, I compare the results with the original execution and report whether the failure was reproducible or flaky.”\*\*



**Cucumber — rerun failed scenarios**



A common approach is using the Cucumber rerun plugin:



plugin = {

&#x20;   "pretty",

&#x20;   "rerun:target/failed\_scenarios.txt",

&#x20;   "html:target/cucumber-report.html"

}



After execution, the failed scenarios are written to:



target/failed\_scenarios.txt



Then a separate runner can execute that file:



@CucumberOptions(

&#x20;   features = "@target/failed\_scenarios.txt",

&#x20;   glue = "stepdefinitions"

)

public class FailedTestRunner {

}



Regression Execution

&#x20;       ↓

&#x20;  Test Failures

&#x20;       ↓

&#x20;Analyze failure

&#x20;       ↓

&#x20;┌───────────────┐

&#x20;│ Application       │ → Raise defect

&#x20;│ defect?           │

&#x20;└───────────────┘

&#x20;       ↓ No

&#x20;Environment / Automation issue?

&#x20;       ↓

&#x20;  Rerun failed test

&#x20;       ↓

&#x20;┌───────────────┐

&#x20;│ Pass → Flaky/     │

&#x20;│ transient         │

&#x20;│ failure           │

&#x20;└───────────────┘



**Do you use retry?”**



Say:



“Yes, where appropriate. I use retry mainly for transient failures, not to mask actual application defects. I keep the retry count limited, usually one or two retries, and I still investigate the original failure using logs and screenshots.”



This is a stronger answer than simply saying “I use retry analyzer to run failed cases again”, because interviewers want to know that you can distinguish real defects from flaky automation.



===========================================================================================

==========================================================================================**Q**

**Q.  What is the defect life cycle?**



**==>** Defect Life Cycle



The Defect Life Cycle is the sequence of stages a defect goes through from the time it is identified until it is closed.



**A typical defect life cycle is:**

&#x20;       **New**

&#x20;        **↓**

&#x20;      **Open**

&#x20;        **↓**

&#x20;   **In Progress**

&#x20;        **↓**

&#x20;      **Fixed**

&#x20;        **↓**

&#x20;     **Retest**

&#x20;     **↙    ↘**

&#x20;  **Pass     Fail**

&#x20;   **↓        ↓**

&#x20; **Closed   Reopened**

&#x20;            **│**

&#x20;            **└──────→ In Progress**



**Explain each status in an interview**



**1. New**



“When I identify a defect during testing, I log it in the defect tracking tool with details such as steps to reproduce, expected result, actual result, severity, screenshots/logs, and environment.**”**



**2. Open / Assigned**



**“**The defect is reviewed and assigned to the appropriate developer or team.”



**3. In Progress**



**“**The developer starts analyzing and working on the defect.”



**4. Fixed / Resolved**



“Once the developer fixes the issue, the defect is marked as fixed or resolved and sent back to QA for verification.”



**5. Retest**



“As a tester, I execute the same steps that originally reproduced the defect and verify whether the fix works.”



**6. Closed**



“If the defect is fixed and the retest passes, I close the defect.”



**7. Reopened**



“If the issue still exists during retesting, I reopen the defect and provide updated evidence or logs.”



**Other possible statuses**



**Depending on the project, you may also see:**



Duplicate — Same defect has already been reported.

Rejected / Not a Bug — The reported behavior is actually expected behavior.

Won't Fix — Team decides not to fix it.

Deferred — Fix is postponed to a future release.

**Cannot Reproduce — Developer cannot reproduce the reported issue.**

**⭐ Interview-ready answer**



**“The defect life cycle starts when a tester identifies and logs a defect. Initially, it is marked New and then assigned to the developer. The developer analyzes it and moves it to In Progress. Once the fix is implemented, it is marked Fixed or Resolved and comes back to QA for retesting. If the issue is fixed, QA closes the defect. If it still exists, QA reopens it and sends it back to development. Depending on the project, defects can also have statuses such as Duplicate, Rejected, Deferred, Won't Fix, or Cannot Reproduce.”**



**============================================================================================**

**============================================================================================**

**Q. How do you handle Flaky tests? expects - Explicit waits, stable locators, retry analyzer, screenshots**



**==>** For an Automation Engineer interview, your answer should directly cover the four things the interviewer expects: explicit waits, stable locators, Retry Analyzer, and screenshots.



Interview-ready answer



“I handle flaky tests by first identifying the root cause rather than simply adding retries. Usually, flaky tests happen because of synchronization issues, unstable locators, dynamic data, environment issues, or timing problems.



**First**, I use explicit waits instead of Thread.sleep(). I wait for a specific condition, such as an element being visible, clickable, or a particular API response/state being available.



WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));

WebElement loginButton = wait.until(

&#x20;   ExpectedConditions.elementToBeClickable(By.id("loginBtn"))

);

loginButton.click();



**Second**, I use stable locators. I prefer unique IDs, stable attributes, or reliable CSS/XPath rather than dynamic XPath expressions based on changing indexes or text.



**Third**, for tests that fail intermittently because of temporary issues, I use TestNG's Retry Analyzer. It allows the failed test to be executed again a limited number of times. But I don't use retries to hide genuine product defects.





@Test(retryAnalyzer = RetryAnalyzer.class)

public void verifyLogin() {

&#x20;   // test steps

}

Inside the Retry Analyzer, I can restrict the retry count, for example to one or two retries.



**Fourth,** I capture screenshots when a test fails. This helps me understand the exact state of the application at the point of failure. Along with screenshots, I check the logs and error messages to identify whether the issue is automation-related or an actual application defect.



**So** my approach is: stabilize synchronization → use stable locators → investigate the root cause → use limited retries only where appropriate → capture screenshots and logs for debugging.



I also monitor flaky tests over multiple executions. If the same test keeps failing intermittently, I fix the underlying problem rather than increasing the retry count.”\*\*



**If interviewer asks: “Why don't you use Thread.sleep()?”**



**Say:**



“Thread.sleep() always waits for the specified amount of time, even if the application is ready earlier. It makes execution slower and doesn't guarantee that the required condition has been met. Explicit waits are better because they wait only until the required condition is satisfied or the timeout is reached.”



**If they ask: “Will Retry Analyzer fix flaky tests?”**



**A strong answer:**



“No. Retry Analyzer only helps identify whether a failure is intermittent. It doesn't fix the root cause. If a test passes on retry, I investigate why it failed initially—such as synchronization, locator instability, test data, environment, or application timing. I use retry as a safety mechanism, not as a replacement for fixing flaky automation.”



**Remember this flow**



**Flaky test → Investigate → Synchronization → Stable locator → Test data/environment → Retry Analyzer → Screenshot + logs → Root-cause fix**



**========================================================================================================================================================================================**



**Q.  What is maven surefire plugin? How do you collect only failed test data when 49 out of 200 fails**



**==>** This is a good Maven + TestNG interview question. The interviewer is usually checking whether you know how Maven executes tests and how you handle failures efficiently.



**1. What is Maven Surefire Plugin?**



“Maven Surefire Plugin is a Maven plugin used to execute unit and automated tests during the Maven build lifecycle. In a Selenium/TestNG project, it integrates Maven with TestNG and runs the test classes according to the configured test patterns or suite XML.”



**For example:**



mvn test



**Maven reaches the test phase and Surefire executes the tests.**



A typical pom.xml configuration can look like:



<plugin>

&#x20;   <groupId>org.apache.maven.plugins</groupId>

&#x20;   <artifactId>maven-surefire-plugin</artifactId>

&#x20;   <version>3.5.3</version>



&#x20;   <configuration>

&#x20;       <suiteXmlFiles>

&#x20;           <suiteXmlFile>testng.xml</suiteXmlFile>

&#x20;       </suiteXmlFiles>

&#x20;   </configuration>

</plugin>



**Surefire also generates test execution results under:**



target/

&#x20;  surefire-reports/



**You can find files such as:**



TEST-\*.xml

\*.txt



These contain information about passed, failed and skipped tests.



**2. Scenario: 200 tests, 49 failed. How do you collect only failed test data?**



This is the important part.



**I'd answer:**



“If 49 out of 200 tests fail, I first collect the failure information from the Surefire/TestNG reports rather than manually checking all 200 tests. Surefire generates reports under target/surefire-reports, where I can identify the failed test cases and their failure messages or stack traces.”



Then I would separate the process into three steps.



**Step 1 — Identify failed tests**



Surefire report contains the execution results.



For example:



Tests run: 200

Failures: 49

Errors: 0

Skipped: 2



**The XML reports can be parsed to extract:**



Test Name

Class Name

Failure/Error

Failure Message

Stack Trace

Execution Time



**Step 2 — Collect failure evidence**



In Selenium automation, I wouldn't collect just the test name.



For every failed test, I would collect:



Test Case Name

Class Name

Failure Reason

Exception

Screenshot

Browser/Environment

Application logs

Execution timestamp



For example:



TC\_Login\_005

Failure: NoSuchElementException

Screenshot: TC\_Login\_005.png

Environment: QA

Browser: Chrome



In your project, this becomes especially useful because your resume mentions advanced logging, including synchronized serial and video logs during automation execution.



**Step 3 — Rerun only failed tests**



If the interviewer means:



“How would you rerun only those 49 failures?”



There are multiple approaches.



With TestNG, we can use the generated failed-suite XML:



testng-failed.xml



After a TestNG execution, it can contain the failed test methods. We can execute that suite again instead of executing all 200 tests.



Conceptually:



mvn test -DsuiteXmlFile=testng-failed.xml



Or configure the Surefire plugin to execute the desired TestNG suite.



**3. Very strong interview answer**



You can say this almost exactly:



“Maven Surefire Plugin is responsible for executing tests during Maven's test phase. In my automation framework, Maven can trigger the TestNG test suite, and Surefire generates the execution reports under target/surefire-reports.



If I have 200 tests and 49 fail, I don't manually analyze all 200. First, I use the Surefire/TestNG reports to identify the 49 failed tests. I collect the test name, class, exception, failure message and stack trace. For UI failures, I also collect screenshots and relevant logs.



Then I use the TestNG failed-test suite, such as testng-failed.xml, to rerun only the failed test cases. This helps me quickly determine whether the failures are genuine defects or transient automation/environment issues.



After rerunning, if some tests pass, I classify them as flaky or environment-related and investigate the root cause. If they fail consistently, I analyze the logs and raise or update the defect with the required evidence.”



**Follow-up question they may ask**



**Interviewer: “What if the same 49 tests fail again?”**



**Good answer:**



“Then I don't keep blindly rerunning them. I compare the failure patterns, stack traces, screenshots and application/system logs. I check whether the common failure is caused by application behavior, test-data issues, synchronization problems, environment instability, or an actual defect. If multiple failures have the same root cause, I group them rather than treating all 49 as independent defects.”



That last point is particularly important for an Automation Engineer: 49 failed tests does not necessarily mean 49 defects. One application/API/environment issue can cause many test cases to fail.



**============================================================================================**

**============================================================================================**

**Q. How do you run parallel tests in TestNG and avoid thread-safety issues?**



**==>** his is another very common TestNG Automation Engineer interview question. The key is not just knowing parallel="methods"—you need to explain how you prevent shared state and WebDriver conflicts.



Interview-ready answer



“In TestNG, I can execute tests in parallel by configuring the parallel attribute in the TestNG XML file. Depending on the requirement, I can run methods, classes, or tests in parallel and control the number of concurrent threads using thread-count.”



<suite name="RegressionSuite" parallel="tests" thread-count="4">



&#x20;   <test name="ChromeTests">

&#x20;       <classes>

&#x20;           <class name="tests.LoginTest"/>

&#x20;           <class name="tests.SearchTest"/>

&#x20;       </classes>

&#x20;   </test>



&#x20;   <test name="FirefoxTests">

&#x20;       <classes>

&#x20;           <class name="tests.CartTest"/>

&#x20;       </classes>

&#x20;   </test>



</suite>

OR

<suite name="RegressionSuite" parallel="methods"  thread-count="5">



**How do you avoid thread-safety issues?**



This is the most important part of the answer.



**1. Don't use a static shared WebDriver**



A common mistake is:



**public static WebDriver driver;**



If multiple tests run simultaneously, different threads can access the same driver, resulting in:



**browser conflicts**

**wrong page interactions**

**flaky tests**

**one test closing another test's browser**



Instead, I use ThreadLocal<WebDriver>.



**public class DriverManager {**



&#x20;   **private static ThreadLocal<WebDriver> driver = new ThreadLocal<>();**



&#x20;   **public static void setDriver(WebDriver webDriver) {**

&#x20;       **driver.set(webDriver);**

&#x20;   **}**



&#x20;   **public static WebDriver getDriver() {**

&#x20;       **return driver.get();**

&#x20;   **}**



&#x20;   **public static void unload() {**

&#x20;       **driver.remove();**

&#x20;   **}**

**}**



Then each thread gets its own WebDriver instance.



**@BeforeMethod**

**public void setUp() {**

&#x20;   **WebDriver driver = new ChromeDriver();**

&#x20;   **DriverManager.setDriver(driver);**

**}**



**@Test**

**public void loginTest() {**

&#x20;   **DriverManager.getDriver().get("https://example.com");**

**}**



**@AfterMethod**

**public void tearDown() {**

&#x20;   **DriverManager.getDriver().quit();**

&#x20;   **DriverManager.unload();**

**}**



**Conceptually:**



Thread-1 ───> ChromeDriver-1 ───> Test A

Thread-2 ───> ChromeDriver-2 ───> Test B

Thread-3 ───> ChromeDriver-3 ───> Test C

Thread-4 ───> ChromeDriver-4 ───> Test D



**Each thread has its own browser.**



**2. Avoid shared mutable test data**



Suppose we have:



static String username;



If multiple threads modify it, one test could overwrite another test's value.



**Instead, I keep test data:**



local to the test

immutable where possible

separately generated for each test

or stored using ThreadLocal when thread-specific state is required.



**3. Be careful with Page Objects**



I don't share the same Page Object instance between parallel threads if it contains mutable state.



For example, instead of:



static LoginPage loginPage;



I create the Page Object using the current thread's driver:



LoginPage loginPage = new LoginPage(DriverManager.getDriver());



Therefore:



Thread 1 → Driver 1 → LoginPage 1

Thread 2 → Driver 2 → LoginPage 2



**4. Reports and logging must also be thread-safe**



When parallel tests run, multiple threads can write logs simultaneously.



I make sure that:



each test has a unique test identifier

screenshots have unique names

logs are associated with the correct test/thread

reporting objects aren't incorrectly shared between threads



**For example:**



String screenshotName = testName + "\_" + Thread.currentThread().getId() + ".png";



This prevents one thread from overwriting another thread's screenshot.



**5. Synchronization where shared resources are unavoidable**



If multiple threads must access a shared resource, I protect the critical section using appropriate synchronization mechanisms.



But I don't synchronize the entire test, because that defeats the purpose of parallel execution.



**The goal is:**



Parallel execution

&#x20;      ↓

Independent resources

&#x20;      ↓

Minimal shared state

&#x20;      ↓

Thread-safe utilities

&#x20;      ↓

Reliable execution



**What I would say in an interview**



“I have used TestNG parallel execution by configuring parallel and thread-count in the TestNG XML. For example, with parallel="methods" and thread-count="5", TestNG can execute methods concurrently using up to five threads.



The main challenge with parallel execution is thread safety. I make WebDriver thread-safe using ThreadLocal<WebDriver>, so every test thread gets its own browser instance. I avoid static mutable variables and shared Page Objects, and test data is kept thread-specific.



I also make sure screenshots, logs and reports are uniquely associated with each test thread so that parallel tests don't overwrite each other's data. Finally, I use synchronization only when accessing a genuinely shared resource rather than synchronizing the whole test.



So the basic principle I follow is: each thread should have its own driver, test data and execution context, with as little shared mutable state as possible.”



**⭐ Interview follow-up: "Why ThreadLocal?"**



**A very good one-line answer:**



“ThreadLocal gives each thread its own isolated copy of the WebDriver reference, so Thread-1 cannot accidentally use or close Thread-2's browser.”



And if they ask “What happens if you use a static WebDriver?”, answer:



“All parallel threads can access the same driver instance, so commands from different tests can interfere with each other, resulting in flaky tests and incorrect execution.”



**===========================================================================================**

**===========================================================================================**



**Q. How do you debug flaky or intermittent test failures?**



**==>** For an Automation Engineer interview, I would answer this with a structured debugging approach rather than saying “I add retries.” Flaky tests are usually caused by timing, environment, test-data, synchronization, or dependency issues.



Interview-ready answer



“When I see a flaky or intermittent test failure, I first try to reproduce the failure and identify whether it is an application issue, automation issue, or environment issue. I don't immediately add a retry because that can hide the actual problem.



**First**, I check the failure pattern. I look at the test execution history to see whether the same test is failing randomly or at a particular step. I compare successful and failed executions.



**Second**, I check logs, screenshots, videos, and stack traces. In my project, logging is particularly important because I worked with embedded and connected systems. I also developed logging that captured synchronized serial and video logs during automated execution, which helps correlate the automation failure with what was happening in the system.



**Third**, I investigate synchronization issues. In Selenium or Playwright, a common cause is that the script performs an action before the element or backend operation is actually ready. I replace hard-coded sleeps with proper explicit waits or condition-based synchronization.



**Fourth**, I check test-data and test-environment issues. For example, another test may modify the same data, a service may not be available, the server may be slow, or an embedded component may not be in the expected state.



**Fifth**, I check test independence and parallel execution. If tests share files, database records, ports, browser sessions, or other resources, one test can affect another. I isolate the test data and resources wherever possible.



Then I run the test repeatedly, for example 20–50 times, to determine whether the failure is reproducible and under what conditions it occurs.



Once I identify the root cause, I fix the underlying issue. Only when an intermittent failure is caused by a genuinely transient external dependency and cannot reasonably be eliminated do I use a controlled retry mechanism, and I make sure the retry is logged so that we don't hide genuine failures.



Finally, I monitor the test over multiple executions to confirm that the flakiness has actually been resolved.”\*\*



**My debugging checklist:** 



Flaky Test

&#x20;   │

&#x20;   ▼

Reproduce the failure

&#x20;   │

&#x20;   ├── Always fails?

&#x20;   │       └── Normal defect / automation issue

&#x20;   │

&#x20;   └── Randomly fails?

&#x20;           │

&#x20;           ▼

&#x20;      Check evidence

&#x20;      ├── Logs

&#x20;      ├── Screenshot

&#x20;      ├── Video

&#x20;      └── Stack trace

&#x20;           │

&#x20;           ▼

&#x20;      Investigate root cause

&#x20;      ├── Synchronization / timing

&#x20;      ├── Test data

&#x20;      ├── Environment

&#x20;      ├── Network / API

&#x20;      ├── Application performance

&#x20;      ├── Shared resources

&#x20;      └── Parallel execution

&#x20;           │

&#x20;           ▼

&#x20;      Fix root cause

&#x20;           │

&#x20;           ▼

&#x20;      Run repeatedly

&#x20;           │

&#x20;           ▼

&#x20;      Monitor stability





**If they ask: “Give me a real example.”**



You can connect it to your experience:



“In embedded automation, an intermittent failure can occur because the ECU or simulation environment has not reached the expected state when the next automation step starts. I would check the automation timestamp against the serial/system logs, verify whether the required response or state transition actually happened, and then improve the synchronization based on the system condition rather than adding a fixed sleep. Because I worked with serial and video logging, those logs can help determine whether the failure is coming from the automation or the embedded system.”



**“What is the difference between a flaky test and an actual defect?”**



**Say:**



“A flaky test produces inconsistent results without a corresponding change in the application behavior—for example, it passes and fails under the same conditions. An actual defect should generally be reproducible when the same faulty condition is present. To differentiate them, I compare logs, test data, environment conditions, and successful versus failed executions.”



**Key phrase to remember:**

**Reproduce → Collect evidence → Identify root cause → Fix → Re-run repeatedly → Monitor.**



**============================================================================================**

**============================================================================================**



**Q. Executing Failed Test Cases in TestNG**



**==>** For an Automation Engineer / TestNG interview, the most common way to execute failed TestNG cases is using the testng-failed.xml file generated after execution.



Interview-ready answer



“In TestNG, when a test case fails, TestNG automatically generates a testng-failed.xml file inside the test-output directory. This XML contains the failed test methods and their required configuration methods.



We can execute this testng-failed.xml file again instead of executing the complete test suite. This is useful for debugging and rerunning only the failed scenarios.”



@Test

public void loginTest() {

&#x20;   // test steps

}



@Test

public void searchTest() {

&#x20;   // test steps

}



@Test

public void checkoutTest() {

&#x20;   // test steps

}

loginTest      → PASS

searchTest     → FAIL

checkoutTest   → PASS



**TestNG generates:**

test-output/

&#x20;   ├── index.html

&#x20;   ├── emailable-report.html

&#x20;   └── testng-failed.xml



The testng-failed.xml will contain the failed searchTest.



You can run it from TestNG / IDE or configure Maven to execute that XML.



**Another approach: IRetryAnalyzer**



If the failure is intermittent, we can implement TestNG's IRetryAnalyzer.



public class RetryAnalyzer implements IRetryAnalyzer {



&#x20;   private int count = 0;

&#x20;   private static final int maxRetryCount = 2;



&#x20;   @Override

&#x20;   public boolean retry(ITestResult result) {



&#x20;       if (count < maxRetryCount) {

&#x20;           count++;

&#x20;           return true;

&#x20;       }



&#x20;       return false;

&#x20;   }

}

Then attach it to the test:



@Test(retryAnalyzer = RetryAnalyzer.class)

public void loginTest() {

&#x20;   // test steps

}



Now, if loginTest() fails, TestNG retries it up to 2 times.



**testng-failed.xml**  	| 	**Retry Analyzer**

testng-failed.xml	|	IRetryAnalyzer

Used after execution	|	Used during execution

Runs failed tests again	|	Automatically retries a failed test

Useful for rerunning a  |	Useful for intermittent/flaky failures

failed suite		|

Generated by TestNG	|	Custom implementation

Manual/CI 		|	rerun	Automatic retry



If they ask “**How do you execute failed test cases in TestNG**?”, **say:**



“TestNG provides a built-in mechanism for this. After suite execution, it generates testng-failed.xml under the test-output folder. I can execute that XML to rerun only the failed test methods instead of the entire suite. For intermittent failures, I can additionally use IRetryAnalyzer to automatically retry the failed test a configured number of times. However, I use retry carefully because I don't want to hide genuine application defects.”



**===========================================================================================**

**===========================================================================================**

**Q. Selenium Grid \& Parallel Execution**



**==>** 	For an Automation Engineer interview, this is a very common topic. Explain it in this order: What → Why → Architecture → How parallel execution works → Example → Challenges.



**1. What is Selenium Grid?**



“Selenium Grid is used to execute Selenium tests remotely on different machines, browsers, and operating systems. Its main purpose is to achieve cross-browser testing and reduce execution time through parallel execution.”



**For example, instead of running 100 tests sequentially:**

**Sequential:**



Test 1 ──► Chrome

Test 2 ──► Chrome

Test 3 ──► Chrome

...

Test 100 ─► Chrome



Total time = 100 × execution time



**With Grid:**



&#x20;                   **Selenium Grid**

&#x20;                        **│**

&#x20;         **┌──────────────┼──────────────┐**

&#x20;         **▼              ▼              ▼**

&#x20;      **Machine 1      Machine 2      Machine 3**

&#x20;       **Chrome         Firefox         Edge**

&#x20;         **│              │              │**

&#x20;      **Tests 1-30     Tests 31-60    Tests 61-100**





The tests can execute simultaneously, significantly reducing total execution time.



**2. Selenium Grid Architecture**



Modern Selenium Grid uses a distributed architecture.



The important components are:



**Router**



The Router is the entry point for WebDriver requests.



**Test Script**

&#x20;   **│**

&#x20;   **▼**

&#x20;**Router**

It receives the request and routes it to the appropriate Grid component.



**Distributor**



The Distributor is responsible for finding an appropriate available slot for a new session.



**For example:**

**Test requests → Chrome**

&#x20;                **│**

&#x20;                **▼**

&#x20;          **Distributor**

&#x20;                **│**

&#x20;         **finds Chrome slot**

&#x20;                **│**

&#x20;                **▼**

&#x20;             **Node**



**Session Map**



It keeps track of active WebDriver sessions and where those sessions are running.



**Event Bus**



Grid components communicate with each other through the Event Bus.



**Nodes**



Nodes are the machines where the actual browser sessions run.



**For example:**



**Node 1 → Chrome**

**Node 2 → Firefox**

**Node 3 → Edge**



So the key distinction is:



Grid manages/distributes the sessions; Nodes actually execute the browser sessions.



**3. What is Parallel Execution?**



Parallel execution means running multiple independent test cases or test classes at the same time, rather than one after another.



Suppose we have 60 tests and each test takes 1 minute.



**Sequential:**



**60 tests × 1 minute = \~60 minutes**



**If we have 3 parallel workers:**



**Worker 1 → 20 tests**

**Worker 2 → 20 tests**

**Worker 3 → 20 tests**



**Approximate execution = \~20 minutes**



**Actual time depends on setup, dependencies, machine capacity, test distribution, etc.**



**4. How do you implement parallel execution in TestNG?**



Since your resume includes TestNG, this is a good example for you.



**For example:**



**<suite name="Regression Suite" parallel="tests" thread-count="3">**



&#x20;   **<test name="Chrome Tests">**

&#x20;       **<classes>**

&#x20;           **<class name="tests.LoginTest"/>**

&#x20;       **</classes>**

&#x20;   **</test>**



&#x20;   **<test name="Firefox Tests">**

&#x20;       **<classes>**

&#x20;           **<class name="tests.SearchTest"/>**

&#x20;       **</classes>**

&#x20;   **</test>**



&#x20;   **<test name="Edge Tests">**

&#x20;       **<classes>**

&#x20;           **<class name="tests.CartTest"/>**

&#x20;       **</classes>**

&#x20;   **</test>**



**</suite>**



**Here:**



parallel="tests"

thread-count="3"



means TestNG can execute up to 3 test groups concurrently.



**5. How does Selenium connect to Grid?**



Instead of creating a local driver:



WebDriver driver = new ChromeDriver();



we create a remote driver:



WebDriver driver =

&#x20;       new RemoteWebDriver(

&#x20;           new URL("http://localhost:4444"),

&#x20;           options

&#x20;       );



**The important concept is:**



**Test**

&#x20;**│**

&#x20;**▼**

**RemoteWebDriver**

&#x20;**│**

&#x20;**▼**

**Selenium Grid**

&#x20;**│**

&#x20;**▼**

**Matching Node**

&#x20;**│**

&#x20;**▼**

**Browser**



**The Grid receives the browser capability request and assigns the test to a suitable available slot.**



**6. Browser-specific execution**



**Y**ou can configure browser options:



ChromeOptions options = new ChromeOptions();



WebDriver driver =

&#x20;   new RemoteWebDriver(

&#x20;       new URL("http://localhost:4444"),

&#x20;       options

&#x20;   );



For Firefox:



FirefoxOptions options = new FirefoxOptions();



WebDriver driver =

&#x20;   new RemoteWebDriver(

&#x20;       new URL("http://localhost:4444"),

&#x20;       options

&#x20;   );



This allows the same automation suite to execute against different browsers.



**7. Selenium Grid vs Parallel Execution**



This is an important interview distinction.



Selenium Grid is infrastructure.



Parallel execution is an execution strategy.



You can have:



**Parallel execution**

&#x20;      **│**

&#x20;      **├── Local machines**

&#x20;      **│**

&#x20;      **├── Selenium Grid**

&#x20;      **│**

&#x20;      **├── Cloud platforms**

&#x20;      **│**

&#x20;      **└── Containers**



Grid makes distributed parallel execution easier, but parallel execution itself is not synonymous with Grid.



**8. What problems do you face with parallel execution?**



This is where interviewers usually go deeper.



**1. Shared WebDriver**



**Bad:**



static WebDriver driver;



Multiple threads accessing the same driver can cause failures.



Instead, use thread-safe driver management, commonly ThreadLocal.



private static ThreadLocal<WebDriver> driver =

&#x20;       new ThreadLocal<>();



Each thread gets its own WebDriver instance.



Thread 1 → Driver 1 → Chrome

Thread 2 → Driver 2 → Chrome

Thread 3 → Driver 3 → Firefox

2\. Shared test data



Suppose:



Thread 1 → creates User123

Thread 2 → updates User123

Thread 3 → deletes User123



**They can interfere with each other.**



**Solution:**



Use independent or dynamically generated test data.



**3. Static variables**



Shared static variables can create race conditions between parallel tests.



**4. File conflicts**



Two tests writing to the same file can corrupt the result.



**5. Database conflicts**



Parallel tests may update the same records.



**6. Environment limitations**



The Grid may have only:



**2 Chrome slots**



but you try to execute:



**10 Chrome tests**



The remaining sessions have to wait for available slots.



**9. How would you explain this based on your project?**



**A good answer for your profile would be:**



**“**In my automation projects, parallel execution is useful especially for regression testing because we can have a large number of test cases. Instead of executing everything sequentially, I would distribute independent test cases across multiple browser or execution instances.



With Selenium Grid, the test uses RemoteWebDriver and sends the browser capability to the Grid. Grid identifies an available node with the required browser and creates the session there.



For TestNG, I can configure parallel execution using parallel and thread-count. I also need to make sure the framework is thread-safe, especially the WebDriver instance, test data, reports, and shared resources. For WebDriver, I would use a separate driver instance per thread rather than sharing a static driver.”



**============================================================================================**

**===========================================================================================**

**Q. What happens if two parallel tests use the same test data?**



**==>** This is a very common follow-up in parallel execution interviews. The key concept is test-data collision / race condition.



**Interview-ready answer**



“If two parallel tests use the same test data and both tests modify that data, they can interfere with each other. This can result in inconsistent or flaky test failures.



For example, suppose both Test 1 and Test 2 use the same user account user123.



Test 1 may update the user's details while Test 2 is trying to validate the original details. Depending on the execution timing, Test 2 may get unexpected data and fail.



Another example is if both tests try to create the same unique user or defect ID. One test may successfully create it, while the second test gets a duplicate-data error.



To avoid this, I would make the test data independent for each parallel execution. I can generate unique data dynamically, maintain separate test-data sets, or create and clean up data for each test.



If database records are involved, I would also make sure that parallel tests don't update the same records and, where appropriate, use transactions or proper data isolation.



So my approach is: don't share mutable test data between parallel tests unless it is intentionally read-only.”\*\*



**Simple example**



**Without isolation:**



Test 1 ──┐

&#x20;        ├──► user123

Test 2 ──┘



Both modify user123 → data collision ❌



**With isolated data:**



Test 1 ──► user\_123\_001

Test 2 ──► user\_123\_002

Test 3 ──► user\_123\_003



Each test works independently → stable parallel execution ✅



**If interviewer asks: "How do you generate unique data?"**



You can say:



“For dynamic test data, I can generate a unique value using a timestamp, UUID, or a combination of test-thread information and a random value.”



Example:



String uniqueUser = "testuser\_" + UUID.randomUUID();



This is particularly useful when tests are creating users, orders, defects, certificates, or other records that must be unique.



**===========================================================================================**

**===========================================================================================**



These are good Automation Engineer interview questions. Based on your resume, I would answer them using your experience with Selenium/Playwright, API automation, embedded/Connected Services testing, logging, and your work with Maven/Gradle/Git/Jenkins-type execution environments.



**1. How do you manage test data and environment configurations?**

**Interview answer**



“I keep test data and environment configurations separate from the automation code. The main goal is to avoid hardcoding environment-specific values inside test cases and make the framework reusable across different environments such as development, SIT, and regression environments.



For environment configuration, I maintain values such as server URLs, API endpoints, credentials through secure mechanisms, timeouts, browser configuration, and other environment-specific parameters in configuration files or environment variables.



**For example, instead of hardcoding:**



https://sit-server/application



inside a test, the test reads the URL from the configuration based on the selected environment.



For test data, I keep reusable data separately in appropriate files or data structures, depending on the requirement. For API testing, this could include JSON request data, while for UI testing it could include user or business data.



I also make sure that tests don't modify shared data when they are running in parallel. Wherever possible, I use unique or dynamically generated test data.



In my projects, this approach is particularly useful because I work with different simulation and integration environments. I have configured and maintained software integration simulation environments for end-to-end validation across multiple embedded modules.



So my approach is configuration separation + reusable test data + environment-specific configuration + secure handling of sensitive values + independent test data for parallel execution.**”**



**Example structure**



**automation-framework/**

**│**

**├── src/**

**│   ├── tests/**

**│   ├── pages/**

**│   ├── api/**

**│   ├── utilities/**

**│   └── components/**

**│**

**├── config/**

**│   ├── dev.properties**

**│   ├── sit.properties**

**│   └── prod.properties**

**│**

**├── testdata/**

**│   ├── users.json**

**│   ├── api-data.json**

**│   └── test-data.xlsx**

**│**

**└── reports/**



**Follow-up: "Why not hardcode test data?"**



“Hardcoding makes maintenance difficult. If the environment URL or test data changes, I would have to modify multiple test scripts. By separating configuration and data, I can change it in one place and reuse the same automation across environments.”



**2. What are your best practices to make automation scripts more maintainable?**

**Interview answer**



“My first principle is to avoid duplication and keep the framework modular. I separate test logic from implementation logic.



For UI automation, I use the Page Object Model, where locators and page-specific actions are maintained separately from test cases.



I create reusable methods for common operations instead of repeating the same code in every test.



I also use meaningful naming conventions and keep test methods small, focused, and easy to understand.



I avoid hardcoded waits and use proper synchronization mechanisms. I also keep test data and environment configurations outside the test scripts.



Another important practice is centralized logging **and** error handling. This makes failures easier to debug. In my project, I worked on an advanced logging framework that captured synchronized serial and video logs during automated execution.



I also make sure tests are independent, especially when executing regression tests in parallel.



Finally, I regularly refactor duplicate or outdated automation code rather than continuously adding new code on top of it.”



**My maintainability checklist**

**Maintainable Automation**

&#x20;       **│**

&#x20;       **├── Page Object Model**

&#x20;       **├── Reusable functions**

&#x20;       **├── Separation of concerns**

&#x20;       **├── No hardcoded data**

&#x20;       **├── External configuration**

&#x20;       **├── Proper waits**

&#x20;       **├── Meaningful naming**

&#x20;       **├── Centralized logging**

&#x20;       **├── Good error handling**

&#x20;       **├── Independent tests**

&#x20;       **└── Code reviews / refactoring**



**Interviewer: "What do you mean by separation of concerns?"**



**“**Each layer should have one responsibility. For example, the test layer contains the test scenario, the page layer handles UI interactions, the API layer handles API operations, the utility layer contains reusable functions, and the configuration layer handles environment-specific values. This way, a change in one area doesn't require changes throughout the framework.”





**3. How do you handle failed test cases in Jenkins or CI/CD pipelines?**

**Interview answer**



**“**When an automated test fails in Jenkins, I first check whether the failure is due to an actual application defect, automation issue, environment issue, or test-data problem. I don't simply rerun everything immediately.



The pipeline should preserve the execution evidence, such as test reports, console logs, screenshots, videos, and application or system logs.



I check the Jenkins console output to identify the failed test and the exact step where it failed. Then I analyze the automation logs and supporting evidence.



If it is a genuine application defect, I document the failure with the required evidence and create or update the defect.



If it is an automation issue, I fix the script or framework component and rerun the affected tests.



If it is an environment or transient issue, I investigate the environment and rerun the relevant tests after confirming the environment is stable.



For flaky tests, I don't use retries as the first solution because retries can hide real problems. If a retry is justified for a known transient dependency, I make sure the retry and original failure are still visible in the reports.



Finally, I configure th**e** pipeline so that reports and logs are published as build artifacts, making it easy to investigate failures even after the Jenkins job finishes.”\*\*



**CI/CD flow y**

**Developer Commit**

&#x20;      **│**

&#x20;      **▼**

&#x20;    **Git**

&#x20;      **│**

&#x20;      **▼**

&#x20;   **Jenkins**

&#x20;      **│**

&#x20;      **▼**

**Build / Compile**

&#x20;      **│**

&#x20;      **▼**

**Environment Setup**

&#x20;      **│**

&#x20;      **▼**

**Run Automation**

&#x20;      **│**

&#x20;      **├───────────────┐**

&#x20;      **▼               ▼**

&#x20;  **Test Pass        Test Fail**

&#x20;      **│               │**

&#x20;      **▼               ▼**

&#x20;**Generate Report    Collect Evidence**

&#x20;                      **│**

&#x20;               **┌──────┼──────┐**

&#x20;               **▼      ▼      ▼**

&#x20;             **Logs  Screenshot Video**

&#x20;                      **│**

&#x20;                      **▼**

&#x20;                **Analyze Failure**

&#x20;                      **│**

&#x20;         **┌────────────┼────────────┐**

&#x20;         **▼            ▼            ▼**

&#x20;      **Defect      Automation    Environment**

&#x20;         **│            │            │**

&#x20;         **▼            ▼            ▼**

&#x20;      **Report        Fix         Stabilize**

&#x20;                      **│**

&#x20;                      **▼**

&#x20;                  **Re-run Test**



**If they ask: "Should Jenkins build be marked failed if one test fails?"**



**A good answer:**



“It depends on the pipeline and test-suite configuration. For a critical smoke or regression suite, a genuine functional failure should normally fail the build or pipeline stage so that the issue is visible. However, I would distinguish between genuine test failures and known infrastructure or flaky failures rather than blindly ignoring failures.”



**============================================================================================**

**===========================================================================================**



**1. Tell me about a time you identified a critical bug through automation.**



**==>** For this behavioral question, use a STAR-format answer and connect it to your actual Forvia work. Your resume supports automation of ECU flashing/performance testing, Connected Services, SIT/regression, and PUMBA/SIMBA automation.



Interview-ready answer



“Yes. One example was during automation and validation of an embedded/Connected Services feature.



Situation: We were performing regression and integration testing, and one of the automated test cases was intermittently failing during the end-to-end flow. Initially, it looked like an automation timing issue because the same test was passing in some executions.



**Task**: My responsibility was to investigate whether the failure was coming from the automation script, the test environment, or the actual system behavior.



Action: I reproduced the scenario multiple times and compared the successful and failed executions. I checked the automation logs along with the system/serial logs and the execution sequence. I found that the expected system state was not being reached correctly before the next step of the workflow was executed. Instead of simply increasing the wait time, I correlated the automation execution with the system logs and identified the actual failure in the underlying flow.



I then isolated the issue, collected the relevant logs and failure evidence, and reported it to the development team with clear reproduction steps. I also updated the automation synchronization/validation so that the test could correctly detect the failure rather than producing an unclear automation error.



**Result**: The issue was confirmed as a product/system-level problem rather than just an automation failure. After it was fixed, I reran the regression scenario and verified that the flow was stable.



The main value of automation in this case was that it helped us repeatedly execute the end-to-end scenario and capture detailed evidence, which made it much easier to identify a problem that could be difficult to catch manually.”



**If interviewer asks: “What made the bug critical?”**



Don't invent severity if you don't have a specific documented example. A safe answer is:



“I considered it critical because it affected an important end-to-end functionality and could prevent the expected system flow from completing. I validated the impact with the development team and made sure the issue was reproduced and supported with logs before treating it as a product defect.”



Follow-up they may ask



**Interviewer: “How did you know it wasn't an automation issue?”**



**Answer**:



“I compared successful and failed executions and correlated the automation logs with the system/serial logs. The automation was sending the expected action, but the underlying system was not reaching the expected state. That evidence helped separate the automation synchronization issue from the actual product behavior.”



This answer also fits your resume particularly well because you have experience with software integration testing, end-to-end Connected Services automation, socket communication, and synchronized serial/video logging



**===========================================================================================**

**===========================================================================================**



**Q. . How do you ensure test coverage and quality metrics?**



**==>** For an Automation Engineer interview, answer this by showing that you measure coverage at both the requirement level and automation level. Your resume supports SIT, sanity, regression, functional/integration/system testing, and automation of SWC and Connected Services scenarios.



**Interview-ready answer**



“I ensure test coverage by first mapping the requirements and business scenarios to test cases. I make sure that critical functional, integration, negative, boundary, and regression scenarios are covered.



For automation, I identify which stable and repetitive scenarios should be automated and track the percentage of relevant test cases that are automated.



I also maintain traceability between requirements, test cases, automation scripts, and defects. This helps me identify if any requirement has no corresponding test coverage.



For example, in my current project, I perform SIT, sanity, regression, functional, integration, and system-level testing for embedded and connected systems. I also automated SWC test cases using PUMBA/SIMBA and worked on end-to-end Connected Services automation.



**For quality metrics, I mainly look at metrics such as:**



Requirement coverage – percentage of requirements covered by test cases.

Test execution percentage – how many planned tests have been executed.

Pass/fail percentage – overall test execution results.

Automation coverage – percentage of suitable regression tests automated.

Defect density – number of defects relative to the size of the functionality being tested.

Defect leakage – defects found later in the testing lifecycle or production.

Defect severity distribution – number of critical, high, medium, and low-severity defects.

Regression stability – whether previously working functionality continues to pass after changes.

**Flaky test rate – how frequently automated tests fail intermittently.**



I don't consider 100% automation coverage to mean 100% quality. I focus on risk-based coverage, giving more attention to critical business functionality, high-risk integrations, and areas with a history of defects.



Finally, I review these metrics after each test cycle and use the results to identify coverage gaps, unstable automation, and areas that need additional testing.”\*\*



Simple example



Suppose there are 100 requirements:



100 Requirements

&#x20;     │

&#x20;     ├── 95 have test cases

&#x20;     │

&#x20;     └── 5 have no coverage

&#x20;             ↓

&#x20;       Coverage = 95%



And you have:



200 Regression Test Cases

&#x20;       │

&#x20;       ├── 150 Automated

&#x20;       └── 50 Manual



Automation Coverage = 75%



If execution results are:



200 Tests Executed

│

├── 180 Passed

├── 15 Failed

└── 5 Blocked



You can report:



Pass rate = 90%

Failure rate = 7.5%

Blocked = 2.5%

If interviewer asks: “Which metric is most important?”



**Don't say just one metric.**



Say:



“There isn't one metric that represents quality by itself. I look at a combination of requirement coverage, risk coverage, defect trends, regression stability, and automation coverage. For example, a suite can have 95% pass rate but still have a critical uncovered requirement, so I always consider business risk along with the numerical metrics.”



⭐ Strong point for your profile



You can specifically mention that your automation isn't limited to UI testing. Your resume shows embedded SIT/regression, Connected Services, SWC automation, ECU flashing/performance automation, socket communication, and Playwright-based web regression/API testing.



That gives you a strong answer to:



**“How do you ensure broad test coverage?”**



“I use multiple levels of testing—functional, integration, system, regression, API, UI, and where applicable hardware/software integration testing—rather than relying only on UI automation.



**===========================================================================================**

**=========================================================================================**



**Q. Describe a challenging situation with developers or deadlines and how you handled it.**



**==>** For your Automation Engineer interview, I’d use a STAR-format example based on your actual project experience—especially your embedded/Connected Services work, where you handled SIT, regression, automation, and environment-related validation





**One challenging situation I faced was when we had a tight deadline for a release, and some of the automation tests were failing because of issues in the test environment and changes in the application.**



The developers were focused on completing the feature and fixing the functional issues, while from the QA side we needed a stable build and enough time to complete regression testing. Because the deadline was close, there was some pressure between development and testing teams.



Instead of treating it as a conflict, I first analyzed the failures and categorized them into three areas: actual product defects, automation issues, and environment/configuration issues. I shared the evidence with the developers, including logs and the exact steps to reproduce the failures, so that we could quickly identify which issues required development changes.



For the automation failures, I worked on fixing the scripts and improving the reusable components. For environment-related problems, I coordinated with the relevant team to get the required configuration and simulation environment stable.



At the same time, I prioritized the regression suite based on critical functionality and release risk. We executed the high-priority tests first instead of waiting for the complete suite to finish.



This helped us avoid unnecessary back-and-forth with developers and focus on the actual blockers. We were able to complete the critical validation within the deadline and provide clear test results to the team.



The main lesson I learned was that during a tight deadline, communication and prioritization are just as important as automation. I always try to bring evidence to discussions and focus on solving the problem rather than assigning blame.



**If they ask: “How did you handle conflict with the developer?”**



Say:



“I don't approach it as QA versus development. I focus on evidence. I provide the failed test case, logs, expected versus actual behavior, and reproduction steps. If it's a genuine defect, we discuss the impact and priority. If it's an automation or environment issue, I take ownership and fix it. This keeps the discussion technical rather than personal



===========================================================================================

===========================================================================================



**Q. How to simulate network conditions in Selenium WebDriver?**



**==>** In an Automation Engineer interview, a good answer is to explain that Selenium WebDriver itself does not directly throttle network speed, but you can use Chrome DevTools Protocol (CDP) with Selenium 4 to emulate network conditions.



**Interview-ready answer**



“We can simulate network conditions in Selenium using Chrome DevTools Protocol. Selenium 4 provides access to Chrome DevTools, so we can emulate conditions such as slow 3G, fast 3G, offline mode, or custom latency and download/upload throughput.



For example, I can use CDP to set network conditions before opening or interacting with the application. Then I can verify how the application behaves under slow or unstable network conditions.”

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.devtools.DevTools;

import org.openqa.selenium.devtools.v145.network.Network;



import java.util.Optional;



public class NetworkTest {



&#x20;   public static void main(String\[] args) {



&#x20;       ChromeDriver driver = new ChromeDriver();



&#x20;       DevTools devTools = driver.getDevTools();

&#x20;       devTools.createSession();



&#x20;       devTools.send(Network.enable(

&#x20;               Optional.empty(),

&#x20;               Optional.empty(),

&#x20;               Optional.empty()

&#x20;       ));



&#x20;       // Simulate slow network

&#x20;       devTools.send(Network.emulateNetworkConditions(

&#x20;               false,       // offline

&#x20;               200,         // latency in ms

&#x20;               500 \* 1024,  // download throughput

&#x20;               500 \* 1024,  // upload throughput

&#x20;               Optional.empty()

&#x20;       ));



&#x20;       driver.get("https://example.com");



&#x20;       // Perform validations



&#x20;       driver.quit();

&#x20;   }

}



**If the interviewer asks “Have you actually used this?”, don't claim hands-on experience unless you have. You can say:**



“I understand and can implement network throttling using Selenium 4 and Chrome DevTools Protocol. The approach is to create a DevTools session, enable the Network domain, and emulate the required latency and throughput. For more complex network mocking, I would use a proxy tool such as BrowserMob Proxy or an external network simulation tool.”



============================================================================================

===========================================================================================



**Q. Root cause of flakiness in Selenium scripts - how to fix, how many ways. Explain Root Cause Analysis techniques ?**



==> For an Automation Engineer interview, answer this as RCA + prevention, not just “use explicit waits.” Flaky Selenium tests usually come from synchronization, unstable locators, environment issues, browser/driver differences, test-data dependencies, and poor test isolation.



**1. What is a flaky Selenium test?**



“A flaky test is a test that sometimes passes and sometimes fails without any relevant change in the application code or test code.”



For example:



Run 1 → PASS

Run 2 → FAIL

Run 3 → PASS

Run 4 → PASS

Run 5 → FAIL



The important point is: the failure is inconsistent and not reliably reproducible.



**2. Root causes of Selenium flakiness**



I would categorize the root causes into these major areas:



**1. Synchronization / timing issues — MOST COMMON**



Example:



driver.findElement(By.id("submit")).click();



The page may not have finished rendering when Selenium tries to click.



Fix



Use explicit waits based on actual conditions:



WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));



WebElement button = wait.until(

&#x20;   ExpectedConditions.elementToBeClickable(By.id("submit"))

);



button.click();



Prefer:



Wait for condition

&#x20;      ↓

Element ready

&#x20;      ↓

Perform action



instead of:



Thread.sleep(5000)

&#x20;      ↓

Hope element is ready



**2. Poor / unstable locators**



For example:



// Bad

//div\[3]/div\[2]/button



If the DOM structure changes, the locator breaks.



Prefer stable attributes:



By.id("loginButton");



or:



By.cssSelector("\[data-testid='login-button']");

Fix



Use a locator hierarchy such as:



ID

↓

data-testid / stable custom attribute

↓

CSS

↓

reliable XPath



Avoid depending on dynamic classes, indexes, or changing DOM structures.



**3. Dynamic elements / AJAX**



Modern applications frequently update elements asynchronously.



For example:



Click Search

&#x20;    ↓

API call

&#x20;    ↓

Spinner

&#x20;    ↓

DOM updated

&#x20;    ↓

Results displayed



If Selenium immediately searches for the result, the test can fail.



Fix



Wait for a meaningful application condition:



wait.until(

&#x20;   ExpectedConditions.visibilityOfElementLocated(

&#x20;       By.id("searchResult")

&#x20;   )

);



Or wait for the spinner to disappear:



wait.until(

&#x20;   ExpectedConditions.invisibilityOfElementLocated(

&#x20;       By.id("spinner")

&#x20;   )

);

**3. StaleElementReferenceException**



This is another very common cause.



Suppose Selenium finds an element:



WebElement element = driver.findElement(By.id("username"));



Then JavaScript refreshes/rebuilds the DOM.



The old reference is no longer valid.



Fix



Locate the element again after the DOM update:



wait.until(

&#x20;   ExpectedConditions.elementToBeClickable(By.id("username"))

).click();



Instead of keeping old WebElement references for too long.



**4. Test data problems**



Sometimes the Selenium script is correct but the test data is not.



Example:



Test expects user = Uzma

But previous test already deleted the user



Then:



Test A → modifies data

&#x20;       ↓

Test B → expects original data

&#x20;       ↓

FAIL

Fix



Use:



Independent test data

Data setup/teardown

Unique test data

API/database setup where appropriate

Avoid dependency between tests

5\. Test dependency



Bad design:



Test 1 → Create user

Test 2 → Login with user

Test 3 → Update user

Test 4 → Delete user



If Test 1 fails, Tests 2–4 may fail too.



Better



Each test should establish its own required state.



Test 1 → Setup → Execute → Cleanup



Test 2 → Setup → Execute → Cleanup



Test 3 → Setup → Execute → Cleanup



This is called test isolation.



**6. Environment instability**



Sometimes the problem isn't Selenium.



For example:



Selenium

&#x20;  ↓

Application

&#x20;  ↓

Backend API

&#x20;  ↓

Database



If the backend is slow or unavailable, the Selenium test may fail.



How I investigate



Check:



Application logs

Server logs

API response

Network failures

Database availability

CPU/memory

Test environment status



This is especially important in your embedded/Connected Services work because your automation can involve multiple systems and environments. Your resume specifically mentions simulation environments and end-to-end validation across embedded modules.



**7. Browser / WebDriver mismatch**



Example:



Chrome = Version 145

ChromeDriver = Version 146



This can cause session or execution failures.



Fix



Maintain compatible:



Browser

&#x20;  +

WebDriver

&#x20;  +

Selenium version



Also keep the execution environment consistent across machines/Jenkins agents.



**8. Network issues**



For example:



Selenium → Application

&#x20;            ↓

&#x20;         API call

&#x20;            ↓

&#x20;      Network delay



The page may take longer than usual.



Fix

Explicit waits

Appropriate timeout configuration

Retry only for genuinely transient operations

Monitor network/API failures

Avoid arbitrary sleep()



**9. Pop-ups / overlays / animations**



Suppose:



Button exists

&#x20;     ↓

Modal overlay still present

&#x20;     ↓

Selenium clicks button

&#x20;     ↓

ElementClickInterceptedException

Fix



Wait for the overlay to disappear:



wait.until(

&#x20;   ExpectedConditions.invisibilityOfElementLocated(

&#x20;       By.cssSelector(".loading-overlay")

&#x20;   )

);



Then click the element.



**10. Parallel execution problems**



Suppose two tests use the same:



Browser session

Test account

File

Database record



at the same time.



They can interfere with each other.



Fix



Use:



Separate WebDriver instances

ThreadLocal WebDriver where appropriate

Unique test data

Independent users/resources

Thread-safe utilities

11\. Poor exception handling



If the test simply fails with:



Element not found



it's difficult to understand the real problem.



Fix



Capture:



Screenshot

Browser console logs

Page source

Test logs

API/network information where relevant

Stack trace



Your resume actually gives you a strong point here: you've worked on advanced logging that captured synchronized serial and video logs during automation execution.



**12. How do you perform Root Cause Analysis?**



This is the part I'd emphasize if the interviewer asks “How do you identify the root cause?”



I use a systematic approach.



**Step 1 — Reproduce**



First determine:



Always fails?

Sometimes fails?

Only fails in Jenkins?

Only fails locally?

Only fails in Chrome?

Only fails during parallel execution?



This immediately narrows the problem.



**Step 2 — Collect evidence**



I collect:



Test logs

Screenshot

Stack trace

Browser logs

Page source

Execution video

Application logs

API response

Environment information



**Step 3 — Categorize the failure**



I classify it as:



Application defect

Automation defect

Synchronization issue

Test-data issue

Environment issue

Infrastructure issue

Browser/driver issue

Network issue

Step 4 — Use 5 Whys



**Example:**



**Why did the test fail?**



→ Element was not clickable.



**Why wasn't it clickable?**



→ Loading overlay was still present.



**Why was the overlay still present?**



→ API response was slow.



**Why was the API slow?**



→ Backend service was under heavy load.



**Why was the service under heavy load?**



→ Another test suite was running simultaneously against the same environment.



Root cause:



Environment contention, not a Selenium locator problem.



This is much better than simply increasing the timeout from 10 to 30 seconds.



**13. Other RCA techniques**



You can mention these in an interview:



5 Whys



Best for finding the underlying cause.



Problem

&#x20;↓

Why?

&#x20;↓

Why?

&#x20;↓

Why?

&#x20;↓

Root Cause

Fishbone / Ishikawa Diagram



Categorize possible causes:



&#x20;                FLAKY TEST

&#x20;                    │

&#x20;      ┌─────────────┼─────────────┐

&#x20;      ↓             ↓             ↓

&#x20;    People        Process       Machine

&#x20;      ↓             ↓             ↓

&#x20;    Code          Test data     Browser

&#x20;    Skill         Timing        Driver

&#x20;                                  │

&#x20;      ┌─────────────┼─────────────┐

&#x20;      ↓             ↓             ↓

&#x20;  Environment     Network      Application

Pareto Analysis



If you have 100 flaky failures, identify which causes account for most failures.



For example:



Synchronization       40%

Test data              25%

Environment            15%

Locator                10%

Browser                 5%

Other                   5%



Then prioritize fixing synchronization and test-data issues first.



Comparison / A-B analysis



Run:



Local → PASS

Jenkins → FAIL



Then compare:



Browser version

OS

Resolution

Environment

Network

Test data

Parallelism

Configuration



This is very useful for CI failures.



**14. Should we use Retry?**



This is a very important interview point.



Don't say:



“I add retry to every flaky test.”



Instead say:



“Retry should not be used as the first solution. First I identify and fix the root cause. Retry can be used for genuinely transient failures such as temporary network or environment issues, but excessive retry can hide real defects.”



That's a strong Automation Engineer answer.



**15. How many ways can we fix Selenium flakiness?**



You can summarize your approach into 8 major areas:



Explicit/condition-based waits

Stable locators

Proper handling of dynamic elements

Test-data management

Test isolation

Environment/browser stability

Better logging and diagnostics

Controlled retry for transient failures



⭐ **Best 2-minute interview answer**



If the interviewer asks this as a direct question, don't explain all 12 causes immediately. Give this answer first:



“The first thing I do when I see Selenium flakiness is identify whether the failure is reproducible. I check whether it happens locally, in Jenkins, only in a particular browser, during parallel execution, or only under certain test data.



The most common root cause I have seen is synchronization. For example, Selenium tries to interact with an element before an AJAX operation or page rendering is completed. I fix this using explicit, condition-based waits rather than unnecessary Thread.sleep.



Other common causes are unstable locators, stale elements, dynamic DOM changes, test-data dependency, test dependency, environment instability, network issues, browser/driver mismatch, and parallel execution conflicts.



For RCA, I first collect evidence such as stack traces, screenshots, logs, browser information and application logs. Then I categorize the failure as an application defect, automation defect, data issue, environment issue, or infrastructure issue.



I also use techniques like 5 Whys, Fishbone analysis and Pareto analysis when the issue is recurring. For example, if an element is not clickable, I don't immediately increase the timeout. I ask why it's not clickable, check whether an overlay is present, whether an API is slow, and whether the environment is overloaded.



Finally, I fix the actual root cause and add preventive measures. I use retry only for genuinely transient failures because retrying everything can hide real defects.”



That answer demonstrates debugging, Selenium knowledge, RCA, CI awareness, and engineering judgment—which is much stronger than simply saying “I use explicit waits.”



============================================================================================

============================================================================================



**Q. How would you add new fields to the object repository?**



**==>** “In my Selenium framework, I maintain the UI elements using the Page Object Model. When a new field or UI element is introduced, I first identify a stable locator for that element, such as an ID, name, CSS selector, or XPath.



I then add the locator in the corresponding Page Object class rather than directly inside the test case. Along with the locator, I create a reusable method if there is an operation that needs to be performed on that field.



For example, if a new Email field is added to the Login page, I would add its locator to the LoginPage class and create a method such as enterEmail(). The test case then calls that method instead of knowing the actual locator. This keeps the test layer independent from the UI implementation.”



Example



Suppose the application gets a new Email field.



Before

public class LoginPage {



&#x20;   private WebDriver driver;



&#x20;   private By username =

&#x20;           By.id("username");



&#x20;   private By password =

&#x20;           By.id("password");



&#x20;   private By loginButton =

&#x20;           By.id("login");



&#x20;   public void enterUsername(String value) {

&#x20;       driver.findElement(username).sendKeys(value);

&#x20;   }



&#x20;   public void enterPassword(String value) {

&#x20;       driver.findElement(password).sendKeys(value);

&#x20;   }



&#x20;   public void clickLogin() {

&#x20;       driver.findElement(loginButton).click();

&#x20;   }

}



**Add the new field**

private By email = By.id("email");



**Then add its reusable action:**



public void enterEmail(String value) {

&#x20;   driver.findElement(email).sendKeys(value);

}



**Now the test remains clean:**



LoginPage loginPage = new LoginPage(driver);



loginPage.enterEmail("test@example.com");

loginPage.enterUsername("priya");

loginPage.enterPassword("password");

loginPage.clickLogin();



**If they ask: “What if the locator keeps changing?”**



Say:



“I first check whether there is a stable attribute such as id, name, data-testid, or another application-specific attribute. I avoid absolute XPath and index-based locators. If the application generates dynamic IDs, I use a reliable relative CSS/XPath strategy. I also keep the locator only in the Page Object so that if it changes later, I need to update it in one place.”



**If they ask: “Do you put every field in Object Repository?”**



A good answer:



“I don't blindly add every element. I add elements that are required for automation and expose reusable actions for them. I keep locators centralized in the Page Object or component layer, while test cases contain only the business flow.”



**============================================================================================**

**============================================================================================**











**============================================================================================**

**============================================================================================**



Thank you for reaching out. Please find my responses below:







1\. Projects using Selenium and Playwright



In my current role at Forvia Faurecia, I have worked on both web UI automation and API testing.



With Selenium, I developed automation for workflows on the Leshan server, where the objective was to automate and validate different application workflows. I also worked on UI automation for automatically creating defects in the defect-tracking system. One of the challenges was making the automation reliable across different application states and handling dynamic elements. I addressed this by designing reusable automation components, implementing proper synchronization, and following a structured framework approach.



With Playwright, I worked on web-based regression and API testing for an AI chatbot UI. The main challenge was validating the integration between the UI and backend services, including AI-driven test case generation. I addressed this by combining UI automation with API validation and creating reusable test flows to improve coverage and execution efficiency.



2\. Ownership of test automation



I have taken ownership of automation from understanding the requirement and test scenarios through framework development, execution, debugging, and result validation.



For example, I developed Python-based automation for ECU flashing and performance testing, automated client-server socket communication including handshake and protocol validation, and built end-to-end automation for Connected Services. I also designed frameworks to automatically build, execute, and manage test cases in PUMBA/SIMBA simulation environments.



I have also taken initiatives to improve the overall testing process, including developing an advanced logging framework that captures synchronized serial and video logs during automated execution. Additionally, I developed an AI-powered defect summary generator using Copilot AI to improve the quality and efficiency of defect reporting.



These contributions were recognized through two Spot Awards at Forvia, including one for automation development and another for Connected Services framework development.



3\. Fast-paced environment and cross-functional collaboration



Working in an automotive product environment has given me experience working in fast-paced projects with changing requirements, tight execution timelines, and multiple dependencies.



I have collaborated with developers, testers, system engineers, and other stakeholders during integration, regression, and system-level testing. My responsibilities involved understanding requirements, preparing automation environments, executing tests, analyzing failures, debugging issues, and communicating results or defects to the respective teams.



I am comfortable taking ownership of tasks independently while also collaborating closely with cross-functional teams to resolve issues and meet project deadlines.



4\. Notice Period / Earliest Joining Availability: Immediate Joiner



I have served notice period, 13/05/2026 is the LWD.



5\. Current and Expected CTC



My current CTC is 6LPA, and my expected CTC is As per market standards.



6\. Location : Pune



Please let me know if you need any additional information from my side. I look forward to discussing the opportunity further



**============================================================================================**

**============================================================================================**











**============================================================================================**

**============================================================================================**











**============================================================================================**

**============================================================================================**













**============================================================================================**

**============================================================================================**













**============================================================================================**

**============================================================================================**









**============================================================================================**

**============================================================================================**











**============================================================================================**

**============================================================================================**




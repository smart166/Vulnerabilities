# Command Injection

## 1.  Command Injection
Command injection attacks are possible when an application passes unsafe user supplied data (forms, cookies, HTTP headers etc.) to a system shell. Command injection attacks are possible largely due to insufficient input validation.
Types of Command Injection are as follows:
-    **Direct command injection:** The application invokes a system command by directly passing user supplied data as arguments to the command. Then the attacker supplies the malicious command as part of the expected arguments. The application executes the original command and then the malicious one.
-    **Indirect command injection:** The application invokes a system command using data from an external source such as a file or an environment variable. The attacker then modifies the contents of the external source to add a malicious command. Then the attacker waits or forces the application to execute the malicious command along with the original one.
-    **Result-based Command Injection & Blind Command Injection**

### *Command Injection* VS *Code Injection* VS *SQL Injection*
**Command Injection:** Extending the default functionality of the application, which execute system commands, without the necessity of injecting code. Executing the command in operation system; it needs to analyze the operation system.
**Code Injection:** It allows the attacker to add his own code that is then executed by the application.
**SQL Injection:** Insert sql query into request data (an entry field) for execution. Need to analyze the server uses which database.


## 2.  Attack Scenario

This project illustrates how to use completable future with work manager.
For illustration purpose, I have used Spring MVC application so that it can be deployed in appliction server.
Application server is requried as work managers are defined in application server only. Work managers are resources of app server.

### How to run the application?
Navigate to main project directory and run mvn package command and then deploy target war file in application server.
If you want to use Eclipse then run following command  to generate ecplise project settings and then import project into Eclipse. 

mvn eclipse:eclipse -Dwtpversion=2.0

After deploying war to application server, open following url in browser.

http:{host}:{port}/TestCFWorkManager

You will see welcome page with a message as "event complete". This is message is getting returned from completable future task upon its completion. This task gets executed by a thread pool associated with work manager. Work manager is defined web.xml as a resource with JNDI as "wm/cfworkers".


If you face any issues with context root or if you are not sure about context root url then you can follow my stackoverflow post - https://stackoverflow.com/a/44225071/6093375

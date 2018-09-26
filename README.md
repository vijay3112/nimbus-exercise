choose below topic:
c Interface with MongoDB within the framework. Provide examples to show mapping of mongodb with Nimbus.

While deployment, container will read all @Configuration components.

Step1:   
To enable MongoDB database, create MongoDB component which should having @Configuration.
Make sure, we should take common driver details into component which should having @Configuration

Step2:
Create common interface for ModelRepositoryFactory which contains to load which database is required.
ModelRepositoryFactory implementation classes should use database which is based on requirement.

Step3:
While getting request from UI, @RestController will trap the request and pass to matching @RequestMapping URL.
By using @RestController annotation, internally it will call @Controller and @ResponseBody. 

Step4:
The @RequestMapping URL call to corresponding @Service components. From @Service component while interacting with Database, 
Make sure it should required Database. DAO layer @Entity will enable MongoDB which is setting default in ModelRepositoryFactory.

step5:
The controller receive response from @Service, it should return to UI with @ResponseBody on UI required context like json/text/xml... etc.

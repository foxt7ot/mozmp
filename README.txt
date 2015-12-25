***************************************************************HOW TO USE THIS**************************************************************
										DO NOT MAKE CUSTOMER CHANGES TO THE VPOINT PROJECT.
									ALL CUSTOMER SPECIFIC CHANGES SHOULD BE MADE IN THE CUSTOMER LAYER.
This is designed to build out vpoint jar file to be used with any customer.  There will be some configurations required on the customer layer. 
After the jar is created a developer should then take everything from the cust_config directory and place it into the customer layer.  this should 
create a vpoint config path.  The version in the config path should be edited to match the different customer settings.  Please make sure to 
updated the config path of the project to include these. Then jar created by this system should then be put into the lib folder of the customer
layer.  Make sure to add that jar to the classpath of the project.  If the customer is already on an update type build the vpoint jar might need to
be added to xstore using the custom-pre.xml script.  

TO MAKE THE JAR
1. open the buildoverrides.properties file.  
2. change the cust= to the 3 digit customer code (ex: Hibbet would be HIB while mars would be MRS)
3. set the xstore base version.  This needs to associate with a folder in the vpoint project.  
	so if your customer is 4.5 and there is no 4.5 customer then one will need to be developed if overrides are required.
	This setting is also used to find any version specific libraries.  For example if xstore 7.1 requires a new library it should be put int
	lib_7.1.  the system will add this to the classpath automatically when building.  It will create the folder if it is not already created.  
4. run build.xml (the default is the best one to run)
5. This should create a XXX-vPoint.jar.  this jar will need to be added to the customer layer lib folder.  
6. DO NOT COMMIT THE CUSTOMER CHANGES TO THIS JAR.  Since it will be used by multiple customers it should stay 
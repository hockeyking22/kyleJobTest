How To Execute tests
---------------------
0. Create a new maven project in eclipse ide (or import if importing over existing project)

1. Setup Maven dependencies in pom.xml (if not already done so)
<dependencies>
        <dependency>
      		<groupId>io.rest-assured</groupId>
      		<artifactId>rest-assured</artifactId>
      		<version>3.0.2</version>
      		<scope>test</scope>
		</dependency>
        <dependency>
            <groupId>org.hamcrest</groupId>
            <artifactId>hamcrest-all</artifactId>
            <version>1.3</version>
        </dependency>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.11</version>
        </dependency>
        <dependency>
            <groupId>pl.pragmatists</groupId>
            <artifactId>JUnitParams</artifactId>
            <version>1.0.4</version>
        </dependency>
        <dependency>
   			 <groupId>io.rest-assured</groupId>
    		 <artifactId>json-schema-validator</artifactId>
   			 <version>3.0.2</version>
		</dependency>
    </dependencies>

2. Run a maven install on the project (can skip this part if your maven dependcies is already set)

3. Check for the following jar files:
io\rest-assured\rest-assured\3.0.2\rest-assured-3.0.2.jar
org\codehaus\groovy\groovy\2.4.6\groovy-2.4.6.jar
org\codehaus\groovy\groovy-xml\2.4.6\groovy-xml-2.4.6.jar
org\apache\httpcomponents\httpclient\4.5.2\httpclient-4.5.2.jar
org\apache\httpcomponents\httpcore\4.4.4\httpcore-4.4.4.jar
commons-logging\commons-logging\1.2\commons-logging-1.2.jar
commons-codec\commons-codec\1.9\commons-codec-1.9.jar
org\apache\httpcomponents\httpmime\4.5.1\httpmime-4.5.1.jar
org\hamcrest\hamcrest-core\1.3\hamcrest-core-1.3.jar
org\hamcrest\hamcrest-library\1.3\hamcrest-library-1.3.jar
org\ccil\cowan\tagsoup\tagsoup\1.2.1\tagsoup-1.2.1.jar
io\rest-assured\json-path\3.0.2\json-path-3.0.2.jar
org\codehaus\groovy\groovy-json\2.4.6\groovy-json-2.4.6.jar
io\rest-assured\rest-assured-common\3.0.2\rest-assured-common-3.0.2.jar
io\rest-assured\xml-path\3.0.2\xml-path-3.0.2.jar
org\apache\commons\commons-lang3\3.4\commons-lang3-3.4.jar
org\hamcrest\hamcrest-all\1.3\hamcrest-all-1.3.jar
junit\junit\4.11\junit-4.11.jar
pl\pragmatists\JUnitParams\1.0.4\JUnitParams-1.0.4.jar
io\rest-assured\json-schema-validator\3.0.2\json-schema-validator-3.0.2.jar
com\github\fge\json-schema-validator\2.2.6\json-schema-validator-2.2.6.jar
com\google\code\findbugs\jsr305\3.0.0\jsr305-3.0.0.jar
joda-time\joda-time\2.3\joda-time-2.3.jar
com\googlecode\libphonenumber\libphonenumber\6.2\libphonenumber-6.2.jar
com\github\fge\json-schema-core\1.2.5\json-schema-core-1.2.5.jar
com\github\fge\uri-template\0.9\uri-template-0.9.jar
com\github\fge\msg-simple\1.1\msg-simple-1.1.jar
com\github\fge\btf\1.2\btf-1.2.jar
com\google\guava\guava\16.0.1\guava-16.0.1.jar
com\github\fge\jackson-coreutils\1.8\jackson-coreutils-1.8.jar
com\fasterxml\jackson\core\jackson-databind\2.2.3\jackson-databind-2.2.3.jar
com\fasterxml\jackson\core\jackson-annotations\2.2.3\jackson-annotations-2.2.3.jar
com\fasterxml\jackson\core\jackson-core\2.2.3\jackson-core-2.2.3.jar
org\mozilla\rhino\1.7R4\rhino-1.7R4.jar
javax\mail\mailapi\1.4.3\mailapi-1.4.3.jar
javax\activation\activation\1.1\activation-1.1.jar
net\sf\jopt-simple\jopt-simple\4.6\jopt-simple-4.6.jar

4. Go to run configurations and add a new junit test under run configurations for _TestCasesSuite.java
which can be found under com.test.runnableTests package.

5. For arguments tab, set the following VM arguments: 
-DapiKey={YOUR_API_KEY_HERE} -DidValue=295693 -DapiParam2=/authentication/guest_session/new -DapiParam=/movie/

6. Click apply to apply the settings and click on the run button to kick off the tests.
On the JUnit tab you should see results for 2 tests (if you click the arrow to see more details)
1. GetMovieDetails
2. PostMovieRating

**Both test cases should pass.

7. You will find the psuedo code test cases under com.test.psuedo.testCases package
8. You will find the test case plans for the other tests under com.test.outlined.testCases package

Thanks for your time and consideration enjoy :).
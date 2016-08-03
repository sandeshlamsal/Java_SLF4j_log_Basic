# SLF4jBasic
SLF4J is basically an abstraction layer. It is not a logging implementation. 
It means that if you're writing a library and you use SLF4J, you can give that library to someone 
else to use and they can choose which logging implementation to use with SLF4J e.g. log4j or the Java logging API. 
It helps prevent projects from being dependent on lots of logging APIs just because they use libraries that are dependent on them.

So, to summarise: SLF4J does not replace log4j, they work together. It removes the dependency on log4j from your library/app.


to use SLF4J
1. add below dependecny in pom.xml

dependency>
        <groupId>org.slf4j</groupId>
        <artifactId>slf4j-api</artifactId>
        <version>1.7.5</version>
    </dependency>
    <dependency>
        <groupId>org.slf4j</groupId>
        <artifactId>slf4j-jdk14</artifactId>
        <version>1.7.5</version>
    </dependency>
    
  2. in class implement the logger as below
  
  static Logger logger = LoggerFactory.getLogger(Hello.class);
  
  And in side method use to perform info,debug,console or sett in xml or .properties file to write on log files.
  
  eg: logger.info("Logger started");
      logger.debug("debug started");
      
      
   

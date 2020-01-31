# Test WSDL2Java

Simple project to test the integrity of _wsdl_ files

## Prerrequisites

  * Java 8
  * Maven 3.6

## Instructions

1. Open pom.xml
1. Check comment from line 55

    ```xml
    <!-- ... -->
    <sourceRoot>${basedir}/src/main/java/</sourceRoot>
    <wsdlOptions>
      <wsdlOption>
        <!-- :: Copy the wsdl file in this directory :: -->
        <wsdl>${project.basedir}/src/main/resources/wsdl/test.wsdl</wsdl>
      </wsdlOption>
      <includes>
        <include>test.wsdl</include>
      </includes>
    </wsdlOptions>

    <!-- ... -->
    ```
1. Copy the wsdl file into dir: **./src/main/resources/wsdl/**

    > Check the file name, in this example "test.wsdl"

1. Run the command

    ```bash
    $ mvn clean install
    ```

1. The generated resources should be in **./src/main/java/**
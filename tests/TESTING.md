[![CircleCI](https://circleci.com/gh/Apicurio/apicurio-registry.svg?style=svg)](https://circleci.com/gh/Apicurio/apicurio-registry)

# Apicurio Registry System and Integration Tests

## Prerequisites
* Installed [GraalVM](https://www.graalvm.org/docs/getting-started/)
* Set `$PATH` and `$GRAALVM_HOME` variables to GraalVM binaries
* Installed `native-image` by command `gu install native-image`

## Before test execution
Before your first run, you have to build native image of apicurio-registry-app. For build you can use the following command:

``` ./mvnw clean package -Pnative```

## Run tests
For run all tests in `tests` package you can use the following command:

```./mvnw verify -pl tests -Pnative -Dmaven.javadoc.skip=true```

If you want to run only specific tests, you can specify it by `-Dit.test` maven option:

```./mvnw verify -pl tests -Pnative -Dmaven.javadoc.skip=true -Dit.test=<SPECIFIC_TEST_PATH>```  

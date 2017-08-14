# gradle-jaxb-example

This small repo shows how to configure gradle to generate JAXB classes from one or more XSD files. The `build.gradle` file includes a custom `genJaxb` task which will generate the classes and then compile them using `javac`.

It uses the [ISO 20022](https://www.iso20022.org/full_catalogue.page) schemas as an example.

To generate the classes, you can run the `jar` task which depends on `genJaxb`:

```
$ ./gradlew jar
```

You can see the results in the `/build/` directory:
```
├── build
│   ├── classes
│   │   └── jaxb
│   │       └── (compiled .class files)
│   ├── generated-sources
│   │   └── jaxb
│   │       └── (generated .java files)
│   ├── libs
│   │   └── gradle-jaxb-example-1.0-SNAPSHOT.jar
...
```

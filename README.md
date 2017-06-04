# example-groovy-gradle-bug
Showing an example of this Groovy - Gradle bug:
https://github.com/gradle/gradle/issues/2245

To grab this project and replicate this bug, please run these commands:
```
git clone https://github.com/wodencafe/example-groovy-gradle-bug
cd example-groovy-gradle-bug
./gradlew build
```

You should see the project fail due to this error:
```
~/workspaces/jobe/GroovyTest ./gradlew build                                                                                                                                     
:compileJava                                                                                                                                                                                         
/home/wodencafe/workspace/GroovyTest/src/main/java/com/foo/main/Main.java:3: error: cannot find symbol                                                                                             
import com.foo.main.GroovyClass;                                                                                                                                                                     
                   ^
  symbol:   class GroovyClass
  location: package com.foo.main
/home/wodencafe/workspace/GroovyTest/src/main/java/com/foo/main/Main.java:8: error: cannot find symbol
                GroovyClass gc;
                ^
  symbol:   class GroovyClass
  location: class Main
2 errors
:compileJava FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':compileJava'.
> Compilation failed; see the compiler error output for details.
```

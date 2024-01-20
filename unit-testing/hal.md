# Unit Testing and the HAL

## What is the HAL?
HAL stands for **H**ardware **A**bstraction **L**ayer. The HAL allows Java code to work with hardware level code. Any WPILib code which uses hardware must eventually reach the HAL. 


## Why do we need to start the HAL?
The HAL must be started at the beginning of every robot program. Typically, the HAL is started automatically during robot program initalization. However, since unit tests are not called in the same way, we must do it. If we do not start the HAL, hardware objects will not function and our code will crash immediately.

## Code Example
The following code should be used in every unit test to start the HAL. 

```
import org.junit.jupiter.api.BeforeAll;

import edu.wip.first.hal.HAL;

public class UnitTest {

    @BeforeAll
    static void setup() {
        //Start the HAL, crash if startup fails
        assert HAL.initalize(500, 0); 

        //other test-specific setup
    }

    //tests below
}
```
Methods annotated with `@BeforeAll` run once before any tests. Any one-time setup should occur in this method. Note that any method annotated with `@BeforeAll` must be static. 
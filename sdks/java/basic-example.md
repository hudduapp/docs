# Basic Example

```java
package com.huddu;

public class Example {
    public static void main(String[] args) {
        
        for (int i=0; i<5; i++){
            ApiClient _c = new ApiClient("<project_id>", "<stream_id>"); // you can optionally also pass a token
            _c.report("<event_id>", "<valid_json_string>");
        }
    }
}
```

This example can be found at [https://github.com/hudduapp/huddu-java/blob/main/src/main/java/com/huddu/Example.java](https://github.com/hudduapp/huddu-java/blob/main/src/main/java/com/huddu/Example.java)

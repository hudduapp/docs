# SDK

The Huddu SDK is the simplest way to create key, value pairs on Huddu. For now there's support for Java and Python with plans for Nodejs to follow soon.

Any languages to add to that list? Tell us in a [community channel!](/platform/other/community)

## Installation

=== "Python"
`    pip install huddu
   `

    !!! info
        It's great practice to keep all your requirements in a requirements.txt file!


    Github Repository: [https://github.com/hudduapp/huddu-python](https://github.com/hudduapp/huddu-python)

=== "Java"
For Maven (in pom.xml):

    1. Add the JitPack repository in \<repositories>

    ```xml
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
    ```

    2\.  Add the dependency to \<dependencies> (ideally choose a commit as the version)

    ```xml
    <dependency>
        <groupId>com.github.hudduapp</groupId>
        <artifactId>huddu-java</artifactId>
        <version>v1-SNAPSHOT</version>
    </dependency>
    ```

    For more information check: [https://jitpack.io/#hudduapp/huddu-java](https://jitpack.io/#hudduapp/huddu-java/v1-SNAPSHOT)

    Github Respository: [https://github.com/hudduapp/huddu-java](https://github.com/hudduapp/huddu-java)

## Initiating the SDK

First, we need a few variables (namely a **collection token** and a **collection identifier**).

1. To obtain the collection token open a collection and switch to the **Authorization tab** and press the **Create Token** button.
2. Getting our collection identifier is simpler. We just need to press the **Connect** button in the top right corner. This will open a drawer that displays our collection identifier.
3. In the same drawer, you will find the region identifier. (in future versions of the sdk you won't have to specify this)

=== "Python"
```python
from huddu import Store

    store = Store(
        token="<auth_token>", # how to obtain? see above
        collection="<collection_identifier>", # how to obtain? see above
        region="<region>" # how to obtain? see above
    )
    ```

=== "Java"
```java
package org.example;

    import com.huddu.Store;
    import com.huddu._exceptions.APIException;

    public class Main {
        public static void main(String[] args) throws APIException {
            Store store = new Store(
                    "<auth_token>",
                    "<collection_identifier>",
                    "<region>"
            );
        }
    }
    ```

## Working with data

The Store class offers the following methods:

- .get() - Get one entry by identifier
- .put() - Create a new entry
- .delete() - delete one entry
- .update() - override an existing entry with new data
- .fetch() - List entry items with a set limit and skip or even by identifier.

## Get

=== "Python"
`python
    store.get(
        id: str,
        start: int = None,
        end: int = None,
    )
    `

=== "Java"
`java
    store.get(
        String id,
        int start,
        int end
    )
    `

### Parameters:

- id: the entry identifier
- start: the line after which the content of the entry should be returned (optional)
- end: the line before which the content of the entry should be returned (optional)

## Put

=== "Python"
`python
    store.put(
        id: str,
        data: str, 
        safe: bool = True
    )
    `

=== "Java"
`java
    store.put(
        String id,
        Object data,
        boolean safe
    )
    `

## Parameters:

- id: the entry identifier
- data: the entry data
- safe: if true will check if an entry with the identifier already exists to prevent overriding it. (optional)

## Delete

=== "Python"
`python
    store.delete(
        id: str
    )
    `

=== "Java"
`java
    store.delete(
        String id
    )
    `

## Parameters

- id: the entry identifier

## Update

=== "Python"
`python
    store.update(
        id: str,
        data: str
    )
    `

=== "Java"
`java
    store.update(
        String id,
        Object data
    )
    `

## Parameters

- id: the entry identifier
- data: the entry data

## Fetch

=== "Python"
`python
    store.fetch(
        ids: List[str] = None,
        skip: int = 0,
        limit: int = 25,
        start: int = None,
        end: int = None,
    )
    `

=== "Java"
`java
    store.fetch(
        ArrayList ids,
        int skip,
        int limit,
        int start,
        int end
    )
    `

### Parameters

- ids: List of ids to query (optional)
- skip: Number of items to skip from results (defaults to 0)
- limit: Number of items to limit to from results (defaults to 25)
- start: the line after which the content of the entry should be returned (optional)
- end: the line before which the content of the entry should be returned (optional)

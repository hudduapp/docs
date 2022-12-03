# SDK

The Huddu SDK is the simplest way to upload, read and delete files.

## Installation


=== "Python"
    ```
    pip install huddu
    ```
    
    !!! note    
        It's great practice to keep all your requirements in a requirements.txt file!



## Initiating the SDK

First, we need a few variables (namely a **collection token** and a **collection identifier**).

1. To obtain the collection token open a collection and switch to the **Authorization tab** and press the **Create Token** button.
2. Getting our collection identifier is simpler. We just need to press the **Connect** button in the top right corner. This will open a drawer that displays our collection identifier.
3. In the same drawer, you will find the region identifier. (in future versions of the sdk you won't have to specify this)


=== "Python"
    ```python
    from huddu import Drive
    
    
    store = Drive(
        token="<auth_token>", # how to obtain? see above
        collection="<collection_identifier>", # how to obtain? see above
        region="<region>" # how to obtain? see above
    )
    ```


## Adding data

The Store class offers the following methods:

* .get() - Get file chunks
* .upload() - Upload a file
* .delete() - delete a file

## Get


=== "Python"
    ```python
    drive.get(
        name: str
    )
    ```


* name: the name of the file you want to retrieve

## Put


=== "Python"
    ```python
    drive.upload(
        name: str,
        data: str = None,
        path: str = None
    )
    ```


## Parameters:

* name: the name of the file you want to create
* data: a string of the data that's contained in the file
* path: if data is not specified: the path to the file to upload

## Delete


=== "Python"
    ```python
    drive.delete(
        name: str
    )
    ```


## Parameters

* name: the name of the file you want to delete
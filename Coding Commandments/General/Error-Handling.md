*  Keep in mind the `Murphy's law` while coding, which says 
> "Anything that can go wrong will go wrong"
*  Prefer handling specific errors, generic error should be the last resort. 

```
// bad code
String getSecondLine(filePath)
    try{
        file = openFile(path);
        lines = file.readLines();
        return lines[1];
    }
    catch(exception){
      print(exception);
      throw
    }
}

// a better approach
String getSecondLine(filePath)
    if (!File.exists(filePath))
        throw FileNotFoundException(filePath);    
    
    file = openFile(path);
    lines = file.readLines();
    if (lines.length < 1)
        throw InvalidOperationException('Not enough lines in the file');
    
    return lines[1];
}

//even better approach
String getSecondLine(filePath)
    if (!File.exists(filePath))
        return null;
    
    file = openFile(path);
    lines = file.readLines();
    if (lines.length < 1)
        return null;
    
    return lines[1];
}
```
*  (In context of code shown above) sometimes it is subjective which approach is best, a lot depends on the context. Generally speaking, exceptions should be used for exceptional scenarios because throwing and catching exceptions is a computationally expensive operation. It is preferable if you can write code in such a way that there is no need to handle exceptions. 
*  If you are doing division ensure denominator is non zero. 
*  Before processing a REST API response, always check the `status` code. 
*  While writing REST APIs, always return the most appropriate HTTP status code and return helpful error messages.
*  Do not return stack traces in the REST API response in case of exceptions.
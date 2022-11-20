
# Python SDK Reference

Lesscode Plus allows you to use python to handle edge cases in your micro workflows. If the problem you aim to solve is simple, we recommend you to use Python. To solve complex problems we recommend you use our C# SDK.

Lesscode Plus uses Iron Python which only has a limited set of features. However, you can use any classes available in .NET core standard library.

This section covers only the coding part of Python SDK. To learn more about how to use Python to handle edge cases, we recommend you to watch our crash course video. 


## Variables Passed to the Custom Script

When you write your custom code on the Python script, you can use special variables automatically created using the Lesscode Plus API engine. Data types of the following variables are Lesscode Plus's HashMaps.

#### context

this variable allows you to read the environment variables and the information about the request.

#### variables

This variable allows you to read all the variables available in the micro workflow.

#### config

This variable allows you to read the configuration of a block

 
## Returning a Value From the Python Script

if you want to return a value from the Python script you can create a variable, name it as 'result' and assign a value to it.

```python
result = "Hello World"
```

## Creating Lesscode Plus's Data Types

Lesscode Plus uses special data types such as HashMaps and AnyType Arrays. To learn more about those data types, you can refer to our C# SDK reference. You can use the following methods to create data types.

#### lcmap

creates a HashMap in the script.

```python
newmap = lcmap()
```

#### lcarray
creates an AnyTypeArray in the script.

```python
newarray = lcarray()
```

## Logging Values

You might also want to log values for debugging. You can use the following methods for the purpose.

#### lcdebug
Logs  a debug value 
```python
lcdebug("Debug value printed")
```

#### lcprint

Prints a value in the console
```python
lcprint("Logged in Console!")
```

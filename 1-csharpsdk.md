
# C# SDK Reference

C# SDK allows you to handle edge cases and, with complex development scenarios, and integrate any 3rd party .NET core library with Lesscode Plus.

To get started with you need to [download the C# SDK from the downloads page](https://lesscode.plus/#/download) which includes all the class libraries and a Visual Studio template for you to get started with. When you open the template with Visual Studio and run it, a console application will open and listen on port 5000 for incoming HTTP requests, which can be used for debugging purposes. You can also compile it and host it anywhere too.

You can create custom blocks for your block-based micro workflows in your Lesscode Plus application in the C# template. 

This section only covers the core concepts required for you to use C# for your application. To learn about the class library in detail [you can read the class library documentation](https://lesscode.plus/cssdk/). Also, you can refer to the crash course video to learn how C# SDK is used practically.



## Special Data Structures in C# SDK

Data structures in block-based micro workflows are represented in C# SDK as follows.

### HashMap

HashMap represents an object in a micro workflow. From C#'s perspective, it's a wrapper around Dictionary<string,object> with enhanced capabilities.


### AnyTypeArray

AnyTypeArray represents an array in a micro workflow. Its a wrapper around List<object> with enhanced capabilities.


## Creating Custom Blocks

To create a custom block you need to create a class, Inherit AbstractBlock and override the OnExecute method.  Then you need to assign a URN (Uniform Resource Name) to the class by using the attribute LessCodeUrn. Once it is created, you can execute this block by using the block "Run custom C# code" and configuring the URN property to the value you have mentioned in the LessCodeUrn attribute.

```csharp
	using LessCodeEngine.Sdk;
	
    [LessCodeUrn("demo:sample-block")]
    public class SampleBlock : AbstractBlock
    {
        protected override void OnExecute()
        {
            var name = Inputs["name"];
            this.Response = $"Hello {name}";
        }
    }
```

To access the inputs in the micro workflow, you can use the Inputs property.
To set the response from the block, you can assign a value to the Response property.

## Creating Custom Commands

To create a custom command that you can execute in the command line, similar to creating a custom block, you can inherit the abstract class AbstractCommand, override the method Execute and use the LessCodeCommand attribute to specify the command name and its description.


```csharp
	using LessCodeEngine.Sdk;
	
    [LessCodeCommand("sample", "Executes the sample command")]
    public class SampleCommand : AbstractCommand
    {
        public override void Execute(string[] args)
        {
            Console.WriteLine("Sample command executed!");
        }

    }
```

After  you compile the application, you can run it with the command line as follows;

In windows

```bash
lesscode sample 
or
dotnet run LesscodeEngine.Cli sample
```
In Linux Bash

```bash
./lesscode.sh sample
or
dotnet run LesscodeEngine.Cli sample
```
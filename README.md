# EnhanceDebugging
## Biml Debugging

A quick example of how to employ BIML debugging.

## For Your Own Use
1. Grab the `Biml` directory and place it into your project
2. Configure the `Config.cs` file accordingly
3. Include this line in your BIML files: `<#@ include file="Path\To\Debug.csbiml"#>`
4. Wrap your BIML files, inside the <BIML> tags, with the following:

````````
 <# try { #>
 <# } catch (Exception ex) { 
        Debug.BimlDump(this.GenerationEnvironment.ToString(), Host.TemplateFile); 
      } #>
````````


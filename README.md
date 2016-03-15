# EnhanceDebugging
## Biml Debugging

A quick example of how to employ BIML debugging.

## For Your Own Use
1. Grab the `Biml` directory and place it into your project
2. Configure the `Config.cs` file accordingly
3. Change `1.Environment.biml` to point at your landing folder for the flat files
4. Include this line in your BIML files: `<#@ include file="Path\To\Debug.csbiml"#>`
5. Wrap your BIML files, inside the <BIML> tags, with the following:

````````
 <# try { #>
 <# } catch (Exception ex) { 
        Debug.BimlDump(this.GenerationEnvironment.ToString(), Host.TemplateFile); 
      } #>
````````
6. Select the files in the following in order to compile (4, 3, 2, 1) then right click and `Generate SSIS Packages`

# A Simple Project

If you are using Haxe/Flash Develop, and you have installed the HaxeUI Templates, you can use these to create a project. In these tutorials, I will be focusing on the OpenFL project template. Since most of the code examples are all based on the HaxeUI Core Module, it really does not matter which template you use. However, the build commands you use may differ.

Since OpenFL and Kha use their own build systems, you will need to use their respective build commands. All other frameworks/engines only require the Haxe build system directly.

I will be taking the perspective of someone who does not necessarily have Haxe or FlashDevelop, since not everyone uses Windows. It does not matter which text editor you choose, but I personally recommend Visual Studio Code as a cross-platform alternative to FlashDevelop.

## Creating your Project
You will firstly need to create your workflow.

 * Create a folder for your new project somewhere on your computer.
 * Within that newly-created project (given that you are using the OpenFL backend), create a folder structure like so:

```
root
| assets/
| --> css/
| --> ui/
| src/
| --> Main.hx
| project.xml
```

 * Inside of `project.xml`, replace whatever is there with the following:

```xml
<?xml version="1.0" encoding="utf-8"?>
<project>
    <meta title="Tutorial" package="Tutorial" version="1.0.0" company="my_name" />
    <app main="Main" file="Tutorial" path="bin" />

    <window background="#FFFFFF" fps="60" />
    <window width="800" height="600" unless="mobile" />
    
    <source path="src" />

    <haxelib name="openfl" />
    <haxelib name="actuate" />
    <haxelib name="haxeui-core" />
    <haxelib name="haxeui-openfl" />

    <assets path="assets/css" rename="css" />
    <assets path="assets/ui" rename="ui" />
</project>
```

Assuming you are familiar with OpenFL, I will not be going over the XML file. However, if you are not familiar, you can check out [this page](http://www.openfl.org/learn/docs/command-line-tools/project-files/xml-format/) for information on the XML format.

 * Once done, open `Main.hx` and replace whatever is there with the following:

```haxe
package;

import haxe.ui.Toolkit;
import haxe.ui.components.Button;
import haxe.ui.core.Screen;

class Main {
    
    
    public static function main() {
        Toolkit.init();
        
        var button:Button = new Button();
        button.text = "Click Me!";
        button.onClick = function(e) {
            trace("Success!");
        };
        
        Screen.instance.addComponent(button);
    }
}
```

Save this file, plus the XML, and test out the build.

To build this project in OpenFL, use the following command in Terminal or Command Prompt (within the folder of your project's directory):

    haxelib run openfl build project.xml neko

Assuming everything was done correctly, this should be the result:

![img](http://image.prntscr.com/image/0156238526a84fffb0f20ffb88489dea.png)

[Next Tutorial](https://github.com/tienery/HaxeUITutorials/blob/master/04UnderstandingHaxeUI.md)

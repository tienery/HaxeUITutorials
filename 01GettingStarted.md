# Getting Started
If you are just getting started with HaxeUI 2, you will need the following repositories installed (via haxelib) onto your computer:

 * [Haxe UI Core](https://github.com/haxeui/haxeui-core) - This is a requirement. In order to use HaxeUI, the core module needs to be installed. You should install it using `haxelib git haxeui-core https://github.com/haxeui/haxeui-core.git`.
 * The Haxe UI Backend you use. If, for example, you are using OpenFL (like in these tutorials) you will need to install the openfl backend module as well: `haxelib git haxeui-openfl https://github.com/haxeui/haxeui-openfl.git`.

The HTML5 backend is only dependant on the Haxe standard library, so there you do not need to install any other library but the HTML5 backend itself. Other backends need their respective frameworks. You can find a list of backends on the core HaxeUI repository in it's README.

HaxeUI 2 currently supports: OpenFL, Flambe, Kha, HTML5, PixiJS, NME, Luxe and hxWidgets (or wxWidgets).

Since HaxeUI supports so many frameworks, it can be difficult to determine if what you do in the code examples throughout these tutorials will be consistent on all frameworks. It is therefore important that by following these tutorials, you take everything with a pinch of salt. In addition, since any or all of the frameworks may still be in Alpha, the examples and their respective results may not be representative of the final release. Please bare this in mind while you go through these tutorials.

## Setup
Once you have installed these, you may optionally download and install the `*.fdz` from [https://github.com/haxeui/haxeui-templates](https://github.com/haxeui/haxeui-templates) for Flash/Haxe Develop. There also contains templates for Kha. Please refer to the [HaxeDevelop Extensions page](http://www.haxedevelop.org/extensions.html) for information on how to install `fdz` files.

Underlying knowledge of the backend you choose to use may be necessary for setup. However, some backends do not require underlying knowledge (such as HTML5). However, since HaxeUI does not have it's own build system yet, you will need to rely on either the build system of the respective backend or the haxe build system itself if that is what the backend recommends. If you do use the haxe build system, you will need to include the `haxeui-core` and `haxeui-[backend]` (where `[backend]` is replaced by the name of the backend) in your hxml file.

Here is an example hxml file for HTML5:

```
-cp src
-main Main
-js bin/example.js
-lib haxeui-core
-lib haxeui-html5
```

[Next Chapter - Understanding Modules](https://github.com/tienery/HaxeUITutorials/blob/master/02UnderstandingModules.md)

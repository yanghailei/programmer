# 标准文件更改后缀名导致不能识别问题
 
    例如：*.mk *.mak都属于makefile文件可以在files->setting下增加如下参数
    
        "files.associations": {
        "*.mk":"makefile",
        "*.mak":"makefile",
        "*.db":"c"
    }      
|Language|Identifier|
|--------|----------|
Language|Identifier
ABAP|abap
Windows|Bat	bat
BibTeX|bibtex
Clojure|clojure
Coffeescript|coffeescript
C|c
C++|cpp
C#|csharp
CSS|css
Diff|diff
Dockerfile|dockerfile
F#|fsharp
Git|git-commit and git-rebase
Go|go
Groovy|groovy
Handlebars|handlebars
HTML|html
Ini|ini
Java|java
JavaScript|javascript
JavaScript React|javascriptreact
JSON|json
JSON with Comments|jsonc
LaTeX|latex
Less|less
Lua|lua
Makefile|makefile
Markdown|markdown
Objective-C|objective-c
Objective-C++|objective-cpp
Perl|perl and perl6
PHP|php
Powershell|powershell
Pug|jade
Python|python
R|r
Razor (cshtml)|razor
Ruby|ruby
Rust|rust
SCSS|scss (syntax using curly brackets), sass (indented syntax)
ShaderLab|shaderlab
Shell Script (Bash)|shellscript
SQL|sql
Swift|swift
TypeScript|typescript
TypeScript React|typescriptreact
TeX|tex
Visual Basic|vb
XML|xml
XSL|xsl
YAML|yaml

---
# VScode C/C++代码格式化问题

## 简易的快速实现代码格式化方式

> Current C++ VSCode Formatted
```c
for (int i = 0; i < 10; i++)
{
    // ...
}
```  
> What You Want C++ VSCode Formatted Code to Look Like
```c
for (int i = 0; i < 10; i++) {
    // ...
}
```  
> You can add this cmd, in setting.json to get what you want.
```
"C_Cpp.clang_format_fallbackStyle": "{ BasedOnStyle: Google, IndentWidth: 4, ColumnLimit: 0}"
```

## 更加专业的代码格式化  
```
"clang-format.executable": "/home/hailei/.vscode/extensions/ms-vscode.cpptools-0.22.2-insiders/LLVM/bin/clang-format",
"clang-format.style": "WebKit",
```

Synergy X Ui library
Our Discord : https://discord.gg/34BFzS3pj7 and https://discord.gg/JnSvN7wdwW

To Making An library Add Load Library First
```Lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/IlikeScript1234/SynergyX/main/Library"))()
```
Add Library
```Lua
local AnyName = library:Add("AnyLibraryName")
```
add label
```Lua
main:CreateLabel("AnyLabel")
```
Add Toggle (Work only print state)
```Lua
AmyName:CreateToggle("Toggle", function(state)
print(state)
end)
```
Add Button
```
AnyName:CreateButton("Any Name", function()
    print("hi how are u bad?")
end)
```

Synergy X Ui library New Update 18 May 2023 Add Notify And Slider

Our Discord : https://discord.gg/34BFzS3pj7 and https://discord.gg/JnSvN7wdwW

To Making An library Add Loader First!
```Lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/IlikeScript1234/SynergyX/main/Library"))()
```
Add Library
```Lua
local AnyName = library:Add("AnyLibraryName")
```
Add Label
```Lua
AnyName:CreateLabel("AnyLabel")
```
Add Toggle (Work only print state)
```Lua
AnyName:CreateToggle("Toggle", function(state)
print(state)
end)
```
Add Button
```Lua
AnyName:CreateButton("Any Name", function()
    print("hi how are u bad?")
end)
```
Add Slider
```Lua
AnyName:CreateSlider("name here", 1, 100, function(val) -- no limit! u can change val to any
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = val
end)  
```
Sent Notify
```Lua
AnyName:CreateNotify("Hello Word", 5) -- 5 is timer u can set what ever u want and hello word u can change word
```

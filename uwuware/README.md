# uwuware v1 example lib

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/XRoLLu/ui-lib/main/uwuware/src.lua"))(); 

local Window = Library:CreateWindow("uwuware lib")

local folder = Window:AddFolder("all example") -- tab

folder2:AddButton({text = "Button", callback = function() 
    print("bUTToN")
end})

folder:AddToggle({text = "The Toggle", callback = function(value) 
print(value)
end})

folder4:AddList({text = "Dropdown", values = {"One","Two","Three"}, callback = function(Name)
    if Name == "One" then
		print("selected one")
	elseif Name == "Two" then
		print("selected two")
	elseif Name == "Three" then
		print("slected three")
    end
end})

folder:AddSlider({text = 'Slider Walkspeed', min = 16, max = 100, incrementalMode = true, callback = function(value) 
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
end});

Library:Init() --ALWAYS USE THIS ON END OF THE CODE TO MAKE IT WORK
```
sorry but this is the only thing that i can found 

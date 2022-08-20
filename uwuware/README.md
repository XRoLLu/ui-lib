# uwuware v1 example lib

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/XRoLLu/ui-lib/main/uwuware/src.lua"))(); 

local Window = Library:CreateWindow("uwuware lib") -- window

local folder = Window:AddFolder("example") -- tab

folder:AddLabel({text = "Label"})

folder:AddButton({text = "Button", callback = function() 
    print("bUTToN")
end})

folder:AddToggle({text = "The Toggle 1", state = false, callback = function(value) 
	print(value)
end})

folder:AddToggle({text = "The Toggle 2", state = true, callback = function(value) 
	print(value)
end})

folder:AddList({text = "Dropdown", values = {"One","Two","Three"}, callback = function(Name)
    if Name == "One" then
		print("selected one")
	elseif Name == "Two" then
		print("selected two")
	elseif Name == "Three" then
		print("slected three")
    end
end})

Window:AddBind({text = "Toggle UI", key = "RightShift", callback = function() 
library:Close() -- idk why this not working
end})

folder:AddSlider({text = 'Slider Walkspeed', min = 16, max = 100, incrementalMode = true, callback = function(value) 
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
end});

Library:Init() --ALWAYS USE THIS ON END OF THE CODE TO MAKE IT WORK
```
sorry but this is the only thing that i can found 

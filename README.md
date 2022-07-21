# UILibrary

USAGE:

local ExploitsWindow = Library:NewMenu("Exploits") -- New Menu

local Toggle = Library:NewToggle("Mana Fly", ExploitsWindow, {
	-- Settings
	Hint = {
	["Title"] = "Fly",
	["Description"] = "This is just fly"
	}
}, function(State)
	print(State)
end)

Toggle:CreateSettingToggle("Hello", function(ToggleState)
	print(ToggleState)
end)

Toggle:CreateSettingButton("Hello", function()
	print("Hello")
end)

Toggle:CreateSettingSlider("Fly Speed", 1, 300, 3, function(CurrentValue)
print(CurrentValue)
end)

Toggle:CreateSettingKeybind("Keybind", nil, function()
	Speed = not Speed;
end)

local Modes = {
	"Hello",
	"Another Hello",
};

Toggle:CreateSettingModePicker("Teleports", Modes, function(CurrentMode)
	print(CurrentMode);
end)

Toggle:CreateSettingColorPicker(Color3.new(255, 255, 255), function(Color)
	print("R: " .. Color.R * 255 .. "G: " .. Color.G * 255 .. "B: " .. Color.B * 255);
end)
